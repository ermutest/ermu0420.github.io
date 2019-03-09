---
layout: page
title: Functional Programming 系列文章
titlebar: Functional
subtitle: <span class="mega-octicon octicon-clippy"></span>&nbsp;&nbsp; 函数式 （Functional Programming ）系列教程
menu: Functional
css: ['blog-page.css']
permalink: /functional
keywords: Functional,Functional Programming,函数式，JAVA 函数式
---

<div class="row">

    <div class="col-md-12">

        <ul id="posts-list">
            {% for post in site.posts %}
                {% if post.category=='mongodb'  or post.keywords contains 'mongodb' %}
                <li class="posts-list-item">
                    <div class="posts-content">
                        <span class="posts-list-meta">{{ post.date | date: "%Y-%m-%d" }}</span>
                        <a class="posts-list-name bubble-float-left" href="{{ site.url }}{{ post.url }}">{{ post.title }}</a>
                        <span class='circle'></span>
                    </div>
                </li>
                {% endif %}
            {% endfor %}
        </ul> 

        <!-- Pagination -->
        {% include pagination.html %}

        <!-- Comments -->
       <div class="comment">
         {% include comments.html %}
       </div>
    </div>

</div>
<script>
    $(document).ready(function(){

        // Enable bootstrap tooltip
        $("body").tooltip({ selector: '[data-toggle=tooltip]' });

    });
</script>