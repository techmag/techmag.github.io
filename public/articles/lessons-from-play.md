---
title: Lessons I wish I had learned before migrating from Java and JSPs to Scala and Play
layout: post
---

I’ve written this article in the hopes that it spares someone on a similar path, the pain of migration, and the feelings of insanity, while moving from the world of Java and JSPs to the world of Scala and the Play Framework. 

Anytime a person falls into a pothole this big they want to place a sign that simply says “watch out” so others can avoid a similar fate. 

### These are my potholes…

This is not meant to be a this is better than that exercise nor is it intended to justify or rationalize or even proselytize any given choices of environments. Each developer has their reasons for doing what they do using the tools they choose to do things with. I can respect that and I’m not going to advocate for the reader to embark upon any changes. 

What I am going to do however is, if you find yourself on this particular path, I hope to speed up your motion by shedding light on the things that I failed to see and the potholes that were not (at least to me) clearly marked up front. 

I’ve been with Java since around the 1.1 to 1.2 days. It has served me well. I looked at the tools that were available and at the time i chose to build a framework. (Yes they say never build a framework but I did anyways and it worked for what I needed to do over until recently. I learned a lot from the process, mostly how to appreciate what a good framework brings to the table.) 

My framework has come to its end of life stage -- oh it could run for many years yet but the cost of maintaining it versus the value and benefits of using someone else’s framework well let’s just say those lines finally crossed. A very expensive lesson (did I mention never build your own framework?) but that is another lesson for another time. 

This lesson is about the process of learning after I choose a new framework and the unexpected challenges that that presented. 

As Julie Chen says on Big Brother:  “Expect the unexpected”. If only it were that easy...

My journey actually started out by choosing Lift. (Sorry not intending to flame a holy war here, just saying here’s what happened and here; is how I felt about what happened.) I felt (IMHO) that Lift might be superior to Play. At least that iw what the Lift guys proclaimed. 

Great -- lets roll up the sleeves, hit the blogs, Google and YouTube, buy all the books and training courses on Lift I can and get this party started! 

Read most of everything and wanted to dive right in, as that is exactly what all the authors encourage - learn by doing. 
So I did. 

Everything worked as expected. Building an example out of a book however is not what real world programming is all about. Yes, thanks to the many examples that were out there I could do a git fetch and have a working app that I could hack but I quickly found they broke easily and I just didn’t have enough context in order to fix them or hack the way I wanted. 

Eclipse wasn’t helping. With Java development I was so used to using the type forward expander to see what my options were when I was working on unfamiliar objects. Ah that looks promising now let’s go read up on that method and see what it really does. An hour or two later I had enough context and material to work things out. Pretty standard process. 

Pothole number one…

Eclipse and Scala aren’t quite as in sync as the world of Java was however so almost constantly I got useless “suggestions”. These useless suggestions were compounded by the fact that a single non-compilable chunk of code in a project seemed to knock the compile off the rails and no suggestions at all would come up. 

Well what is someone to do if that want to get something working, have exhausted almost every option and have spent hours (sometimes days) praying to the great google god and still can’t find a way to make something, even something relatively trivial actually work? 

Note: Scala uses “Domain Specific Language” (DSL) in various places. Basically you can within the normal usage of the language design and implement your own micro-language in a specific portion of the  world where your talents are used to program. 

These DSLs are virtually un-searchable in Google. So trying to find examples of how something is used is virtually impossible. Partly due to “newness” perhaps but more likely due to this syntactic sugar and it’s somewhat fluid syntaxless syntax. 

Ah - thank heaven for the official Google group for Lift development. 

The particular “thing” I was trying to get to work was Social Logins. Not completely trivial unless you look at the plugin that is supposed to make it work with a few lines of code. 

Does everything in Scala work within a few lines of code I wondered? Maybe...

Strip out all that boilerplate and ceremony and its amazing how little is actually left. 

I started asking questions on the official Lift channel. After years of searching StackOverflow and many many other sources for answers you know what really grinds my gears? Developers that are too lazy to ask a great question. I typically takes me 2 hours to write a question as I want to accomplish several things. 

I want an accurate answer 
I want to see if I might already have my own answer. I’m always amazed at how many times just asking a better question gets me to the answer.
I want to take others through the same journey so they can easily see if this question applies to their situation (or not)
I want to set the answerer up so they can answer in such a way as this question need not be repeated again hopefully saving the community time, energy and focus. 
I want Google to notice this question when asked and present it as a viable candidate for the answer 

Google is after all the most likely place developers go to first when trying to figure something out and given that I’ve spent a minimum of at least 2 hours searching (per question) and I haven’t found anything truly relevant, or sometimes even readable, I want to serve the community as I find things out for myself. 

Martin Odersky, the father of Scala, in one of his presentations, mentioned that the Scala community might be one of the most unfriendly communities in the world of development that he has experienced, when compared to others. 

Based on what I experienced next I think I can understand why he felt that way. 

Apparently it’s not good to ask the only place that Lift has as an official source of information for any of that information as they are all very busy. They happily tell you this rather quickly. Their documentation, and the collection of books that the group moderators have published, answer just about everything. Oh and please obey all the rules while you’re at it. And this group doesn’t have any need for outsiders helping out as they’ve solved all the problems already with their documentation. 

Of course this is the point at which I noticed a torrent of messages telling everyone to stop asking about “x” (a recent change that caused things not to work with the “lift” framework for templates). It was not a bug after all but a documented thing and therefore need not be asked about.  Hey I’m on board -- I did my homework -- I saw the memo -- I’m not asking that question! 

Along my research travels I discovered the “official place” to search for questions. I used that tool, a google custom search, to search for info on how to implement the aforementioned social login plugin and low and behold apparently I had become at least ½ of the documentation on the subject. 

