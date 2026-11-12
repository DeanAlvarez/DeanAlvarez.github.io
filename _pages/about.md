---
layout: home
permalink: /
title: "About"
redirect_from: 
  - /about/
  - /about.html
---

I'm a Ph.D. candidate in Computer Science at the University of Illinois Urbana-Champaign, advised by Professor [ChengXiang Zhai](https://czhai.cs.illinois.edu/).

I study how to make any document collection navigable. My work develops **Hypergraph of Text**, a structure that organizes a collection's content for browsing and analysis, together with methods for building it at scale and interfaces, including conversational ones, that help people explore and make sense of large text collections. More broadly, I work on information retrieval, information access, natural language processing, and product search.

<!-- ## Research Vision

I believe that the future of information access lies in **structured understanding** rather than just keyword matching. When we can represent the collective knowledge of humanity as an interconnected graph, we unlock new possibilities for:

- **Education**: Personalized learning paths through knowledge networks
- **Research**: Accelerated discovery through intelligent literature navigation
- **Decision Making**: Better insights through comprehensive information synthesis -->

## Recent Highlights

<div class="research-highlights">
<div class="research-card">
<h4>Co-organizing ECOM'26</h4>
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

## Selected Publications

{% assign selected = site.publications | where: 'selected', true | sort: 'date' | reverse %}
<ul class="pub-list">
{% for pub in selected %}{% include publication-entry.html pub=pub %}{% endfor %}
</ul>

[All publications →](/publications/)

## Beyond Research

Outside of research I enjoy reading, philosophy, listening to music, and strategy games.

---

<div class="cta-section">
<h3>Learn More</h3>
<p>Interested in collaborating or learning more about my work? Check out my <a href="https://scholar.google.com/citations?user=WCSG8bwAAAAJ&hl=en">Google Scholar</a> for publications, or explore my <a href="/background/">Background</a> for a complete overview of my journey.</p>
</div>
