---
layout: page
title: bookshelf
permalink: /books/
nav: true
nav_order: 4
---
> “The man who does not read has no advantage over the man who cannot read.” — Mark Twain

{% comment %} Separate books by category and sort by status {% endcomment %}
{% assign technical_books_all = site.books | where: "category", "Technical Books" %}
{% assign technical_reading = technical_books_all | where: "status", "Currently Reading" | sort: "order" %}
{% assign technical_completed = technical_books_all | where: "status", "Completed" | sort: "order" %}
{% assign technical_books = technical_reading | concat: technical_completed %}

{% assign other_books_all = site.books | where: "category", "Other Books" %}
{% assign other_reading = other_books_all | where: "status", "Currently Reading" | sort: "order" %}
{% assign other_completed = other_books_all | where: "status", "Completed" | sort: "order" %}
{% assign other_books = other_reading | concat: other_completed %}

{% assign courses = site.books | where: "category", "Courses" | sort: "order" %}

{% assign book_cover_style = "object-fit: cover; border-radius: 4px; box-shadow: 0 2px 8px rgba(0,0,0,0.1); display: block;" %}
{% assign book_status_style_reading = "background: rgba(255, 193, 7, 0.75); color: #333;" %}
{% assign book_status_style_completed = "background: rgba(76, 175, 80, 0.75); color: white;" %}

## Technical Books

<div style="display: flex; flex-wrap: wrap; gap: 1%; margin-bottom: 40px;">
{% for book in technical_books %}
  <div style="width: 19%; margin-bottom: 20px;">
    <div style="position: relative;">
      {% if book.cover %}
        <img src="{{ book.cover | relative_url }}" alt="{{ book.title }}" style="width: 100%; height: 255px; {{ book_cover_style }}">
      {% else %}
        <div style="width: 100%; height: 255px; background: #e0e0e0; display: flex; align-items: center; justify-content: center; border-radius: 4px;">
          <span style="color: #666; text-align: center; padding: 10px; font-size: 12px;">No Cover</span>
        </div>
      {% endif %}

      {% if book.status %}
        <div style="position: absolute; bottom: 0; left: 0; width: 100%; padding: 6px 0; text-align: center; font-size: 10px; font-weight: 600; text-transform: uppercase; letter-spacing: 0.5px; border-radius: 0 0 4px 4px; {% if book.status == 'Currently Reading' %}{{ book_status_style_reading }}{% else %}{{ book_status_style_completed }}{% endif %}">
          {{ book.status }}
        </div>
      {% endif %}
    </div>
  </div>
{% endfor %}
</div>


## Online Courses

<div style="display: flex; flex-wrap: wrap; gap: 2%; margin-bottom: 40px;">
{% for book in courses %}
  <div style="width: 31%; margin-bottom: 20px;">
    <div style="position: relative;">
      {% if book.cover %}
        <img src="{{ book.cover | relative_url }}" alt="{{ book.title }}" style="width: 100%; height: 169px; {{ book_cover_style }}">
      {% else %}
        <div style="width: 100%; height: 169px; background: #e0e0e0; display: flex; align-items: center; justify-content: center; border-radius: 4px;">
          <span style="color: #666; text-align: center; padding: 10px; font-size: 12px;">No Cover</span>
        </div>
      {% endif %}

      {% if book.status %}
        <div style="position: absolute; bottom: 0; left: 0; width: 100%; padding: 6px 0; text-align: center; font-size: 10px; font-weight: 600; text-transform: uppercase; letter-spacing: 0.5px; border-radius: 0 0 4px 4px; {% if book.status contains 'Currently' %}{{ book_status_style_reading }}{% else %}{{ book_status_style_completed }}{% endif %}">
          {{ book.status }}
        </div>
      {% endif %}
    </div>

    <div style="margin-top: 8px; font-size: 13px; color: #333; text-align: center; font-weight: 500;">
      {{ book.title }}
    </div>
  </div>
{% endfor %}
</div>



## Other Books

<div style="display: flex; flex-wrap: wrap; gap: 1%; margin-bottom: 40px;">
{% for book in other_books %}
  <div style="width: 19%; margin-bottom: 20px;">
    <div style="position: relative;">
      {% if book.cover %}
        <img src="{{ book.cover | relative_url }}" alt="{{ book.title }}" style="width: 100%; height: 255px; {{ book_cover_style }}">
      {% else %}
        <div style="width: 100%; height: 255px; background: #e0e0e0; display: flex; align-items: center; justify-content: center; border-radius: 4px;">
          <span style="color: #666; text-align: center; padding: 10px; font-size: 12px;">No Cover</span>
        </div>
      {% endif %}

      {% if book.status %}
        <div style="position: absolute; bottom: 0; left: 0; width: 100%; padding: 6px 0; text-align: center; font-size: 10px; font-weight: 600; text-transform: uppercase; letter-spacing: 0.5px; border-radius: 0 0 4px 4px; {% if book.status == 'Currently Reading' %}{{ book_status_style_reading }}{% else %}{{ book_status_style_completed }}{% endif %}">
          {{ book.status }}
        </div>
      {% endif %}
    </div>
  </div>
{% endfor %}
</div>

