---
layout: post
title: May developments by the Ark community
tags: [Ark, Development, Monthly]
excerpt_separator: <!--more-->
---
<!-- 
General idea : review the cool PRs merged in the month.
Explain clearly (avoid too technical stuff), show with screenshots.
-->

May has been a pretty productive month for the Ark community. Let's review what has been developed !
<!--more-->
## Ark explorer

xxx PRs merged in the ark-explorer repository, that's a lot ! We selected some to share here.


## Ark mobile
xxx PRs merged in the ark-mobile repository.

#### Wallet import : allow the user to hide/show the passphrase while typing it
By air1one.

To improve security on wallet import, allow to hide the passphrase with a hide/show icon switch.

Hide mode only displays the word we are entering and hides all the other words.

TODO add screenshot

#### Generate and import passphrase in all possible bip39 languages 
By air1one.

Allow to generate and import passphrase in any language (from the possible languages defined in bip39 wordlist).

A new option "Passphrase language" is available in Settings :

![Passphrase language in settings](/assets/img/posts/passphrase-wordlist-settings.png)
TODO replace screenshot

The language selected will be used to generate a new wallet (the passphrase will be in this language), and also for importing an existing wallet from a passphrase (we will be able to enter the passphrase in this language).

For wallet import, entering a passphrase in english will still work even if we select a different language in "Wordlist language". (we might want to generate wallets in a specific language but import a previous wallet which was generated in english)

## Ark net
xxx PRs merged in the ark-net repository.