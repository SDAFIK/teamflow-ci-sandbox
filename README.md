# TeamFlow CI Sandbox

Public, fictional-data-only GitHub Actions test repository for the **TeamFlow Guard Stage 8** acceptance process.

This sandbox intentionally creates one failed and one successful GitHub Actions run, so the TeamFlow GitHub App can later be tested against *real* workflow events. It does not deploy code or connect to any database, provider API, or production workspace.

## Safety boundaries

- Only synthetic test content is permitted; never commit keys, tokens, sensitive data, invitations, or user information.
- Test branch: `stage8/live-ci-test`.
- `ci-outcome.txt` on that branch contains either `fail` or `pass`; the workflow exits accordingly.
- The workflow has `contents: read` permissions and no external credentials or network calls.
- An actual GitHub Actions failure/success **does not itself prove** TeamFlow received a signed App webhook. That verification requires the separate TeamFlow GitHub App installation, authorized workspace mapping, delivery receipt, and observed isolated ingestion.

See [TeamFlow Stage 8 runbook](https://github.com/SDAFIK/TeamFlow-Guard/blob/main/docs/STAGE8_REAL_INTEGRATION_ACCEPTANCE.md).
