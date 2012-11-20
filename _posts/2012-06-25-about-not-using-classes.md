---
title: "About Not Using Classes "
layout: post
description: "A recent Smashing Magazine's Article titled \"Classes? Where We’re Going, We Don’t Need Classes!\" by Heydon Pickering made me think a lot about the way I write CSS and HTML, It also reminded me of an idea I had a while ago. The article in question, despite the good intention, is receiving a lot of critiques, expecially from SMACSS / OOCSS users. Many of those people only understood the part about not using classes, instead of the wider scope of the article and the good points it made. Let's see what those points are and what instead is wrong with this approach."
---

A recent Smashing Magazine's Article titled "<a href="http://coding.smashingmagazine.com/2012/06/19/classes-where-were-going-we-dont-need-classes/" rel="nofollow" target="_blank">Classes? Where We’re Going, We Don’t Need Classes!</a>" by <a href="https://twitter.com/heydonworks" rel="nofollow" target="_blank">Heydon Pickering</a> made me think a lot about the way I write CSS and HTML, It also reminded me of an idea I had a while ago. The article in question, despite the good intention, is receiving a lot of critiques, expecially from SMACSS / OOCSS users. Many of those people only understood the part about not using classes, instead of the wider scope of the article and the good points it made. Let's see what those points are and what instead is wrong with this approach.


## The good points ##

As said in the introduction the article made some rather interesting good points, here they are.

### Classes are arbitrary ###

Classes in CSS are something derived from object oriented programming, as of that, they are defined on an arbitrary basis. In fact they can be compared to pet names, they have no meaning outside the developers who use them.

### Parity between users and bots ###

The article scored a point by saying that what bots and users read should be the same, so where the bot percives the markup and the content inside of it in a "binary" way, the user percives the content and its hierarchy in a visual way. The information we present to both should be as much as possible the same.

### Content is king ###

As frontend developer we are more excited about the code we write, the nesting of elements we put together, than about the real meaning we try to pass to users and bots. We have to change this approach. 

### The document outline is useful and you should use it ###

HTML5 revised its <a href="http://html5doctor.com/outlines/" rel="nofollow" target="_blank">document outlining algorithm</a>, making the hierarchy of a document more important than ever before. What that means is easy: more possibilities to rely on hierarchy thus reducing the need of classes or artificial hierarchical solutions.

### Context Matters ###

When designing a page, the context in which the elements appear is important. As the mentioned article reads, an `<h1>` inside an `<aside>`, has a different role than one inside an `<article>`. We probably wouldn't have a document outline algorithm if there was no hierarchy or distinction between same elements into different contexts. Context is one of the most powerful feature we can have in HTML and CSS. Not using it, is foolish.


## And now the bad ones ##

Despite the number of good and meaningful advices the article gives, here are some things that hasn't been kept into consideration. Please mind this are my opinions, thay are not an universal truth.

### Bots are an anomaly ###

One thing that has not been kept in mind by the author is that bots are an anomaly of the web, we built the web for people, and people don't care about the code underneath a website, developers and bots do.
Semantics in HTML, is an exercise of style we put together to ease the work of the machines in understanding the content of a document, that we found could also improve the maintainability of our code. Semantics in CSS, is an exercise of style we put together to ease the work of other developers in understanding and maintaining our code. The web isn't the place to present computer readable content to humans, off course we could, but that shouldn't be our main purpose. We should design and organizate pages for our users.

### We write code for other developers not for users ###

The code we write is our product, we usually share it with other developers and we go back to it from time to time. If the code isn't clear and clean enough we spend more time (and money) trying to understand it rather than implementing new features. Since we code for a living, bad code = lost money. So our CSS deserves the same semantic threatment we want to reserve to our HTML.  
How do we achieve both? Simple, we pollute the HTML a bit with our classes and everyone can live in peace and harmony. In the comments below the article the author says that whereas a new developer could understand a semantic piece of HTML, he wouldn't understand a piece of HTML with classes in it. That's true, but an important thing to note is that the code we write is not enough and cannot be self descriptive, that's why we have styleguides and documentation, to explain other developers what our code means and how it should be used.


### We don't live in a perfect world ###

In a perfect world, we wouldn't have old browsers, we wouldn't write HTML and probably not even CSS, but dear readers, this isn't a perfect world and for our joy, we have to deal with awkward things daily. That's why we are web designers and that's why we have and use classes. If all browsers would be so advanced to support the new selectors, and our customer don't demand to support IE7, we could reduce the usage of classes a lot, but that's not today. Sadly. 
	
## Truth lies in the middle ##

We write code for developers, and we write content for our users.

It's important to aknowledge when we can use a different approach. Driving a jeep with all it's fine settings and customizations for offroad driving in the city is pretty senseless. the opposite is also true, a citycar is not suitable for offroad driving.

Finally I want to give the author, who had a lot of courage in publishing such a forward looking article, all my respect. With every technology we first have to get to the extreme of it to properly understand what the best usage is, that article is one of those extreme examples, you cannot ignore it. It forces you to think about what you have been doing ever since.

That said, I will give Heydon's approach a try, and will mix it with some ideas of my own to bring it a step down from its extremeness. You will discover how in an upcoming article.

Hope you enjoyed

Luca


<a href="https://twitter.com/intent/tweet?button_hashtag=ldnoclass&text=I've%20found%20this%20interesting%20article" class="twitter-hashtag-button" data-related="lucadegasperi" data-url="http://www.lucadegasperi.com/blog/2012/06/23/about-not-using-classes" data-dnt="true">Tweet #ldnoclass</a>
<script>!function(d,s,id){var js,fjs=d.getElementsByTagName(s)[0];if(!d.getElementById(id)){js=d.createElement(s);js.id=id;js.src="//platform.twitter.com/widgets.js";fjs.parentNode.insertBefore(js,fjs);}}(document,"script","twitter-wjs");</script> hashtag to discuss about this article.