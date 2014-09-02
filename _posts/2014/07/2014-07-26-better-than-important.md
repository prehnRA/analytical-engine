---
layout: post
tags: css
---

you can chain the same class together in a selector to to boost specificity (forget !important):

{% highlight css %}
.bar.bar {
  color: green;
}
  
.bar {
  color: red;
}
  
/* bar is still green */
{% endhighlight %}
