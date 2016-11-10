---
layout: default
---

# jekyll variables

- `site.title` : {{ site.title }} - de site title uit `config.yml`
- `layout` : {{ layout }}
- `page.url` : {{ page.url }}
- `page.date` : {{ page.date }}
- `page.path` : {{ page.path }}

All pages:

{% for p in site.pages %}
- url: `{{ p.url }}` - path: `{{ p.path }}`
{% endfor %}

