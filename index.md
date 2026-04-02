---
layout: default
title: "ShieldSmart — Simple Security for Real People"
description: "Practical, jargon-free cybersecurity tips and tools for everyday people."
permalink: /
---

<section class="hero" aria-labelledby="hero-heading">
  <div class="container hero-inner">
    <div class="hero-text">
      <span class="hero-eyebrow">Digital security for everyone</span>
      <h1 id="hero-heading" class="hero-title">
        Security Isn&rsquo;t About Being Paranoid&mdash;<em>It&rsquo;s About Being Smart</em>
      </h1>
      <p class="hero-body">
        You don&rsquo;t have to be a hacker&rsquo;s target to get hacked. Every day,
        ordinary people lose money, photos, and private messages to simple, preventable
        mistakes. Learn the habits that actually make a difference.
      </p>
      <div class="hero-actions">
        <a href="{{ '/blog/' | relative_url }}" class="btn btn-primary btn-lg">Read the Tips</a>
        <a href="{{ '/tools/' | relative_url }}" class="btn btn-outline btn-lg">Browse Tools</a>
      </div>
    </div>
    <div class="hero-stat-card" aria-label="Security threat statistics">
      <div class="stat-item">
        <span class="stat-number">3.4B</span>
        <span class="stat-label">phishing emails sent <em>every day</em></span>
      </div>
      <div class="stat-divider" aria-hidden="true"></div>
      <div class="stat-item">
        <span class="stat-number">81%</span>
        <span class="stat-label">of breaches involve stolen or weak passwords</span>
      </div>
      <div class="stat-divider" aria-hidden="true"></div>
      <div class="stat-item">
        <span class="stat-number">$4.9M</span>
        <span class="stat-label">average cost of a data breach in 2024</span>
      </div>
    </div>
  </div>
</section>

<section class="reality-check" aria-labelledby="reality-heading">
  <div class="container">
    <div class="reality-inner">
      <h2 id="reality-heading" class="section-title">&ldquo;But I&rsquo;m not interesting enough to hack.&rdquo;</h2>
      <p class="section-subtitle">
        Attackers rarely target <em>you specifically</em>. They run automated tools that try millions
        of accounts at once, looking for the easiest doors to push open. A few simple habits slam those doors shut.
      </p>
      <div class="myth-grid">
        <div class="myth-card">
          <span class="myth-icon" aria-hidden="true">&#x1F4B8;</span>
          <h3>Financial theft</h3>
          <p>Credential-stuffing attacks try leaked passwords on banking sites automatically—no targeting required.</p>
        </div>
        <div class="myth-card">
          <span class="myth-icon" aria-hidden="true">&#x1F4F7;</span>
          <h3>Ransomed memories</h3>
          <p>Ransomware encrypts your photos and documents and demands payment. It doesn&rsquo;t care who you are.</p>
        </div>
        <div class="myth-card">
          <span class="myth-icon" aria-hidden="true">&#x1F465;</span>
          <h3>Identity fraud</h3>
          <p>Your name and date of birth are worth money on the dark web—used to open credit cards or file false taxes.</p>
        </div>
        <div class="myth-card">
          <span class="myth-icon" aria-hidden="true">&#x1F4E7;</span>
          <h3>Account takeover</h3>
          <p>Compromised accounts are used to scam your contacts, extort you, or lock you out of your digital life.</p>
        </div>
      </div>
    </div>
  </div>
</section>

<section class="categories-section" aria-labelledby="categories-heading">
  <div class="container">
    <h2 id="categories-heading" class="section-title">Where do you want to start?</h2>
    <p class="section-subtitle">Pick a topic and learn one thing today. Small steps add up.</p>
    <div class="category-grid">
      <a href="{{ '/blog/' | relative_url }}#passwords" class="category-card cat-passwords">
        <span class="cat-icon" aria-hidden="true">&#x1F511;</span>
        <h3>Passwords</h3>
        <p>Stop reusing passwords and make the one change that protects all your accounts.</p>
      </a>
      <a href="{{ '/blog/' | relative_url }}#phishing" class="category-card cat-phishing">
        <span class="cat-icon" aria-hidden="true">&#x1F3A3;</span>
        <h3>Phishing</h3>
        <p>Learn to spot fake emails, texts, and links before you click.</p>
      </a>
      <a href="{{ '/blog/' | relative_url }}#two-factor" class="category-card cat-two-factor">
        <span class="cat-icon" aria-hidden="true">&#x1F510;</span>
        <h3>Two-Factor Auth</h3>
        <p>Add a second lock so a stolen password isn&rsquo;t enough to get in.</p>
      </a>
      <a href="{{ '/blog/' | relative_url }}#updates" class="category-card cat-updates">
        <span class="cat-icon" aria-hidden="true">&#x1F504;</span>
        <h3>Software Updates</h3>
        <p>Why &ldquo;remind me later&rdquo; is one of the riskiest buttons you press.</p>
      </a>
      <a href="{{ '/blog/' | relative_url }}#wifi" class="category-card cat-wifi">
        <span class="cat-icon" aria-hidden="true">&#x1F4F6;</span>
        <h3>Wi-Fi Safety</h3>
        <p>What to do&mdash;and not do&mdash;on public networks.</p>
      </a>
      <a href="{{ '/blog/' | relative_url }}#backups" class="category-card cat-backups">
        <span class="cat-icon" aria-hidden="true">&#x2601;</span>
        <h3>Backups</h3>
        <p>Protect your files so theft, disaster, or ransomware can&rsquo;t erase them.</p>
      </a>
    </div>
  </div>
</section>

<section class="posts-preview" aria-labelledby="posts-heading">
  <div class="container">
    <div class="section-header-row">
      <h2 id="posts-heading" class="section-title">Latest Tips</h2>
      <a href="{{ '/blog/' | relative_url }}" class="see-all-link">See all &rarr;</a>
    </div>
    <div class="posts-grid">
      {% for post in site.posts limit:3 %}
      <article class="post-card">
        {% if post.category %}
        <span class="category-badge category-{{ post.category | downcase | replace: ' ', '-' }}">{{ post.category }}</span>
        {% endif %}
        <h3 class="post-card-title"><a href="{{ post.url | relative_url }}">{{ post.title }}</a></h3>
        <p class="post-card-excerpt">{{ post.excerpt | strip_html | truncate: 130 }}</p>
        <div class="post-card-meta">
          <time datetime="{{ post.date | date_to_xmlschema }}">{{ post.date | date: "%b %-d, %Y" }}</time>
          {% if post.read_time %}<span>&middot; {{ post.read_time }} min read</span>{% endif %}
        </div>
      </article>
      {% endfor %}
    </div>
  </div>
</section>

<section class="tools-banner" aria-label="Browse security tools">
  <div class="container tools-banner-inner">
    <div class="tools-banner-text">
      <h2>Find the right tool for the job</h2>
      <p>Our curated directory lists the best free and paid security software, filtered by category and platform. No affiliate links.</p>
    </div>
    <a href="{{ '/tools/' | relative_url }}" class="btn btn-light btn-lg">Browse the Directory &rarr;</a>
  </div>
</section>
