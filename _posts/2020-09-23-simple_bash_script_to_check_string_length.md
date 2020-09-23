---
layout: post
title: A simple Bash script to check string length
---

Right now I use Git from Bash. As you may be aware, good commit messages should have less than 50 characters for the initial line and less than 72 (I use this limit) for the following lines (don't forget to separate them with a blank line!). I needed a way to check the length of my commit messages from the command line. Using online tools for this seemed like too much of a hassle, so I just made a simple script to do this for me from the command line:

{% highlight bash %}
#!/bin/bash/
echo ${#1}
{% endhighlight %}

That's it! All you need to do now is save it as something short and convenient (I called it len without the ".sh" extension because I use Python a lot) and move it to the "bin" directory. Linux users may have to give it execution permissions. I am using MINGW64 on Windows where this step isn't required.

Now, given that there's a file called "len" in the "bin" directory with the above code, it should work by just typing "len <string>" (don't forget quotes if your string has spaces!):

{% highlight bash %}
User@Computer MINGW64 /
$ len "this is a string"
16
{% endhighlight %}

Just how it should be, simple but useful. This hack could go far beyond mere commit messages. Put this script to good use!
