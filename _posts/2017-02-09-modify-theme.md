---
layout: post
title:  "Modify theme minima!"
date:   2017-02-09 19:01:00 -0800
categories: jekyll update
---
First of all locate minima theme.
{% highlight bash %}
bundle show minima
{% endhighlight %}
Command line returns:
{% highlight bash %}
/Library/Ruby/Gems/2.0.0/gems/minima-2.1.0
{% endhighlight %}
Jekyll is using liquid template engine.
I downloaded an bootstrap template startbootstrap-freelancer-gh-pages. Now I want to migrate this template with my website.
First I copied <head> code from index.html to _include/head.html:
{% highlight html %}
<!-- Bootstrap Core CSS -->
  <link href="vendor/bootstrap/css/bootstrap.min.css" rel="stylesheet">
  <!-- Theme CSS -->
  <link href="css/freelancer.min.css" rel="stylesheet">
  <!-- Custom Fonts -->
  <link href="vendor/font-awesome/css/font-awesome.min.css" rel="stylesheet" type="text/css">
  <link href="https://fonts.googleapis.com/css?family=Montserrat:400,700" rel="stylesheet" type="text/css">
  <link href="https://fonts.googleapis.com/css?family=Lato:400,700,400italic,700italic" rel="stylesheet" type="text/css">
  <!-- HTML5 Shim and Respond.js IE8 support of HTML5 elements and media queries -->
  <!-- WARNING: Respond.js doesn't work if you view the page via file:// -->
  <!--[if lt IE 9]>
  <script src="https://oss.maxcdn.com/libs/html5shiv/3.7.0/html5shiv.js"></script>
  <script src="https://oss.maxcdn.com/libs/respond.js/1.4.2/respond.min.js"></script>
  <![endif]-->
{% endhighlight %}
Second I need to change the url using liquid engine:
Relative URL
Prepend the baseurl value to the input. Useful if your site is hosted at a subpath rather than the root of the domain.
{{ "/assets/style.css" | relative_url }}
/my-baseurl/assets/style.css
Absolute URL
Prepend the url and baseurl value to the input.
{{ "/assets/style.css" | absolute_url }}
http://example.com/my-baseurl/assets/style.css


[jekyll-docs]: http://jekyllrb.com/docs/home
[jekyll-gh]:   https://github.com/jekyll/jekyll
[jekyll-talk]: https://talk.jekyllrb.com/
