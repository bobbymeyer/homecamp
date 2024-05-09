---
layout: default
title: "HomeCamp '24"
---


<h1 class='title bento'>HomeCamp '24</h1>

<div class='grid lg:grid-cols-3'>
{% for post in site.posts reversed %}

<a href='{{ post.url }}' class='bento'>
<div class='grid h-full items-center'>
    <h1 class='text-4xl'>
        {{ post.title }}
    </h1>
    {% assign future_date = post.date | date: "%s" | plus: 518400 | date: "%B %d, %Y" %}
    <i>{{ post.date | date: "%B %d, %Y" }} - {{ future_date }}</i>
</div>
</a>

{% endfor %}
</div>
