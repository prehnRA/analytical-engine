---
layout: post
---

to avoid getting the "stack level too deep" error with factory girl, you must
avoid circular relationships between your factories. You can use factory girl
callbacks to lazily fill in these relationships only if they don't already
exist:

{% highlight ruby %}
  FactoryGirl.define do
    factory :author do
      posts { [FactoryGirl.build(:post)] }
    end

    factory :post do
      before(:create) do |post|
        post.author = FactoryGirl.build(:author) if post.author.nil?
      end
    end
  end
{% endhighlight %}
