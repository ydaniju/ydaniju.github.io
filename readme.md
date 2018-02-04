# Go Mental with HTML Meta

Chances are when you begin to learn web development you focus more on how to 
build beautiful and responsive websites. Achieving this mean you'd spend more 
time writing hundreds or thousands of lines of code within the `<body>` tag. 
Should you have a reason to write anything within the `<head>`, it would likely be 
to include some `js` or `css` code.

This is how my story was anyway until I learnt my lesson the hard way when I 
just finished what I thought was a good job—responsive, beautiful, and easy to 
navigate. The display on resizing my browser was like in this example:

<figure class="desc-img">
  <figcaption>Fig 1 - Page display from resized desktop window.</figcaption>
  <img src="responsive_browser.png" width="400" alt="responsive browser"/>
</figure>

I didn't notice my error until I was at home the following weekend and decided
to check my beautiful work from the past week. I was shocked when I saw it on a 
**real** mobile device—my phone.

<figure class="desc-img">
  <figcaption>Fig 2 - Page display on mobile browser before adding viewport meta.</figcaption>
  <img src="no_scale_meta.png" width="400" height="400" alt="mobile browser without scale meta"/>
</figure>

After doing my research, I was able to fix the problem. We'd discuss that under the 
scenarios where metas are very helpful.

Lesson learnt from that experience was meta elements found in the head tags of 
web pages aren't just for decorative reasons. They get lesser credit than they deserve 
and should be take seriously.

## So what really are do meta elements anyway?

According to [w3.org](https://www.w3.org/TR/html5/document-metadata.html#the-meta-element)
"The meta element represents various kinds of metadata that cannot be expressed using the title, base,link, style, and script elements."

Metadata are a set of data that describes and gives information about other data.

In other words, your meta elements enclose information about ypur web page.

## Scenarios


I realized that my pages' `head` is missing the 
<a href="https://developer.mozilla.org/en/docs/Mozilla/Mobile/Viewport_meta_tag"
 target="_blank">
viewport meta tag</a>. Throwing it somewhere in the head like so 

```html
  <!DOCTYPE html>
  <html>
    <head>
      <meta name="viewport" content="width=device-width, initial-scale=1">
      <title>My Blog</title>
    </head>
```

After this simple addition, the mobile browser display was just as it was for the resized browser!

<figure class="desc-img">
  <figcaption>Fig 3 - Page display on mobile browser after adding viewport meta.</figcaption>
  <img src="scale_meta.png" width="400" alt="mobile browser with scale meta"/>
</figure>
