# Guide for implementing the Standard for Public Code

*This is a beginning of how a guide for someone that wants to implement the Standard for Public Code with their codebase could look like.*

We want the guide to be built with the Community, like the the Community translations. (And also generating a website similarly with one page per criterion.)

It should help when someone asks the question "How can I meet this requirement?" or "What do I need to do to meet this requirement?"

It can contain examples of implementations, tools, methods that would meet a specific requirement. The things that are added should almost be considered to be "pre-approved", meaning that if you were using the guide (and in good spirit) you are almost certain to get a pass when assessed by the Foundation for Public Code.

We should keep in mind "there's more than one way to do it": where it makes sense, provide multiple options, especially linking to examples.

The guide could also invite for conversation about solutions in specific cases.

It may have some general advice inspired by the sections "How to test", "what you need to do" and "further reading" sessions. We should also critically evaluate if links in the sections Further reading should move here.

As seen from the text below, advice that touches on the entire criterion goes just under the criterion heading.
Advice specific to each requirement goes below the requirement heading. When we start, there might not be advice for every single reuirement.
We will likely divide this document to one page per criteria before publishing, just like how the Standard itself is published.

---

<!-- The implementation guide could start by linking to all compliant codebases since these should inthemselves be examples on every requirement. -->
<!-- Link to good README files in the start? They span several criteria, but none of them requires it. -->
<!-- This should be linked somewhere: https://blog.publiccode.net/news/2020/12/09/how-to-start-a-standard-compliant-repository.html -->

## Code in the open

