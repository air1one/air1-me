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

#### Enhance responsiveness of the footer

[#157 by dated](https://github.com/ArkEcosystem/ark-explorer/pull/157)

On smaller screens, the footer was not displayed centered and we were losing Version and Date information. 

Before :

![Footer responsiveness before](/assets/img/posts/may-dev/footer-before.png)

After :

![Footer responsiveness after](/assets/img/posts/may-dev/footer-after.png)

#### Remove link for vote, registration and signature creation transactions

[#183 by dated](https://github.com/ArkEcosystem/ark-explorer/pull/183)

In transactions lists, there is a link for the 'recipient'. But for transactions like votes, registrations and signature creations, this link pointed to nowhere and resulted in a 404 error.

Before :

![Recipient link before](/assets/img/posts/may-dev/recipient-before.png)

After :

![Recipient link after](/assets/img/posts/may-dev/recipient-after.png)

Also, [#226 by dated](https://github.com/ArkEcosystem/ark-explorer/pull/226) adds missing transactions labels like 'Multisignature registration' to be displayed in this 'recipient' column.

## Ark mobile
xxx PRs merged in the ark-mobile repository.

#### Enforces uniqueness of profile names

[#155 by dated](https://github.com/ArkEcosystem/ark-mobile/pull/155)

Fix to ensure that we cannot create 2 profiles with the same name.

#### Wallet import : allow the user to hide/show the passphrase while typing it
[#157 by air1one](https://github.com/ArkEcosystem/ark-mobile/pull/157)

To improve security on wallet import, allow to hide the passphrase with a hide/show icon switch.

Hide mode only displays the word we are entering and hides all the other words.

![Passphrase hidden](/assets/img/posts/may-dev/passphrase-hide.png)

#### Generate and import passphrase in all possible bip39 languages 
[#148 by air1one](https://github.com/ArkEcosystem/ark-mobile/pull/148)

Allow to generate and import passphrase in any language (from the possible languages defined in bip39 wordlist).

A new option "Passphrase language" is available in Settings :

![Passphrase language in settings](/assets/img/posts/may-dev/settings.png)

So now we can generate a new wallet, say, in French :

![Passphrase generate in French](/assets/img/posts/may-dev/passphrase-generate.png)

And also get word suggestions in this language :

![Passphrase suggestions in French](/assets/img/posts/may-dev/passphrase-suggest-fr.png)

## Ark net
xxx PRs merged in the ark-net repository.