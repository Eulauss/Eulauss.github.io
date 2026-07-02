---
layout: page
permalink: /research/
title: Research
description:
nav: true
nav_order: 1
---

{% include publication_badge_styles.liquid %}

<p>
  <strong>Notes.</strong> <sup>*</sup> indicates equal contribution.
  <span style="color: #d73a49;">(&alpha;-&beta;)</span> indicates alphabetical author order.
</p>

<h2 class="bibliography">Preprints</h2>

<div class="publications">
{% bibliography --query @*[status=preprint] %}
</div>

<h2 class="bibliography">Accepted Papers</h2>

<div class="publications">
{% bibliography --query @*[status=accepted] %}
</div>

<h2 class="bibliography">Talks</h2>

{% assign talks = site.data.talks | sort: "sort_key" %}
{% if talks and talks.size > 0 %}
  <ol>
    {% for talk in talks %}
      <li>
        {% if talk.date %}{{ talk.date }}{% endif %}
        {% if talk.title %} <em>{{ talk.title }}</em>.{% endif %}
        {% if talk.url %}
          <a href="{{ talk.url }}" target="_blank" rel="external nofollow noopener">{{ talk.event }}</a>
        {% else %}
          {{ talk.event }}
        {% endif %}
        {% if talk.location %}, {{ talk.location }}{% endif %}{% if talk.note %}. {{ talk.note }}{% else %}.{% endif %}
      </li>
    {% endfor %}
  </ol>
{% endif %}
