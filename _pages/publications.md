---
layout: page
permalink: /publications/
title: Publications
description:
nav: true
nav_order: 1
---

<!-- _pages/publications.md -->

{% include publication_badge_styles.liquid %}

<p>
  <strong>Notes.</strong> <sup>*</sup> indicates equal contribution.
  <span style="color: #d73a49;">(&alpha;-&beta;)</span> indicates alphabetical author order.
</p>

<h2 class="bibliography">Preprints</h2>

<div class="publications">
{% bibliography --query @*[status=preprint] %}
</div>

<h2 class="bibliography">Accepted</h2>

<div class="publications">
{% bibliography --query @*[status=accepted] %}
</div>
