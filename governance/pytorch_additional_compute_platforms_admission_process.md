# PyTorch Foundation Additional Compute Platforms Admission Process

## Introduction

The PyTorch Foundation recognizes the importance of compute platforms in expanding PyTorch's reach across diverse computing environments. Out-of-tree compute platforms play a critical role in enabling PyTorch workloads on a wide range of hardware, and their visibility within the PyTorch community benefits both compute platform vendors and PyTorch users.

To ensure that compute platforms presented on the PyTorch community Additional Compute Platforms page meet a consistent standard of quality, maturity, and community value, the Accelerator Integration Working Group has established this governance process for admitting compute platforms to the Additional Compute Platforms page on the [pytorch.org](http://pytorch.org) website. This document defines the admission requirements, admission process, and lifecycle management for compute platforms to be posted and removed from the Additional Compute Platforms page.

## Purpose and Scope

This process governs the admission and ongoing management of compute platforms that wish to be listed on the PyTorch Additional Compute Platform webpage so that users may discover the appropriate packages for the compute platforms that they are looking for PyTorch support for. It aims to:

* Ensure listed compute platforms meet a minimum bar of quality, stability, and usability for PyTorch users.  
* Provide a transparent and fair process for evaluating compute platform submissions.  
* Maintain community trust by periodically validating that listed compute platforms continue to meet requirements.
* Promote innovation and broaden hardware support within the PyTorch ecosystem.
* Provide discoverability of source, binaries and documentation for supported compute platforms to the community.

## Admission Requirements

Compute platform submissions are evaluated against a set of quality criteria as follows.

**Functional Requirements:**

1. **PyTorch Integration:** The compute platform is integrated through PyTorch's official backend/accelerator mechanisms (via either dedicated keys or PrivateUse1 key).
2. **Feature List**: Provide a clear feature list that explains the current supported functions, along with the corresponding API list.
3. **Working CI**: Compute platform has a demonstrable working CI covering a representative set of supported hardware (optional: software versions, and critical PyTorch functionality). The submission should clearly document which declared architectures are covered by CI and which are validated through other means.
4. **CI Integration**: Integrate with hud dashboard via [CRCR System](https://docs.pytorch.org/docs/main/accelerator/ci.html) and display results are on dedicated HUD pages for the downstream repo.
5. **Release Plan:** Compute platform has a release cadence and consistent version releases.
6. **Package**: Binary installation package together with user manual is available. Documentation must clearly indicate where to obtain the binaries, runtime/build dependencies, and any build recipes, even where actual distribution remains subject to the vendor's own terms.

**Maintenance Requirements:** 

1. **Maintainer**: The compute platform must be backed by a dedicated group of maintainers to ensure long-term maintenance sustainability. Effective communication channels must be provided, all inquiries sent via designated channels must receive timely replies, including an initial acknowledgment.
2. **Maintenance:** The entity must be committed to supporting and maintaining their projects for the next 12 months at a minimum (starting from the date the application is approved).
3. **Release**: Compute platforms must regularly release and maintain a maximum version gap of three minor versions (equivalent to six months).
4. **Security**: Compute Platform maintainers need to provide a documented security policy for vulnerability reporting, including expected response, fix, and disclosure timelines. Vulnerabilities confined to the platform’s own out-of-tree code need be handled under this policy; while a report also involves in-tree PyTorch code, maintainers must coordinate disclosure following the PyTorch security policy.

## Admission Process

### Submission

The compute platform needs to submit an application that covers the **Functional Requirements** and **Maintenance Requirements** above by opening an issue in the application repository. 

### Review Applications

The Co-chair of the Accelerator Integration Working Group (or a delegate designated by the Co-chair) conducts a pre-review of the submission against the Admission Requirements.

* If the pre-review identifies gaps, the submitter is required to fix the gaps.  
* If the pre-review passes, the Co-chair initiates a vote.  
* Voting members are defined in the Accelerator Integration Working Group charter.   
* A quorum requires more than half of the Working Group’s eligible voting members to participate; the vote then passes by a simple majority of those who participate. 

## Periodic Review

Every 6 months, all listed compute platforms are reviewed by the Accelerator Integration Working Group to ensure they continue to meet the Admission Requirements. Specifically:

* The review requires platform maintainers to submit an updated self-assessment against the [Admission Requirements](#admission-requirements) with current evidence.  
* The Accelerator Integration Working Group verifies the current quality of all assessments.  
* If a compute platform fails to satisfy Admission Requirements, the platform maintainers are notified with a clear description of the deficiencies.  
* Platform maintainers are given 60 days to implement the necessary changes. If the deficiencies are not resolved within 60 days, or if the platform maintainers do not respond, the compute platform is retired and removed from the Additional Compute Platforms page.

## Offboarding

The compute platform retirement process will be triggered under any of the following scenarios:

* The platform fails to meet admission requirements during periodic reviews and rectification is not completed within the specified timeframe above.  
* The platform maintainers inform the WG that they will stop supporting integration with PyTorch.

When a compute platform is retired:

* Platform maintainers are notified of the retirement decision and the specific reasons.  
* The compute platform is removed from the PyTorch website's Additional Compute Platforms page.  
* Platform maintainers are asked to remove any references to being listed on the PyTorch Additional Compute Platforms page from their repository and project website.

Retired or rejected compute platforms can reapply via the standard submission process after resolving all issues that led to their retirement or rejection.

## Benefits

Approved compute platforms receive:

* Listing on the PyTorch Additional Compute Platforms page as a recognized platform backend.  
* A blog post announcing the new platform listing from the PyTorch marketing team.  
* Collaboration opportunities with the Accelerator Integration Working Group and the broader PyTorch ecosystem.

## Maintaining this Document

The Accelerator Integration Working Group is responsible for the development, modification, and interpretation of this document. 

## Publishing this Document

The most current version of this document is available in the TAC GitHub repository: [https://github.com/pytorch-fdn/tac/tree/main/docs/governance](https://github.com/pytorch-fdn/tac/tree/main/docs/governance)