---
layout: page
title: Teaching
icon: fas fa-chalkboard-teacher
order: 1
---

## Graduate Teaching Assistant — Sungkyunkwan University

Labs and exercise sessions for undergraduate Computer Science courses. Weekly
exercises and their solutions are published below.

### Basis and Practice in Programming (DASF004-41)

<style>
  .teaching-list { list-style: none; padding-left: 0; }
  .teaching-list li {
    display: grid;
    grid-template-columns: 110px 1fr auto;
    gap: 0.75rem;
    align-items: baseline;
    padding: 0.4rem 0;
    border-bottom: 1px solid rgba(128,128,128,0.15);
  }
  .teaching-list li time {
    color: var(--text-muted-color, #888);
    font-variant-numeric: tabular-nums;
    font-size: 0.88rem;
  }
  .teaching-list li .tag {
    font-size: 0.75rem;
    padding: 0.15rem 0.5rem;
    border-radius: 999px;
    background: rgba(128,128,128,0.12);
    color: var(--text-muted-color, #888);
  }
  .teaching-list li .tag.solution { background: rgba(40, 167, 69, 0.15); color: #198754; }
  .teaching-list li .tag.exercise { background: rgba(13, 110, 253, 0.12); color: #0d6efd; }
  @media (max-width: 560px) {
    .teaching-list li { grid-template-columns: 1fr auto; }
    .teaching-list li time { grid-column: 1 / -1; }
  }
</style>

{% assign course_posts = site.posts | where_exp: "p", "p.categories contains 'Basis and Practice in Programming_DASF004_41'" | sort: "date" %}

#### Exercises

<ul class="teaching-list">
{% for post in course_posts %}
  {% if post.categories contains 'Exercices' %}
  <li>
    <time>{{ post.date | date: "%b %-d, %Y" }}</time>
    <a href="{{ post.url | relative_url }}">{{ post.title }}</a>
    <span class="tag exercise">exercise</span>
  </li>
  {% endif %}
{% endfor %}
</ul>

#### Solutions

<ul class="teaching-list">
{% for post in course_posts %}
  {% if post.categories contains 'Solutions' %}
  <li>
    <time>{{ post.date | date: "%b %-d, %Y" }}</time>
    <a href="{{ post.url | relative_url }}">{{ post.title }}</a>
    <span class="tag solution">solution</span>
  </li>
  {% endif %}
{% endfor %}
</ul>
