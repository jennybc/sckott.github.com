---
name: open-schol
layout: post
title: On principles for open scholarly infrastructure for software
date: 2015-11-05
author: Scott Chamberlain
sourceslug: _drafts/2015-11-05-open-schol.Rmd
tags:
- infrastructure
- open science
---

[Geoff Bilder][geoff], [Jennifer Lin][jlin], and [Cameron Neylon][cam] wrote a [blog post][post] back in February this year titled [_Principles for Open Scholarly Infrastructures_][post]. In it, they explore the principles, describe why we need them, and talk a bit about implementation.

They don't disuss an organization that primarily makes software, but I thought exploring these principles with respect to software would be a useful exercise. I discuss this with respect to rOpenSci specifically, but try to make broader points about software where possible.

## The principles

They discussed three principles, and within each of the three principles they outlined a set of guidelines to follow. What follows is a short synopsis of each guideline, and I address some of the (paraphrased) points they brought up under each principle (those that apply more to software).

### Governance

> If an infrastructure is successful and becomes critical to the community, we need to ensure it is not co-opted by particular interest groups.


* __Be cross-disiplinary__: rOpenSci started out narrowly focused on ecology and evolution. Since then, we've recognized many pain points across disciplines that could be greatly ameliorated by good software. We've been accumulating colleagues from a variety of disciplines.
* __Be transparent__: We've strived to be open about our governance, and will continue to do so. The [Jupyter][jupyter] and [Dat][dat] projects are other good examples of this.

### Sustainability

> An organisation that is both well meaning and has the right expertise will still not be trusted if it does not have sustainable resources to execute its mission.


* __Mission consistent revenue__: We're lucky in that we've found funding from foundations that share our goals. This is critical to our long-term success so that our mission doesn't diverge from its path.
* __Revenue based on services, not data__: Exactly! In software, this means make open source software, which we do - all open licensed, free to use from academic to non-profit to enterprise. Instead of value-added services, we offer assurance of quality and long-term maintenance, both hard to to in academic software given short-term nature of most grants, graduate student positions, etc.

### Insurance

> Long term trust requires the community to believe it retains control.


* Liberally licensed open source software goes a long way towards making sure that the software is owned by the community (even if properietary derivatives are made).
    * __Open source__: Bingo! Everything we do is open source. This is suprisingly not ubiquotous in academic software, due to combination of some not bothering to use a license (essentially meaning it can't be re-used anywhere), or using a very restrictive license, either out of not considering the consequences or on purpose for competitive or monetary gain.
    * __Open data__: We're generally not a data provider, but if/when we do, it will surely be completely open. As an example, we do maintain a web API for the [Fishbase](http://www.fishbase.org/) dataset at [ropensci/fishbaseapi](https://github.com/ropensci/fishbaseapi/).

## rOpenSci as infrastructure?

Towards the end of the post, Bilder et al. ask:

> What would an organisation actually look like if run on these principles?

They list [ORCID][orcid] and [CERN][cern] as examples. They didn't mention software per se, but I think software can be thought of as infrastructure. I think [rOpenSci][ros] is an example of software infrastructure. Let me explain.

But wait, are we actually infrastructure? I think we are in a sense. We are building a long-lasting framework for building and maintaining software, supporting the people that make the software, and maintaing the underlying tools to make it all run smoothly. 

We provide a number of services that places us more into the role of infrastructure:

* Code review (see our [onboarding process][onboarding])
* Community standards for quality software (see our [development guidlines][guide] and [policies][policies])
* General purpose software that solves all reasonable use cases
* Liberally licensed software that can be used in all settings (almost all our software is [MIT][mit] licensed)
* Low level clients for many data science tools

In some ways, rOpenSci isn't infrastructure. For example, we are specific to a single programming language. However, this could change in time, and anyway, R is one language, but used widely across most sectors and in most disciplines. 

## Centralization

Bilder et al. stated:

> Many of the consequences of these principles are obvious. One which is less obvious is that the need for forkability implies centralization of control. ... Centralization can be hugely advantageous though – a single point of failure can also mean there is a single point for repair.

This is a key point about the rOpenSci model. We do centralize software of a particular type that fits our mission. Because we centralize in terms of physical location in our GitHub account, we can:

* Jump in to fix a problem quickly in case one of our community maintainers is away or unable to respond in a timely manner
* Maintain a certain level of software quality
* Enforce a community that is welcoming to all, that encourages less experienced contributors, and marginalized groups

We try to balance nurturing less experienced developers with 

## References

Bilder G, Lin J, Neylon C (2015) Principles for Open Scholarly Infrastructure-v1, retrieved 2015-10-15, http://dx.doi.org/10.6084/m9.figshare.1314859

[geoff]: http://www.gbilder.com/blog/
[jlin]: https://about.me/jenniferlin
[cam]: http://cameronneylon.net/
[post]: http://cameronneylon.net/blog/principles-for-open-scholarly-infrastructures/
[orcid]: http://orcid.org/
[cern]: http://home.web.cern.ch/
[ros]: http://ropensci.org/
[onboarding]: https://github.com/ropensci/onboarding
[guide]: https://github.com/ropensci/packaging_guide
[policies]: https://github.com/ropensci/policies
[mit]: http://choosealicense.com/licenses/mit/
[jupyter]: http://jupyter.org/
[dat]: http://dat-data.com/
