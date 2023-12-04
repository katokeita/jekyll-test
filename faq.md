---
layout: common
---

# FAQ

{% assign doclist = site.pages | sort: 'url' %}

{% for faq in site.data.faq %}
    {% for doc in doclist %}

        {% if doc.url contains faq.category %}

## {{ faq.name }} {{doc.title}}
{{doc.content}}

パーマリンク：[{{doc.title}}]({{doc.path}})

        {% endif %}

    {% endfor %}
{% endfor %}