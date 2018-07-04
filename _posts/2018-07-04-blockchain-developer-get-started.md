---
layout: post
title: Blockchain Developer - How to get started
tags: [Blockchain, Development]
excerpt_separator: <!--more-->
---

I see a lot of people on the internet asking "How can I get from "regular" developer to blockchain developer ?".

I was exactly in this situation. I didn't know much about blockchain or cryptography, but I was motivated so I started to learn by myself. Here are some recommendations based on my experience.
<!--more-->

## What's a blockchain developer anyway?

That's a good question right ? The term "blockchain developer" is so generic that we don't really know what's behind it. Let's quickly review what makes *you* a blockchain developer.

First and obvious point, you have a good understanding of the technology : you know what's a blockchain, what are the technologies involved, and have some kind of a culture in the area (knowing different examples of how it's applied on real projects).

You might think you need to be a cryptography expert : **wrong**. The best thing in software development is abstraction : you can use crypto libraries understanding what it does at a higher level, without getting into the nitty-gritty of its implementation.

So what are the kind of things you can develop ?
* Applications using APIs : you're probably already doing that as a "regular" developer, the only difference here is the API you're querying would be the one of a blockchain project.
* Blockchain library or core code : here you're inside the box and are implementing the blockchain features. You need a bit more knowledge but again, libraries are here to help you.

Sounds clearer ? Good, now let's get you started.

## Read, read, read

Yeah, start by reading a lot.

I can't recommend enough reading [Mastering Bitcoin](https://bitcoinbook.info/) by Andreas Antonopoulos. By understanding how Bitcoin works, you are already half-way to your blockchain developer goal.

Also, explore how other projects leverage the technology to provide real-world value. From decentralized file sharing to logistic management, there are a lot of applications.

## Practical exercises

Time to interact with the network ! Based on what you read before you can pick a project you like to continue on with the "exercises". If in doubt, I'm suggesting you to check out my favorite project [Ark.io](https://ark.io).

### Create a wallet

This is the best way to start interacting with the network. Create your own wallet using one of the app from your project.

You don't have to put real money to do that : every cryptocurrency has a Devnet / Testnet. Just check how you can access it, generate your wallet, and get some coins in it (you might need to ask people to send you some).

Once you have a wallet with coins in it, you can play and send transactions to a new wallet of yours for example. See how it propagates to the network and gets recorded on the blockchain.

### Set up your node

The next logical step is to set up your own node ! Just follow the instructions from your project to get it done.

Then play with your node to see what it is to be part of the network :
* Check that you are in sync and receiving the last blocks
* Explore the last transactions (you should be able to do that with a Command Line Interface)
* Query your own API with a http client (if your node comes with API included)
* ... go on and test any other thing your node is providing

## Contribute to a project

Finally some coding ! Great thing about blockchain projects is that they are for the most part opensource.

I chose to go with [Ark.io](https://ark.io) because among other things, they are really welcoming external contributors. I recommend you to check it out if you haven't already.

Usually, for one project you have different kind of repositories you can contribute to :
* Node implementations in different languages
* Client libraries in different languages
* Wallet applications for desktop / mobile / web / ...

For a newcomer, I find wallets are the best way to get started :
* It's visual : you can see your changes in the user interface
* You can start fixing bugs or coding features without getting into the "blockchain stuff"
* You will understand and get comfortable with this first layer, it will give you confidence to go "down" to the other layers 😉

Now go and start coding ! Check the open issues and see if you can help resolve them. Talk with the team, they might have some suggestions for you.

You can also go by yourself and test things, see what you can improve. Don't worry there is always something you can do 😀

## Keep it going and always keep learning

You're on track, now keep contributing to opensource blockchain projects as you will gain experience and start mastering the technology. Remember, by doing this you are also building your "blockchain portfolio" as your opensource developments can be seen by everyone.

My last advice would be : always keep learning. Things are moving fast in this space and you want to keep an eye on what's happening. Not only you will "step up your game" but you might also find great opportunities or projects to work for.

*Thanks for reading ! Now what would you recommend to a newcomer ? Leave a comment !*

***[Follow me on Twitter](https://twitter.com/Air1Ark)** to be informed about new articles !*

