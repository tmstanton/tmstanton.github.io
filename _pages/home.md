---
title: "Home"
layout: homelay
permalink: /
---

<h1 class="home-hero">{{ site.name }}</h1>
<p class="home-hero-sub">{{ site.title }}, {{ site.institution }}</p>

I am an astronomer working on the chemical, nebular and stellar properties of galaxies in the local and early Universe, aiming to answer key questions about the evolution of galaxies across cosmic time.

{% capture selected %}{% bibliography --query @*[selected=true] %}{% endcapture %}
{% if selected contains "pub-entry" %}
## Selected publications

<div class="section-card selected-pubs" markdown="0">
{{ selected }}
<p style="margin: var(--space-4) 0 0;"><a href="{{ '/publications' | relative_url }}">All publications &rarr;</a></p>
</div>
{% endif %}

## About me

I was raised in Wiltshire in South West England. I moved to Edinburgh for my undergraduate degree in 2016, and stayed for another ten years thanks to some combination of the beauty of Edinburgh, my Scottish ancestry, and my aversion to hot weather.
My research primarily focuses on chemical abundance studies in the stellar and gas-phases across cosmic time.
I love to present my research to all types of audiences, and have been fortunate enough to travel the world sharing my science.
When not researching, I can be found with my nose in a fantasy novel, glued to the Playstation, baking, at the bouldering wall or out on a hike.
