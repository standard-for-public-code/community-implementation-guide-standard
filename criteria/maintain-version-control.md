---
order: 6
redirect_from:
  - criteria/version-control-and-history
---
# Maintain version control [![This criterion in the Standard for Public Code]({{site.url}}/assets/link-symbol.png)](https://standard.publiccode.net/criteria/maintain-version-control.html)

<!-- SPDX-License-Identifier: CC0-1.0 -->
<!-- written in 2022 by The Foundation for Public Code <info@publiccode.net> -->

## Requirements

### All files in a codebase MUST be version controlled.

Git is great.

See a list of git options under [All source code for any policy and software in use (unless used for fraud detection) MUST be published and publicly accessible](code-in-the-open.md).

#### Resources

* [Producing OSS: Version Control Vocabulary](https://producingoss.com/en/vc.html#vc-vocabulary) by Karl Fogel.
* [GitHub Skills](https://skills.github.com/) by GitHub for learning how to use GitHub or refresh your skills.
* [Git Cheat Sheet](https://education.github.com/git-cheat-sheet-education.pdf) by GitHub, a list with the most common used git commands.

### All decisions MUST be documented in commit messages.

#### Tools

* [gnitpick](https://github.com/Seravo/gnitpick) a tool that helps check the messages of every commit.

#### Further reading

* [A note on commit messages](https://bitcrowd.dev/a-note-on-commit-messages) by Bitcrowd contains a lot fo good tips for commit messages.

### Every commit message MUST link to discussions and issues wherever possible.

### The codebase SHOULD be maintained in a distributed version control system.

Git is great.

### Contribution guidelines SHOULD require contributors to group relevant changes in commits.

### Maintainers SHOULD mark released versions of the codebase, for example using revision tags or textual labels.

#### Examples

* [Mosip Registration releases](https://github.com/mosip/registration/releases)

### Contribution guidelines SHOULD encourage file formats where the changes within the files can be easily viewed and understood in the version control system.

<!-- Make a list of preferred file formats -->

### It is OPTIONAL for contributors to sign their commits and provide an email address, so that future contributors are able to contact past contributors with questions about their work.
