---
layout: post
title: May developments by the Ark community
tags: [Ark, Development, Community]
excerpt_separator: <!--more-->
---
<!-- 
General idea : review the cool PRs merged in the month.
Explain clearly (avoid too technical stuff), show with screenshots.
-->

May has been a pretty productive month for the Ark community 😎 Let's review what has been developed !
<!--more-->

*PR stands for Pull Request, it corresponds to the changes submitted by the community to the official Ark repositories. When a PR is accepted, it is merged into the Ark repository.*

## Ark explorer

91 PRs merged in the ark-explorer repository, that's a lot ! We selected some to share here.
*To see the full list, [check this Github filter](https://github.com/ArkEcosystem/ark-explorer/pulls?page=1&q=is%3Apr+merged%3A2018-05-01..2018-05-31&utf8=%E2%9C%93).*

#### Fix wrong transactions being shown in a wallet

[#180 by ItsANameToo](https://github.com/ArkEcosystem/ark-explorer/pull/180)

Sometimes when navigating to a wallet, it would briefly show the correct transactions of the wallet but then replace them with the latest transactions (transactions from everyone as on the home page).

This PR added a check so that it will no longer show those wrong transactions.

#### Enhance responsiveness of the footer

[#157 by dated](https://github.com/ArkEcosystem/ark-explorer/pull/157)

On smaller screens, the footer was not displayed centered and we were losing Version and Date information. 

Before :

![Footer responsiveness before](/assets/img/posts/may-dev/footer-before.png)

After :

![Footer responsiveness after](/assets/img/posts/may-dev/footer-after.png)

#### Fix color for special transactions / Fix color for missed blocks

[#146 by ItsANameToo](https://github.com/ArkEcosystem/ark-explorer/pull/146)

Originally, special transactions such as votes, signatures and delegate registrations were given a green color, as the recipient corresponded to the current wallet. However, they are actually outgoing transactions (and are also shown on the 'sent' page) and should therefore be indicated in red.

[#218 by ItsANameToo](https://github.com/ArkEcosystem/ark-explorer/pull/218)

In Delegate Monitor, status 1 and 4 both indicate a block being missed, either in current round (1) or previous round (4). However, status 4 was not being colored yellow, but grey instead (such as the regular "awaiting spot" is colored). This PR changed the color to be yellow too :

![Block missed color](/assets/img/posts/may-dev/block-missed.png)

#### Remove link for vote, registration and signature creation transactions

[#183 by dated](https://github.com/ArkEcosystem/ark-explorer/pull/183)

In transactions lists, there is a link for the 'recipient'. But for transactions like votes, registrations and signature creations, this link pointed to nowhere and resulted in a 404 error.

Before :

![Recipient link before](/assets/img/posts/may-dev/recipient-before.png)

After :

![Recipient link after](/assets/img/posts/may-dev/recipient-after.png)

Also, [#226 by dated](https://github.com/ArkEcosystem/ark-explorer/pull/226) adds missing transactions labels like 'Multisignature registration' to be displayed in this 'recipient' column.

#### Added a tooltip when the search returns no results

[#178 by ItsANameToo](https://github.com/ArkEcosystem/ark-explorer/pull/178)

When you searched something but it had no result, you didn't get any feedback. Added a tooltip that shows when nothing was found and dismisses automatically after 1500ms.

![Search tooltip](/assets/img/posts/may-dev/search-tooltip.png)

#### Server requests optimizations

[#210](https://github.com/ArkEcosystem/ark-explorer/pull/210),
[#212](https://github.com/ArkEcosystem/ark-explorer/pull/212),
[#214](https://github.com/ArkEcosystem/ark-explorer/pull/214),
[#215](https://github.com/ArkEcosystem/ark-explorer/pull/215) by air1one

In Delegate Monitor page, there was a huge amount of server requests to get informations from the node. These PRs help reduce the server load and make the Delegate Monitor page faster.

## Ark mobile
8 PRs merged in the ark-mobile repository.
*To see the full list, [check this Github filter](https://github.com/ArkEcosystem/ark-mobile/pulls?page=1&q=is%3Apr+merged%3A2018-05-01..2018-05-31&utf8=%E2%9C%93).*

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
25 PRs merged in the ark-net repository.
*To see the full list, [check this Github filter](https://github.com/ArkEcosystem/ark-net/pulls?page=1&q=is%3Apr+merged%3A2018-05-01..2018-05-31&utf8=%E2%9C%93).*

#### Logging framework and full log coverage

[#29](https://github.com/ArkEcosystem/ark-net/pull/29),
[#35](https://github.com/ArkEcosystem/ark-net/pull/35),
[#46](https://github.com/ArkEcosystem/ark-net/pull/46) by sharkdev-j,
[#47](https://github.com/ArkEcosystem/ark-net/pull/47) by air1one

Big work on logging : now we can have a full trace of what's going on.

#### Added ability to generate passphrase & accounts

[#7 by sharkdev-j](https://github.com/ArkEcosystem/ark-net/pull/7)

Title speaks for itself 😉

## Ark client

5 PRs merged in the ark-client repository.
*To see the full list, [check this Github filter](https://github.com/ArkEcosystem/ark-client/pulls?page=1&q=is%3Apr+merged%3A2018-05-01..2018-05-31&utf8=%E2%9C%93).*

#### Fix for USB init error on machines without USB port

[#41 by wownmedia](https://github.com/ArkEcosystem/ark-client/pull/41)

Ark-client tried to initialize a USB port to check if a Ledger is connected, when no USB port can be initialized the app crashed.

Added error handling for the loading of the modules that manage the Ledger. This prevents a crash when no USB port exists on the system. The user is warned when no support for the Ledger is available and all methods that might use the Ledger have an additional check if Ledger support is enabled or not.

#### Fix crash if trying to send a transaction from a new account

[#37 by wownmedia](https://github.com/ArkEcosystem/ark-client/pull/37)

When a new account is created it is not known by all the nodes. When trying to send to/from this account using the postTransaction() method the app was crashing.

## Good job, Ark community 💪

With that much work from the community, we can't show everything here. But we can mention the other  repositories with merged PRs this month : 
[ark-node](https://github.com/ArkEcosystem/ark-node),
[ARK-PHP](https://github.com/ArkEcosystem/ARK-PHP),
[ARKcommander](https://github.com/ArkEcosystem/ARKcommander),
[ark-desktop](https://github.com/ArkEcosystem/ark-desktop),
[arky](https://github.com/ArkEcosystem/arky),
[ark-go](https://github.com/ArkEcosystem/ark-go),
[ark-deployer](https://github.com/ArkEcosystem/ark-deployer),
[ARK-JSON-RPC](https://github.com/ArkEcosystem/ARK-JSON-RPC),
[ark-js](https://github.com/ArkEcosystem/ark-js).

Congratulations, Ark community ! Great, great work this month. Let's keep this going, with [Ark V2 coming to DevNet](https://ark.io/countdown), June will be a busy month !

*Special thanks to @dated and @ItsANameToo for helping me select some of their PRs 👍👍*