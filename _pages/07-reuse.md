---
layout: chapter
title: 7. Reuse
id: chapter7
permalink: /chapters/7/
previousPage:
  href: /chapters/6/
---

Reuse is something not worth striving for but if it comes up as a bonus then great.

99.99999% of the time I suggest duplication over reuse which goes against all my natural instincts as an engineer. But what works for all other programming languages does not work for the weirdly wonderful and unique CSS.

Let's take a look at a couple of interesting examples

## e.g. Clearfix

	.clearfix {}

## e.g. Red

	.red {}

## e.g. Float left

	.pull-left {}

The interesting thing about each of these class names is how they are nothing to do with what the element is, but to do with how the element *looks*. This breaks [semantics](/chapters/2/) which in turn break foundations which cause all sorts of problems.