# Jeremy Rand

_**Critical Decentralisation Cluster 36c3 - Namecoin Introduction (Jeremy Rand)**_

[youtu.be/b-sWa2YzJjE](https://youtu.be/b-sWa2YzJjE)

_**Abstract**_

Namecoin is a blockchain (first project forked from Bitcoin) that implements a decentralized DNS and public key infrastructure, which is resistant to censorship, hijacking, and other tampering. This talk will explain the basics of how Namecoin works and what it can be used for.

_**Transcription**_

_Diego:_ For those of you who don't know, we are also streaming this. If you go to decentral.community on the front index page is a youtube link where we are streaming these things. So even if you have to go get some food, use the restroom, go to another talk, you can still open that up on your phone, put your headphones in and be here all day every day. So that's fantastic.

We've got our next talk for you, Jeremy Rand from Namecoin is here, and he's gonna be telling you all about this project that he works on. It's really interesting, I think, it's actually one of the few use cases of blockchain. There's actually not that many, don't tell people. And he's gonna tell you this one. So thanks so much. Let's give a hand to Jeremy.

_Jeremy:_ All right. So I'm Jeremy Rand from Namecoin, and yeah today I'm gonna talk about just what the heck this Namecoin thing is for anyone who's not already super familiar with it. So let's get started.

So DNS, if you're not familiar with how DNS works, it's basically the thing that maps domain names, i.e. a human readable name like say riot.80 to an IP address, which is how your computer actually has to find the website, and unfortunately DNS is vulnerable to censorship, i.e. making a domain name not resolved at all. DNS is also vulnerable to hijacking and making a domain name point to the wrong website. And both of these issues are because DNS is way too centralized. So what features would be considered to be desirable in a DNS like system. Ideally.

So first of all we want it to be decentralized, right? So that means that there's no central entity who can change what a domain name maps to. We also wanted to be global meaning that if two different people look up the same domain name they end up going to the same website. And we also want it to be human meaningful meaning that a domain name is something that a human can actually remember and choose rather than something that looks pseudo random. And unfortunately there is an unfair the well-known conjecture called Zuko's Triangle which states that you can only get two out of those three properties at any given time.

So for as some examples of how Zuko's Triangle works. Uh cryptographic keys, let's say, I don't know, a Bitcoin or Monero address, they're decentralized meaning there's no central third party who can change what a Monero address points to. They're also global – if two people send money to the same Monero address, the same person will get the money, but they are not human meaningful – you look at a Monero address, for a Bitcoin address or .onion domain something like this, it looks pseudo-random.

Also on the triangle we have DNS and DNSSEC. These are global – if you enter, if two people enter the same DNS domain name in a web browser they do end up with the same website. They're also human meaningful DNS, domain names they look like something a human would choose, but they are not decentralized. And that makes us very sad.

There's also another set of systems on the third end of the triangle, things like Bookmarks or Petnames, or GNU name system, or I2P. And these are decentralized because there's no central third party who can change what your Bookmarks point to. They're also human meaningful – you can choose what you name your Bookmarks. But they are not global – you might have a Bookmark and your friend might have a Bookmark, they might have the same name, but they can point a totally different websites.

So if you want to achieve all three of these properties at once, sadly this is a very hard problem, because it generalizes to a class of problems called the decentralized global consensus problem. And this problem was actually first analyzed by Lamport back in the 1970s, and Lamport actually came up with a math proof saying this is impossible to solve.

Some time later, when Wikipedia was first being built, the Wikimedia Foundation really wanted to make Wikipedia peer-to-peer app instead of running on a central servers. And so they had their cryptographers try to look into whether that could be done. And their cryptographers ended up independently reproducing Lamport's argument that this is impossible. And meanwhile in the cypherpunk community there were lots of efforts to build a peer-to-peer currency. And in that context this was called the double spend problem. And they also decided this was not possible to solve.

Well as most of us know today this class of problems, that include Zuko's Triangle, was finally solved by Bitcoin in 2009. That's why peer-to-peer currencies are a thing. So, hmm does that mean we can solve Zuko's Triangle using Bitcoin? Maybe.

So the first person to sort of suggest this was Appamatto. He posted this on the Bitcoin IRC channel in 2010, and he said: “I had an idea for a Bitcoin-like DNS system. Basically, each generating block allows you to define a new name, and transactions are remappings of the names to IP addresses”. And he says: “Although there have been attempts to tackle DNS in a distributed way in the past, I don't think there have been solutions that fully removed authority from the equation”.

And he also saw the parallels in these problems as well, because he said: “If there was such a solution, it probably would have been possible to implement Bitcoin directly on top of it, and we all know that didn't happen”. And so Appamatto proposed a system that he called BitDNS that would achieve this.

And another community member Theymos replied, and he said: “Well why don't we just generate ‘domain credits’ that allow me to generate a domain and then we can transfer around those domain credits still”. And this had the advantage compared to Appamatto original proposal that you could register names trustlessly without being a miner yourself. And this was basically the first ever invention of the concept of a utility token.

So that was in the Bitcoin scene. Elsewhere in the DNS related scene Dan Kaminsky and Aaron Swartz have been looking into Zuko's Triangle for quite a while. My understanding is they actually had a long-running bet to see whether Aaron could find a way to solve it. And at some point then Dan Kaminsky got really interested in Bitcoin. And Dan told Aaron you know since DNS and a currency are actually really similar problems, uh you know, Zuko's Triangle might make Bitcoin impossible too.

And Aaron initially thought that that made no sense because you know Bitcoin obviously does work. But he pondered this for a few days, and then he concluded that you know Dan is actually right. But that doesn't mean Bitcoin is impossible, it just means we can actually use Bitcoin to solve Zuko's Triangle. And Aaron proposed a system called Nakanames, which resembled BitDNS quite closely although he wasn't aware a BitDNS at the time.

Well a couple of months later Vincent Durham actually released something that did this. It was Namecoin.

So Namecoin is basically what DNS would look like if it were on a blockchain. It uses the .bit top-level domain. So as a result of using its own top-level domain it interoperates with the DNS and it doesn't conflict with it. So you can have a single computer that speaks both Namecoin and DNS at the same time, Namecoin is in its TLD, DNS uses all the other TLDs, they don't conflict. Namecoin is highly censorship resistant because censoring a .bit domain is basically the equivalent of trying to freeze Bitcoins. It's also hijacking resistant, because hijacking a .bit domain is roughly as hard as stealing Bitcoins.

So Namecoin is simultaneously decentralized, global and human meaningful. It squares the triangle.

So what are the other use cases that is really fun, that you can do with Namecoin is you can actually use Namecoin as a decentralized public key infrastructure. So for example, let's say that you want to look up a public key for, I don't know say, TLS, Tor onion services or PGP, or OTR or something like that. Namecoin can actually do this in a decentralized way. So for example let's say that you have a website that uses HTTPS. You can put a TLS certificate fingerprint in your .bit domain, and visitors to your website can then verify your certificate without relying on a public certificate authority. So this is kind of similar to how DNSSEC/DANE do TLS, but this doesn't… Namecoin doesn't need that ICANN root key like DNSSEC does.

So I'm gonna wrap up by just sharing some kind of cool trivia things about Namecoin that might pick your interest. First of all, as Diego alluded to, it's the only non-Bitcoin cryptocurrency where Satoshi Nakamoto actually directly had a hand in development. Specifically Satoshi invented the idea of merged mining which allows Namecoin reuse Bitcoin mining proof-of-work which is the reason why Namecoin has a massively high hashrate, in fact it right now it's around 70% of Bitcoin’s hashrate, so it's huge, and in fact for 48 hours a couple years ago we actually had a higher hashrate than Bitcoin due to the hash war between Bitcoin and BCH. So in addition we were endorsed by WikiLeaks in 2011 – Julian Assange actually mentioned Namecoin in his conversation with Google CEO Eric Schmidt. What was kind of funny was that Assange actually mentioned Namecoin first, and he explained what Namecoin was by saying: “Oh, it's basically a Bitcoin based DNS system” except the Google CEO was kind of not very literate about technology, who knew, and he had no idea what Bitcoin was, and so Assange had to back up and explain what Bitcoin was before he get back to explaining that what Namecoin was. We were all so favorably mentioned in ICANN report in 2014 which is I guess a little bit surprising, turns out even the establishment people seem to find us at least mildly interesting. Who knew?

The founder of the Internet Archive Brewster Kahle said some nice things about us in 2016, and then between 2016 and 2017 we actually had some really interesting, real-world usage of Namecoin that actually got into the news, because the NSA whistleblowers “The Shadow Brokers” leaked a bunch of NSA malware code using a Namecoin domain name in order to evade censorship. So that was kind of interesting. And speaking of things that made the news – the New York Times actually alleged in 2018 that Saudi Arabian intelligence actually recruited a Twitter employee to spy on my Twitter account. We're not totally sure why Saudi intelligence thought Namecoin was worth spying on, but the best guess we can have is that Namecoin was maintaining a fork of some TLS code by Moxie Marlinspike, and the Saudis were interested in Moxie, they kind of wanted to surveil me as an extension of that, and then this year the US Department of Justice actually indicted three people for doing that spying operation for Saudi Arabia, and one of the people they indicted is the same guy that that time specifically said was spying on the free software developers including me. So interesting.

So finally we really love collaborating with other projects. For example we're currently collaborating with Monero on enabling anonymous name registrations. So if you have a cool idea that we might be able to work together on, please talk to me, we love collaborating. As you can see I'm wearing a t-shirt with the Namecoin logo, should be really easy to find me at a distance, so hopefully you'll have no trouble finding me. And that is my presentation, so thank you!

Do we have time for questions? We do. Cool.

_Audience:_ Hi, thanks for the talk, amazing stuff. How is Namecoin better than ENS?

_Jeremy:_ How is Namecoin better than ENS? So ENS the Etherium name service, for anyone is not familiar with it, one of the interesting things about ENS that is not very well known is ENS actually has a backdoor in it. Would you believe that ENS actually has a backdoor and they bragged about this at an ICANN meeting. They actually said that… well they were asked a question about someone who wanted, who is like well if someone registers a name that we think we should have rightful ownership of how do we enforce a trademark claim against them, and the ENS developer actually replied that yeah yeah there's actually a mechanism in ENS that can let four out of the seven ENS developers change the mapping of names. So generally speaking I would not recommend trusting a blockchain based system where the developers think that's an appropriate thing to have in there. Did they finally take that out? Okay, okay. So that's interesting that they you're saying they've taken that out. I'll assume you're correct. I would still not recommend going with software by developers who leave that in there for years. Okay, go.

_Audience:_ I think they charge like 640 something dollars a year for a three letters domain, and I still don't know why and how they use the money, then who will use the money.

_Jeremy:_ Did you know that the auctions the ENS does were actually not done in a decentralized way…

_Audience:_ They use this…

_Jeremy:_ Yeah, yeah, they're using a centralized service because apparently they figured out that using a decentralized way of doing the auction wouldn't actually scale properly on their blockchain. It’s my understanding of why they do that. I think the system is called OpenSea that they're using, is that right?

_Audience:_ It's like a game items, I think. That's over, the auction is over, so now you can just register by a domain, you have to pay every year, mm-hmm, it's like five dollars for any domain, and three and four letters is more expensive, but I don't know who has the money and…

_Jeremy:_ For what it's worth, generally speaking so the Namecoin developers actually briefly looked at the idea of doing auction-based sales of names, and we actually rejected that idea for other reasons, just because we decided that the auction based systems are probably ripe for abuse in order to censor things. Because what that means is in practice if the names were being auctioned then someone who has lots of money to throw at a problem, they can just make sure that names they don't want getting registered don't get registered. So generally speaking I don't think auctions are a good idea for a decentralized naming system because they're a tool that can be used for censorship.
