---
order: 7
redirect_from:
  - criteria/require-review
---
# Require review of contributions [![This criterion in the Standard for Public Code]({{site.url}}/assets/link-symbol.png)](https://standard.publiccode.net/criteria/require-review-of-contributions.html)

<!-- SPDX-License-Identifier: CC0-1.0 -->
<!-- written in 2022 by The Foundation for Public Code <info@publiccode.net> -->

This is a short guide that can be useful if you haven't thought about reviewing code from external contributors before: [10 universal steps for open source code review](https://opensource.com/article/22/10/code-review), by Red Hat.

## Requirements

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

### he review process SHOULD confirm that a contributionconforms to the standards, architecture and decisions set out in the codebase in order to pass review.

The pull request template should include what needs to be reviewed.

### Reviews SHOULD include running both the software and the tests of the codebase.

### Contributions SHOULD be reviewed by someone in a different context than the contributor.

### Version control systems SHOULD NOT accept non-reviewed contributions in release versions.

### Reviews SHOULD happen within two business days.

Note: "happen" does not mean "be completed".

### Performing reviews by multiple reviewers is OPTIONAL.
