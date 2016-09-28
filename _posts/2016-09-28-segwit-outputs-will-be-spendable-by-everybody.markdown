---
published: true
title: "SegWit outputs will be spendable by everybody."
layout: post
---
> If Core cannot maintain its 51% attack going, SegWit outputs will be spendable by everybody.

[comment on r/btc](https://www.reddit.com/r/btc/comments/54rglu/the_final_countdown_segwit/d84d4ei)

**False.**

In soft forks, a upgrade mechanism that has been designed into Bitcoin since its creation, new rules are added through a combination of miner supermajority and rules in fully validating nodes that recognise the addition and enforce them. Once a supermajority 95% of the last measurement period is signalling that they will enforce the rule (see [BIP9](https://github.com/bitcoin/bips/blob/master/bip-0009.mediawiki)), nodes that recognise this change will begin rejecting blocks without this flag outright and begin validating transactions as conforming to these rules. There is no situation in which after this point they will accept a block which does not enforce these rules, regardless of what portion of miners decide to mine non conforming blocks.  

If a node sees a rule activation through BIP9 that it does not understand, it will refuse to relay these transactions as it knows that it can no longer assure validity of them, and will not itself mine these transactions into a block. Nodes running with rules activated they do not understand are not operating at a risk of producing invalid blocks, and will not be able to receive transactions created with these new rules, for example, a 0.4 node will not be able to produce a P2SH address for anybody to send to.  

This is the same style of system which was used to soft fork in P2SH type outputs, which implemented an entirely new nested scripting system with a new opcode. According to [p2sh.info](http://p2sh.info/) these scripts store approximately 11.35% of all Bitcoin value in existence, and is the basis of multisignature security such as provided by BitGo. As with SegWit, there is no credible risk of these outputs being stolen. 