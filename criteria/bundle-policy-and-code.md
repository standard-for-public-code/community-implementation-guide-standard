---
order: 2
---
# Bundle policy and source code

<!-- SPDX-License-Identifier: CC0-1.0 -->
<!-- written in 2022 by The Foundation for Public Code <info@publiccode.net> -->

## Requirements

### The codebase MUST include the policy that the source code is based on.

Include links in the documentation to the policies that underpin the codebase or its deployments.
If the policy is short, include it in full.
If the policy is long, make sure that at least a summary is available in the documentation.
Note that links to several layers of the policy might be useful, for example that the codebase aims to implement an EU directive, but a feature might specifically be made to comply with the law that is the implemenation of the directive in a single member state. In this case both levels are useful to include.
When adding new features, document what policy they are meant to implement.
Look if your context have collections of policies that apply to public organizations, like [these for digitalization by the Swedish Agency for Digital Governement](https://www.digg.se/regler-och-rekommendationer).

### The codebase MUST include all source code that the policy is based on, unless used for fraud detection.

(Do we have examples of this? OpenFisca?)

### All policy and source code that the codebase is based on MUST be documented, reusable and portable.

(Do we have examples of policy that is reusable and portable?)

### Policy SHOULD be provided in machine readable and unambiguous formats.

(Can most codebases do this?)

#### Tools

* [Free online tools for building BPMN, CMMN and DMN diagrams at bmpn.io](https://bpmn.io/) by Camunda.
* [BPMN Quick Guide](https://www.bpmnquickguide.com/view-bpmn-quick-guide/) by Trisotech.

### Continuous integration tests SHOULD validate that the source code and the policy are executed coherently.

(Any examples?)
