--- 
name: phylogenetic-signal-simulations
layout: post
title: phylogenetic signal simulations
author: Scott Chamberlain
date: 2011-05-18 08:13:00 -05:00
sourceslug: _posts/2011-05-18-phylogenetic-signal-simulations.md
tags: 
- ggplot2
- ape
- Phylogenetics
---

I did a little simulation to examine how K and lambda vary in response to tree size (and how they compare to each other on the same simulated trees). I use Liam Revell's functions fastBM to generate traits, and phylosig to measure phylogenetic signal.

<br /><br />

Two observations:

+ First, it seems that lambda is more sensitive than K to tree size, but then lambda levels out at about 40 species, whereas K continues to vary around a mean of 1.
+ Second, K is more variable than lambda at all levels of tree size (compare standard error bars).

<br /><br />

Does this make sense to those smart folks out there?
<br /><br />

<script src="https://gist.github.com/977999.js?file=phylogeneticsignal_sim.R"></script><br />

<br /><br />


<img src="http://4.bp.blogspot.com/-hY0LQNsBzWc/TdNOJFMZzkI/AAAAAAAAEcg/SYeSCgUfyOY/s400/physig_sim.jpeg">
