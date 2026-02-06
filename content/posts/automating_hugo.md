+++
date = '2026-02-06T13:36:37+01:00'
draft = false
title = 'Automating Hugo'
tags = ['Hugo', 'Github Actions', 'DevOps']
+++
## Created GH workflow to publish my Hugo site

After the decision was made to start using Hugo for my blog notes, I wanted it to publish as automated as possible.

**Github Actions to the rescue.**

I have opted for two environments: dev & prod. Where all branches not called **main** will be deployed in the dev environment.
I also opted for installation of the [Hugo](https://gohugo.io/) and [Dart](https://dart.dev/) from source directly; it turned out to be  the quickest workflow executions.


The full workflow is in the Github repo of course. 

Things I want to look at in the future:

- more caching
- create website URLs based on the branch name
- combine the two workflows, as they are very similar

But now first, learn more about Hugo and how to use it.