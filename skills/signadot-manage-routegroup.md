---
name: Group sandboxes with a route group
description: Create a route group that spans multiple sandboxes for a multi-service change, inspect it, then delete it.
api: openapi/signadot-openapi-original.yml
operations: [list-sandboxes, apply-routegroup, get-routegroup, delete-routegroup]
---

# Manage a Signadot route group

A RouteGroup stitches several sandboxes together so a change touching multiple services can be
tested end to end. Base URL `https://api.signadot.com/api/v2`.

## Auth
Header `signadot-api-key: <your key>`; `{orgName}` is a path parameter. Errors use the
`ErrorResponse {code, error, requestId}` envelope.

## Steps
1. **Find the sandboxes** — `list-sandboxes` (`GET /orgs/{orgName}/sandboxes`) to collect the
   routing keys / labels of the sandboxes you want to group.
2. **Create/update the route group** — `apply-routegroup`
   (`PUT /orgs/{orgName}/routegroups/{routegroupName}`) with a `spec.match` selecting the member
   sandboxes by label. Idempotent PUT-by-name upsert.
3. **Inspect** — `get-routegroup` (`GET /orgs/{orgName}/routegroups/{routegroupName}`) and read
   `endpoints` for the combined preview URLs; check `status` for readiness.
4. **Tear down** — `delete-routegroup` (`DELETE /orgs/{orgName}/routegroups/{routegroupName}`).

## Notes
- Multi-cluster RouteGroups are an Enterprise feature.
- Route groups collapse if constituent sandboxes go temporarily unready; re-check `status`.
