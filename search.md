---
layout: page
title: Search
permalink: /search/
---
<form action="{{ site.url }}/search/" method="get">
  <label for="search-box">Search</label>
  <input type="text" id="search-box" name="query">
  <input type="submit" value="search">
</form>



<script>
  (function() {
    var cx = '013333465573234887905:-_9xc2mru6s';
    var gcse = document.createElement('script');
    gcse.type = 'text/javascript';
    gcse.async = true;
    gcse.src = 'https://cse.google.com/cse.js?cx=' + cx;
    var s = document.getElementsByTagName('script')[0];
    s.parentNode.insertBefore(gcse, s);
  })();
</script>
<gcse:search>Loading... Please wait</gcse:search>
