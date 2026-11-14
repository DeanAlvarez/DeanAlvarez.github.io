---
layout: home
permalink: /
title: "About"
redirect_from: 
  - /about/
  - /about.html
---

<p class="notice">I'm looking for a research internship for summer 2027.</p>

I'm a PhD student in Computer Science at the University of Illinois Urbana-Champaign, advised by [ChengXiang Zhai](https://czhai.cs.illinois.edu/), and an NSF Graduate Research Fellow. I study how to organize text collections so that people and AI agents can browse them, not only search them. My work centers on **Hypergraph of Text**, a structure for making any document collection navigable, along with methods for building it, ways of evaluating it, and interfaces for exploring it. I'm especially interested in scientific literature, where knowing you've seen everything relevant matters most.

## Projects

<div class="project-list">
{% for p in site.data.projects %}{% if p.featured %}{% include project-card.html project=p %}{% endif %}{% endfor %}
</div>

[All projects →](/projects/)

## Selected Publications

{% assign selected = site.publications | where: 'selected', true | sort: 'date' | reverse %}
<ul class="pub-list">
{% for pub in selected %}{% include publication-entry.html pub=pub %}{% endfor %}
</ul>

[All publications →](/publications/)

## Recent Highlights

<div class="research-highlights">
<div class="research-card">
<h4>Co-organized ECOM'26</h4>
<p>2026 · Organized the data challenge for the SIGIR 2026 Workshop on eCommerce, extending the TREC Product Search track.</p>
</div>
<div class="research-card">
<h4>CHIIR 2026 Doctoral Consortium</h4>
<p>2026 · Presented my work on <a href="/publication/CHIIR-2026-conversation-enhanced-browsing">conversation-enhanced browsing</a> with Hypergraph of Text.</p>
</div>
<div class="research-card">
<h4>TREC 2025 Product Search Track</h4>
<p>2025 · Co-organized the track and built its product search baselines; presented the <a href="/publication/TREC-2025-product-search-overview">track overview</a>.</p>
</div>
<div class="research-card">
<h4>NSF GRFP Fellow</h4>
<p>2025 · Supporting my research on "New Generation of Information Access via Intelligent Assistant"</p>
</div>
</div>

## Beyond Research

Outside of research I enjoy reading, philosophy, listening to music, and strategy games.

---

<div class="cta-section">
<h3>Learn more</h3>
<p>{% if site.author.cv %}My <a href="{{ site.author.cv | relative_url }}">CV</a> has the full picture. {% endif %}You can find my papers on <a href="{{ site.author.googlescholar }}">Google Scholar</a> and more about my path on the <a href="/background/">Background</a> page.</p>
</div>
