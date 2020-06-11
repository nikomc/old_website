---
layout: post
title: "Partisan Trust in American Institutions"
author: "Niko McCarty"
categories: blog
tags: [blog,trust,pew,d3,data,dataviz]
image: column_interior.jpg
sect: home
mathjax: true

---

In an effort to practice with D3.js, I put together a simple lollipop chart (actually called a "Cleveland Dot Plot") based on newly released [Pew Research Center](https://www.people-press.org/2020/04/09/public-holds-broadly-favorable-views-of-many-federal-agencies-including-cdc-and-hhs/) data. 

The code is also _directly_ adapted from code written by [bl.ocks user Thanaporn](https://bl.ocks.org/Thanaporn-sk/210d359e6e0c10898ff1329a88ed20c6). I only rewrote minor parts of the code to make it more understandable for political survey results of this type. The visualization, which can be found in the embedded CodePen window below, is based on survey results in which Democrats (both lean Dem. and registered Dem.) and Republicans (both lean Rep. and registered Rep.) were asked whether they had a favorable opinion of several different government agencies, from the U.S. Postal Service to ICE. The only thing that everyone agrees on: the post office is popular across the board.

Check out the code and visualization below:

<iframe height="404" style="width: 100%;" scrolling="no" title="Trust in Institutions - D3.js" src="https://codepen.io/nsmccarty/embed/BajjbXG?height=404&theme-id=dark&default-tab=result" frameborder="no" allowtransparency="true" allowfullscreen="true">
  See the Pen <a href='https://codepen.io/nsmccarty/pen/BajjbXG'>Trust in Institutions - D3.js</a> by Niko McCarty
  (<a href='https://codepen.io/nsmccarty'>@nsmccarty</a>) on <a href='https://codepen.io'>CodePen</a>.
</iframe>

You can view all of these code files and other data visuals on my [GitHub](https://github.com/nikomc/dataviz/tree/master/20200610_trust_institutions).
