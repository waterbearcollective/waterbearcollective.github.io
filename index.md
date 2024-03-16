---
layout: front.njk
---

<h1> Edge Collective </h1>

<div class="posts-area">

{% for note in collections.notes reversed %}
  <div class="post">
    <div class="note-contents">
      <div class="image">
        <a href="{{ note.url }}">
          <img src="{{ note.data.image }}"/>
        </a>
      </div>
      <div class="text">
        <h3><a href="{{ note.url }}">{{ note.data.pageTitle }}</a></h3>
        <p>{{ note.data.blurb }}</p>
        <em>Updated: {{ note.date | date: "%Y-%m-%d" }}</em>
      </div>
    </div>
  </div>
{% endfor %}
</div>

