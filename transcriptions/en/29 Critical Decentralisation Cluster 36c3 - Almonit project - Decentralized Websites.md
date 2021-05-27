# neiman

_**Critical Decentralisation Cluster 36c3 - Almonit project: Decentralized Websites**_

[youtu.be/YIg2KOo7KH4](https://youtu.be/YIg2KOo7KH4)

_**Abstract**_

Almonit is a project for decentralized websites and web services. Decentralized websites and web services are an alternative to the way the web functions today. They combine decentralized storage (like IPFS), decentralized name services (like ENS) and P2P networks in order to replace the server-based model of the web. This lecture describes the Almonit project, its architecture, the technical details of the technology and the ecosphere in which it is created. Come discover the state-of-the-art of this up-and-coming area!

_**Transcription**_

_Diego:_ Yeah, ok, it's working. So I'm going to invite our esteemed speaker, who needs no introduction, so I shall not introduce. Please, introduce yourself for the audience real fast.

_Eyal:_ Hi everybody, I'm … mathematician. I did a PhD in mathematics from Berlin. I do consulting, I do freelancing and, I do open source projects, I'm doing Bisq since a few years now. But today I'm going to speak about Almonit and decentralized websites which is quite new.

_Diego:_ Ok, so yeah, I need the microphone back just so I can say I'm leaving the stage, because if I was to leave the stage while he was talking, it would be kind of weird and awkward and stuff. So I am now leaving the stage, let's give a great big hand, not for me yeah.

_Eyal:_ Thank You Diego, who already thanked himself. But nevertheless actually I was about to begin with introducing myself, but this happened, so let's begin with our project right. How do you pass it here, oh yeah right, good.

Almonit. Almonit is a new project we begin at about half a year ago. I don't know if you have ever began like a new open source community project, what when you begin your like aiming for the stars, and that why our first slogan was “Decentralizing the web”. And when you see this, you think two things, one: you're like: “What? The 2017?” And second, you say: “Hey, ain’t the web already decentralized?” And yes, the web was designed in decentralized way, and it began decentralized, but I think that it didn't scale so well and still being decentralized. For example, DNS supposed to be decentralized but we are about to sell the dog alt domain to a third party, which is a commercial company, which we don't know what they will do with it. Email is supposed to be decentralized, I mean it is decentralized architecture. It's like a fairy vests, but everybody is Gmail. I have my own email domain and my emails often go to a spam folder or sometimes they are just rejected, which is somehow ok for me, because my professional hat is the crazy guy who is into privacy, in decentralization, and people hire me because of it. But my lawyer had private domain, and when her emails start to go to spam folder, she had to switch to something which is backed by Google, because she couldn't afford losing customers over that, so it doesn't seem professional. So the web was decentralized, it's still quite decentralized, but there is still centralization element in that.

The other issue with this slogan, “Decentralize the web”, is that it's very vague, doesn't really say what we do. And in the last six month we actually what we did was “Dwebsites tools”. “Dwebsites” is how we call decentralized websites. And what I mean by “Dwebsites tools” is I'm gonna show you a movie, yeah this one, ok. I hope it's good enough. It's not great so great quality. This is a record of what we are going to publish in two weeks. It's a search engine. I mean you saw search engines in your life, nowadays they all look the same. The nice thing about this search engine is that it's a decentralized search engine, which is a decentralized website, for decentralized websites. It's a bit long, but what you should really remember is that you can use it to find which decentralized website exist. And it doesn't hang on our server, so it's run like you know on decentralized p2p network, which means it's completely private or as private as the p2p network is. And it's not really censorable, because try to DDoS IPFS it's quite or even block it it's quite a task. So what's the advantage of this, it's gonna be released in two weeks, what we have now in our website is a directory of decentralized websites, and I'm going to speak about it a bit more later on, ok. I'm a bit not much you when it comes to using Mac.

Now let's address the lion in the room, because we have a strange logo we have a lion, and we have a strange name, and unless you are a Hebrew speaker you don't know what it means. So let's do begin with the lion, why do we have a lion. Well we have a lion because Mozilla got a fox, and we like Mozilla, and lion and fox relates. So now we got a fox and a lion, and together we got a jungle which is cool, because it's also kind of our statement. We want the Internet to be like a jungle. There are entities who wanted nowadays to be like a field — very organized, very planned, sterile maybe, something like is being decided by that person who plans the field, and other people who live in the field. And we want to be like a jungle, which is slightly more chaotic, but also more rich, more fertile, and you know in the jungle you have lions, in the field you have hogs. So we got what the jungle thing.

It also I like to read, so I try like in every talk that I give to at least mention one book. This book is from the 90s, the end of the 90s, it is “Seeing Like a State” by James C. Scott. He speaks about and mostly against high modernism, which is how he called the state that were formed in the twentieth century, which well trying to control and plan the lives of the citizens as much as possible. It's very forth intriguing, I don't agree with much of the stuff that he writes, but this goes for every book that I read, and what's relevant for us here, is that in the first chapters he speak about the science of forestry, so designing a forest. Apparently by the first chapter it began in Germany in the end of the 18th century, and before that forest where a bit like a jungle, but not as diverse, but still something rich and chaotic. But for the state a forest was a place from which you take wood, and we started to design the forest, such with it we'll have mostly wood and not other stuff, and also the kind of wood that they have, and also that you could access that. So the German forest, I do a lot of bicycle trips, the German forest is very organized, its rows in this, I was never lost in a German forest. I was lost in Ukraine in the forestry for half a day. In a German forest if I get lost I have to choose the direction second after half an hour I'm out. I noticed it like myself with the bicycle trips and when I saw it in the book, so it was good for the state for the beginning, because they got like really good lumber and a lot of it, and they needed it for construction. It was bad for the farmers, it for this bad for people who lived near the forest, who live of the forest, for the ecosphere, but what turned out after a century, in the end of the 19th century, it was also bad for the forest, because suddenly the third generation of woods that were planted didn't grow. It grew up in the first and second generation, because the forest was so fertile, because it was so diverse. And when again, I'm quoting the book, I didn't really found other good sources for that. a new word entered the German vocabulary, a “waldsterben”, it was a phenomena that happened apparently in the end of the 19th century. And I think that this story makes you understand maybe why we want the jungle and not a field, and not like something so science. Of course you also don't want the internet to be a complete chaos, because we are not living in the Wild West, and there is also bad people who want to do bad stuff. But you should govern it around what people do and not tell people what to do around what you want.

Then there is another element here which is the word Almonit. Almonit is Hebrew, it means anonymous. It's a feminine form of the adjective. So we are into privacy. The other cool thing is with Tel Aviv, I'm from Tel Aviv originally. Tel Aviv has an alley called “Almonit Alley”. It's “Simta Almonit”, “simta” is an “alley” Hebrew. It is very small alley, and if you enter the alley, in the end of alley you see a statue of a golden lion, and it's nice when things work out.

That's about us, the project, the name, the lion. And now we can speak about Dwebsites. So Dwebsites was not invented by us. We also don't build Dwebsites, we make tools for Dwebsites. I know Dwebsites from ZeroNet from 2015, which was a project, we did decentralized websites, I liked it. It's different than us also, I mean it's quite different than us, but the idea is the same. Perhaps it was before, I'm not so sure to be honest. And to explain what is it in the way that we make it, we refer to let's first speak like you know “explain to me like five years old, what is a website”. So this is me, this is a picture of me with a friend drew when I was 20. I already didn't have any hair, but I still didn't have a hat. And I want to surf the internet, regular websites. So I got name, and I go to a name service, DNS, and I ask the name service: “Hey, where can I find the content of this name?” And the name service gives me back the IP or the address of a server, and I go to the server and I ask for it. So the server gives me the website, and then nowadays begin kind of exchange of me and the server, like back and forth. This is the dynamics of websites, because that's the websites are not static nowadays. Sometimes we have, I mean sometimes, there are always other people in the Internet, I tend to think that all the people look like me, so it's written “not me”, but let's assume it's still me, and I the other “not me” speaks with the server, the server lets us communicate, and you have more dynamics. And I stress this dynamic, because this is the part which is difficult to recreate in decentralized website. The whole talking back and forth with the server, the server being someone that connects people, that remember states, that lets you know that you speak to one person which is connected to it, and not to a million, who try to scam you. This is what is difficult to recreate.

So now we go to Dwebsites. And it's still me, but now I have a different name. This name is not part of the DNS registry, it's a some random name. And instead of going to DNS I go to a decentralized name service, like NamesCon which was here yesterday, we actually use ENS, Ethereum Name Service. It's based on Ethereum. There are two reasons why we use it. I'm not a huge fan of Etherium, but I'm a huge fan of ENS. I think what they've been doing a very good job of trial and error of how to create a decentralized name service. It's still in alpha, so it's not perfect. But they did a good job. And B they also did a good job of like business process. So it's supported by some browser, people know of it, and the fair thing is that the Dwebsite in the comment form, will just begin where, we're about 10 when we began, so it was natural to use it.

I'm not going to say exactly how ENS works, because that's like another topic for another lecture, but what is important for us standard things — it's where you can buy the name, the name points to some kind of value, like IP or something else. The purchase process is automatic, and it's irreversible. So now you are away from the whole DNS thing: “hey, my name can be taken”, which happens once in a while, or the price can go up etc, etc, it's predictable. And it is private as much as Ethereum is private, and I know that there are Monero people here, and I love Monero, who will tell me that Etherium is completely not private, but let's say it's a different model of privacy when buying with a DNS, at least I don't have to use my credit card and do KYC, and this kind of stuff, and give my address.

The non-standard thing that it gives me is that one name can point to many values. So you can have one point it to a Monero wallet, which actually I think some people even do, or to Ethereum wallet, or to different, to an IP or some decentralized storage. It has a complex ownership model, so now it's not like one person owned the name, you can have a multisig owning a name, you can do something which changes with time, like today I owe the name, but in one year it will automatically switch to someone else. And it creates some kind of interest in new stuff that you can do with it. And it also has the automation of ownership, which connects of course to number two.

So I go to ENS, I get from them something, and what I get is an address in decentralized storage of this file-sharing peer-to-peer network of where the website is. We use IPFS for that, because IPFS, again it's a topic for a whole lecture, but it really fits this decentralized website thing. There are people who use SWAM I think there are also people who use DAT which is another decentralized storage or file-sharing peer-to-peer network. IPFS is definitely the most common one.

IPFS standard thing is file-sharing, so we all know what it is. And the less standard thing is that names are hashes of content. So you cannot now copy my website and give it a different name, because will be a different hash. It's really easy linking between different repositories of IPFS, between different files. And this is important for website. You can link from one to the another really easy. You can link inside, it's so convenient in IPFS. And again like in ENS we have good infrastructure. So they have libraries, Javascript libraries, and Rust, and they have a whole big ecosphere of people walking on it, which makes easier for us to do stuff with that, because I think one of the problem with ZeroNet was that the ecosphere was not so diverse. And here we are building infrastructure of ENS and IPFS, which helps us just to be more reachable.

Why do you need decentralized websites. What I think, that the first reason is one I call “the big three lions of decentralization”, what you get from almost every peer-to-peer network on decentralization project, which is: censorship resistance, it is super difficult to block IPFS or every other p2p network which is big enough, it's robust, the same thing goes for DDoS — it's very difficult to take offline, so if you're an activist organization can be a really good solution for you. And it's private as far as Ethereum and IPFS are private, which is up to discussion, and can also be improved, and we will be happy to actually also check some more private networks to do it in.

The non-standard thing is that you can do collective websites. So this comes to this complex ownership of names. You can do one website which is owned by a group, and every person of the group can change it, but then like half of the group can ban someone, if he something or she did something not ok. You can have like a society moderating and managing themselves, which is very nice and it's really difficult to do with the DNS model. You will have to start to manage access to the server, and still there will be operators. Here it is so easy and natural to do that, and it's one big pros of the Dwebsites which I like.

The cons of Dwebsites, and you should always say of course what is bad with what you do, it is slower. You know Google has a AMP which I hate but it's super fast, Dwebsites are slower. How fast is it really depends, because it's a huge website, then sometimes from p2p net where you can get big files very quickly, but still the connection to the p2p network takes the time. And the privacy, as I said already twice, depends on ENS and IPFS. So it's also something to consider, because sometimes you can just monitor those networks and know what people do. So it is a consideration.

Now the question comes to what do we do with Dwebsites. And the first thing that we do is the search engine. So right now we begin with just a directory like Yahoo start directory from the 90s, where you have all the websites there one by one. It worked well when there were 20, now we are like in the hundreds, so it's a complete cons. I designed it, I shouldn't be designing stuff, so it's also not so pretty. This one designed another member of the project, who is much better than mine, and it's a proper search engine. The great thing about it is private, and this is really private, because it's really done mostly client-side. I mean people know that you use… if somebody really monitors the network maybe we can use know that you did a search, but not knowing what you searched. It's decentralized. And the other thing is of course it's more difficult to scale. It's great for a few hundred websites, it would work for a few thousands, probably for a few dozens thousands we should also be ok, especially using the special IPFS linking options. So we can do decentralized databases, but if it gets to millions or billions of websites, we have a lot of research to do. There is a field called “distributed information retrieval”, and there is a relatively old and known project even from Germany, if I'm not mistaken of distributed search engine called YaYc, if I remember correctly. We have got to study from them, and we want to see how we can use IPFS, or DAT, or SWAM, special properties to scale it better, and to make it faster.

Second thing that we do invest in first, we publish was a browser extension, because it's great if you do a Dwebsite you still have to access it somehow. You can use our extension right now mostly to access websites, it works in Firefox, in Chromium based browsers, and we also want in the future, like in the near future, to have it working  on Tor, so you can have darkweb, where our end goal for this is actually to have it more like decentralization add-on. And the other thing is that you may think this is temporarily, because if these things really takes off let's say in five years or whatever, it's a dream. When Firefox and Chromium, and Chrome, and Google will just add support for resolving at themselves, you will not need anymore their browser extension. But I think it's very important to know how this thing is being resolved, because if instead of going to a p2p network, you just took everything from a Google server or from some gateway, when you just added like a centralized bottleneck in between. And our extension we always say, it's “the most decentralized add-on for decentralized websites”. So we really make an effort to do random choices, so you will not always go for the same path and one gateway, IPFS, one node, one seed not get too much power and this kind of stuff.

And the third thing which is in planning, in the development, is what we call Almonit Build, name may be changed, and this lets you build decentralized websites. If you find the topic interesting right now, there are two things that you can do: one you can talk to us and try to help with our infrastructure and the algorithms, and stuff like this, but the other thing is you could build a Dwebsite, because we need more of those, and we need people experimenting with those. And if you are a web developer you can experiment, but if you just want, maybe you want an easy tool for that. With the Almonit Build would be like a simple UI that you can build websites. It will be for personal websites, obviously the first thing because it's so easy and simple. Blogs or CMS, like content management system, because everybody is Medium, and I don't use Medium, I don't like medium, and I would be happy I have like my WordPress blog. But Medium is easy, and I would be happy to give like as easy but decentralized alternative for that. And e-commerce if you want to open shops and I'm in favor of legal shops by the way.

State of the ecosphere. So we've been doing it for half a year, when we started we were pretty sure, we accounted there are 13 websites, 3 of them were ours, so 10 besides us. And now there are like over 100. And I think what people do websites on, is first thing of all… personal website, you know I love developers — they do sometimes boring stuff, sometimes beautiful stuff, sometimes strange stuff. This stripe is here is like a shell website, where you have to actually walk to see what's there and it's really cool. There are many of us. And the other thing which is there a lot of is blockchain projects for very obvious reasons. One of them I think blockchain router has only a Dwebsite, I couldn't find the regular website which is cool, and it's a beautiful website. So if you actually download the add-on afterwards, the extension, and look for websites check out that websites, really beautiful.

And when there are already people who thought to commercialize it or to monetize it, I give it four examples. The first one which for me was the first, the most obvious, is the centralized exchanges, because the central exchanges always have an issue of… exchange is not supposed to have an operator. But if you have a website, when you operate the website, and it is literally operating. Basically one that I did, that's why we didn't have a website, we did a software, and the software supposed to be updated from the p2p network, but people like software less and less. So lots of the centralized exchanges it have been moving to Dwebsites, all of them seems to be an experimental stage, well it seems that you can still use it, I didn't try myself. Other thing is e-commerce, and this is mostly selling merchandise, but you know that's what that is for merchandise. Then gambling. Only one, but it will come I guess. It's also one of the first things that you do in anything. And this one is “Who Is Staking Sats?” is actually selling subdomains or set off a decentralized domain, because Nick Johnson from ENS load kind of repository from GitHub, it was cloned a few times, and people were selling subdomains and other peoples were buying that, which is nice, I mean cool. And then of course I guess people here know what is Rule 34, meaning what if you do something at the internet, people will use it for porn. So people have been using it for porn, but it censored. And when I say porn in this case, this is like the most softcore of the softcore existing. It's a hentai drawing of stuff, so it's light, it's like Rule 34 in quotation marks.

Yes there are already some browsers that support it. Of course the alternative one Opera supports it very, well I think the first one. Status which is a Dat browser for the smartphone support it. And they've been doing very good job with it. Brave have been announced that we are going to support it, but I'm not sure what is up with it. At least in my Brave browser it's not working yet. And soon like in a few years other will come. So we don't really think of Firefox or Google obviously yet.

That's it if you want to follow us, go to our Twitter, go on Almonit, we don't tweet very much. What we tweet is like updates on the projects, kind of articles that we write on our blog, and when somebody makes a new decentralized websites, because we monitor of it. We let people know as a new interesting decentralize websites. You can write us for any good reason, the world you know, we are sitting both near the computer waiting for emails, we are always happy for those. We also have a Dwebsite, alimonit.eth, and there is a blog in blog. alimonit.eth. Or if you don't feel like going to a Dwebsite, because you have to need right now to either have Opera or install an extension for that, you can go to our boring website almonit.club, which is a complete clone of it.

Thank you very much. This would be all. Yeah, so I will be happy to answer any questions, if anybody has some. One gentlemen, but I can hardly see you, I apologize.

_Audience:_ First of all thank you for the talk, it was quite interesting, and have a good luck with Almonit. One question. So obviously IPFS is the best at the time for the storage, but isn't ENS is kind of not that good solution in future proof, I mean because it's based on a Ethereum anyway, and it's decentralized but it is locked to Ethereum of sorts. Like is it really a good solution or are there any alternatives at all?

_Eyal:_ It's a good question. I would say that the ENS people themselves don't think with what we have now is the final version, and right what now, what we have is partly not a great solution. First thing of all because what we have now is… I mean, you can we can change everything using… sorry, like signatures of seven people. So it's not the final version. We also have another issue which scares me a bit, which is squatting. I mean what's problem with ENS, it will be a bigger problem with ENS. And it is tethered to Ethereum, Ethereum has itself, having change is going to Ethereum 2.0, and you don't know what will happen in this sphere. That said I like ENS because it is the best naming system with ISO. Namecoin is great, I don't know it that much to really compare completely. But ENS has been doing great jobs, and Nick Johnson who I think founded it, as far as I know has been do a good job. So it's a good reason to use it. We can switch from one ENS version to another, from one domain, decentralized name service to another. We can even support a few. So we are not tethered to this. The decentralized search engine can really easily switch to another same system. So I think it's a best solution which we have for now, and you know you have to see how things develop.

Other questions? Ok, so since this doesn't seem to be the case, I'm gonna give you back the lovely Diego.

_Diego:_ Thank You Neiman. Let's give a hand. Namecoin is pretty good, you should consider it. The Namecoin guys are floating around here somewhere. And I disagree about squats. He says squats would be a problem. Everybody should be doing squats. It's a different kind of squat, but you should be squatting, if you want to extend your life lift weights.