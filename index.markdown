---
# Feel free to add content and custom Front Matter to this file.
# To modify the layout, see https://jekyllrb.com/docs/themes/#overriding-theme-defaults

layout: page
---

<h1>Latest Post</h1>
{% for post in site.posts limit:1 %}
<div><a href="{{ post.url }}">{{ post.title }}</a></div>
{% endfor %}

<br />
<h1>Recent Posts</h1>
{% for post in site.posts offset:1 limit:5 %}
... Show the next two posts ...
{% endfor %}

<h1>Categories</h1>
<p>
{% for category in site.categories %}
<span><a href="/categories/{{category[0]}}/">{{ category[0] }}({{ category[1].size }})</a></span>
{% endfor %}
</p>

<h1>Tags</h1>
<p>
{% for tag in site.tags %}
    #{{ tag[0] }}
{% endfor %}
</p>


<!-- <div id="archives">
{% for category in site.categories %}
  <div class="archive-group">
    {% capture category_name %}{{ category | first }}{% endcapture %}
    <div id="#{{ category_name | slugize }}"></div>
    <p></p>

    <h3 class="category-head">{{ category_name }}</h3>
    <a name="{{ category_name | slugize }}"></a>
    {% for post in site.categories[category_name] %}
    <article class="archive-item">
      <h4><a href="{{ site.baseurl }}{{ post.url }}">{{post.title}}</a></h4>
    </article>
    {% endfor %}
  </div>
{% endfor %}
</div> -->
