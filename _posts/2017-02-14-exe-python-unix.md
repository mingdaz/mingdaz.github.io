---
layout: post
title:  "How to make a Python script executable on Unix?"
date:   2017-02-14 19:01:00 -0800
categories: python unix
---

First make the script executable:
{% highlight bash %}
$ chmod +x myscript.py
{% endhighlight %}

Second add the corresponding binary file to first line of the script
{% highlight bash %}
#!/usr/local/bin/python
{% endhighlight %}



[jekyll-docs]: http://jekyllrb.com/docs/home
[jekyll-gh]:   https://github.com/jekyll/jekyll
[jekyll-talk]: https://talk.jekyllrb.com/
