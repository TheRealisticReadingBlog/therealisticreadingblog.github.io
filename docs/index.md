---
# Feel free to add content and custom Front Matter to this file.
# To modify the layout, see https://jekyllrb.com/docs/themes/#overriding-theme-defaults

layout: home
title: Home
pagination: true
---

<h1>{{ page.title }}</h1>


<p>
Hello, World! 🌍
This is my homepage created with Jekyll and GitHub Pages.

Originally, I looked into creating a website with Wordpress. However, it became evident that that was a bit overkill for what I wanted!

As a developer by day, I'd consider myself quite with Github - and with no upfront cost, it's a great option to get started.

</p
>
{% for post in paginator.posts %}
  <article>
    <h2><a href="{{ post.url | relative_url }}">{{ post.title }}</a></h2>
    <p>{{ post.excerpt }}</p>
  </article>
{% endfor %}

<!-- Pagination Links -->
<div class="pagination">
  {% if paginator.previous_page %}
    <a href="{{ paginator.previous_page_path | relative_url }}">&laquo; Previous</a>
  {% endif %}

  <span>Page {{ paginator.page }} of {{ paginator.total_pages }}</span>

  {% if paginator.next_page %}
    <a href="{{ paginator.next_page_path | relative_url }}">Next &raquo;</a>
  {% endif %}
</div>