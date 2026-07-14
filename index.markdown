---
# Feel free to add content and custom Front Matter to this file.
# To modify the layout, see https://jekyllrb.com/docs/themes/#overriding-theme-defaults

---

<ul class='post-list'>
    {% for dir in site.collections %}
      {% assign collection = dir.label %}
      {% for page in site[collection] %}
        <li>
          <img class='collection-icon' src="{{ src }}" alt="">
          <h2> <a href="{{ page.url | prepend: site.baseurl }}">{{ page.title }}</a> </h2>
          <small>{{ page.date | date: "%b %-d, %Y" }}</small>
        </li>
      {% endfor %}
    {% endfor %}
  </ul>