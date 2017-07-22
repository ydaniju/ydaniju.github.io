---
layout: post
title:  "Go mental with HTML meta"
description: "We like to build very beautiful web interfaces and spend all out ime making everything inside the <body> beautiful. Why do we neglect the <head>"
date:   2017-07-22 11:33:23 +0100
categories: jekyll update
permalink: go_mental_with_html_meta
source: meta_play
---

Chances are when you begin to learn web development you focus more on how to 
build beautiful and responsive websites. Achieving this mean you'd spend more 
time writing hundreds or thousands of lines of code within the `<body>` tag. 
Should you have a reason to write anything within the head, it would likely be 
to include some `js` or `css` code.

This is how my story was anyway until I learnt my lesson the hard way when I 
just finished what I thought was a good job—responsive, beautiful, and easy to 
navigate. The display on resizing my browser was like in this example:

<figure class="desc-img">
  <figcaption>Fig 1 - Page display from resized desktop window.</figcaption>
  <img src="{{site.url}}/assets/images/responsive_browser.png" width="400" alt="responsive browser"/>
</figure>

I didn't notice my error until I was at home the following weekend and decided to peruse my beautiful work during the week. I was shocked when I saw it on a 
**real** mobile device—my phone.

<figure class="desc-img">
  <figcaption>Fig 2 - Page display on mobile browser before adding viewport meta.</figcaption>
  <img src="{{site.url}}/assets/images/no_scale_meta.png" width="400" alt="mobile browser without scale meta"/>
</figure>

After doing my research, I realized that my pages' `head` is missing the 
<a href="https://developer.mozilla.org/en/docs/Mozilla/Mobile/Viewport_meta_tag"
 target="_blank">
viewport meta tag</a>. Throwing it somewhere in the head like so 

{% highlight html %}
  <!DOCTYPE html>
  <html>
    <head>
      <meta name="viewport" content="width=device-width, initial-scale=1">
      <title>My Blog</title>
    </head>
{% endhighlight %}

After this simple addition, the mobile browser display was just as it was for the resized browser!

<figure class="desc-img">
  <figcaption>Fig 3 - Page display on mobile browser after adding viewport meta.</figcaption>
  <img src="{{site.url}}/assets/images/scale_meta.png" width="400" alt="mobile browser with scale meta"/>
</figure>
