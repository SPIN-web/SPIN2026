---
layout: home
permalink: /artifacts
order: 4
---

# Artifact Evaluation for SPIN 2025

For the second time, SPIN 2025 features artifact evaluation (AE),
which is mandatory for all submissions to the category **Full Tool Papers** and strongly encouraged for papers in other categories as well.

## Important Dates

There will be two AE rounds: one for **mandatory** artifact, and one for **non-mandatory** ones.

### Mandatory AE for **Full Tool Papers**:

  |----------------------|-----------------------------------------------------------|
  | February 27, 2025    | Artifact submission deadline                               |
  |    March 6, 2025     | Smoke-test review                                         |
  |    March 9, 2025     | Author response to smoke test                             |
  |    March 24, 2025    | Artifact notification                                     |

<hr style="height:15px; visibility:hidden;" />

### Voluntary AE for **accepted papers** in other categories:

|----------------------|-----------------------------------------------------------|
|   April 7, 2025      | Artifact submission deadline                               |
|   April 14, 2025     | Smoke-test review                                         |
|   April 17, 2025     | Author response to smoke test                             |
|     May 1, 2025      | Artifact notification                                     |



## Artifacts and Evaluation Criteria

An artifact is any additional material (software, data sets, machine-checkable proofs, etc.)
that substantiates the claims made in the paper and ideally renders them fully reproducible.
For example, an artifact might consist of a tool and its documentation,
input files used for tool evaluation in the paper,
and configuration files or documents describing parameters used in the experiments.

The Artifact Evaluation Committee (AEC) will read the corresponding paper and evaluate the artifact according to the following criteria:

- consistency with and reproducibility of results presented in the paper
- completeness
- documentation and ease of use
- availability in a permanent online repository (ideally, with a Digital Object Identifier (DOI))

The evaluation will be based on the [EAPLS guidelines](https://eapls.org/pages/artifact_badges/), and the AEC will decide which of the badges — among Functional, Reusable, and Available — will be assigned to a given artifact.
The corresponding badges will be added to the title page of the paper in case of acceptance.

## Submission Guidelines

Artifacts should be submitted via the EasyChair SPIN 2025 submission website:
[https://easychair.org/conferences/?conf=spin2025](https://easychair.org/conferences/?conf=spin2025) in the track _Artifacts_.

The following information should be provided in your EasyChair submission:

1. Artifact submission should have the same title and authors as the submitted/accepted paper.
2. Upload a PDF file of the submitted/accepted paper.
3. The abstract should summarize the content of the artifact and its relation to the paper. In particular, the abstract should:
   - provide an URL (preferably a DOI) to a publicly available zipped archive containing the artifact and all relevant files
   - provide a SHA256 checksum of the zipped archive file to ensure consistency; The checksum can be generated with:
     - Linux: `sha256sum <file>`
     - Windows: `CertUtil -hashfile <file> SHA256`
     - MacOS: `shasum -a 256 <file>`
   - (if required) discuss special requirements for running the artifact (specific hardware resources, installation of proprietary software, etc.)
   - clearly state which claims of the paper are supported by the artifact. If some claims cannot be reproduced, shortly justify the reasons.

## Artifact Guidelines

The artifact should be a self-contained package runnable either on the [TACAS 23 Artifact Evaluation VM](https://doi.org/10.5281/zenodo.7113223) (VM) or in a Docker/Podman container provided by the authors.
Authors should test their artifact on the VM or in the container prior to the submission and include all relevant instructions.
Instructions should be clear and specify every step required to build and run the artifact, assuming no specific knowledge and including steps that the authors might consider trivial (e.g., building steps for the container).

In particular, the artifact should contain:

- A file `License.txt` containing the license for the artifact. The license must at least allow the AEC to evaluate the artifact w.r.t. the criteria mentioned above.
- A README file containing:
  - detailed step-by-step instruction for an early light review (smoke test) that allows reviewers to: (1) verify that the artifact can properly run; and (2) perform a short evaluation of the artifact before the full evaluation and detect any difficulties
  - detailed step-by-step instructions for use of the artifact and reproduction of results in the paper, including the estimated reproduction time
- all code, binaries, example files, documentation, scripts, etc., required to reproduce the results in the paper.

In principle, we require authors to supply a completely self-contained artifact to ensure long-term availability.
**Namely, no internet access is allowed in the VM or container.**
If internet access is strictly necessary for your artifact, please contact the AEC chairs.

### VM

We recommend to prepare the artifact based on the [TACAS 23 Artifact Evaluation VM](https://doi.org/10.5281/zenodo.7113223).
The virtual machine is based on an Ubuntu 22.04 LTS image with the following additional packages: `build-essential`, `cmake`, `clang`, `mono-complete`, `openjdk-8-jdk`, `python3.10`, `pip3`, `ruby`, and a 32-bit `libc`.
VirtualBox guest additions are installed on the VM; it is therefore possible to connect a shared folder from the host computer.

The instructions must include all necessary steps for the installation and setup on the "clean" TACAS-23 VM
(**Do not submit the modified VM!**).
In the best case, the authors would set up a script which performs all or almost all steps for the setup of their tool in the VM automatically.
In particular, authors should not rely on instructions provided by external tools.

### Container

An artifact built on Docker or Podman should include a Dockerfile that automates setup from a base image, such as Ubuntu. To ensure long-term availability and offline accessibility, please also submit the generated container image.

## Artifact Preparation Suggestions

In the following, we list some general suggestions for preparing the artifact:

- Keep the reproduction simple through easy-to-use scripts and detailed instructions.
- When writing step-by-step instructions, assume minimum expertise of users.
- Document in detail how to reproduce most, or ideally all, of the experimental results of the paper using the artifact.
- State resource requirements and/or the environment in which you successfully tested the artifact.
- For experiments requiring a large amount of resources, we strongly recommend providing a way to reproduce a representative subset of results such that results can be reproduced on various hardware platforms in reasonable time. Do include the full set of experiments for those reviewers with sufficient hardware or time.
- Do not submit a virtual machine; only submit your files, which AEC members will copy into the provided virtual machine.
- For the “Available” badge, you must upload your artifact to a permanent repository (e.g. [Zenodo](https://zenodo.org/), [figshare](https://figshare.com/), or [Dryad](https://datadryad.org/)) that provides a Digital Object Identifier (DOI), and use that link in your submission. This excludes other repositories such as an institutional or personal website, source code hosting services, or cloud storage.
- In case the artifact cannot comply with some of the guidelines, please do not hesitate to contact the AEC chairs before the AE submission deadline. An example is proprietary software such as Matlab.

## Artifact Evaluation Committee

TBA
