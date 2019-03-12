---
layout: page
title: Search
permalink: /search2/
---

<form class="form-inline my-2 my-lg-0" method="get" action="{{site.baseurl}}/search2/">
          <input class="form-control mr-sm-2" id="search-box" type="search" placeholder="Search" aria-label="Search" name="query">
          <button class="btn btn-info shadow-sm my-2 my-sm-0" type="submit" value="search">Search</button>
        </form>
<ul id="search-results"></ul>

<script>
  window.store = {
    {% for post in site.posts %}
      "{{ post.url | slugify }}": {
        "title": "{{ post.title | xml_escape }}",
        "author": "{{ post.author | xml_escape }}",
        "category": "{{ post.category | xml_escape }}",
        "content": {{ post.content | strip_html | strip_newlines | jsonify }},
        "url": "{{ post.url | xml_escape }}"
      }
      {% unless forloop.last %},{% endunless %}
    {% endfor %}
  };
</script>
<script src="{{'/bs/assets/javascripts/lunr.min.js' | prepend: site.baseurl}}"></script>
<script src="{{'/bs/assets/javascripts/search.js' | prepend: site.baseurl}}"></script>
