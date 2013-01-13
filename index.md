---
layout: page
title: Welcome
tagline: If you can dream it, you can do it!
---
{% include JB/setup %}

## About Me  

    
Hi. Welcome to my blog. I am Piyush and I love to code, read (anything but fiction. I enjoy reading philosophical books, stuff related to computer science, software development, tech blogs and probably anything which makes me think about my work and life in general), write (mostly technical stuff though I might start blogging more about various things I learn from people around me). I am opinionated but with a very impressionable mindset. I am always on a lookout for mentors and people from whom I can learn. I have been a professional programmer for almost 3 years now and am enjoying it more as I dive deeper. I have worked developing flight scheduling solutions for airline/aviation industry. I recently joined **Thought**Works because I felt a strong resonance in my values and goals with them. I am having fun here. Hope you enjoy my blogs.  

## Blogs  

<ul class="posts">
  {% for post in site.posts %}
    <li><span>{{ post.date | date_to_string }}</span> &raquo; <a href="{{ BASE_PATH }}{{ post.url }}">{{ post.title }}</a></li>
  {% endfor %}
</ul>

