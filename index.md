# Implementation guide to the Standard for Public Code 0.7.1

This guide should help when someone asks the question "How can I meet this requirement?" or "What do I need to do to meet this requirement?"

It can contain examples of implementations, tools, methods that would meet a specific requirement.
The things that are added should almost be considered to be "pre-approved", meaning that if you were using the guide (and in good spirit) you are almost certain to get a pass.

We should keep in mind "there's more than one way to do it": where it makes sense, provide multiple options, especially linking to examples.

The guide could also invite for conversation about solutions in specific cases.

It may have some general advice inspired by the sections "How to test", "What you need to do" and "Further reading" sessions.
We should also critically evaluate if links in the sections Further reading in the Standard for Public Code itself should move here.

Advice that touches on the entire criterion goes just under the criterion heading.
Advice specific to each requirement goes below the requirement heading.

* [Criteria](criteria/){% assign sorted = site.pages| sort:"order" %}{% for page in sorted %}{% if page.dir == "/criteria/" %}{% if page.name != "index.md" %}{% if page.title %}
  * [{{page.title}}](.{{page.url}}){% endif%}{% endif%}{% endif%}{% endfor %}

## Public assessments

Below is a list of codebases that have made a Standard for Public Code assessment.
They can serve as an inspiration if you want to see how others are meeting the requirements of the standard.

| Codebase Repository | Assessment link | Version |
|---|---|---|
| [Standard for Public Code](https://github.com/standard-for-public-code/standard-for-public-code) | [Link](https://www.standardforpubliccode.org/docs/standard-for-public-code.html) | 0.8.1 |
| [Governance Game](https://github.com/governance-game/governance-game) | [Link](https://github.com/governance-game/governance-game/blob/develop/standard-for-public-code-assessment.html) | 0.7.0 |
| [Govdirectory](https://github.com/govdirectory/website) | [Link](https://www.govdirectory.org/standard-for-public-code/) | 0.8.0 |

If you want the assessment of a codebase you maintain or contribute to to be added to this list, we invite you to [make a pull request](https://github.com/standard-for-public-code/community-implementation-guide-standard/compare).
Out of courtesy, we ask you to only add links to assessments where you have the consent of that codebase's community.
