# Guide for implementing the Standard for Public Code 0.7.0

This guide is built with the Community, like the Community translations.

It should help when someone asks the question "How can I meet this requirement?" or "What do I need to do to meet this requirement?"

It can contain examples of implementations, tools, methods that would meet a specific requirement.
The things that are added should almost be considered to be "pre-approved", meaning that if you were using the guide (and in good spirit) you are almost certain to get a pass when assessed by the Foundation for Public Code.

We should keep in mind "there's more than one way to do it": where it makes sense, provide multiple options, especially linking to examples.

The guide could also invite for conversation about solutions in specific cases.

It may have some general advice inspired by the sections "How to test", "what you need to do" and "further reading" sessions.
We should also critically evaluate if links in the sections Further reading should move here.

Advice that touches on the entire criterion goes just under the criterion heading.
Advice specific to each requirement goes below the requirement heading.

* [Criteria](criteria/){% assign sorted = site.pages| sort:"order" %}{% for page in sorted %}{% if page.dir == "/criteria/" %}{% if page.name != "index.md" %}{% if page.title %}
  * [{{page.title}}](.{{page.url}}){% endif%}{% endif%}{% endif%}{% endfor %}
