---
layout: home
permalink: /artifacts
order: 4
---

# Artifact Evaluation

For the second time, SPIN 2026 features artifact evaluation (AE),
which is mandatory for all submissions to the category **Full Tool Papers** and strongly encouraged for papers in other categories as well.

Note that a submission to **Full Tool Papers** will be considered for acceptance
only if its accompanying artifact receives at least the **Functional Badge** in artifact evaluation.
(The evaluation results of a non-mandatory artifact will not influence the acceptance of the corresponding paper.)

## Important Dates

There will be two AE rounds: one for **mandatory** artifacts, and the other for **non-mandatory** ones.

### Mandatory AE for **Full Tool Papers**:

|----------------------|-----------------------------------------------------------|
| January 25, 2026 | Artifact submission deadline |
| February 6, 2026 | Smoke-test review |
| February 9, 2026 | Author response to smoke test |
| February 19, 2026 | Artifact notification |

<hr style="height:15px; visibility:hidden;" />

### Voluntary AE for **accepted papers** in other categories:

TBA

## Artifacts and Evaluation Criteria

An artifact is any additional material (software, data sets, machine-checkable proofs, etc.)
that substantiates the claims made in the paper and ideally renders them fully reproducible.
For example, an artifact might consist of a tool and its documentation,
input files used for tool evaluation in the paper,
and configuration files or documents describing parameters used in the experiments.

The Artifact Evaluation Committee (AEC) will evaluate the artifact according to the following criteria:

- consistency with and reproducibility of results presented in the paper
- completeness (does the artifact support every claim in the paper, or only some)
- documentation and ease of use
- availability in a long-term archiving repository (ideally, with a Digital Object Identifier (DOI))

The evaluation will be based on the [EAPLS guidelines](https://eapls.org/pages/artifact_badges/), and the AEC will decide which of the badges — among Functional, Reusable, and Available — will be assigned to a given artifact.
The corresponding badges will be added to the title page of the paper in case of acceptance.

**Important**

All AEC members: please read the [**reviewer instructions**](./AE_instructions.md) carefully.

We also recommend artifact authors go through the instructions
so that you know how reviewers will evaluate your submission and can prepare a better artifact accordingly.

## Submission Guidelines

Artifacts should be submitted via the EasyChair SPIN 2026 submission website:
[https://easychair.org/conferences/?conf=spin2026](https://easychair.org/conferences/?conf=spin2026) in the track _Artifacts_.

The following information should be provided in your EasyChair submission:

1. Artifact submission should have the same title and authors as the submitted/accepted paper.
2. Upload a PDF file of the submitted/accepted paper.
3. The abstract should summarize the content of the artifact and its relation to the paper. In particular, the abstract should:
   - provide a URL (preferably a DOI) to a publicly available zipped archive containing the artifact and all relevant files
   - provide a SHA256 checksum of the zipped archive file to ensure consistency; The checksum can be generated with:
     - Linux: `sha256sum <file>`
     - Windows: `CertUtil -hashfile <file> SHA256`
     - MacOS: `shasum -a 256 <file>`
   - (if required) discuss special requirements for running the artifact (specific hardware resources, installation of proprietary software, etc.)
   - clearly state which claims of the paper are supported by the artifact. If some claims cannot be reproduced, shortly justify the reasons.

## Packaging Guidelines

The artifact should be a self-contained package runnable on the [TACAS 23 Artifact Evaluation VM](https://doi.org/10.5281/zenodo.7113223) (VM)
or a container image (Docker/Podman) provided by the authors.
Authors should test their artifact on the VM or in the container prior to the submission and include all relevant instructions.
Instructions should be clear and specify every step required to build and run the artifact,
assuming no specific knowledge and including steps that the authors might consider trivial (e.g., building steps for the container).

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

We recommend authors prepare the artifact based on the [TACAS 23 Artifact Evaluation VM](https://doi.org/10.5281/zenodo.7113223).
The VM is based on an Ubuntu 22.04 LTS image with the following additional packages: `build-essential`, `cmake`, `clang`, `mono-complete`, `openjdk-8-jdk`, `python3.10`, `pip3`, `ruby`, and a 32-bit `libc`.
VirtualBox guest additions are installed on the VM; it is therefore possible to connect a shared folder from the host computer.

The instructions must include all necessary steps for the installation and setup on the "clean" TACAS-23 VM
(**Do not submit the modified VM!**).
In the best case, the authors would provide a script to perform all or almost all steps for the setup of their tool in the VM automatically.
In particular, authors should not rely on instructions provided by external tools.

In case of technical difficulties for your artifact to run on the TACAS VM,
and you prefer submitting a whole VM image (OVF/OVA), please contact the AEC chairs in advance.

### Container

A container-based artifact should include a Dockerfile that automates setup from a base image, such as Ubuntu. To ensure long-term availability and offline accessibility, please also submit the generated container image.

## Documentation Guidelines

### Recommended README Structure

- **Abstract**: briefly mention the paper that the artifact supports, the content of the artifact, where to find the artifact (e.g., DOI), which claims in the paper are supported, resource requirements of the artifact, etc.
- **List of content**: briefly describe each file/folder in the artifact
- **Environmental setup**: explain the hardware requirements, software dependencies, and installation steps of the artifact;
  an installation script and a sanity check to test if the setup was successful are highly recommended.
- **Smoke test**: provide commands to run the artifact with small examples and the **expected outputs** of the executions;
  the reviewers should be able to easily check if the artifact has been set up successfully by running these smoke tests.
- **Full reproduction**: provide commands to reproduce the reported results in the paper;
  ideally, the authors should specify which claim, figure, table, etc., can be reproduced by what command and
  explain how to interpret the generated data.
  - If a complete reproduction of the results in your paper requires high resources (e.g., months of CPU time),
    please prepare a demo experiment that can be finished by a common computer in reason time (e.g., one day).
  - If your experiments involve randomness, we recommend fixing the random seed in your artifact to facilitate the comparison.
- **Data analysis**: in case the generated data requires post-processing, include the scripts and explain their usage;
  we recommend submitting the data obtained in your own experiments (e.g., all the log files and measurements) for comparison.
- **Complete logs**: for trouble shooting, we recommend appending the complete logs of commands used by the artifact.
- **Trouble shooting and/or known issues**: document how to trouble-shoot and/or known issues of the artifact if any

### Additional Tips

- Keep the reproduction simple through easy-to-use scripts and detailed instructions.
- When writing step-by-step instructions, assume minimum expertise of users.
- State resource requirements and/or the environment in which you successfully tested the artifact.
- Specify the amount of time needed/expected for each step.
- For experiments requiring a large amount of resources, we strongly recommend providing a way to reproduce a representative subset of results such that results can be reproduced on various hardware platforms in reasonable time. Do include the full set of experiments for those reviewers with sufficient hardware or time.
- For the “Available” badge, you must upload your artifact to a permanent repository (e.g. [Zenodo](https://zenodo.org/), [figshare](https://figshare.com/), or [Dryad](https://datadryad.org/)) that issues a DOI, and use that link in your submission. This excludes other repositories such as an institutional or personal website, source code hosting services, or cloud storage.
- In case the artifact cannot comply with some of the guidelines, please do not hesitate to contact the AEC chairs before the AE submission deadline. An example is proprietary software such as Matlab.

