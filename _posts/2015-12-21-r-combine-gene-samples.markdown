---
title: Taking the mean of duplicate measurements of genes in a 50k gene data frame
date: 2015-12-21 22:06:00 Z
categories:
- jekyll
- update
layout: post
---

Suppose you have measurements of 50001 gene samples, but some of them are duplicates.
Taking the means of all those genes is trivial in R:

{% highlight R %}
combined.samples <- aggregate(samples, by=list(aggregate$gene_id), FUN=mean)
{% endhighlight %}
