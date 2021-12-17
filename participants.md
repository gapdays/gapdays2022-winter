---
layout: page
title: Participants
participants:
  - {name: Max Horn, affiliation: TU Kaiserslautern, Germany}
  - {name: Wilf Wilson, affiliation: University of St Andrews, Scotland}
  - {name: Ruth Hoffmann, affiliation: University of St Andrews, Scotland}
  - {name: Russ Woodroofe, affiliation: University of Primorska, Slovenia}
  - {name: Alexander Konovalov, affiliation: University of St Andrews, Scotland}
  - {name: Anna Sucker, affiliation: RWTH Aachen, Germany}
  - {name: Lucas Wollenhaupt, affiliation: RWTH Aachen, Germany}
  - {name: Daniel Rademacher, affiliation: RWTH Aachen, Germany}
  - {name: Bettina Eick, affiliation: TU Braunschweig, Germany}
  - {name: Ibrahim Alotaibi, affiliation: University of Sydney, Australia}
  - {name: W. Edwin Clark, affiliation: University of South Florida, USA}
  - {name: Frank Lübeck, affiliation: RWTH Aachen, Germany}
  - {name: Alexander Cant, affiliation: TU Braunschweig, Germany}
  - {name: Nusa Zidaric, affiliation: Leiden University, Netherlands}
  - {name: Maryna Raievska, affiliation: Institute of Mathematics of NAS of Ukraine, Kyiv, Ukraine}
  - {name: Iryna Raievska, affiliation: Institute of Mathematics of NAS of Ukraine, Kyiv, Ukraine}
  - {name: Sergio Siccha, affiliation: TU Kaiserslautern, Germany}
---

<ol>{% assign participants = page.participants | sort: "name" %}
{% for p in participants %}
  <li>
    <strong>{{ p.name }}</strong>
    {% if p.affiliation != null %} ({{ p.affiliation }}){% endif %}
    {% if p.links != null %}
        {% for item in p.links %}
            <a href="{{ item[1] }}">({{ item[0] }})</a>
        {% endfor %}
    {% endif %}
    <br/>
      {% if p.talk != null %} Talk: {{ p.talk }}{% endif %}
  </li>
{% endfor %}
</ol>

{% if site.data.feedback.size > 0 %}

<ul>
{% for p in site.data.feedback %}
  <li>
    <strong>{{ p.name }}</strong>
    {% if p.package != null %} (author of {{ p.package }}){% endif %}
    <br/>
    {% if p.feedback != null %} {{ p.feedback }}{% endif %}
  </li>
{% endfor %}
</ul>

{% endif %}
