---
order: 3
redirect_from:
  - criteria/reusable-and-portable-codebases
  - criteria/create-reusable-and-portable-code
---
# Make the codebase reusable and portable [![This criterion in the Standard for Public Code]({{site.url}}/assets/link-symbol.png)](https://standard.publiccode.net/criteria/make-the-codebase-reusable-and-portable.html)

<!-- SPDX-License-Identifier: CC0-1.0 -->
<!-- written in 2022 by The Foundation for Public Code <info@publiccode.net> -->

## Requirements

### The codebase MUST be developed to be reusable in different contexts.

#### Examples

* [OpenFisca](https://openfisca.org/en/packages/) is reused in many different countries.
* [Decidim](https://decidim.org/usedby/) is reused in many different countries and on many different levels.

### The codebase MUST be independent from any secret, undisclosed, proprietary or non-open licensed software or services for execution and understanding.

(This is more of a "don't do" rather than a "do like this"; is there anything that a guide should have here?)

### The codebase SHOULD be in use by multiple parties.

Through the nature of open source software, it might be hard to know who is using the codebase if they are not actively contributing to it. Therefore you might want to consider using an opt-in telemetry option in the configuration so that re-users can make themselves known. (As a bonus, this could also enable a way to communicate security related updates.)

#### Examples

* [Signalen](https://signalen.org) started in Amsterdam then became used in many municipalities.

### The roadmap SHOULD be influenced by the needs of multiple parties.

Create a steering group of interested parties, especially those with budget to make changes. Have a regular roadmap video conference held by the steering group. After each, update the feature roadmap document in the repository.

Developers should have a technical roadmap informed by the feature roadmap. Create a steering group of senior developers who keep a technical roadmap up to date in the repository.

#### Examples

### The development of the codebase SHOULD be a collaboration between multiple parties.

### Configuration SHOULD be used to make source code adapt to context specific needs.

(e.g.: Signalen logos)
(Municipio color schemes)

### The codebase SHOULD be localizable.

(Add some of the Further reading from the standard here instead?)

#### Tools

<!-- List of tools for translations -->
* [gettext](https://www.gnu.org/software/gettext/)
* [Translatewiki](https://translatewiki.net/)
* [Crowdin](https://crowdin.com/)
* [Weblate](https://weblate.org/)
* [Transifex](https://www.transifex.com/)
* [Poedit](https://poedit.net/)

#### Examples

* [Decidim](https://crowdin.com/translate/decidim) (using Crowdin)
* [FixMyStreet](https://fixmystreet.org/customising/language/) (using Transifex or PoEdit)

#### Further reading

* [Internationalization techniques: Authoring HTML & CSS](https://www.w3.org/International/techniques/authoring-html) by the World Wide Web Consortium.

### Source code and its documentation SHOULD NOT contain situation-specific information.

(can we find examples that were fixed? maybe Omgevingsbelied database tests?)

### Codebase modules SHOULD be documented in such a way as to enable reuse in codebases in other contexts.

## Further reading

* [OpenAPI Specification](https://spec.openapis.org/oas/latest.html) by the OpenAPI Initiative defines a standard, programming language-agnostic interface description for human and machine-readable HTTP APIs.

### The software SHOULD NOT require services or platforms available from only a single vendor.
