# OpenEnterpriseRiskManagementGuidance

## Risk Management for Open-Weight Models
Open-weight models give enterprises greater control to inspect, evaluate, modify, and operate models in their own environments. This flexibility also changes how models are evaluated, where safeguards are applied, and who maintains them over time. 

This joint NVIDIA–Microsoft repository offers resources to help enterprises deploy open-weight models safely, securely, and responsibly. The repository is organized as follows.

### Papers
Guidance papers to support risk management and governance of open-weight model deployments.

### Taxonomy
The risk taxonomy provides a shared vocabulary for how risks arise in AI systems, grouping risk types (L2) under broader risk categories (L1) to support effective management. It will be updated regularly as new risks emerge.

### Evaluations
Maps evaluations to the risk taxonomy and will be updated regularly with open-source benchmarks, evaluations published by NVIDIA and Microsoft, and community contributions.

### Mitigations
Controls, organized by system layer (model, runtime, harness, and application).

## Contributing
We encourage developers, security practitioners, researchers, and others working in this space to contribute evaluations that can help strengthen this shared body of work. Open a propose-evaluation issue with the risk type it addresses, the task and language it covers, its scoring method, and its known limitations. Mapping gaps and new risk types are equally welcome.

See [CONTRIBUTING.md](CONTRIBUTING.md) for what a proposal needs to include and how pull requests are reviewed.

## Maintainership
This repository sits in the NVIDIA org and is co-maintained by NVIDIA and Microsoft. Changes to the papers, taxonomy, evaluations, and mitigations require approval from a maintainer at each organization; [CODEOWNERS](.github/CODEOWNERS) enforces this. Everything else follows ordinary single-approval review.

[GOVERNANCE.md](GOVERNANCE.md) sets out the approval rules in full, how a paper revision is published, and how a third-party contributor becomes a maintainer.

## Citing this work

Microsoft and NVIDIA. *Risk Management for Open-Weight Models in Enterprise.* Edited by Andrew Berkley, April Chen, Michael Boone, Eileen Long, and Arun Rao. Version 1.0, October 2026. https://github.com/NVIDIA/OpenEnterpriseRiskManagementGuidance

The paper: [Risk Management Guidance.pdf](Papers/Risk%20Management%20Guidance.pdf) · revision history: [Papers/CHANGELOG.md](Papers/CHANGELOG.md) · further citation formats: [CITATION.md](CITATION.md)

<details>
<summary>BibTeX</summary>

```bibtex
@techreport{msft_nvidia_2026_openweight,
  author = {{Microsoft} and {NVIDIA}},
  editor = {Berkley, Andrew and Chen, April and Boone, Michael and Long, Eileen and Rao, Arun},
  title = {Risk Management for Open-Weight Models in Enterprise},
  institution = {Microsoft and NVIDIA},
  year = {2026},
  month = oct,
  version = {1.0},
  url = {https://github.com/NVIDIA/OpenEnterpriseRiskManagementGuidance}
}
```

</details>
