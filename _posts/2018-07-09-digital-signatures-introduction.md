---
layout: post
title: "Digital signatures : a gentle introduction"
tags: [Cryptography, Signatures, Blockchain]
---

Struggling with digital signatures ? Great, this article is for you. I promise I will not use complicated terminology, yet you will understand perfectly the logic behind it.

## Here is the situation

You and your friend Diane were victim of identity usurpation : you received messages from someone claiming to be her, and you had no way to verify it directly without grabbing your phone and calling her.

### The system

So you both decided it was time to set up a system so that neither of you gets scammed again. Here is what you imagined :
* From now on when she'll send you a message, it will be encrypted in a very particular way : she'll substitute each letter with the 4th letter following it in the alphabet. A becomes E, B => F, etc.
* People have no way to know your encryption method ! So when you receive a message encrypted this way, you'll be sure it comes from her.

*Actually, this encryption method is very weak and people could know about it. But today we'll just believe that you designed an encryption method that nobody but you can know about.*

### First message

You tell Diane to send you a message to test it right away. You receive this :

> Lipps mxw Hmeri

You decrypt it :

>Hello its Diane

Great ! This was really sent by Diane.

Now for the next messages you decide to make a small adjustment : she'll send you the message encrypted **and** the message in clear. It's more convenient for you to see right away the content of the message and then verify it by decrypting the encrypted part. This way the first message would look like this :

>Lipps mxw Hmeri / Hello its Diane

### Usurpator is back

A few days pass. Then you receive a new message :

>Lipps mxw Hmeri / Hi its Diane plz call me 132-433-459

It's looking suspicious. You decrypt the encrypted part :

>Hello its Diane

Uh oh. It is encrypted correctly, but it does not correspond at all to the message in clear ! And you know **you should only trust the encrypted message**, as only Diane could have generated it.

You understand what happened : the usurpator intercepted your first test message, and tried to send another one looking like it. But as he doesn't know how to encrypt, he couldn't do anything but send the same encrypted part as the first message, which did not fool you.

## Lessons learned

### Encryption for identity verification

If you manage to set up a system where one person can encrypt a message in her own way (she's the only one who can encrypt it this special way), and everyone can verify that indeed she encrypted it, then you have an identity verification system. This is what digital signatures are all about.

### Trust the encrypted message

Here we sent the message in clear along with the encrypted message. In the next article about digital signatures you will understand why.

But for now, remember : it's only the encrypted message which allows us to verify the identity of the sender.

***Clear enough ?** Don't miss my next article where I'll get into more details about digital signatures.*

***[Follow me on Twitter](https://twitter.com/Air1Ark)** to be informed about new articles !*