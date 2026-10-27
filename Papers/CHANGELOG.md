# Changelog — *Risk Management for Open-Weight Models in Enterprise*

All notable changes to `Papers/Risk Management Guidance.pdf` are recorded here.

The paper is a joint Microsoft–NVIDIA publication. Version numbers below are assigned
retroactively to the uploads already in the repository history; dates are the UTC commit
dates of the file in
[NVIDIA/OpenEnterpriseRiskManagementGuidance](https://github.com/NVIDIA/OpenEnterpriseRiskManagementGuidance).

| Version | Date (UTC) | Commit | Pages |
|---|---|---|---|
| 1.0 | 2026-10-15 | [`cf06442`](https://github.com/NVIDIA/OpenEnterpriseRiskManagementGuidance/commit/cf06442df59758ab69d83d822ca1586d3e7dc2c4) | 22 |
| 0.2 | 2026-10-15 | [`2c0a6c7`](https://github.com/NVIDIA/OpenEnterpriseRiskManagementGuidance/commit/2c0a6c74a2) | 22 |
| 0.1 | 2026-10-13 | [`d1c251c`](https://github.com/NVIDIA/OpenEnterpriseRiskManagementGuidance/commit/d1c251cf54) | 23 |

---

## [1.0] — 2026-10-15 — Public release

### Changed
- Repository URL corrected throughout from `github.com/NVIDIA/OpenERMGuidance` to
  `github.com/NVIDIA/OpenEnterpriseRiskManagementGuidance`, in both the contribution
  note following "Editors and Contributors" and the "How to Cite" entry.
- "How to Cite" entry now names the editors: *Edited by Andrew Berkley, April Chen,
  Michael Boone, Eileen Long, and Arun Rao.*
- Appendices A and B merged into a single "Appendix" containing the evaluation mapping
  table and the risk definitions; the cross-reference in §3.4 was updated to point at
  "the Appendix" rather than at Appendix B and Appendix A individually.
- Figure 1 caption shortened from "Risk Taxonomy (October 2026)" to "Risk Taxonomy";
  the taxonomy version is now carried by the publication date rather than the figure.
- Appendix evaluation table (Table 1) re-laid out so risk categories, risk types,
  descriptions, and evaluation methods align row-by-row; the preceding version's
  column drift had separated several descriptions from their risk types.
- Groundedness and Hallucinations split into two separate rows in Table 1
  (Groundedness; Hallucinations), rather than one combined
  "Groundedness/Hallucinations" entry.
- Modified BBQ attributed in two places in Table 1: "Modified BBQ (NVIDIA)" against
  Ideological Bias, and "Modified BBQ (Geopolitical, Political & Religious Bias)"
  against the Bias category.
- Contents entries renumbered for the merged appendix.

## [0.2] — 2026-10-15 — Reformatted for external publication

### Added
- Title page: "A Joint Microsoft and NVIDIA Publication", October 2026.
- Abstract summarizing the taxonomy, the ISO/IEC- and NIST-derived risk management
  guidance, the worked example, and the paper's place as the first in the series.
- Keyword list (open-weight models; AI risk management; risk taxonomy; AI governance;
  AI safety; AI security; model evaluation; red teaming; NIST AI RMF; ISO/IEC 23894;
  ISO/IEC 42001; enterprise AI deployment).
- Table of contents with page numbers, and page numbering throughout.
- "How to Cite" section following the Editors and Contributors list.
- Executive Summary: new paragraph separating model access from deployment —
  open-weight models can also be deployed through managed platforms, with
  responsibility for controls depending on the service and configuration.
- Executive Summary: new paragraph stating that model evaluation alone does not
  establish the safety of an agent or application, and that enterprises must also
  assess permissions, data access, connected tools, runtime behavior, and operational
  controls in the deployed system.
- §4.4 Evaluations: paragraph on Microsoft Foundry's built-in evaluators, support for
  custom evaluation criteria, automated red teaming, and configurable content-safety
  controls, with the caveat that deployers should confirm which controls their
  deployment supports, including preview status, and complement them with application
  testing, monitoring, and human oversight.
- Appendix: "Sexual Content, Including Non-Consensual Sexual Imagery" added as a
  distinct row in the evaluation mapping table.

### Changed
- **Framing of open- vs. closed-weight risk.** "Neither open-weight nor closed-weight
  AI models are inherently more or less risky" replaced with "Weight openness alone
  does not determine an AI system's risk. Risk depends on the model, use case,
  deployment, and safeguards." The same replacement was made in the Conclusion, where
  "open-weight models are [not] inherently more dangerous than closed-weight models"
  became the "weight openness alone does not determine an AI system's risk" formulation.
- NIST framework abbreviated consistently as "AI RMF" rather than "RMF".
- §4.2 citation corrected to NIST SP 800-37 / SP 800-30 (previously cited as
  "RMF/SP 800-30 ... 800-37").
- Evaluation mapping table renamed from "Appendix — Evaluation Resources" to
  "Appendix A. Risk Categories Mapped to Evaluations", with the caption
  "Table 1: Evaluations mapped to a selected set of risk types"; risk definitions
  became "Appendix B. Risk Definitions".
- Table 1 risk-type labels aligned with the Appendix B definitions:
  "Insecure Code Generation" → "Malicious Code Generation (Malicious Code Execution
  Risk)"; "Loss Of Control" → "Misaligned Generation against System Goal
  (Loss of Control Risk)".
- Table 1 content rows consolidated: "Hate & Harassment, and Violence" →
  "Hate, Harassment, and Violence"; the separate "Suicide & Self-Harm" row folded into
  harmful-content types "including self-directed harm".
- Footnote on Risk Source corrected: "trigger a comprising event" →
  "trigger a compromising event".
- Spelling normalized to US English throughout the risk definitions (authorised →
  authorized, behaviour → behavior, organisation → organization, licence → license,
  memorised → memorized, recognisable → recognizable, dehumanises → dehumanizes,
  marginalised → marginalized, favouring → favoring, categorising → categorizing).
- Footnotes renumbered after the "Enterprise" definition moved from an asterisked note
  under the Executive Summary to footnote 1.
- Em-dash separators in the contributor list replaced with colons
  ("Microsoft —" → "Microsoft:", "NVIDIA —" → "NVIDIA:").
- Bulleted lists in §2.1 and elsewhere given consistent bullet glyphs and font
  alignment; hyphenation and line breaks reflowed throughout.
- "Approved risk tolerances and criterion" → "criteria".

### Removed
- "Classified as Microsoft-NVIDIA Confidential" page markings on every page.
- Jailbreaking row from the evaluation mapping table (HarmBench, StrongREJECT), along
  with its description of adversarial prompts circumventing safeguards — consistent
  with §3.4, which excludes attack techniques such as jailbreaking and prompt injection
  from the taxonomy itself.
- Asterisk notation and its explanatory note marking risk types whose risk may extend
  beyond the model layer to the runtime and harness.

## [0.1] — 2026-10-13 — Initial internal draft published to the repository

### Added
- Executive Summary; §2 Definitions and Scope (existing frameworks, risk definition and
  scope); §3 Risk Taxonomy (overview, structure, risk categories, current taxonomy and
  future updates); §4 Risk Management Process Guidance (scope/context/criteria, risk
  assessment, evaluations, risk mitigation, monitoring); §5 worked enterprise use case;
  §6 Conclusion.
- Appendix: Evaluation Resources table and risk definitions.
- Editors and Contributors list for Microsoft and NVIDIA.

---

### Maintaining this file
Add a new section at the top for each published revision of the PDF, newest first, using
the Added / Changed / Removed headings above. Link the commit that introduced the
revision. Substantive changes — taxonomy risk types, evaluation mappings, or risk
definitions — require approval from a maintainer at each organization before the
revision is published; see the joint approval README.
