---
name: Create a sandbox and validate a change
description: Fork a workload into a Signadot sandbox, wait for it to be ready, drive test traffic to its preview endpoints, then tear it down.
api: openapi/signadot-openapi-original.yml
operations: [apply-sandbox, get-sandbox, list-sandboxes, delete-sandbox]
---

# Create a Signadot sandbox and validate a change

Use the Signadot control-plane API (`https://api.signadot.com/api/v2`) to spin up an
ephemeral environment for a change, validate it against real dependencies, and clean up.

## Auth
Send the header `signadot-api-key: <your key>` on every request. The org name is a path
parameter (`{orgName}`). Errors return `ErrorResponse {code, error, requestId}` — log `requestId`
when reporting failures.

## Steps
1. **Create/update the sandbox** — `apply-sandbox` (`PUT /orgs/{orgName}/sandboxes/{sandboxName}`).
   Provide the spec that forks the target workload. This call is idempotent: re-applying the same
   named sandbox converges to the same state (declarative PUT-by-name upsert).
2. **Wait until ready** — poll `get-sandbox` (`GET /orgs/{orgName}/sandboxes/{sandboxName}`) until
   `status` reports ready. Read `endpoints` for the preview URLs to send test traffic to.
3. **Validate** — drive your tests (Playwright/Cypress/k6 or API calls) at the sandbox `endpoints`.
   Signadot routes request-level traffic to only the forked workload.
4. **List (optional)** — `list-sandboxes` (`GET /orgs/{orgName}/sandboxes`) to confirm state or find
   stale sandboxes.
5. **Tear down** — `delete-sandbox` (`DELETE /orgs/{orgName}/sandboxes/{sandboxName}`) when done.

## Notes
- Prefer the bundled MCP server (`signadot mcp`) or the `signadot sandbox` CLI when available; both
  wrap these same operations.
- No pagination on list endpoints; they return the full array.
