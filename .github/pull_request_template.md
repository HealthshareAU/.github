## What & why
<!-- 1–3 sentences. What changed, and why. Mention anything the title doesn't. -->

## Jira
[<JIRA_ISSUE>](https://healthshare.atlassian.net/browse/<JIRA_ISSUE>)
<!-- Replace <JIRA_ISSUE>, e.g. BK-000. -->
<!-- Dependencies — must link PRs, not issues: Depends on #id #id -->

## Testing
<!-- How was this verified? Tick what applies and delete the rest. -->
- [ ] Unit / integration tests added or updated
- [ ] Infrastructure: change-set preview or plan reviewed (rows and replacements as expected)
- [ ] Deployed to test / sandbox and checked
- [ ] Not applicable — <!-- why, e.g. docs or comments only -->
<!-- Steps a reviewer can follow, and anything that can't be verified locally and where to check it instead. -->

## Risk & rollback
- Risk: Low / Medium / High — <!-- why -->
- Security-sensitive (auth, permissions, user input, secrets)? No <!-- or Yes — what -->
- Deploy/runbook steps after merge: **None** <!-- or list them -->
- Safe to revert by reverting this PR? Yes <!-- or No — why -->

## Logging and secrets
- [ ] No passwords, tokens, API keys, session ids or other credentials are logged, put in error messages or shown on dashboards.
- [ ] No patient data is logged (names, dates of birth, contact details, addresses, Medicare / DVA / IHI or other health identifiers, booking notes). Log record ids instead.
- [ ] Any new request or response field that carries personal data or a secret is added to the service's log masking list (e.g. the website's `PiiFields`; the marketplace masker from BK-1209).
- [ ] No secrets in code, config files or test fixtures. Secrets come from AWS Secrets Manager or the pipeline.
