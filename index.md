---
layout: default
---

### Downloads

{% assign books = site.static_files | where: "ebook", true %}

<ol>
{% for item in site.data.data %}
{% assign ebk = "/books/" | append: item.name | append: ".epub" %}
{% assign pbk = "/books/" | append: item.name | append: ".pdf" %}
{% if item.type == "ebook" %}
<li>{{item.name}} (<a href="{{ebk}}">EPUB</a>, <a href="{{pbk}}">PDF</a>) <small>{{ item.date }}</small></li>
{% elsif item.type == "pdf" %}
<li>{{item.name}} (<a href="{{pbk}}">PDF</a>) <small>{{ item.date }}</small></li>
{% endif %}
{% endfor %}
</ol>

  
### Miscellaneous

<ol>
{% for bpage in site.bits %}
<li><a href="{{bpage.id}}">{{bpage.title}}</a></li>
{% endfor %}
</ol>


<div style="clear: both;"></div>
