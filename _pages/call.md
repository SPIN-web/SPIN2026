---
layout: home
permalink: /cfp
order: 3
---

# Call for Papers

The SPIN symposium aims at bringing together researchers and practitioners interested in automated tool-based techniques for the analysis of software as well as models of software, for the purpose of verification and validation. The symposium specifically focuses on concurrent software but does not exclude the analysis of sequential software. Submissions are solicited on theoretical results, novel algorithms, tool development, and empirical evaluation.

The SPIN symposium originated as a workshop focusing on explicit state model checking, specifically as related to the SPIN model checker. However, over the years it has evolved to a broadly-scoped symposium for software analysis using any automated techniques, including model checking, automated theorem proving, and symbolic execution. An overview of the previous SPIN symposia (and early workshops) can be found at: [https://spinroot.com/spin/Workshops/](https://spinroot.com/spin/Workshops/).
[Previous Proceedings of SPIN](https://link.springer.com/conference/spin) can be found at Springer's website.

## Topics

Topics of interest include, but are not limited to:

- Formal verification techniques for automated analysis of (concurrent) software/hardware, including:
  - Model checking
  - Deductive verification
  - Automated theorem proving, including SAT and SMT
  - Abstraction and symbolic execution techniques
  - Static analysis and abstract interpretation
  - Modular and compositional verification techniques
  - Verification of timed, probabilistic, hybrid, and quantum systems
  - Automated testing using advanced analysis techniques
  - Program synthesis
  - Derivation of specifications, test cases etc. via formal analysis
  - Formal specification languages, temporal logic, design-by-contract
  - Formal analysis of learned and learning systems
  - Formal and Hybrid Methods in Artificial Intelligence
  - Verification of Spatial and Spatio-Temporal Systems
  - Any combination of the above

- Application and/or engineering of verification tools, including:
  - Case studies of interesting systems or with interesting results
  - Implementation of novel verification tools
  - Benchmarks and comparative studies for verification tools
  - Verification tools using modern hardware, e.g.: multi-core CPU, GPU, TPU, cloud, and quantum

## Important Dates

| Date              | Event                                                                 |
| ----------------- | --------------------------------------------------------------------- |
| January 22, 2026  | Abstract submission deadline                                          |
| January 29, 2026  | Paper submission deadline                                             |
| February 5, 2026  | Artifact submission deadline for tool-related papers (mandatory)      |
| March 5, 2026     | Notification of acceptance (all papers & tool-related artifacts)      |
| March 12, 2026    | Artifact submission deadline for accepted non-tool papers (voluntary) |
| April 9, 2026     | Notification of acceptance for additional artifacts                   |
| April 15–16, 2026 | Symposium                                                             |

<p><em>All deadlines are AoE (anywhere on Earth).</em></p>

## Submission Categories and Guidelines

Papers should be submitted via the EasyChair SPIN 2026 submission website: [https://easychair.org/conferences/?conf=spin2026](https://easychair.org/conferences/?conf=spin2026) in the track _SPIN 2026 Papers_, where you can then select the respective paper category.

The proceedings of SPIN 2026 will be published in Springer's _Lecture Notes in Computer Science_ series. Submissions should adhere to the LNCS format, see Springer's website for [detailed instructions](https://www.springer.com/gp/computer-science/lncs/conference-proceedings-guidelines). Please take into account Springer's [Book authors code of conduct](https://www.springernature.com/gp/authors/book-authors-code-of-conduct) when preparing submissions.

With the exception of survey and history papers, the papers should contain original work that has not been submitted or accepted for publication elsewhere.

We are soliciting three categories of papers:

- **Full Research Papers** describing fully developed work and complete results (16 pages, excluding bibliography and appendices);

- **Full Tool Papers**, accompanied by a **Mandatory Artifact**, describing work that is closely-related to the development or the evaluation of a verification tool or similar (16 pages, excluding bibliography and appendices);
  A submission to this category will be considered for **acceptance only if its accompanying artifact receives at least the Functional Badge**
  in [artifact evaluation](./artifacts.md).

- **Short Papers** presenting tools, technology, experiences with lessons learned, new ideas, work in progress with preliminary results, and novel contributions to formal methods (6 pages, excluding bibliography and appendices). Note: Artifact evaluation is optional for short papers but highly recommended for those with a focus on tools. In the latter case, we recommend submitting the artifact to the mandatory AE deadline.

All papers that conform to submission guidelines will be peer-reviewed by members of the program committee. Submissions will be evaluated on the basis of originality, the importance of contribution, soundness, evaluation, quality of presentation, and appropriate comparison to related work.

At least one author of each accepted paper must attend the symposium and present the paper. Authors will be asked to sign a copyright transfer or alternatively choose an [Open Access](https://www.springer.com/gp/computer-science/lncs/open-access-publishing-in-computer-proceedings) option, subject to a publication fee on behalf of the authors. Some universities may have special arrangements for discounts.

A Best Paper award will be announced and handed out at the conference.

<!-- A selection of the best papers will be invited to a special issue of the [*International Journal on Software Tools for Technology Transfer*](https://sttt.cs.uni-dortmund.de/) (STTT). -->

## Artifact Evaluation

SPIN 2026 will feature artifact evaluation, performed by an Artifact Evaluation Committee (AEC).
The AEC evaluates artifacts based on documentation, availability, reproducibility of results, and tool reusability (if applicable).
Artifact submission is mandatory for **Full Tool Papers**.
While artifact submission is optional for papers in other categories,
we highly encourage authors of papers involving tool development and empirical evaluation to submit an artifact for evaluation.
Papers with an accompanying artifact may be awarded one or more badges from the [EAPLS artifact badging scheme](https://eapls.org/pages/artifact_badges/).
More details can be found on the page about [artifacts]({{ site.baseurl }}{% link _pages/artifacts.md %}).
