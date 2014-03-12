---
layout: page
title: my insights
tagline: software, life and more...
---
{% include JB/setup %}

## About Me


Hi. Welcome to my blog. I am Piyush and I love to code. I enjoy reading philosophical books, stuff related to computer science, software development, tech blogs and probably anything which makes me think about my work and life in general, write - mostly technical stuff though I might start blogging more about various things I learn from people around me. I am opinionated but with a very impressionable mindset. I am always on a lookout for mentors and people from whom I can learn. I am coding professionally for almost 4 years now and am enjoying it more as I dive deeper. I have worked developing scheduling (flight/crew) solutions for airline/aviation industry. Hope you enjoy my blogs.

[TW]: http://www.thoughtworks.com

## Blogs

<ul class="posts">
  {% for post in site.posts %}
    <li><span>{{ post.date | date_to_string }}</span> &raquo; <a href="{{ BASE_PATH }}{{ post.url }}">{{ post.title }}</a></li>
  {% endfor %}
</ul>

## My github repo

[Github][github]
[github]: https://github.com/piyush0101/
