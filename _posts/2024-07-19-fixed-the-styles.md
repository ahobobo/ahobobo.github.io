---
layout: blog
title: Finally Fixed Github Pages Styles.
---

Turns out github pages does not use the latest version of Jekyll or something.

I have had styles working on my local machine for a while. However, after github got them, the styles would not work for some
reason. Looking in the dev tools, i noticed that the styles where not being compiled. For some reason, github does not seem
to have the `@forward` and `@use` rules of scss implemented.

The result was that the styles sheet for the site was just full of scss rules instead of the actual styles.

The fix I have implemented for now is to just take out the use and forward statements. I was under the impression that `@import`
was soon to be deprecated and that folks would have to use the new forwarding and using rules. For whatever reason, github
seems to not have gotten the memo just yet.