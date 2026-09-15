---
layout: default
title: "Aarav Vikram"
avatar: "assets/inkitt-avatar.png"
author_name: "Aarav Vikram"
bio: "Hi, I’m Aarav Vikram — dev by day, Literotica writer by…....questionable life choices."
quote: "You're the writer, right? I wonder how you got this so wrong — feels like someone is too much into the romance to actually read the tragedy."
quote_footer: "from Timeless Love Quest"
---

<div class="container">
  <!-- Profile Header -->
  <img src="{{ page.avatar | relative_url }}" alt="{{ page.author_name }}" class="profile-img">
  <h1>{{ page.author_name }}</h1>
  {% if page.bio %}
  <p class="bio">{{ page.bio }}</p>
  {% endif %}

  <!-- Social Icons Bar -->
  <div class="social-row">
    {% for social in site.data.links.socials %}
      <a href="{{ social.url }}" target="_blank" rel="noopener" title="{{ social.platform }}">
        <img src="{{ 'assets/icons/' | append: social.icon | append: '.svg' | relative_url }}" alt="{{ social.platform }}">
      </a>
    {% endfor %}
  </div>

  <!-- Terminal Quote Box -->
  {% if page.quote %}
  <div class="terminal-box">
    <div class="terminal-header">
      <div class="terminal-dots">
        <span class="dot red"></span>
        <span class="dot yellow"></span>
        <span class="dot green"></span>
      </div>
      <span class="terminal-title">quote.txt</span>
    </div>
    <div class="terminal-body">
      <span class="prompt">&gt;</span>
      <div class="quote-content">
        <p class="quote-text">"{{ page.quote }}"</p>
        {% if page.quote_footer %}
        <p class="quote-footer">— {{ page.quote_footer }}</p>
        {% endif %}
      </div>
    </div>
  </div>
  {% endif %}

  <!-- Link Pills -->
  <div class="links">
    {% for item in site.data.links.links %}
      {% if item.url %}
        <a href="{{ item.url }}" class="link-card{% if item.featured %} featured{% endif %}" target="_blank" rel="noopener">
          {% if item.badge %}
            {% if item.badge contains '/' or item.badge contains '.' %}
              <img src="{{ item.badge | relative_url }}" class="thumb-badge" alt="">
            {% else %}
              <span class="thumb-badge emoji-badge" aria-hidden="true">{{ item.badge }}</span>
            {% endif %}
          {% endif %}
          <span>{{ item.title }}</span>
        </a>
      {% else %}
        <div class="link-card{% if item.featured %} featured{% endif %}">
          {% if item.badge %}
            {% if item.badge contains '/' or item.badge contains '.' %}
              <img src="{{ item.badge | relative_url }}" class="thumb-badge" alt="">
            {% else %}
              <span class="thumb-badge emoji-badge" aria-hidden="true">{{ item.badge }}</span>
            {% endif %}
          {% endif %}
          <span>{{ item.title }}</span>
        </div>
      {% endif %}
    {% endfor %}
  </div>

  {% include footer.html %}
</div>
