---
layout: default
title: Welcome
---

I am a rising senior at Harvard, studying statistics and computer science
([CSE](http://www.seas.harvard.edu/programs/graduate/computational-science-and-engineering/master-of-science-in-cse)).
I'm currently a research assistant in the [Huttenhower
Lab](http://huttenhower.sph.harvard.edu/), where I build tools to analyze
microbiome data. I'm broadly interested in applications of statistics and
computer science to biological and social sciences problems. 


{% for post in site.posts %}

<article class='post'>
  <h1 class='post-title'>
    <a href="{{ site.path }}{{ post.url }}">
      {{ post.title }}
    </a>
  </h1>
  <div class="post-date">{{ post.date | date: "%b %-d, %Y" }}</div>
  {{ post.content }}
</article>

{% endfor %}

