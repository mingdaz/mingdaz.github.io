---
layout: post
title:  "Debug Jekyll post does not show up"
date:   2017-02-14 19:01:00 -0800
categories: jekyll
---

Stack overflow link:
```
http://stackoverflow.com/questions/30625044/jekyll-post-not-generated
```
Reasons:
- The post is not placed in the `_posts` directory.
- The post has incorrect title. Posts should be named `YEAR-MONTH-DAY-title.MARKUP`
- The post's date is in the future. You can make the post visible by setting `future: true` in `_config.yml` ([documentation](https://jekyllrb.com/docs/configuration/#build-command-options))
- The post has `published: false` in its front matter. Set it to `true`.
- The title contains a `:` character. Replace it with `&#58`.

