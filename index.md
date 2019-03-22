---
# Feel free to add content and custom Front Matter to this file.
# To modify the layout, see https://jekyllrb.com/docs/themes/#overriding-theme-defaults

# FRONT MATTER

#tags:
#    - jekyll
#    - blog
#    - minimalista
#show_footer: TRUE

layout: default
#title: "Leandro Ribeiro Moura"
#helloworld: "Hello World com Liquid"


---

<!--LIQUID TEMPLATE
<h1>{{ page.helloworld }}</h1>

{% for tag in page.tags %}
    {{ tag }}
{% endfor %}


{% if page.show_footer %}
<footer>
    <p>Show!</p>
</footer>
{% endif %}-->

<head>
<link rel="stylesheet" href="css/main.css">
</head>


<div class="content list">
  {% if site.posts.size == 0 %}
    <h2>No post found =( </h2>
  {% else %}
    {% for post in site.posts %}
      <div class="list-item">
        <h2 class="list-post-title">
          <a href="{{ site.baseurl }}{{ post.url }}">{{ post.title }}</a>
        </h2>
        <div class="list-post-date">
          <time>{{ post.date | date_to_string }}</time>
        </div>
      </div>
    {% endfor %}
  {% endif %}
</div>