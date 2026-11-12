---
title: "Talks"
layout: page
permalink: /talks/
---

# Talks

I enjoy communicating to specialist and non-specialist audiences about my research, the JWST mission and astronomy in general!
Below I list my recent (and upcoming) invited and contributed conference presentations. 

<div class="banner-frame" markdown="0">
<img src="{{ '/images/conference-talks.jpg' | relative_url }}" alt="Me, presenting EXCELS results at the Tokyo 2026 Meeting" loading="lazy">
<div class="banner-caption">Presenting results from the EXCELS survey at the 'Towards the Full Bloom of First Star, Galaxy, and Black Hole Formation Exploration: JWST + Multi-Facility Observations and Theory for Future Programs' meeting in Tokyo (2026). </div>
</div>


<style>
.talks-feature {
    display: grid;
    grid-template-columns: 1fr 1fr;
    gap: 20px;
    align-items: start;
    margin: 25px 0 35px;
}

.talks-feature-image img {
    width: 100%;
    height: auto;
    display: block;
    border-radius: 8px;
}

.talks-feature-video {
    width: 100%;
    aspect-ratio: 16 / 9;
}

.talks-feature-video iframe {
    width: 100%;
    height: 100%;
    border: none;
    border-radius: 8px;
}

.talks-feature .banner-caption {
    margin-top: 8px;
}

@media (max-width: 700px) {
    .talks-feature {
        grid-template-columns: 1fr;
    }
}
</style>

<div class="talks-feature">

    <div class="talks-feature-image">
        <img src="{{ '/images/conference-talks.jpg' | relative_url }}"
             alt="Me, presenting EXCELS results at the Tokyo 2026 Meeting"
             loading="lazy">

        <div class="banner-caption">
            Presenting results from the EXCELS survey at the
            'Towards the Full Bloom of First Star, Galaxy, and
            Black Hole Formation Exploration: JWST + Multi-Facility
            Observations and Theory for Future Programs' meeting
            in Tokyo (2026).
        </div>
    </div>

    <div class="talks-feature-video">
        <iframe
            src="https://www.youtube.com/embed/1UBjutKzmrc?start=2785&end=3491"
            title="Featured conference talk"
            allowfullscreen>
        </iframe>
    </div>

</div>


{% assign invited = site.data.talks | where: "type", "invited" %}
{% assign contributed = site.data.talks | where_exp: "t", "t.type != 'invited'" %}

{% if invited.size > 0 %}
<div class="section-card" markdown="0">
<h2>Invited Talks</h2>
{% for talk in invited %}{% include talk.html talk=talk %}{% endfor %}
</div>
{% endif %}

{% if contributed.size > 0 %}
<div class="section-card" markdown="0">
<h2>Contributed Talks</h2>
{% for talk in contributed %}{% include talk.html talk=talk %}{% endfor %}
</div>
{% endif %}

{% unless site.data.talks.size > 0 %}
<p class="text-muted">No talks listed yet. Add entries to <code>_data/talks.yml</code>.</p>
{% endunless %}
