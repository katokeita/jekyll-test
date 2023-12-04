---
layout: common
---

# FAQ

{% assign doclist = site.pages | sort: 'url' %}

{% for faq in site.data.faq %}
    {% for doc in doclist %}

## {{ faq.name }}

        {% if doc.url contains faq.category %}

### {{doc.title}}
{{doc.content}}

パーマリンク：[{{doc.title}}]({{site.url}}{{site.repository}}{{doc.url}})

        {% endif %}

    {% endfor %}
{% endfor %}