---
layout: post
title: A pro tip for using functions in Python
---

Use the names of function parameters when calling functions. This improves readability and enables functions to work even if the order of the parameters is different:

{% highlight python %}
def fun(a, b, c):
  pass
  
fun(a=1, b=7, c=13)
{% endhighlight %}

The following calls would work in the exact same way:

{% highlight python %}
fun(a=1, c=13, b=7)
{% endhighlight %}
{% highlight python %}
fun(b=7, a=1, c=13)
{% endhighlight %}
{% highlight python %}
fun(b=7, c=13, a=1)
{% endhighlight %}
{% highlight python %}
fun(c=13, a=1, b=7)
{% endhighlight %}
{% highlight python %}
fun(c=13, b=7, a=1)
{% endhighlight %}
