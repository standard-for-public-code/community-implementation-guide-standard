---
order: 16
---
# Document codebase maturity

<!-- SPDX-License-Identifier: CC0-1.0 -->
<!-- written in 2019 - 2022 by The Foundation for Public Code <info@publiccode.net> -->

## Requirements

### A codebase MUST be versioned.

Remember to document your versioning strategy to make it clear to other contributors.

#### Resources

* [Semantic versioning](https://semver.org/), one common specification for versioning of software.

#### Examples

* [OS2Forms tags](https://github.com/OS2Forms/os2forms/tags) (following semantic versioning)

### A codebase that is ready to use MUST only depend on other codebases that are also ready to use.

### A codebase that is not yet ready to use MUST have one of the labels: prototype, alpha, beta or pre-release version.

#### Examples

#### Further reading

* [Service Design and Delivery Process](https://www.dta.gov.au/help-and-advice/build-and-improve-services/service-design-and-delivery-process) by the Australian Digital Transformation Agency, describes how to follow the service design and delivery process: what you need to do in Discovery, Alpha, Beta and Live stages.
* [Service Manual on Agile Delivery](https://www.gov.uk/service-manual/agile-delivery) by the UK Government Digital Service, among other things it describes the phases discovery, alpha, beta, live and retirement of an agile project.

<!-- When we add these two above, we should also remove them from the standard -->

### A codebase SHOULD contain a log of changes from version to version, for example in the CHANGELOG.

#### Examples

* [OpenZaak CHANGELOG](https://github.com/open-zaak/open-zaak/blob/main/CHANGELOG.rst)
