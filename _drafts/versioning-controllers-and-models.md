---
layout: post
---

consider this pattern along with feature flags&mdash; versioned controllers and models:

{% highlight ruby %}
# app/controllers/foos_controller.rb
class FoosController < ApplicationController
  # Old and busted…
end

# app/controllers/edge/foos_controller.rb
class Edge::FoosController < ApplicationController
  # New hotness…
end

# config/routes.rb
if Rails.env.production?
  resources :foos
else
  resources :foos, controller: 'edge/foos'
end

{% endhighlight %}
