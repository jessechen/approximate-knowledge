---
layout: default
title: Words
permalink: /words/
---
<div class="home">
    <h1 class="page-heading">Index of all words</h1>
    <ol>
        {% assign sortedPosts = site.posts | sort: "origin" %}
        {%- for post in sortedPosts -%}
        <li>
            <a href="{{ post.url | relative_url }}">{{ post.title | escape }}</a>
            ({{ post.origin }})
        </li>
        {%- endfor -%}
    </ol>
</div>
