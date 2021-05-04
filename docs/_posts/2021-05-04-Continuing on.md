---
layout: post
title: "Continuing On"
comments: true
date: 2021-05-04 01:58:00 -8000
categories: blog
---

I'm learning a lot (relearning, mostly) about how to set up this blog. I want to document my
journey so others like me can have something to look upon.  

I had a bit of trouble with implementing **Disqus**.  

Lots of similar problems were spouted back in the early 2010s, but most of the solutions
didn't apply to the current implementation, any many of the workarounds were no longer possible through generic means.

> aka adding localhost as a trusted domain.

Disqus no longer allows this.

Code was fixed after a closer inspection. I was missing a curly brace right after the meat of the function! Oops!

    var disqus_config = function () {
      this.page.url = '\{\{site.url\}\}\{\{page.url\}\}' 
      this.page.identifier = '{{page.id}}';
      //missing curly brace!! -> "};"
    //rest of function...

It really just goes to show you that getting frustrated with things can lead to a lot of silly mistakes. My advice is to always just try to take your time with things
and start over if you're not getting anywhere.
