---
layout: page
title: Registration
registration_state: closed
---

{% case page.registration_state %}
{% when 'notyet' %}
<p class="message">Registration will be open soon.</p>

{% when 'closed' %}
<p class="message">Registration is closed.</p>

{% when 'open' %}
<p class="message">Registration is open.</p>

In order to participate in this meeting, please register with us, even if you only
want to join for parts of the meeting.

To register please send an email to [{{site.email}}](mailto:{{site.email}}) with the following contents.
```
Registration for {{site.title}}

Name: ...
Affiliation: ...
```

<p>
If you have any questions
regarding registration, or in general, feel free to
<a href="mailto:{{site.email}}">contact us via email</a>.
</p>

{% endcase %}