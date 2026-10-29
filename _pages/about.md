---
title: "About"
layout: page
permalink: /about/
---

# About

<div class="section-card">
<div class="pi-card">
<img src="{{ site.photo | prepend: '/images/' | relative_url }}" class="pi-photo" alt="{{ site.name }}" width="160" height="160">
<div>
<h2 class="pi-name">{{ site.name }}</h2>
<p style="font-style: italic; color: var(--text-secondary);">{{ site.title }}, {{ site.institution }}</p>
<div class="pi-links">
{% if site.email %}<a href="mailto:{{ site.email }}" class="icon-link" title="Email" aria-label="Email">{% include icon.html name="envelope" %}</a>{% endif %}
{% if site.links.cv and site.links.cv != "" %}<a href="{{ site.links.cv | prepend: '/' | relative_url }}" class="icon-link" title="CV" aria-label="CV">{% include icon.html name="cv" %}</a>{% endif %}
{% if site.links.google_scholar and site.links.google_scholar != "" %}<a href="{{ site.links.google_scholar }}" class="icon-link" title="Google Scholar" aria-label="Google Scholar">{% include icon.html name="google-scholar" %}</a>{% endif %}
{% if site.links.github and site.links.github != "" %}<a href="{{ site.links.github }}" class="icon-link" title="GitHub" aria-label="GitHub">{% include icon.html name="github" %}</a>{% endif %}
{% if site.links.researchgate and site.links.researchgate != "" %}<a href="{{ site.links.researchgate }}" class="icon-link" title="ResearchGate" aria-label="ResearchGate">{% include icon.html name="researchgate" %}</a>{% endif %}
</div>
{% if site.data.pi[0].education %}
<ul style="margin-top: var(--space-4);">
{% for education in site.data.pi[0].education %}
<li>{{ education | replace: "-","&#8211;" }}</li>
{% endfor %}
</ul>
{% endif %}
</div>
</div>
</div>

The evolution of galaxies can be understood through their chemical evolution: the abundances of different elements trace the overarching processes regulating galaxy evolution, and preserve a record of their star-formation histories.
Stars forge heavier elements in their cores through nucleosynthesis, and release these metals into the surroundings upon their deaths via supernovae or stellar winds.
Over time, the gravity of galaxies leads to the accretion of recycled metals and new pristine gas, fuelling the next generations of star formation.
Tracing these processes, and breaking up what we mean by a 'metal' into different elements, offers a unique and powerful window into galaxy evolution.

I am an astronomer working on the chemical, nebular and stellar properties of galaxies in the local and early Universe, aiming to answer some key questions.
How did the first galaxies form stars and produce their first heavy elements? How do the relative abundances of different elements reveal the stellar populations responsible for enriching galaxies? How do chemical abundances constrain the processes regulating the evolution of galaxies across cosmic time?
I investigate these questions using a mix of spectroscopic and photometric observations (Keck, the Very Large Telescope, the Hubble Space Telescope and the James Webb Space Telescope) and theoretical modelling of chemical evolution and nebular properties.

Currently, I am a postdoctoral research associate at the Institute for Astronomy at the University of Edinburgh, working with Professor Ross McLure.
In this position, I am leading the development of nebular models which account for variable chemical abundance patterns observed at high-redshift, and investigating the impact of these patterns on the nebular emission of galaxies.
Prior to this position, I completed a PhD at the Institute for Astronomy,  University of Edinburgh, under the supervision of Fergus Cullen as part of the ERC- and UKRI-funded project 'ICE'.
Highlights from my PhD include the most precise measurement of α-enhancement in high-redshift systems, the first published sample of high-redshift Argon abundances, and a statistical analysis of the mass-metallicity and fundamental metallicity relationships up to _z > 8_. 

Beyond my research, I am committed to mentoring and supervision.
I have led observational astronomy labs, and taught in scientific and coding workshops at the University of Edinburgh, and delivered lectures on nebular astrophysics and academic writing as part of the Edinburgh School of Extragalactic Astrophysics. 
I have also participated in publc outreach, communicating exciting developments in high-redshift galaxy research and the emerging science from the JWST mission.
I am particularly interested in furthering diversity, equality and inclusion within astronomy and astrophysics, with a focus on widening participation.

{% if site.data.grants %}
<div class="section-card">
<h3>Grants</h3>
<ul>
{% for grant in site.data.grants %}
<li>{{ grant.name }}</li>
{% endfor %}
</ul>
</div>
{% endif %}

{% if site.data.awards %}
<div class="section-card">
<h3>Awards</h3>
<ul>
{% for award in site.data.awards %}
<li>{{ award.name | replace: "-","&#8211;" }}</li>
{% endfor %}
</ul>
</div>
{% endif %}

{% if site.data.funders %}
<div class="section-card">
<h4>Sponsors</h4>
<div class="sponsor-logos" style="display: flex; flex-wrap: wrap; align-items: center; justify-content: center; gap: var(--space-6);">
{% for funder in site.data.funders %}
<a href="{{ funder.url }}" target="_blank"><img src="{{ funder.image | prepend: '/images/' | relative_url }}" alt="Funder logo" style="max-height: 80px; max-width: 200px; border-radius: 0;" loading="lazy"></a>
{% endfor %}
</div>
</div>
{% endif %}
