---
layout: post
title: What are Ark plugins and why it matters
tags: [Ark, Development, V2, Plugins]
excerpt_separator: <!--more-->
---

Plugins were introduced in the new version or Ark, V2, which is now live for testing **on Devnet**. This feature allows you to create a custom behavior for your node in a clean and standard way.
<!--more-->

## Let's start with an example

Say you own a business and you want to get notified instantly when you receive a transaction on your Ark address.

With v1, you basically would have 2 options :

1. Use a public (or your own) API to get the latest transactions for your address, making a request every minute or less if you want to be notified *almost* instantly
2. Fork the official Ark core repository, make some changes to have a custom node which will check for every new block if there is a transaction for you

We can quickly see what's not optimal here  :
* Option 1 works but you make a lot of API requests.
* Option 2 works but you're hacking into the core code and it becomes a mess when you want to get the latest updates from the official repository.

## Plugin system to the rescue

The new plugin system can help you here !

Now you can fork the official Ark core repository, but instead of tweaking the core code you will write your plugin in a different folder.

You will implement an *event listener* which listens on new blocks forged, and sends you a notification when there is a transaction for you in it.

So what's different ? Well you have now a custom node, with the core strictly **identical to the official Ark repository** and your custom implementation **in a separate plugin**.

## Benefits

The first benefit is **stability / security** for your node. You don't touch the core code so you will not introduce bugs in it. Also, updating your node with the latest updates will be easy (no merge to do).

For your custom implementation, the plugin system provides you a **friendly and simple framework**. You will be able to write various plugins for your needs and keep them clear and organized.

Last but not least, you can share your plugin so that **others can benefit** and even improve on it !

## Final thoughts : Wordpress of blockchains

This plugin system is a big part of the new modular architecture of Ark V2, and we can understand why it's called the *Wordpress of blockchains*.

Indeed, plugins published for Ark will potentially work directly with any Ark-V2-based blockchain ! This is powerful 💪

*Thanks for reading ! For more details about developing a plugin read [this blog post](https://blog.ark.io/setting-up-new-plugins-in-ark-core-v2-example-7fac69993a73) by the Ark team.*

***[Follow me on twitter](https://twitter.com/Air1Ark)** to be informed about new blog posts !*