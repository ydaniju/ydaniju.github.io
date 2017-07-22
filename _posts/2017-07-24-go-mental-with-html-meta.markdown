---
layout: post
title:  "Go mental with HTML meta"
description: "We like to build very beautiful web interfaces and spend all out ime making everything inside the <body> beautiful. Why do we neglect the <head>"
date:   2017-07-22 11:33:23 +0100
categories: jekyll update
source: meta_play
---

Chances are whn you begin to learn web development you focus more on how to build beautiful and responsive websites. Achieveing this mean syou'd spend more time 
writing hundreds or thousands of lines of code within the `<body>` tag. Should you have a reason to write anything within the head, it would be to include some `js` or 
`css` code.

This is how my story was anyway until I learn my lesson the hard way when I 
just finished what I thought was a good job—responsive, beautiful easy to 
navigate. The display on resizing my browser was like in this example:

<div class="desc-img">
  <img src="{{site.url}}/assets/images/responsive_browser.png" width="400" alt="responsive browser"/>
</div>

I didn't notice my error until I was at home the following weekend and decided to peruse my beatiful work during the week. I was shocked when I saw it on a 
**real** mobile device—my phone.

<div class="desc-img">
  <img src="{{site.url}}/assets/images/no_scale_meta.png" width="400" alt="mobile browser without scale meta"/>
</div>

{% highlight ruby %}
def print_hi(name)
  puts "Hi, #{name}"
end
print_hi('Tom')
#=> prints 'Hi, Tom' to STDOUT.
{% endhighlight %}

Check out the [Jekyll docs][jekyll-docs] for more info on how to get the most out of Jekyll. File all bugs/feature requests at [Jekyll’s GitHub repo][jekyll-gh]. If you have questions, you can ask them on [Jekyll Talk][jekyll-talk].

[jekyll-docs]: https://jekyllrb.com/docs/home
[jekyll-gh]:   https://github.com/jekyll/jekyll
[jekyll-talk]: https://talk.jekyllrb.com/
