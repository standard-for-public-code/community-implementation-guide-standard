---
order: 13
---
# Publish with an open license

<!-- SPDX-License-Identifier: CC0-1.0 -->
<!-- written in 2022 by The Foundation for Public Code <info@publiccode.net> -->

## Requirements

### All code and documentation MUST be licensed such that it may be freely reusable, changeable and redistributable.

#### Tools

* [Choose a license](https://choosealicense.com/), a tool that guides you through the process of picking a license that suits you
* [Joinup Licensing Assistant](https://joinup.ec.europa.eu/collection/eupl/solution/joinup-licensing-assistant/jla-find-and-compare-software-licenses), helps comparing licenses or select them on various properties

#### Resources

* [Animated video introduction to Creative Commons](https://creativecommons.org/about/videos/creative-commons-kiwi) by Creative Commons Aotearoa New Zealand, that also explains the basic concept of free licenses.
<!-- When we add the one above, we should also remove it from the standard -->
* [A Quick Guide to Software Licensing for the Scientist-Programmer](https://journals.plos.org/ploscompbiol/article?id=10.1371/journal.pcbi.1002598)
* [Open source licenses: What, which, and why](https://arstechnica.com/gadgets/2020/02/how-to-choose-an-open-source-license/) by Ars Technica explains with some nuance the difference between the most common licenses.

### Software source code MUST be licensed under an OSI-approved or FSF Free/Libre license.

### All code MUST be published with a license file.

### Contributors MUST NOT be required to transfer copyright of their contributions to the codebase.

This may be impossible for civil servants in some jurisdictions so if that is a requirement they are effectively prohibited from contributing.

### All source code files in the codebase SHOULD include a copyright notice and a license header that are machine-readable.

Note that there are some competing standards regarding machine-readable license info:

* The [Licensee](https://github.com/licensee/licensee) tool is used by GitHub, GitLab, and others.
* The [REUSE](https://reuse.software/) spec seems to conflict with `Licensee` becuase it "consciously and opinionatedly breaks from convention" by looking in the LICENSES directory for licenses named after their SPDX identifier and does not take in to account the COPYING or LICENSE files which are the common convention by overwhelming majority.

Can we find good real-world examples of navigating this?

#### Examples

* [Curl is REUSE compliant](https://daniel.haxx.se/blog/2022/06/17/curl-is-reuse-compliant/)

### Codebases MAY have multiple licenses for different types of code and documentation.

#### Examples

* [Docusaurus](https://github.com/facebook/docusaurus#license) is using MIT for code and CC BY 4.0 for documentation
