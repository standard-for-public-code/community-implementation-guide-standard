---
order: 16
redirect_from:
    - criteria/document-maturity
---
# Document codebase maturity [![This criterion in the Standard for Public Code]({{site.url}}/assets/link-symbol.png)](https://standard.publiccode.net/criteria/document-codebase-maturity.html)

<!-- SPDX-License-Identifier: CC0-1.0 -->
<!-- written in 2019 - 2022 by The Foundation for Public Code <info@publiccode.net> -->

## Requirements

### The codebase MUST be versioned.

Remember to document your versioning strategy to make it clear to other contributors.

#### Resources

* [Semantic versioning](https://semver.org/), one common specification for versioning of software.

#### Examples

* [OS2Forms tags](https://github.com/OS2Forms/os2forms/tags) (following semantic versioning)

### The codebase MUST prominently document whether or not there are versions of the codebase that are ready to use.

#### Examples

#### Further reading

* [Service Design and Delivery Process](https://www.dta.gov.au/help-and-advice/build-and-improve-services/service-design-and-delivery-process) by the Australian Digital Transformation Agency, describes how to follow the service design and delivery process: what you need to do in Discovery, Alpha, Beta and Live stages.
* [Service Manual on Agile Delivery](https://www.gov.uk/service-manual/agile-delivery) by the UK Government Digital Service, among other things it describes the phases discovery, alpha, beta, live and retirement of an agile project.

<!-- When we add these two above, we should also remove them from the standard -->

### Codebase versions that are ready to use MUST only depend on versions of other codebases that are also ready to use.

### The codebase SHOULD contain a log of changes from version to version, for example in the CHANGELOG.

#### Examples

* [OpenZaak CHANGELOG](https://github.com/open-zaak/open-zaak/blob/main/CHANGELOG.rst)

### The method for assigning version identifiers SHOULD be documented.

### It is OPTIONAL to use semantic versioning.
