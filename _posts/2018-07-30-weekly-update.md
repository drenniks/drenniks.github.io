---
layout: post
title: "(Late) Weekly Update"
date: 2018-07-30
---

I should have posted this last Friday - better late than never!
<br>
<br>
Last week, I was able to plot the average Lyman-Werner background versus halo mass for halos with new Pop3 stars. To get the Lyman-Werner background, I had to try a few different things. First, I tried to sort through the halo tree, to trace halos back to the dataset right before the pop3 star was born. This brought up multiple problems. Some Pop3 stars are not in any halos (at least not that Rockstar could pick up), so I could not trace their history. Other Pop3 stars were in parent halos (meaning they are the first of their lineage), so I also could not trace their history. While this was good practice using <a href="https://ytree.readthedocs.io/en/latest/"><font color="#0000ff">ytree</font></a>, I abandoned this method. 
<br>
<br>
I ended up implementing an idea from my advisor. To calculate the background, I simply added up the flux from each radiating star in the simulation, apart from any stars within the virial radius of the halo I was focused on. This resulted in a sensible plot, although I need to determine what to do about duplicate halos. I am finding that most of the halos at lower redshift lie below the mass threshold limit from <a href="http://iopscience.iop.org/article/10.1086/319014/pdf"><font color="#0000ff">Machacek+ 2001</font></a>, but there are some halos at higher redshifts which lie well above the threshold. 
<br>
<br>
So far, I am finding that the halos that lie above the threshold have Pop3 or Pop2 stars just outside the virial radius of the halo, driving the Lyman-Werner background up. I figured this out by using an interactive plot I came up with using the <a href="https://matplotlib.org/users/event_handling.html"><font color="#0000ff">mpl_connect</font></a> function from matplotlib. This is a really cool part of matplotlib that I didn't know existed until this plot! 
<br>
<br>
In other news, I volunteered at the <a href="https://scienceatl.org/cso/"><font color="#0000ff">Chief Science Officers</font></a> Summer Institute, here at Georgia Tech, on Thursday. This is an awesome program where students from local high school and middle schools are elected to be Chief Science Officers at their school. They are required to bring STEM programs to their schools and be leaders in the community. This is the first year of the event happening in Georgia, so it was very exciting to be part of a group of people so motivated to bring science to the public.
<br>
<br>
<br>
<br>
<script id="dsq-count-scr" src="//https-drenniks-github-io.disqus.com/count.js" async></script>