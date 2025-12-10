# Implementation guide to the Standard for Public Code 0.7.1

This guide should help when someone asks the question "How can I meet this requirement?" or "What do I need to do to meet this requirement?"

It can contain examples of implementations, tools, methods that would meet a specific requirement.
The things that are added should almost be considered to be "pre-approved", meaning that if you were using the guide (and in good spirit) you are almost certain to get a pass.

We should keep in mind "there's more than one way to do it": where it makes sense, provide multiple options, especially linking to examples.

For inspiration of existing solutions that may not have been added here yet, check the assessments of [users of the Standard for Public Code](https://github.com/standard-for-public-code#whos-using-the-standard-for-public-code).

The guide could also invite for conversation about solutions in specific cases.

It may have some general advice inspired by the sections "How to test", "What you need to do" and "Further reading" sessions.
We should also critically evaluate if links in the sections Further reading in the Standard for Public Code itself should move here.

Advice that touches on the entire criterion goes just under the criterion heading.
Advice specific to each requirement goes below the requirement heading.

* [Criteria](criteria/){% assign sorted = site.pages| sort:"order" %}{% for page in sorted %}{% if page.dir == "/criteria/" %}{% if page.name != "index.md" %}{% if page.title %}
  * [{{page.title}}](.{{page.url}}){% endif%}{% endif%}{% endif%}{% endfor %}
