---
layout: common
---

# Jekyll test page

Jekyll回りのテスト

## Site Variables

### site.url

{{site.url}}

{% assign doclist = site.pages | sort: 'url'  %}

{% for doc in doclist %}
    [{{ doc.name }}]({{ site.baseurl }}{{ doc.url }})
{% endfor %}

{% if site.url contains "katokeita" %}
    katokeita
{% endif %}

{{ layout.commonAssetsUrl }}
{{ commonAssetsUrl }}

## Page Variables

### page.title

{{page.title}}

### page.url

{{page.url}}

### page.date

{{ page.date}}

### page.id

{{page.id}}

### page.dir

{{page.dir}}

### page.name

{{page.name}}

### page.path

{{page.path}}

## Layout Variables

### layout.test

{{layout.test}}
