---
layout: home
permalink: /AE_instructions
order: 0
---

# Artifact Evaluation — Reviewer Instructions

First, please carefully read the [call for artifacts](./artifacts.md)
and check if the artifact under evaluation adheres to the instructions for authors.

Below are the instructions for artifact reviewers.

## Important Dates

There will be two rounds of reviews:
the first round for mandatory artifacts of **Regular Tool Papers**,
and the second round for voluntary artifacts of other papers.
Please stay in contact during both AE periods as some reviewers may be assigned artifacts from both categories.

### Mandatory Artifacts:

|----------------------|-----------------------------------------------------------|
| February 3, 2026 | Artifact submission deadline |
| February 6, 2026 | Artifact bidding due |
| February 11, 2026 | Smoke-test reviews due |
| February 14, 2026 | Author responses due (with possible fixes to artifacts) |
| February 24, 2026 | Full reviews due |
| February 25-28, 2026 | AEC discussion |
| March 04, 2026 | Artifact notification |

### Voluntary Artifacts:

|----------------------|-----------------------------------------------------------|
| March 16, 2026 | Artifact submission deadline |
| March 19, 2026 | Artifact bidding due |
| March 23, 2026 | Smoke-test reviews due |
| March 26, 2026 | Author responses due (with possible fixes to artifacts) |
| March 31, 2026 | Full reviews due |
| April 1-3, 2026 | AEC discussion |
| April 9, 2026 | Artifact notification |

## Artifact Bidding

In artifact evaluation, we aim to evaluate the degree to which the artifact supports the claims of the paper
but not the novelty or significance of the claims themselves.
Therefore, you do not need to be an expert in the topics of the paper (as opposed to paper bidding).
When placing your bids, please prioritize your ability and confidence to execute (and spot potential issues of) the artifact
based on its packaging (VM or container) and the environment (Linux, MacOS, or Windows) that the authors tested the artifact.
**In principle, please bid all artifacts that you are able/have enough resources to test.**

## Smoke Test

Smoke tests are used to spot technical issues (e.g., installation) and allow authors to fix minor problems in their artifacts.
The review should be uploaded on EasyChair, clearly indicating that it is related to the smoke test. 
In your smoke-test reviews, please report whether you are able to set up the artifact and run the tests provided by authors.
Ideally, the authors should also provide the expected outputs of these tests so that
reviewers can easily compare the obtained results on their machines to the expected results.
If the smoke tests failed on your machines, clearly document the error messages for authors to debug.
The smoke-test phase is the only interaction with the authors.
**Please make sure you can evaluate the artifact by the end of this phase.**

## Full Evaluation

In this stage, your goal is to reproduce the data reported in the paper by the artifact.
The review should be uploaded on EasyChair (by editing the previous one), it is related to the full evaluation. 
Please read the evaluation section of the paper carefully to understand its experimental design.
(It would be nice to also browse through the proposed approach,
but it is not strictly necessary to figure every technical detail.)
Identify the claims the artifact supports, and generate the data using the corresponding commands given by the authors.
The authors should clearly state how to reproduce each claim in the paper,
including any necessary post-processing steps.
Remember to allocate enough time for the evaluation.
**Ideally, you should be able to reproduce the data and compare them to those reported by the authors.**

## Your Review

In your final reviews, please clearly state which badges you recommend and the corresponding justifications.
Please familiarize yourself with the [EAPLS guidelines](https://eapls.org/pages/artifact_badges/).
Below we summarize the crucial assessment criteria:

- **Available Badge**: The artifact is archived in a public long-term preserving platform (e.g., Zenodo) and has a DOI;
  it is relevant to the paper and adds value beyond the text in the article.
- **Functional Badge**: The artifact is complete (all required dependencies bundled), exercisable (can produce results),
  consistent (the produced results matched those in the paper), and documented (enough descriptions for reproduction).
- **Reusable Badge**: The artifact meets the requirement of the Functional Badge and is very well-structured/documented
  to facilitate reusing or repurposing some or all parts of the artifact.
  (For example, one can use the artifact to perform experiments for another different paper.)

Note on the consistency of results:
It is very likely that the results reproduced by you with the artifact do not match exactly with the results reported in the paper
(e.g., due to different machines).
Therefore, when evaluating the consistency, focus on trends rather than the exact numbers.
