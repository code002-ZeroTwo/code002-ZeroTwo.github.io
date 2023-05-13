---
layout: page
title: Twitter like application
description: a simple project with some simple features of twitter
img: assets/img/12.jpg
importance: 1
category: work
---

This is a twitter like application with features like user authentication, verification, 
tweeting the twitting , liking other's tweet, following and unfollowing other users,
visiting other's profile,etc


followings are the images of the this project, a brief visual description of what 
this app looks like.

<br>
<div class="row">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.html path="assets/img/pics/login page.png" title="example image" class="img-fluid rounded z-depth-1" %}
    </div>
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.html path="assets/img/pics/register page.png" title="example image" class="img-fluid rounded z-depth-1" %}
    </div>
</div>
<div class="caption">
    login and register page. to login and register.
</div>
<div class="row">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.html path="assets/img/pics/front.png" title="front page" class="img-fluid rounded z-depth-1" %}
    </div>
</div>
<div class="caption">
    this is what appears after login.
</div>

Following shows the screen after clicking on all posts and following respectively.


<div class="row justify-content-sm-center">
    <div class="col-sm-8 mt-3 mt-md-0">
        {% include figure.html path="assets/img/pics/post of following users.png" title="posts of followings" class="img-fluid rounded z-depth-1" %}
    </div>
    <div class="col-sm-4 mt-3 mt-md-0">
        {% include figure.html path="assets/img/pics/other's profile.png" title="other's profile" class="img-fluid rounded z-depth-1" %}
    </div>
</div>
<div class="caption">
    navigate through the app. you can see posts posted by all the users or you can just see the posts of users that you are following.
</div>

<!--
The code is simple.
Just wrap your images with `<div class="col-sm">` and place them inside `<div class="row">` (read more about the <a href="https://getbootstrap.com/docs/4.4/layout/grid/">Bootstrap Grid</a> system).
To make images responsive, add `img-fluid` class to each; for rounded corners and shadows use `rounded` and `z-depth-1` classes.
Here's the code for the last row of images above:

{% raw %}
```html
<div class="row justify-content-sm-center">
    <div class="col-sm-8 mt-3 mt-md-0">
        {% include figure.html path="assets/img/6.jpg" title="example image" class="img-fluid rounded z-depth-1" %}
    </div>
    <div class="col-sm-4 mt-3 mt-md-0">
        {% include figure.html path="assets/img/11.jpg" title="example image" class="img-fluid rounded z-depth-1" %}
    </div>
</div>
```
-->

{% endraw %}
