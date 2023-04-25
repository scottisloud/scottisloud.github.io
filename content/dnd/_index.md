---
layout: default
title: Encryption Dungeon
pagination:
    enabled: false
menu: main
#tagline: Some sales engineers and a professor come together to solve a mystery!
---

</br>
<h1>Welcome to the Encryption Dungeon</h1>

<div class="dnd">
<!-- Post list which might be nice somewhere else that isn't the home page! -->
<ul class="post-list">
    {% for post in site.categories.dnd %}
      <div class="post postContent">
          <!-- This is totally optional -->
          <div class="postDay">
            {{post.tag}} 
          </div>
          <!--the above is optional -->
          <br>
          <div class="postTitle">
              <!-- Provides conditional for link list posts. If variable "link" is present in the post file, post title links to source and inserts an arrow. If no link variable is present, the title links to the post itself -->
              <a class='postLink' href="{% if post.link %}{{post.link}}{% else %}{{ post.url }}{% endif %}">{{ post.title }}</a>{% if post.link %}<span class="link-arrow"> &rarr;</span>{% endif %}
          </div>
          {% if post.link %}
              <div class="permalink">
                  <a href="{{ post.url }}">Permalink</a>
              </div>
              <br />
          {% endif %}
          <div class="postExt">
              {{ post.excerpt }}
          </div>
        </div>
    {% endfor %}
  </ul>
</div>






