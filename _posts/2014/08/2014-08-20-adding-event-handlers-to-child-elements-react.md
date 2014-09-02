---
layout: post
---

in React, you can't add props after a component has been rendered (for example,
a dynamic child component)

but you CAN clone it and add props:
{% highlight coffeescript %}
# … in your component
renderChild:
  React.Children.map @props.children, (kid)=>
    React.addons.cloneWithProps kid, onClick: (e)-> alert 'hurray'
{% endhighlight %}
