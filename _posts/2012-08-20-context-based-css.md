---
title: "Context Based CSS"
layout: post
description: "If you haven't been on mars for the past few years, you might have heard the word OOCSS. OOCSS stands for object oriented CSS. It is a methodology for writing clean and performant CSS other developers (and yourself) will love to work with. OOCSS methodologies come from developers maintaining huge portals (for example Yahoo) and sharing their code with hudreds of other developers. But, if you aren't a CSS Jedi Master, and you are not building the next Google, OOCSS's potential can quickly turn your maintainability dreams into a deadly classitis syndrome with some risks of overengineering. Something you absolutely don't want. Here's a cure."
trackdetail: "{post: 'Context Based CSS'}"
---

If you haven't been on mars for the past few years, you might have heard the word OOCSS. OOCSS stands for object oriented CSS. It is a methodology for writing clean and performant CSS other developers (and yourself) will love to work with. OOCSS methodologies come from developers maintaining huge portals (for example Yahoo) and sharing their code with hudreds of other developers. But, if you aren't a CSS Jedi Master, and you are not building the next Google, OOCSS's potential can quickly turn your maintainability dreams into a deadly classitis syndrome with some risks of overengineering. Something you absolutely don't want. Here's a cure. <a href="http://lucadegasperi.com/blog/2012/08/20/context-based-css">meet the context</a>.



## What's context ##
From the dictionary context is refered as "the parts of a piece of writing, speech, etc., that precede and follow a word or passage and contribute to its full meaning" and also "the conditions and circumstances that are relevant to an event, fact, etc". Both are equally valid and help us introduce context inside CSS. From my personal interpretation an element's context is the first parent climbing the DOM three upwards that is relevant to the modifications we want to apply. Let me give you an example.


## Applying context ##

Usually, following OOCSS principles, when you want an element's variation, you add a class to it. That small <code>button different</code> class statement can quickly become huge especially if you plan on having many different variations.

<script src="https://gist.github.com/3398306.js?file=without-context.html"></script>

<script src="https://gist.github.com/3398306.js?file=without-context.css"></script>

Now instead let's try to apply some context. Since we know that the button inside the titlebar will look a bit different than a standard button in the document's body, The titlebar will be our button's context.


<script src="https://gist.github.com/3398306.js?file=with-context.html"></script>

<script src="https://gist.github.com/3398306.js?file=with-context.css"></script>

We wrote almost the same amount of CSS like before but our HTML is cleaner, on a larger scale we can save some precious bites.


## Organizing the CSS ##

Is it better to place an element's context modification after the context declaration itself or after the element's declaration? Well, this is up to you. Personally I place the context rules after the element itself. So instead of this

<script src="https://gist.github.com/3398306.js?file=declaration-after-context.css"></script>

I prefer

<script src="https://gist.github.com/3398306.js?file=declaration-after-element.css"></script>

This is due because placing the context rules after the element's default rules, makes it easier to search for what we are looking for once we need to modify those rules.

## When context is not enough ## 

With all this awesomeness in one place there should be some drawbacks. In fact you should use context modifiers only when appropriate. If you start seeing some repeating patterns among an element's context modifiers like the example below with the <code>background: red;</code> rule

<script src="https://gist.github.com/3398306.js?file=when-context-is-not-enough.css"></script>

It might be time to refactor your code and probably add another class to the element itself.

## Recap ##

You might say you have done something similar to this for quite a long time without giving it a name. What's important is the awarness that what you do is actually producing some quality code and not some crappy unmaintainable code. This technique is suitable for medium sized projects and helps the problem of class cluttering the HTML quite a lot. For bigger projects you could consider something like Snook's <a href="http://smacss.com">SMACSS</a> approach.