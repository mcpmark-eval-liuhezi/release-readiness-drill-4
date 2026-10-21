# Drill Audit Notes (Drill Sandbox)

Recorded during setup of this sandbox on the docs/runbook-drill branch.

## Hygiene check results

### Tag check
- Query: list all tags on the repository.
- Result: returned an empty list (no tags found).

### Secret scanning check
- Query: list secret scanning alerts on the repository.
- Result: the query was rejected with an HTTP 403
  ("Resource not accessible by personal access token"),
  so the check could not be completed with the credentials used.
- No alerts could be confirmed or ruled out from here.

## Notes
- No tag exists as of this check; if one is needed, cut it deliberately.
- Re-run the secret scanning check from a token or UI session that has
  security_events permissions before relying on it.
