# Implementation guide to the Standard for Public Code

This is a repository for guiding implementation choices for the criteria of the [Standard for Public Code](https://www.standardforpubliccode.org).

[![pages-build-deployment](https://github.com/standard-for-public-code/community-implementation-guide-standard/actions/workflows/pages/pages-build-deployment/badge.svg)](https://github.com/standard-for-public-code/community-implementation-guide-standard/actions/workflows/pages/pages-build-deployment)
[![Test](https://github.com/standard-for-public-code/community-implementation-guide-standard/actions/workflows/test.yml/badge.svg)](https://github.com/standard-for-public-code/community-implementation-guide-standard/actions/workflows/test.yml)

## Contribute

The Standard for Public Code is [community governed](https://github.com/standard-for-public-code/standard-for-public-code/blob/develop/GOVERNANCE.md).

Join our [community calls](https://community.standardforpubliccode.org/), come say hello on our [discussion board](https://github.com/standard-for-public-code/standard-for-public-code/discussions), or feel free to leave an issue on any of [our repositories](https://github.com/orgs/standard-for-public-code/repositories).

Anyone may propose a possible method of meeting a criterion or requirement.
Besides adding examples, this is [our roadmap](roadmap.md) for this codebase.

Examples should be placed closest to their relevant component.
If the proposal is specific to a requirement, then the example should be place under the requirement.
If the proposal is spanning several requirements of a criterion, it should be placed in the criterion above the requirements.
If the proposal spans multiple criteria it should be above the list of criteria.

For further real world examples of Standard for Public Code implementation, check out [existing users' assessments against the Standard](https://github.com/standard-for-public-code#whos-using-the-standard-for-public-code).

### Review of a contributions

Before we merge a pull request of a new or updated proposal, it needs to be reviewed.

## Problems, suggestions and questions in issues

You can report problems, suggest changes or ask questions by [creating a GitHub issue](https://docs.github.com/en/issues/tracking-your-work-with-issues/creating-an-issue) for this project in the [GitHub Issues](https://github.com/standard-for-public-code/community-implementation-guide-standard/issues).

## Preview, build and deploy

This site is built using Jekyll.
Ensure ruby is installed and run `bundle install`.

To view changes, the `script/serve.sh` script will build locally and allow you to view it on localhost:4000.

To test your changes, `script/test-all.sh` will run the markdown linter and link checks.

When changes are merged to the `main` branch, they will be automatically deployed by GitHub.

## Code of Conduct

This repository uses a [code of conduct](CODE_OF_CONDUCT.md), please respect it.

## License

All contributions must be submitted under [CC0 1.0](LICENSE.md).
