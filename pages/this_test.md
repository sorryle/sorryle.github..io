---
layout: page
title: 自考计算机科学与技术
titlebar: 自考计算机科学与技术
subtitle: <span class="mega-octicon octicon-clippy"></span> &nbsp;&nbsp; 学习计算机的课程笔记，打计算机基础，方便自己以后学习应用层的东西时更简单，提升自己学历，毕竟能力不行，学历来凑。
menu: 自考计算机科学与技术
css: ['blog-page.css']
permalink: /this_test
---

<div class="row">

    <div class="col-md-8">
    
        <!-- Blog list -->
        <ul id="posts-list">
            {% for post in site.posts %}
            <!-- 判断如果界面的category属性是自考计算机科学与技术就添加进进行展示 -->
             {% if post.category == '自考计算机科学与技术' %}
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
        {% include disqus-comments.html %}
    
    </div>
    
    <div class="col-md-4">
        {% include sidebar-post-tag.html %}
    </div>

</div>
<script>
    $(document).ready(function(){

        // Enable bootstrap tooltip
        $("body").tooltip({ selector: '[data-toggle=tooltip]' });
    
    });
</script>
