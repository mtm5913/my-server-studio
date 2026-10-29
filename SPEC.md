# Lesson 01 specification

## STUDIO-001 · Launch a tested calculator on an existing server

**Status:** New launch and runtime verification passed; learner observation, keep decision and summary review recorded. Full PR CI passed for the evidence commit.
**Next step:** Confirm checks on the latest PR revision, then review for merge and issue closure.
**Instructor implementation:** [issue #9](https://github.com/kaw393939/373_hosting/issues/9).
Create your own issue from the [lesson template](.github/ISSUE_TEMPLATE/studio-calculator.md).

## Agreed result

Launch the supplied published calculator image through your existing Traefik
network and a nonconflicting HTTPS hostname. Preserve unrelated services and
host access. Do not add another proxy/updater or build a substitute image.
The [release selection](studio/calculator-release.json) supplies the expected
commit and multi-platform digest independently of the running website.
An explicitly agreed adoption of a matching existing deployment is recorded
as adoption, not a fresh launch. This bounded lesson does not certify the whole
server baseline or a vulnerability-free image.

- **Public hostname:** https://calc.megan373lab.xyz (chosen by learner; DNS verified).
- **New launch or adopted deployment, and reason:** New launch completed after learner approval; doctor found no matching deployment. [Initial launch evidence](studio/launch-evidence.json) preserves this separately from later verification.
- **Own issue / feature branch:** [Issue #1](https://github.com/mtm5913/my-server-studio/issues/1); `codex/studio-001-calculator`.
- **Agreed scope or actual access/configuration gap:** Approved single calculator on existing `hosting-web` network, using existing Traefik. Launch and verify passed.

Release source: [calculator-release.json](studio/calculator-release.json).
Pinned image: `docker.io/kaw393939/is373_ci_cd@sha256:aec414c990a5de6ed74c9e8dcb105b78f6358c03a8cea70a9d40dcda51c3a8fa`.
Expected source commit: `4600202bad42da0c5ffb11d83ce8364671293d3d`.

Private SSH targets and configuration stay in ignored local state. Share only
reviewed, selected evidence; never commit credentials or raw server output.

## Evidence to keep

| Evidence | Actual result / link |
|---|---|
| Prepared Black/Pylint/pytest and real-image browser checks | Local fast checks passed: 91 tests, 2 E2E deselected because local Docker daemon was unavailable. [Full PR CI](https://github.com/mtm5913/my-server-studio/actions/runs/40956101078) passed for `b083517`: 91 non-E2E tests and 2 real-image Chromium E2E tests passed. Initial sandbox test bind failure resolved by rerunning with permission. |
| Hosted image/commit, trusted HTTPS, valid and rejected API cases | Launch and verify passed; [latest sanitized evidence](studio/evidence.json). AI browser check: 6 × 7 showed 42 in browser and API, with Results match. |
| Preservation of unrelated services | Nine existing containers unchanged in identity, state and published ports during launch/verification; this is the selected scope only. |
| Own prediction, check interpretation, browser observation and keep/revise reason | [LEARNING.md](LEARNING.md): initial guesses and AI routing explanation disclosed; check interpretation, 8 ÷ 2 observation and keep decision recorded. Independent full request-path explanation remains pending. |
| Accuracy review before publishing learner excerpts | Learner reviewed, corrected wording, then approved the revised summary and authorized commit. |
| Actual PR, latest CI, merge and issue closure | [PR #2](https://github.com/mtm5913/my-server-studio/pull/2), linked to issue #1. [CI run](https://github.com/mtm5913/my-server-studio/actions/runs/40956101078) passed all three jobs for `b083517`. Check any newer revision before merge. Merge and issue closure pending. |

Link the exported `studio/evidence.json`, actual CI and issue/PR when available.
CI does not deploy this server. A fixture, green check, timestamp, closed issue
or AI assertion alone does not establish the full result. `status` reports
recorded evidence and readiness for instructor review; it does not grade,
certify authorship or establish understanding.

## Optional instructor history

The records below are background, not steps to repeat. Their original anchors
remain here so earlier links continue to work.

## HOST-001 · Keep the Traefik dashboard private

[Historical requirement and evidence](book/changes/hosting-spec-history.md#host-001--keep-the-traefik-dashboard-private).

## HOST-002 · Controlled host maintenance

[Historical requirement and evidence](book/changes/hosting-spec-history.md#host-002--controlled-host-maintenance).

## HOST-003 · Companion image security maintenance

[Historical requirement and evidence](book/changes/hosting-spec-history.md#host-003--companion-image-security-maintenance).
