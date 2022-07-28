---
order: 1
---
# Code in the open

<!-- SPDX-License-Identifier: CC0-1.0 -->
<!-- written in 2022 by The Foundation for Public Code <info@publiccode.net> -->

Share generously about your work and [radiate your intent](https://medium.com/@ElizAyer/dont-ask-forgiveness-radiate-intent-d36fd22393a3).

The Welsh Land and Property Data publish [open weeknotes](https://welsh-revenue-authority.github.io/weeknotes/property-data-poc/) from their development team, this is a great way of communicating what you are working on.

## Requirements

### All source code for any policy in use (unless used for fraud detection) MUST be published and publicly accessible.

### All source code for any software in use (unless used for fraud detection) MUST be published and publicly accessible.

Consider using a git service or self hosting a git repository.
While this requirement is about publishing, to really enable collaboration, this should also be where you do your development.
That is, you should preferrably not just mirror the code publicly since that will make it harder for everyone (you included) to get an overview of the ongoing work.

<!-- List of git-platforms -->
* [GitHub](https://github.com/): +largest community, +free for FOSS codebases, -cannot be self-hosted, -possibly GDPR-problems, -not FOSS
* [GitLab](https://gitlab.com/): +can be self-hosted, -hosted version is not FOSS
* [Gitea](https://gitea.io/):
* [Codeberg](https://codeberg.org): (hosted Gitea)
* [Sourcehut](https://sourcehut.org): -still in alpha
* [IEEE SA open](https://saopen.ieee.org/): (hosted GitLab)
* [Bitbucket](https://bitbucket.org/): -cannot be self-hosted, -not FOSS
* [Gitpod](https://www.gitpod.io/): (packing around other git services) +can be self-hosted

<!-- Check if some countries already have repository guidelines or provide hosted services for public orgs and list them here too -->

### Contributors MUST NOT upload sensitive information regarding users, their organization or third parties to the repository.

### Any source code not currently in use (such as new versions, proposals or older versions) SHOULD be published.

Tag releases so they can be found/checked-out from source control.
Link old releases, make them easilly avialble for download.
Publish releases before you start using them, or at the same moment if pre-publish is not possible for example a hot-fix in production.

### The codebase MAY provide the general public with insight into which source code or policy underpins any specific interaction they have with an organization.
