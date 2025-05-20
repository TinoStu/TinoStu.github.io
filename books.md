---
layout: single
title: "Books"
permalink: /books/
---

## Recommended Reading:

{% assign book_section = site.data.recommended_reading | where_exp: "group", "group.category == 'Books'" | first %}

{% if book_section and book_section.items %}
  <div class="grid__wrapper">
    {% for book in book_section.items %}
      <div class="archive__item" style="margin-bottom: 2em; padding: 1em; border: 1px solid #333;">
        {% if book.header_note %}
          <p style="background-color: #0078D4; color: white; padding: 0.3em 0.6em; text-align: left; font-size: 0.9em; display: inline-block; margin-bottom: 0.5em;">
            <strong>{{ book.header_note }}</strong>
          </p>
        {% endif %}

        {% if book.image %}
          <div class="archive__item-teaser" style="text-align: center; margin-bottom: 1em;">
            <a href="{{ book.url }}" target="_blank" rel="noopener noreferrer">
              <img src="{{ book.image | relative_url }}" alt="{{ book.title }} cover" style="display: block; width: auto; max-width: 100%; height: auto !important; max-height: 260px; margin-left: auto; margin-right: auto;">
            </a>
          </div>
        {% endif %}

        <div class="archive__item-body">
          <h3 class="archive__item-title" style="margin-bottom: 0.25em;">
            <a href="{{ book.url }}" target="_blank" rel="noopener noreferrer">{{ book.title }}</a>
          </h3>
          {% if book.subtitle %}<p class="archive__item-excerpt" style="font-size: 0.9em; margin-bottom: 0.5em;">{{ book.subtitle }}</p>{% endif %}
          {% if book.edition %}<p style="font-size: 0.85em; margin-bottom: 0.25em;"><strong>{{ book.edition }}</strong></p>{% endif %}
          {% if book.authors %}<p style="font-size: 0.85em; margin-bottom: 1em;">By: {{ book.authors }}</p>{% endif %}

          {% if book.publisher_logo %}
            <div style="text-align: right; margin-bottom: 1em;">
              <img src="{{ book.publisher_logo | relative_url }}" alt="Publisher Logo" style="max-height: 25px;">
            </div>
          {% endif %}
          
          <p style="font-size: 0.9em; margin-top: 0.5em;">
            <strong>Link:</strong> <a href="{{ book.url }}" target="_blank" rel="noopener noreferrer">{{ book.url }}</a>
          </p>
        </div>
      </div>
    {% endfor %}
  </div>
{% else %}
  <p>No recommended books found in the 'Books' category.</p>
{% endif %}