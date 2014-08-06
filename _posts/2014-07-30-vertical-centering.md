---
sourceurl: http://zerosixthree.se/vertical-align-anything-with-just-3-lines-of-css/
tags:
  - CSS
  - layout
---

Sebastian Ekström shows us three lines for vertically centering anything in CSS:

{% highlight css %}
.element {
  position: relative;
  top: 50%;
  transform: translateY(-50%);
}
{% endhighlight %}

i'd <a href="http://philipwalton.github.io/solved-by-flexbox/demos/vertical-centering/" target="_blank">solve it with flexbox</a> (prefixed support about the same, better unprefixed support)