Share generously about your work and [radiate your intent](https://medium.com/@ElizAyer/dont-ask-forgiveness-radiate-intent-d36fd22393a3).

The Welsh Land and Property Data publish [open weeknotes](https://welsh-revenue-authority.github.io/weeknotes/property-data-poc/) from their development team, this is a great way of communicating what you are working on.

### All source code for any policy and software in use (unless used for fraud detection) MUST be published and publicly accessible.

Consider using a git service or self hosting a git repository.
While this requirement is about publishing, to really enable collaboration, this should also be where you do your development.
That is, you should preferrably not just mirror the code publicly since that will make it harder for everyone (you included) to get an overview of the ongoing work.

<!-- List of git-platforms -->
* [GitHub](https://github.com/): +largest community, +free for FOSS codebases, -cannot be self-hosted, -possibly GDPR-problems, -not FOSS
* [GitLab](https://gitlab.com/): +can be self-hosted, -hosted version is not FOSS
* [Gitea](https://gitea.io/):
* [Codeberg]((https://codeberg.org)): (hosted Gitea)
* [Sourcehut](https://sourcehut.org): -still in alpha
* [IEEE SA open](https://saopen.ieee.org/): (hosted GitLab)
* [Bitbucket](https://bitbucket.org/): -cannot be self-hosted, -not FOSS
* [Gitpod](https://www.gitpod.io/): (packing around other git services) +can be self-hosted

<!-- Check if some countries already have repository guidelines or provide hosted services for public orgs and list them here too -->

### Any source code not currently in use (such as new versions, proposals or older versions) SHOULD be published.

Tag releases so they can be found/checked-out from source control.
Link old releases, make them easilly avialble for download.
Publish releases before you start using them, or at the same moment if pre-publish is not possible for example a hot-fix in production.

## Bundle policy and source code

### A codebase MUST include the policy that the source code is based on.

Include links in the documentation to the policies that underpin the codebase or its deployments.
If the policy is short, include it in full.
If the policy is long, make sure that at least a summary is available in the documentation.
Note that links to several layers of the policy might be useful, for example that the codebase aims to implement an EU directive, but a feature might specifically be made to comply with the law that is the implemenation of the directive in a single member state. In this case both levels are useful to include.
When adding new features, document what policy they are meant to implement.
Look if your context have collections of policies that apply to public organizations, like [these for digitalization by the Swedish Agency for Digital Governement](https://www.digg.se/regler-och-rekommendationer).

### A codebase MUST include all source code that the policy is based on.

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

## Create reusable and portable code

### The codebase MUST be developed to be reusable in different contexts.

#### Examples

* [OpenFisca](https://openfisca.org/en/countries/) is reused in many different countries.
* [Decidim](https://decidim.org/usedby/) is reused in many different countries and on many different levels.

### The codebase MUST be independent from any secret, undisclosed, proprietary or non-open licensed code or services for execution and understanding.

(This is more of a "don't do" rather than a "do like this"; is there anything that a guide should have here?)

### The codebase SHOULD be in use by multiple parties.

Through the nature of open source software, it might be hard to know who is using the codebase if they are not actively contributing to it. Therefore you might want to consider using an opt-in telemetry option in the configuration so that re-users can make themselves known. (As a bonus, this could also enable a way to communicate security related updates.)

#### Examples

* [Signalen](https://signalen.org) started in Amsterdam then became used in many municipalities.

### The roadmap SHOULD be influenced by the needs of multiple parties.

Create a steering group of interested parties, especially those with budget to make changes. Have a regular roadmap video conference held by the steering group. After each, update the feature roadmap document in the repository.

Developers should have a technical roadmap informed by the feature roadmap. Create a steering group of senior developers who keep a technical roadmap up to date in the repository.

#### Examples

### Configuration SHOULD be used to make code adapt to context specific needs.

(e.g.: Signalen logos)
(Municipio color schemes)

### The codebase SHOULD be localizable.

(Add some of the Further reading from the standard here instead?)

#### Tools

<!-- List of tools for translations -->
* [gettext](https://www.gnu.org/software/gettext/)
* [Translatewiki](https:/translatewiki.net)
* [Crowdin](https://crowdin.com/)
* [Weblate](https://weblate.org/)
* [Transifex](https://www.transifex.com/)
* [Poedit](https://poedit.net/)

#### Examples

* [Decidim](https://crowdin.com/translate/decidim) (using Crowdin)
* [FixMyStreet](https://fixmystreet.org/customising/language/) (using Transifex or PoEdit)

### The codebase SHOULD include a machine-readable metadata description, for example in a publiccode.yml file.

#### Tools

* [publiccode.yml web editor](https://publiccode-editor.developers.italia.it/)

#### Examples

* [OpenZaak](https://github.com/open-zaak/open-zaak/blob/main/publiccode.yaml)
* [VerificaC19, the official Italian customization of the EU Digital COVID Certificate Verifier App for the Android Operating System](https://github.com/ministero-salute/it-dgc-verificaC19-android/blob/develop/publiccode.yml)

### Code and its documentation SHOULD NOT contain situation-specific information.

(can we find examples that were fixed? maybe Omgevingsbelied database tests?)

## Welcome contributors

### The codebase MUST allow anyone to submit suggestions for changes to the codebase.

#### Examples

* GitHub pull requests like [https://github.com/publiccodenet/standard/pulls](https://github.com/publiccodenet/standard/pulls)
* [Self-hosted Gitea pull requests](https://git.fsfe.org/FSFE/fsfe-website/pulls)
* (add a good gitlab example)

### The codebase MUST include contribution guidelines explaining what kinds of contributions are welcome and how contributors can get involved, for example in a CONTRIBUTING file.

#### Resources

* [Instructions for adding a CONTRIBUTING file on GitHub](https://docs.github.com/en/communities/setting-up-your-project-for-healthy-contributions/setting-guidelines-for-repository-contributors)

#### Examples

* [OpenZaak CONTRIBUTING](https://github.com/open-zaak/open-zaak/blob/main/CONTRIBUTING.md)
* [OpenGovernment CONTRIBUTING](https://github.com/opengovernment/opengovernment/blob/master/CONTRIBUTING.md)
* [Git CodingGuidelines](https://github.com/git/git/blob/master/Documentation/CodingGuidelines) is an example of a mature codebase with extensive guidelines
* [Template for gemeente Amsterdam](https://github.com/Amsterdam/amsterdam.github.io/blob/master/CONTRIBUTING.md)

<!-- Possible generic template here? -->

### The codebase MUST document the governance of the codebase, contributions and its community, for example in a GOVERNANCE file.

#### Examples

* [OpenRefine GOVERNANCE](https://github.com/OpenRefine/OpenRefine/blob/master/GOVERNANCE.md), example of a fairly mature governance structure
* [Simple template for GOVERNANCE file](https://about.publiccode.net/activities/supporting-codebase-governance/governance-template.html)

### The codebase SHOULD advertise the committed engagement of involved organizations in the development and maintenance.

#### Examples

* [OS2 Rollekatalog](https://os2.eu/produkt/os2rollekatalog) (in Danish)
* [CKAN (see the footer)](https://ckan.org/)
* [MasterPortal](https://www.masterportal.org/maintainer-group-en.html)

### The codebase SHOULD have a publicly available roadmap.

This could also be solved by having public task boards/kanban boards with suitable columns and issues/stories at high level (sometimes called Epics).

#### Examples

* [Notify roadmap](https://www.notifications.service.gov.uk/features/roadmap)
* [Simple template for technical roadmap](https://about.publiccode.net/activities/supporting-codebase-governance/technical-roadmap-template.html)

### The codebase SHOULD publish codebase activity statistics.

#### Examples

* [GitHub Insights - Contributors](https://github.com/publiccodenet/standard/graphs/contributors)

### The codebase MAY include a code of conduct for contributors.

#### Examples

## Make contributing easy

### The codebase MUST have a public issue tracker that accepts suggestions from anyone.

#### Examples

* GitHub Issues like [https://github.com/publiccodenet/standard/issues](https://github.com/publiccodenet/standard/issues)
* [Self-hosted Gitea Issues](https://git.fsfe.org/FSFE/fsfe-website/issues)
* (add a good gitlab example)
* [Tasks in Phabricator](https://phabricator.wikimedia.org/maniphest/)

### The codebase MUST include instructions for how to privately report security issues for responsible disclosure.

#### Examples

* [OpenZaak SECURITY](https://github.com/open-zaak/open-zaak/blob/main/SECURITY.rst)

### The documentation MUST link to both the public issue tracker and submitted codebase changes, for example in a README file.

In many platforms, like GitHub, GitLab, Gitea etc. these links are automatically provided in the interface. If you don't use the features of the platform, for example if you have a separate issue tracker, then you must provide these links.

### The codebase MUST have communication channels for users and developers, for example email lists.

Preferrably, anyone should be able to join these and start discussing without requiring an invite or other manual intervention.

#### Tools

##### Mailing lists

* [Mailman](http://list.org/)

##### Chat

* [RocketChat](https://rocket.chat/)
* [Mattermost](https://mattermost.com/)
* [Matrix](https://matrix.org/)
* [Gitter](https://gitter.im/)
* IRC

##### Fora

* [Discourse](https://www.discourse.org/)
* [Github Discussions](https://docs.github.com/en/discussions)

##### Video

* [Jitsi](https://jitsi.org/)
* [BigBlueButton](https://bigbluebutton.org/)

##### Audio

* [Mumble](https://www.mumble.info/)

#### Examples

* [FixMyStreet community page with multiple options](https://fixmystreet.org/community/)
* [OpenZaak mailing list (Mailman/Postorius/Hyperkitty)](https://lists.publiccode.net/mailman/postorius/lists/openzaak-discuss.lists.publiccode.net/)
* [CivicTech Sweden (RocketChat)](https://chat.civictech.se/home)
* [Publiccode.yml forum (GitHub discussions)](https://github.com/publiccodeyml/publiccode.yml/discussions)

### The documentation SHOULD include instructions for how to report potentially security sensitive issues on a closed channel.

## Maintain version control

### The community MUST have a way to maintain version control for the code.

Git is great.

See a list of git options under [All source code for any policy and software in use (unless used for fraud detection) MUST be published and publicly accessible.](#All-source-code-for-any-policy-and-software-in-use-unless-used-for-fraud-detection-MUST-be-published-and-publicly-accessible)

#### Resources

* [Producing OSS: Version Control Vocabulary](https://producingoss.com/en/vc.html#vc-vocabulary) by Karl Fogel.
* [GitHub Learning Lab](https://lab.github.com/) by GitHub for learning how to use it or refresh your skills.
* [Git Cheat Sheet](https://education.github.com/git-cheat-sheet-education.pdf) by GitHub, a list with the most common used git commands.

### All files in a codebase MUST be version controlled.

### All decisions MUST be documented in commit messages.

### Every commit message MUST link to discussions and issues wherever possible.

### The codebase SHOULD be maintained in a distributed version control system.

Git is great.

### Contributors SHOULD group relevant changes in commits.

### Maintainers SHOULD mark released versions of the codebase, for example using revision tags or textual labels.

#### Examples

* [Mosip Registration releases](https://github.com/mosip/registration/releases)

### Contributors SHOULD prefer file formats where the changes within the files can be easily viewed and understood in the version control system.

<!-- Make a list of preferred file formats -->

### Contributors MAY sign their commits and provide an email address, so that future contributors are able to contact past contributors with questions about their work.

## Require review of contributions

### All contributions that are accepted or committed to release versions of the codebase MUST be reviewed by another contributor.

Use "protected branches" to configure rules on how contributions can be merged.

#### Resources

* [About protectected branches in GitHub](https://docs.github.com/en/repositories/configuring-branches-and-merges-in-your-repository/defining-the-mergeability-of-pull-requests/about-protected-branches)
* [About protectected branches in GitLab](https://docs.gitlab.com/ee/user/project/protected_branches.html)

### Reviews MUST include source, policy, tests and documentation.

The pull request template should include what needs to be reviewed.

#### Resources

* [About pull request templates in Gitea](https://docs.gitea.io/en-us/issue-pull-request-templates/)
* [About pull request templates in GitHub](https://docs.github.com/en/communities/using-templates-to-encourage-useful-issues-and-pull-requests/creating-a-pull-request-template-for-your-repository)
* [About description templates in GitLab](https://docs.gitlab.com/ee/user/project/description_templates.html)

#### Examples

* [Signalen backend](https://github.com/Signalen/backend/blob/master/.github/pull_request_template.md)

### Reviewers MUST provide feedback on all decisions to not accept a contribution.

#### Examples

### Contributions SHOULD conform to the standards, architecture and decisions set out in the codebase in order to pass review.

The pull request template should include what needs to be reviewed.

### Reviews SHOULD include running both the code and the tests of the codebase.

### Contributions SHOULD be reviewed by someone in a different context than the contributor.

### Version control systems SHOULD NOT accept non-reviewed contributions in release versions.

### Reviews SHOULD happen within two business days.

Note: "happen" does not mean "be completed".

### Reviews MAY be performed by multiple reviewers.

## Document codebase objectives

Be on the lookout for people, organizations and initiatives with similar objectives to see if you can collaborate rather than compete.

### The codebase MUST contain documentation of its objectives, like a mission and goal statement, that is understandable by developers and designers so that they can use or contribute to the codebase.

#### Examples

* [Omgevingsbeleid objectives](https://github.com/Provincie-Zuid-Holland/Omgevingsbeleid-Frontend#objectives)
* [Vision and mission of Govdirectory](https://github.com/govdirectory/website/blob/main/CONTRIBUTING.md#direction)

### Codebase documentation SHOULD clearly describe the connections between policy objectives and codebase objectives.

#### Examples

### The codebase MAY contain documentation of its objectives for the general public.

#### Examples

## Document the code

**Tools**

* [Docusaurus](https://docusaurus.io/)
* [Read the docs](https://readthedocs.org/)
* [mkdocs](https://www.mkdocs.org/)
* [readme.so](https://readme.so/) is a tool to create a README file

**Resources**

* [How to write a README](https://github.com/Amsterdam/amsterdam.github.io/blob/master/guides/write-a-readme.md), guide from the municipality of Amsterdam.

### All of the functionality of the codebase, policy as well as source, MUST be described in language clearly understandable for those that understand the purpose of the code.

#### Examples

### The documentation of the codebase MUST contain a description of how to install and run the source code.

#### Examples

### The documentation of the codebase MUST contain examples demonstrating the key functionality.

#### Examples

### The documentation of the codebase SHOULD contain a high level description that is clearly understandable for a wide audience of stakeholders, like the general public and journalists.

#### Examples

* [CKAN](https://ckan.org/): "CKAN is an open-source DMS (data management system) for powering data hubs and data portals. CKAN makes it easy to publish, share and use data. It powers hundreds of data portals worldwide."
* [OpenFisca description](https://openfisca.org/doc/index.html)

### The documentation of the codebase SHOULD contain a section describing how to install and run a standalone version of the source code, including, if necessary, a test dataset.

#### Examples

### The documentation of the codebase SHOULD contain examples for all functionality.

#### Examples

### The documentation SHOULD describe the key components or modules of the codebase and their relationships, for example as a high level architectural diagram.

#### Examples

* [DigiTransit UI architecture](https://github.com/HSLdevcom/digitransit-ui/blob/v2/docs/Architecture.md)
<!-- There may be some good examples in https://commons.wikimedia.org/wiki/Category:Software_architecture -->

### There SHOULD be continuous integration tests for the quality of the documentation.

### The documentation of the codebase MAY contain examples that make users want to immediately start using the codebase.

#### Examples

* [CKAN showcase implementations](https://ckan.org/showcase)

### The code MAY be tested by using examples in the documentation.

## Use plain English

### All codebase documentation MUST be in English.

#### Examples

* [Notify documentation](https://github.com/alphagov/notifications-manuals/wiki)

### All code MUST be in English, except where policy is machine interpreted as code.

### All bundled policy not available in English MUST have an accompanying summary in English.

### Any translation MUST be up to date with the English version and vice versa.

This applies to everything that is in a "released" state. During development, lag may occur.

### There SHOULD be no acronyms, abbreviations, puns or legal/non-English/domain specific terms in the codebase without an explanation preceding it or a link to an explanation.

While you should try to keep the language plain, don't be afraid to create a glossary for terms that are specific for the domain and would cause even more confusion if they were not used.

### The name of the codebase SHOULD be descriptive and free from acronyms, abbreviations, puns or organizational branding.

#### Examples

* [FixMyStreet](https://www.fixmystreet.com/)

### Documentation SHOULD aim for a lower secondary education reading level, as recommended by the Web Content Accessibility Guidelines 2.

#### Resources

* [Understanding Reading Level of the WCAG](https://www.w3.org/WAI/WCAG20/Understanding/reading-level.html) with resources for evaluating the reading level of a text

#### Tools

* [LanguageTool](https://languagetool.org/) - spelling and grammar
* [Grammarly](https://www.grammarly.com/) - grammar
* [Hemingway text editor](https://hemingwayapp.com/) - readability
* [Upgoer 5 text editor](https://splasho.com/upgoer5/) by Theo Sanderson, only allows 1000 most common words

### Any code, documentation or tests MAY have a translation.

# Use open standards

### For features of a codebase that facilitate the exchange of data the codebase MUST use an open standard that meets the Open Source Initiative Open Standard Requirements.

### Any non-open standards used MUST be recorded clearly as such in the documentation.

### Any standard chosen for use within the codebase MUST be listed in the documentation with a link to where it is available.

#### Examples

### If no existing open standard is available, effort SHOULD be put into developing one.

### Standards that are machine testable SHOULD be preferred over those that are not.

### Functionality using features from a standard that is not an open standard MAY be provided if necessary, but only in addition to compliant features.

## Use continuous integration

### All functionality in the source code MUST have automated tests.

Most code coverage tools have functionality to exclude specific lines if needed.

### Contributions MUST pass all automated tests before they are admitted into the codebase.

### The codebase MUST have guidelines explaining how to structure contributions.

#### Examples

* [CKAN pull request guidlines](http://docs.ckan.org/en/latest/contributing/pull-requests.html)

### The codebase MUST have active contributors.

### The codebase guidelines SHOULD state that each contribution should focus on a single issue.

#### Examples

* [CKAN pull request guidlines](http://docs.ckan.org/en/latest/contributing/pull-requests.html)

### Source code test and documentation coverage SHOULD be monitored.

### Policy and documentation MAY have testing for consistency with the source and vice versa.

### Policy and documentation MAY have testing for style and broken links.

Also explain, and if needed provide links, how the testing is done so that the contributor can be efficient when making their contributions. I.e. list any linters that are used.

## Publish with an open license

### All code and documentation MUST be licensed such that it may be freely reusable, changeable and redistributable.

#### Tools

* [Choose a license](https://choosealicense.com/), a tool that guides you through the process of picking a license that suits you
* [Joinup Licensing Assistant](https://joinup.ec.europa.eu/collection/eupl/solution/joinup-licensing-assistant/jla-find-and-compare-software-licenses), helps comparing licenses or select them on various properties

#### Resources

* [Animated video introduction to Creative Commons](https://creativecommons.org/about/videos/creative-commons-kiwi) by Creative Commons Aotearoa New Zealand, that also explains the basic concept of free licenses.
<!-- When we add the one above, we should also remove it from the standard -->
* [A Quick Guide to Software Licensing for the Scientist-Programmer](https://journals.plos.org/ploscompbiol/article?id=10.1371/journal.pcbi.1002598)

### Software source code MUST be licensed under an OSI-approved open source license.

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

## Use a coherent style

### Contributions MUST adhere to either a coding or writing style guide, either the codebase community’s own or an existing one that is advertised in or part of the codebase.

#### Examples

* Basic guidelines: [OpenZaak](https://github.com/open-zaak/open-zaak/blob/main/CONTRIBUTING.md) 
* Guidelines of a very mature project: [Git](https://github.com/git/git/blob/master/Documentation/CodingGuidelines)

### Contributions SHOULD pass automated tests on style.

#### Resources

* [List of linters](https://github.com/caramelomartins/awesome-linters) by Hugo Martins.

<!-- When we add the one above, we should also remove it from the standard -->

### The codebase SHOULD include inline comments and documentation for non-trivial sections.

#### Examples

### The style guide MAY include sections on understandable English.

#### Examples

## Document codebase maturity

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
