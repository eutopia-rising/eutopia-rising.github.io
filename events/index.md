---
title: Eutopia Rising Events
layout: page
---

<section>
  {% assign page_list = site.pages | sort: "date" | where: "event", "true" %}
  {% for page in page_list reversed %}
  <article>
    {% if page.image.title %}
    <figure>
      <img src="{{ page.dir}}{{ page.image.title }}" width="970" alt="{{ page.title | escape_once }}" itemprop="image">

      {% if page.image.caption_url and page.image.caption %}
      <figcaption class="text-right">
	<a href="{{ page.image.caption_url }}">{{ page.image.caption }}</a>
      </figcaption>
      {% elsif page.image.caption %}
      <figcaption class="text-right">
	{{ page.image.caption }}
      </figcaption>
      {% endif %}
    </figure>
    {% endif %}
    <h1><a href="{{ page.url }}">{{ page.title }}</a></h1>
    <time>{{ page.date | date: "%B %-d, %Y" }}</time>
    {{ page.content }}
  </article>
  {% endfor %}
</section>
