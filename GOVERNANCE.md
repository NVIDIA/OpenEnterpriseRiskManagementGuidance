# Joint Approval and Maintainership

This repository is published jointly by NVIDIA and Microsoft. It sits in the NVIDIA
GitHub organization and is co-maintained by both companies. This document states who
approves what, and what "jointly approved" means for the artifacts published here.

## Maintainers

Maintainership is held by named individuals at each organization, not by the
organizations in the abstract. The current maintainer sets are defined in
[`CODEOWNERS`](.github/CODEOWNERS) as two GitHub teams:

| Team | Organization | Scope |
|---|---|---|
| `@NVIDIA/openerm-maintainers` | NVIDIA | All paths |
| `@NVIDIA/openerm-maintainers-msft` | Microsoft | All paths |

Editors of the current publication are Andrew Berkley (Microsoft), April Chen
(Microsoft), Michael Boone (NVIDIA), Eileen Long (NVIDIA), and Arun Rao (NVIDIA).

## What requires joint approval

**Dual approval — one maintainer from each organization.** These artifacts carry the
joint Microsoft–NVIDIA name, and neither company publishes a change to them alone:

- `Papers/` — any new paper, and any revision to a published paper, including the PDF
  and its entry in `Papers/CHANGELOG.md`.
- `Taxonomy/` — risk categories (L1), risk types (L2), and risk definitions.
- `Evaluations/` — additions, removals, and re-mappings in the evaluations index, and
  any change to how an evaluation is attributed or described.
- `Mitigations/` — controls, and the system layer (model, runtime, harness,
  application) a control is assigned to.
- `README.md`, this file, `CONTRIBUTING.md`, `CITATION.cff`, `LICENSE`, `security.md`.

**Single approval — any maintainer.** Everything else: typo and link fixes that do not
change meaning, formatting, repository tooling, issue and PR templates, and CI
configuration.

A reviewer may escalate a single-approval change to dual approval at their discretion.
When in doubt, request both.

## How approval is recorded

1. Changes land through pull requests. Direct pushes to `main` are disabled.
2. `CODEOWNERS` requires review from both maintainer teams on the paths listed above;
   branch protection requires those reviews before merge.
3. The approving reviews on the pull request are the record of joint approval. Approval
   given in email, chat, or a meeting is not sufficient on its own — a maintainer who
   has that approval states it in the pull request and approves there.
4. For a paper revision, both organizations' approvals must be on the pull request that
   carries the final PDF, not on an earlier draft of it.

## Publishing a paper revision

1. Open a pull request containing the revised PDF and the new `CHANGELOG.md` section
   describing the revision.
2. Both organizations' maintainers review the diff of the paper content, not only the
   changelog. For a PDF, include an extracted-text diff in the pull request body so
   reviewers can see what changed.
3. On dual approval, merge. The merge commit is the publication event, and the
   changelog entry cites it.
4. Do not amend a published PDF in place without a changelog entry. Every published
   revision gets its own entry.

## Becoming a maintainer

Third-party contributors are welcome and may become maintainers. The path:

1. A sustained record of merged, substantive contributions — typically several accepted
   evaluation mappings, risk type proposals, or mitigation entries.
2. Nomination by an existing maintainer in a public issue.
3. Agreement from a maintainer at each organization. Maintainership is granted by
   adding the contributor to the maintainer team of the organization that nominated
   them, or to a third-party maintainer team with the same path scope.

Maintainers who are inactive for six months may be moved to emeritus status by dual
approval and restored on request.

## Disagreement between organizations

If the two organizations' maintainers do not agree on a change, the change does not
merge. Unresolved disagreements on taxonomy or evaluation content are documented in the
issue so the reasoning is public, and the existing published artifact stands unchanged
until agreement is reached.

## Licensing and contribution terms

Contributions are accepted under the repository
[`LICENSE`](LICENSE). By opening a pull request, a contributor confirms they have the
right to submit the work under that license and that it is not subject to third-party
terms that conflict with it. See [`CONTRIBUTING.md`](CONTRIBUTING.md).

Security issues are not reported through pull requests or public issues; follow
[`security.md`](security.md).
