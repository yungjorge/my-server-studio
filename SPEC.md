# Lesson 01 specification

## STUDIO-001 · Launch a tested calculator on an existing server

**Status:** New launch verified; full PR CI passed for the implementation commit. Learner review pending.
**Next step:** Confirm your clone with the coach, then follow [Lesson 01](studio/lesson-01.md).
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

- **Public hostname:** https://calc.104-248-208-29.nip.io
- **New launch or adopted deployment, and reason:** New launch; doctor found no conflicting route.
- **Own issue / feature branch:** [#1](https://github.com/yungjorge/my-server-studio/issues/1) / codex/studio-001.
- **Agreed scope:** One pinned image on the existing is373-qa proxy network, using the existing le resolver. No proxy changes or public container port.

Private SSH targets and configuration stay in ignored local state. Share only
reviewed, selected evidence; never commit credentials or raw server output.

## Evidence to keep

| Evidence | Actual result / link |
|---|---|
| Prepared Black/Pylint/pytest and real-image browser checks | Black, Pylint and 91 tests passed locally; browser E2E passed in [PR CI](https://github.com/yungjorge/my-server-studio/actions/runs/42335741107) for implementation commit 70122bf |
| Hosted image/commit, trusted HTTPS, valid and rejected API cases | [Launch evidence](studio/evidence.json): trusted HTTPS, matching image and commit, 6 × 7 = 42 (200), division by zero (400), numeric string rejected (422). |
| Preservation of unrelated services | All three existing containers unchanged; QA and production health returned OK after launch. |
| Own prediction, check interpretation, browser observation and keep/revise reason | [LEARNING.md](LEARNING.md), Pending; disclose assistance |
| Accuracy review before publishing learner excerpts | Pending |
| Actual PR, CI, merge and issue closure | [PR #2](https://github.com/yungjorge/my-server-studio/pull/2); [passing implementation CI](https://github.com/yungjorge/my-server-studio/actions/runs/42335741107); merge and issue closure pending |

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
