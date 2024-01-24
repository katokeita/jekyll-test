---
layout: common
---

# FAQ

{% assign doclist = site.pages | sort: 'url' %}


{% for faq in site.data.faq %}

<h3>{{ faq.name }}</h3>

<div class="faqBody">

<ul>

    {% for doc in doclist %}
        {% if doc.url contains faq.category %}

<li>
    <dl id="">
        <dt class="q"><span class="mark">Q</span><span class="text">{{doc.title}}</span></dt>
        <dd class="a toggleText">
            <span class="mark">A</span><span class="text">{{doc.content}}</span>
            パーマリンク：[{{doc.title}}]({{site.url}}{{site.repository}}{{doc.url}})
        </dd>
    </dl>
</li>

        {% endif %}
    {% endfor %}
</ul>
</div>
{% endfor %}
