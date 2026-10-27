# Contributing

We welcome contributions from developers, security practitioners, researchers, policy
teams, and anyone else working on open-weight model risk. The most useful contributions
are evaluations mapped to the risk taxonomy, gaps in that mapping, and new or refined
risk types.

Before contributing, read [`GOVERNANCE.md`](GOVERNANCE.md) — this repository is
co-maintained by NVIDIA and Microsoft, and changes to the taxonomy, evaluations,
mitigations, and papers require approval from a maintainer at each organization.

## Ground rules

- **Open an issue first** for anything beyond a typo or broken link. Proposals are
  discussed in the issue before a pull request is opened, so contributors do not spend
  effort on a change that is out of scope.
- **One change per pull request.** A new evaluation mapping and a taxonomy revision are
  two pull requests.
- **Cite sources.** Every factual claim about an evaluation, benchmark, or risk needs a
  citation to a paper, dataset card, repository, or standard. Unsourced claims are not
  merged.
- **No confidential or proprietary material.** Do not submit anything you are not free
  to publish under this repository's license, including internal evaluation results,
  unreleased model behavior, or customer data.
- **No vulnerability reports.** Security issues go through [`security.md`](security.md),
  not through issues or pull requests.
- **No unredacted harmful content.** Prompts and examples that demonstrate a harm should
  be described, referenced, or truncated — not reproduced in full.

## Proposing an evaluation

Open a *propose-evaluation* issue. Required:

| Field | What to provide |
|---|---|
| Evaluation name | As it is published, with the version or release date |
| Source | Paper, repository, or dataset URL; DOI where one exists |
| Risk type(s) | The L2 risk type(s) from the taxonomy it exercises, and the L1 category |
| Task and modality | What the model is asked to do; text, code, image, audio, multimodal |
| Languages and locales | Covered, and known coverage gaps |
| Scoring method | Automated classifier, exact match, human rating, LLM judge — and the judge model if applicable |
| Reported reliability | Inter-rater agreement, judge validation, or test-retest figures, where published |
| License and access | How others obtain the data and under what terms |
| Known limitations | Saturation, contamination risk, distribution shift, label noise, cultural scope |

An evaluation is mapped to the narrowest risk type it genuinely measures. If it
measures several, say so and justify each mapping. "Related to" is not a mapping.

## Proposing a taxonomy change

Risk categories (L1) are intended to remain stable; risk types (L2) are expected to
change as the risk landscape evolves. A proposal should state:

- The proposed risk type name and a one-paragraph definition in the style of the
  existing definitions in the paper's appendix.
- The L1 category it belongs under, and why it is not covered by an existing L2 type.
- Evidence the risk is realized in deployed systems — incidents, published research, or
  evaluation results.
- The system layer(s) where it arises: model, runtime, harness, or application.
- At least one evaluation that could detect it, or an explicit statement that none is
  known.

Attack techniques — jailbreaking, prompt injection, adversarial suffixes, token-level
and Unicode tricks — are deliberately out of scope for the taxonomy, which describes
risks rather than the methods used to trigger them. Proposals framed as techniques will
be redirected to the risk they produce.

## Proposing a mitigation

State the control, the system layer it applies at, the risk type(s) it reduces, what it
does not cover, and its cost in utility or latency where known. Controls that have been
measured are preferred over controls that are merely recommended; include the
measurement.

## Corrections to a published paper

Open an issue describing the error and the correction, with a source. Accepted
corrections are published as a new revision of the PDF with an entry in
[`Papers/CHANGELOG.md`](Papers/CHANGELOG.md). Published revisions are not amended
silently.

## Pull request requirements

- Branch from `main`; keep the branch current with `main` before requesting review.
- Reference the issue the pull request resolves.
- Describe what changed and why in the pull request body. For a change to a PDF, include
  an extracted-text diff so reviewers can see the content change.
- Sign your commits (`git commit -S`) if your organization requires it; unsigned commits
  are accepted otherwise.
- Expect review from maintainers at both organizations on taxonomy, evaluations,
  mitigations, and papers. Review may take longer than for a single-owner repository;
  this is by design.

## Licensing

By submitting a contribution you confirm that you have the right to submit it and that
it may be published under the repository's [`LICENSE`](LICENSE). Do not submit material
encumbered by terms that conflict with that license, including content copied from
sources with incompatible licensing.

## Code of conduct

Discussion stays on the substance of the risk, the evidence, and the evaluation. Treat
other contributors professionally. Maintainers may close or lock threads that do not.