That magical moment, plus the fact that a lot of the pages in the Lift Wiki (the official source of documentation of everything you are no longer supposed to ask about) come up as completely empty, yet to be populated. 

When I took a second look at Play and I saw tons of glorious documentation it didn’t take long to make an executive decision that if I was not already in the Lift insider’s club and I actually wanted to get things done then perhaps Lift is not the platform I should be searching for. 

So I rebooted my efforts and move over to the Play camp. 

With all that glorious documentation things would go far better far faster right? 

One would think so, however… 

I went back and got some books on Play and some training courses and I was still running through everything I could find on Scala. (.map(x => y) solves everything? Really???) 

I have an Apple TV so when I got tired of sitting at my computer desk I could retire to the couch and continue the education on the big screen.

More potholes, bigger ones too...

Here is where it all started to get funky. 

Watch video, head to laptop, follow along. Pause video, rewind and go over. 

Not working. 

Hmmm. 

Obviously missing something. 

Go back to computer desk, scour blogs, try code. Not working. 

Is it Play? 
Is it Scala? 
Is it me? 

I know there’s a bad Memorex pun in there somewhere but back to the real world. I have people breathing down my neck to get stuff done. 

I’m cramming in more and more education and yet nothing, and I mean nothing, is working. I read more and more documentation, extending my days to burn the candle at many ends. I break down and (shudder) cut and paste code (I loathe doing that as I want to understand everything that I type and everything about everything that I type too). 

Wow - I started to wonder perhaps I’m better suited to a job that requires me to say things like: “would you like fries with that?” 

Is this what it feels like to be an old dog when your master comes along with a new trick? 

What happens when a type A like me hits a wall like this? 

You dig in and read and watch and try even harder. 

How bad was it? 

I gave up watching House of Cards (blasphemy I know right?) in favour of my stack of “watch later” YouTube videos on the topics of Scala and Play. (Hey Toronto Java Users Group (TJUG) you guys rock! Thank you for those videos and yes you guys a TypeSafe too!) 

Gradually I started to notice things. 

Gradually I started to get some things to work. 

As more things worked I put together the pieces that I’m about to share here. 

Hindsight is always 20/20 right? 

Well forewarned is also forearmed so here goes. Programmers need all the arms they can get after all :)

First of all I started paying attention to the dates that things were published. Coming from the Java world if something was published it pretty much worked no matter when it was published. It might be deprecated on rare occasions but at least that would lead to the new way of doing it in short order. 

So looking for only recent material was not something this Java programmer had to worry about. You just found answers and moved on. 

Moving from Java 1.2 to 1.3 and so on was relatively painless. Yes there were some show stoppers in the early days but by and large if it worked in one version it worked in the next. 

Turns out that that is one of the things that the Scala community really didn’t like and choose not to have for Scala itself. Backwards compatibility be damned, their goal is to make a great language and if backwards compatibility would get in the way of that goal then they would have no part of it.

Great I thought - now put a freaking pothole sign on that for all us Java developers that are just catching up with you please! 

This is compounded by the fact that Google tends to favour old, established posts. 

Especially old posts that are visited often and the visitors remain on the page for a while. 

(I wonder how many others like me are sitting on those pages wondering why the code doesn’t work and yet feeding the google monster as they do so making it more likely to happen to even more others.) 

You search for things and lo and behold chances are you get a old post on the topic. Those old posts don’t have a warning label or a best before date as they didn’t realise the costs and side effects of the Scala community choices. 

It’s not until one has already figured out that recent posts are the only posts you want but more accurately posts specific to the exact version you are currently working with that these types of posts finally start showing up. You change what you’re searching for, for starters and how you search for it. 

I’ll also digress here a little bit and say this: 

The compiler, when it fails in situations like this, where a novice developer knows little about what is really going with Scala (and/or Play) typically has nonsensical error messages. At least messages that have no real bearing on the root problem (what you have to fix) that actually caused the compile error. 

The blue fairy has lost her tinkle dust - try using extended algebra on that ham sandwich. 

What? 

(No that is not a real error but it might as well be for all the good these things do).

Typing one of those compiler nonsensical errors into Google, because hey that’s the first place you look right, means you end up wading through days worth of drivel trying to decipher what is actually going on. 

This is the “you don’t know what you don’t stage” because if you had any idea that that particular error was in fact nonsensical you would simply go change the line above where the error appears and get the compiler back on track (or at least get a sensical error) and not waste the next 2 days trying to decode drivel.  

They say if that by the time you can tell good advice from bad advice, well you just don’t need any advice at all by then now do you? 

Thankfully Play has done a great job of making their entire site version searchable. Assuming, of course, you know the importance of paying attention to the versions. 

Pothole ahead -- pay attention to the exact version you are working with and don’t stray from it --ever!

Just like Scala, Play has also adopted the “we don’t care what breaks when we move to the next version so upgrade at your own peril” approach. 

Hindsight is always 20/20 right? 

I hope you discovered this article or were at least smarter than me in figuring out the version sensitivity before you invested a ton of time, energy and money learning what used to work in prior versions of the Scala language and the Play platform.

Any other gems I can leave you with? 

Hmm map doesn’t solve every problem in the Scala world but man they sure do pitch it like it does! 

Took me a long time to realize that one idiom Scala programs tend to adopt is “a collection of one”. Again makes perfect sense once you see the pattern but until then your mind is going “no I don’t want to deal with a collection of these things I only want one of them damn it!” 

As a collection of none can now be treated without errors, a collection of one makes perfect sense. 

So maybe having just the right map is all it takes :) 

That and having all those crazy potholes clearly marked! 
