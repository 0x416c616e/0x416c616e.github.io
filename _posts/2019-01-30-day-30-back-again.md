---
layout: "post"
title: "Day 30: Back again"
date: 2019-01-30 11:05:38 -0600
---

## Back from a short hiatus

I was busy with other things, but now I'm back on track to do more daily coding. I will not count the skipped days towards the number for the #100daysofcode challenge. From now on, if I miss a day due to real life circumstances, that day will not count towards it. This way, I will have to make sure I put more work into coding in order to complete the 100 days.

## Article module

Today, I finished the bare-bones version of the article module in the static site generator program. It involved a lot of coding and debugging. I am very proud of how far this project has come. It's always nice looking back at the fact you started with nothing and developed a whole app. SSG isn't finished yet, but I decided to make pre-release version 0.2 on GitHub. You can make, view, edit, or delete articles now.

## Labels on GitHub and "good first issue"

I've been using GitHub issues for a while now, but it has many different features, so I just stuck with the basic stuff. But now that GitHub issues are part of my normal open source development routine, I'm starting to notice some of the optional features, like adding labels. Apparently there is one label in particular called "good first issue" and I think searching for issues with this label can help me submit more pull requests to other people's projects, which will change me from being a primarily solo developer to having more experience in team projects, which is one of the big advantages of open source to begin with.

## Travis CI

Did a lot of manual testing and debugging today, hence why I am looking into Travis CI and Python unit testing more. I only vaguely understand CICD and Travis CI. I think you can either use their official website or even do some self-hosting. I might want to set up an Ubuntu VM on my hypervisor so that I can install Docker on it and then set up Travis CI in Docker. I currently have Docker set up on an Ubuntu VM on my desktop, but if I want to develop on my MacBook, it'd be better to have the VM on my hypervisor because it's low-power and on 24/7.

## An important part of learning is doing things gradually

If a learner gets told about a million complicated concepts when they're first starting out, they can easily be overwhelmed and give up. I think part of effective learning for new programmers is to start with the basics and not be too concerned with more advanced things. If you tell someone a lot of irrelevant info, or make it seem like learning something is daunting, then they are less likely to succeed.

It's all too easy for a beginner to ask something like "how do I make an app?" or "how do I make a website?" but they should really scale down their expectations. If someone wants to learn how to make an app, odds are they have an unrealistic idea of how long it will take for learning that. I remember many years ago when I tried to look up how to make a video game -- when I was really young, I guess I was expecting for there to be some 10 minute answer. There isn't. When I realized that it was a lot more complicated than I had initially thought, I got demoralized. Learning a new programming language over the span of many months is one thing. It's really not that hard if you give yourself enough time. But if you tell yourself that you're going to learn a complicated subject in just a matter of days, you're setting yourself up for failure.

Part of people seeking out answers to questions like this is that they have a rough idea of how long they think it should take. But instead of trying to learn how to make a website, or how to make an app, change your goals to things like how to use variables, what strings are, how to write a function, what an array is, how to create a class, how to use a for loop, etc. These are goals that are more easily achievable because they are specific and limited in scope, as opposed to bigger and more nebulous goals like "learning to make a game" or "learning to make an app." Then you'll get positive reinforcement because you were able to meet your learning goal for the day, rather than trying to learn everything all in one go, which is impossible.

## My personal #100daysofcode

Maybe some people are using #100daysofcode as a way to start out with coding, but I've got a few years of experience with college and personal projects of my own, even before I started this. So although I'm not an expert, I'm not a complete beginner either. On Twitter, I saw some people posting about their new learning. That's great -- everyone has to start somewhere. But I wonder how many people are using it as a way to simply get better at programming, rather than starting from being a total beginner. 

## Unit testing in Python

Python has a built-in unittest module. I may or may not use that, but I will making unit tests in the near future.

## Udemy quasi-autodidactism

I just bought another Udemy course, this time about Python unit testing. Sometimes I like to learn things completely on my own, and other times I like to take short/self-paced online courses to help guide me to learn something new. Programming with Udemy is somewhere in between college classes and being a true polyglot.

Unit testing is the kind of thing that's really helpful, but you don't know that it exists when you first start doing basic coding stuff. But in the back of your head, you're thinking "okay, after I add this feature, I need to run the program and test it to make sure it does what I intended it to" and unit testing is basically a better-realized version of that, incorporating automation. This goes along with continuous integration and agile development, allowing people to commit more often and even merge to master more frequently, all without having to compromise security and stability (for the most part). 

## Pull requests

I learned more about pull requests today. I think I do too many commits and not enough pull requests, code review, or issues. The newer GitHub contributions tracker feature shows all four, and most of my progress is commits and issues, which is not very well-rounded.

## Writing vs. reading

Writing code is a lot easier than reading. But working on other people's open source projects will force you to read other people's code more. 

## Code reviews

I am trying to get more into all the other features GitHub has to offer, and code review is one of them. I tried code review today. It definitely seems like a useful feature and I'll be sure to use it more in the future. It seems more geared towards group development than solo apps, but I think it can be useful as a way of getting you to re-read your code so you don't forget what it is.

## Comments are lies waiting to happen

The best kind of code is self-documenting. Of course, that's not always possible, but you want to make it as readable as possible. But when you write too many verbose comments, you run the risk of someone modifying the accompanying code without changing the comment that goes with it. This is like bit rot, but for documentation.

You need to comment every now and then, but overdoing it will be counterproductive.

## Code smells

I am learning more programming jargon, such as smells. A code smell is when something seems amiss. Too many comments is smelly and an indication of bad design choices. If you have to take 10 lines to explain a function, maybe it wasn't written very well.

## Random learning

Watched some random programming videos to learn more about Python and useful programming topics. I try not to spend too much time on this, because it can be a slippery slope of time-wasting with interesting-but-not-very-useful learning ("edutainment"), but time management is an essential skill for software developers, because software is all paid for with money, and that money goes to the people who are developing the product. So the longer you take to finish an app, the higher the cost will be. This is why waterfall development is falling out of style, and more people are adopting agile (or at least their own personal interpretation of agile). 

It's good to keep up with industry trends as opposed to being so focused on your own bubble and tech choices that you become obsolete. But at the same time, you can't afford to waste too much time on it. Just learn what new categories of tech are being developed, what is gaining traction, what is losing steam, learn new novel programming concepts, etc. 

## Tech moves too quickly to keep up with everything 100% of the time

I learned about RESTful APIs in my web development and databases class. I reference that class at SIUE a lot because of how much useful stuff was in it (compared to classes about MIPS32 assembly or C++, which are not as useful these days). But anyway, now there are people who insist that GraphQL is a superior alternative to REST. But back in the day, people said SOAP was obsolete and you should switch to REST, or some other kind of API. I think sometimes we forget that a lot of new tech won't have any staying power. Just look at the average tech startup or JavaScript framework. Most tech startups fail within a year or two, and many JS frameworks or npm modules get abandoned relatively quickly.

## "The wrong generation" and 20/20 hindsight

Some people say "I was born in the wrong generation" because they like older music. Nothing wrong with older music, but the issue is that they're comparing the *best* music of the past to the *worst* music of today, while simultaneously ignoring all the awful music from previous generations that are all but forgotten. It wasn't all Beatles and Led Zeppelin. There were lots of mediocre bands that you've never heard of -- and with good reason. I'm not saying mainstream music is the best, but what I am saying is that we choose to ignore the losers of previous generations and focus on the winners. It's the same way with tech too... sort of.

It's kind of the opposite for software. People think all old stuff is bad just because it's old, and new tech must all be good because it's new, and you need to strike while the iron is hot. Microsoft really dropped the ball on mobile, and Satya Nadella once said this:

> If you don’t have a real stake in the new, then just surviving on the old – even if it is about efficiency – I don’t think is a long-term game.

After missing out on mobile, allowing Google and Apple to dominate it, they realized that they should have gotten in on it earlier. Now, I think they are overcompensating for this loss with their recent failures of trying to branch out into newer tech. HoloLens, Azure, Bing, and lots of other things -- sure, they might seem like okay-ish products, at least to some people, but a lot of them might not have longevity because MS (and many other companies) seem to want to get into new tech before figuring out if it will really be profitable or not. There are a lot of tech fads that die off, so even the most successful company in a particular area of tech might go under. VR was hyped up a year or two ago, but it still hasn't really caught on because it's too expensive and doesn't really have a practical use-case just yet. The VR demo booths at tech conferences seem cool, but that's because you'll only spend a maximum of a few minutes on it before moving on to some other display in the event. In reality, it's a cheap gimmick that wears off quickly. 

It's not just about VR headsets. A lot of modern software stuff is just fads that will be gone with the wind. There's a lot of slow-moving tech that's still around, like PHP and MySQL, and there's also a lot of newer stuff that is still really useful and growing, like Python and Django. But there's also a lot of new tech that will probably cease to exist in 5 years' time. 

I am a generalist who likes to dabble in many tech sub-fields, OSes, and programming languages because I don't think I'm the Nostradamus of tech. I don't want to put all my time into a single area of tech that may or may not do well in the future. The author of *Hackers and Painters* claimed that tools really do matter, and that you can't succeed without the right toolchain. But he listed really ancient languages and technologies that aren't widely used these days. So was he right in his time? Maybe. But all I'm saying is that you want to separate yourself from your tools. You want to be a full stack developer, not a Rails developer. You are a computer programmer, not a Java programmer. Learn to distance yourself slightly from the tools you use. Familiarity and experience are important, but so is the ability to adapt and learn new things. You need to exercise your brain and learn new stuff while you still have decent neuroplasticity, before it decays in your later years. 

## Closing issues

I did more GitHub issues on the SSG repo. There are many aspects to GitHub and git, and I didn't learn them all at once. It's good to learn some things a little bit at a time. Then you give yourself some time to synthesize what you learned, as opposed to cramming and immediately moving on to the next topic.

## Preparing for my next app: solving a real-world problem

Learned more about microphones, earbuds, binaural audio, headphone jacks, splitters, 3.5mm connectors, etc. for an upcoming project. The thing is that my dad wants to get better hearing aids, but he also wants to save money. Hearing aids cost thousands of dollars. His audiologist gave him a quote for $4,000. That's absurd. So instead, I've decided that I'm going to develop some low-cost hearing aids instead. I already showed him a quick-and-dirty prototype of doing "live monitoring" where you have headphones in and they're outputting the audio from your computer's microphone. He noticed that it was louder and helped his hearing. However, he didn't like the latency and also didn't like hearing his own echo. But this was just the beginning. 

He ordered a pair of binaural earbuds, which are basically earbuds combined with microphones. I also got an audio splitter, because I want to try using it with a smartphone. I'm not 100% sure that my idea will work, in which case, I can always use it with a Raspberry Pi instead. 

## Real-time signal processing

There is a real-time signal processing library called OpenMHA. I think it's written in C, though I didn't look too much into it. If I can't go the phone route, I will look at what a German physicist posted on GitHub: a repo for software and hardware instructions for making your own DIY open source hearing aids. The hardware involved is kind of bulky and I'm not entirely sure how good the performance will be, but I'm going to at least try it. Computer science is, after all, about problem solving. Not computers.

I hope I will be able to make a cheap alternative to hearing aids for my dad, though there are some obstacles that might not be possible to overcome with this strategy, especially because he has relatively high requirements for what it will do. Being someone who does not have hearing impairments, it will be harder for me to develop it because I will have to constantly check in with my dad to have him test the progress I'm making on it. But this is a good example of human-computer interaction, a sub-field of CS involving testing with people to see what they want in tech, and see how easily they can use it.

The OpenMHA/Raspberry Pi solution is not the best, so I am hoping the splitter I ordered will be able to work with a phone instead, and then I can just write an Android app. My dad uses an iPhone but I have much more experience with Java than with Swift. Not only that, but newer iPhones don't have headphone jacks, and due to the nature of the way this project would work, bluetooth latency would make it worse, so wired earbuds are better. 

## Slow shipping

Speaking of online orders, I bought some 50 Ω resistor cables a while ago, and they still haven't shipped. They were super cheap, but the cost is the wait. It seems like a lot of cheap overseas orders have to wait until they have enough orders to fill an entire shipping container, because that spreads out the cost of shipping among lots of little things, making it cheaper per customer who wants to buy things from a different country. It sounds good, because of the lower costs, but it also means massive wait times for getting what you paid for. It's not a huge deal, but when you need something soon, it's a really bad idea to get overseas stuff with slow shipping. That being said, it's a niche item that isn't really easy to find in retail stores. And besides, as much as I like computer stores, I think they're starting to go the way of the dinosaur. Amazon has a lot of bad business practices, but the reason why they do so well is because of the convenience and selection of obscure things that are harder to find in normal stores.

## Protonmail and Google Voice

Today I made another protonmail account so that I can have a different github account. I prefer not to use my primary email addresses for github because people can see which emails you list. You have to list an email address that is associated with your github account in order for the contributions to count (I think), and I care about that, so I have to use a real email address.

I made the separate account so that I can experiment more with pull requests, remote branches, merge conflicts, code review, and things like that. This is preparing me to be better at group programming projects. At the last hackathon I attended, I was sharing files with someone using Dropbox, which was not very efficient. In the time since then, less than a year, I have learned so much, and it's funny to look back and see how little I knew about git and things like that. I feel much more competent now.

Protonmail requires either a donation or a phone number in order to confirm your account, and I use Google Voice, which is a VoIP service that lets you get another phone number. Then, you can get around sign-up limitations. Of course, it's good to support causes that are good, and protonmail is a good secure/private email provider.

## Randomly-generated passwords

I've been doing this for a while, but I only just now thought to write about. I use a password manager that lets you create randomly-generated keys. I use them when I make new accounts, such as when I made my new protonmail account. 

## Signal

On the topic of encrypted communications, Signal is my favorite messaging app. However, not many people use it. But I like how I can write test messages in Signal on my phone, and also look at them on my desktop or laptop too. It's a good model for security: secure by default, and security made simple. A lot of the reason why people don't implement extra security measures into their daily tech habits is because of the perceived barrier to entry, such as a learning curve or not having mobile support. But Signal is extremely user-friendly. Convenience is often the enemy of security, but Signal proves that these topics aren't mutually-exclusive.

## PGP and Keybase

I wasn't able to get around to it tonight, but I really want to get into email encryption and put public keys on Keybase. I also want to learn more about key security in general. I've come across a lot of login credentials and keys on GitHub, some for databases, some for APIs. I'm not sure if they are all valid, or if other people have already misused them, or if some of them are maybe public keys that can be shared publicly without any consequences. Overall, it's a topic I want to learn more about.

## Book idea

Considering how I've written so many mini-essays about programming, I am thinking about turning this website into a free e-book once I'm done. I will have to edit out all of the boring daily progress stuff, but I will still keep the essays about technology. It will definitely need a lot of editing, but it's still a good cause.

I think converting a blog into a book can be easier than writing a book straight-up because you only write a small amount every day, but you write consistently. By contrast, a book seems like such a daunting task, because it's so long and there's so much to do. But if you look at other programming-related books (that are more about commentary instead of technical details), such as *Hackers and Painters* or *The Cathedral and the Bazaar*, you'll see they largely consist of short, disconnected essays on topics all relating to the umbrella topic -- of tech/programming. 

I think I will call my book *A Neophyte's Musings on Open Source Development* and it will include essays and information about tech and my 100daysofcode journey with github. 

## One big weakness

There is one area I am sorely lacking in terms of open source: contributing to other people's projects. Right now, I am doing a lot of coding for my own apps and websites, but not really much of anything at all for other community-developed projects. It seems pretty easy to learn the commands and do the solo git stuff, but that's more about technical skills, whereas contributing to a group project seems more about teamwork and social skills, at least to some degree.

## Open source vs. selling your proprietary apps

A few days ago, I watched some Youtube videos by the Youtuber TechLead, who is a former Google tech lead who now does entrepreneurial development as well as videos reflecting on software development. In one of his videos, he mentioned how he doesn't really do open source, instead opting to keep things proprietary and charging money for them. There are a few issues with this though: for him, he probably didn't try to sell some of his first fully-fledged programs. I think my first ones won't be as good as ones I will be able to make in the future, so I would rather create resume-padders and a nice online portfolio instead of being some unknown software developer who tries to sell copies for money. I don't think people really pay much money for software these days -- at least not up-front. People want everything to be free, but then they're okay with in-app purchases. Or they want something to be free completely, at least in terms of money, and pay with their data or time (watching ads) instead.

Open source encourages me to have good coding practices, because other people can see what I'm writing. Not only that, but it allows for collaboration much more easily, impresses employers/recruiters, and also provides people with a public ledger that shows how often you develop personal projects (or other open source stuff). It's true that open source is generally harder to monetize than proprietary software, but there is still value in building up your portfolio. Getting your foot in the door to get a job as a software developer can be more important than making a few $1-10 app sales here and there. People aren't going to trust some random developer who nobody's ever heard of before. They would rather install a well-known proprietary app than an unknown one. Trust and reputation are a huge deal in software. By contrast, when you release your projects as open source, people don't need to rely on trust -- they can audit the source code themselves to verify that there isn't any malware in it. This is especially important in our day and age where plenty of things get hacked and cybercrime has turned from silly pranks into serious fraud to help criminals make a lot of money.

I might switch over to a proprietary model in the future, but I am still very much a fan of open source. I use a lot of open source projects, so it feels good to be able to write my own. 

## Transition in attitude from consumer to creator

I used to think of software as things to use. Things to download and install. Websites were these things that magically existed somewhere. But now, after studying IT and computer science, as well as teaching myself a lot of things on my own, I've come to see software as something you can create. It might sound obvious, but I think that a lot of modern technology, especially phones and tablets are more geared towards media consumption rather than creation. This is a tragedy, because past generations were growing up with computers that had programming manuals, and although my generation grew up with computers that didn't come with any compilers or IDEs built-in, you always had the option to download and install them. Coding on Android or iOS isn't really a thing. I think they will only be serious platforms when they have good support for development tools instead of social media, games, and single-purpose consumer-oriented apps.

Computers are empowering because they allow people to make great things. But cloud and mobile are, in many ways, reversing this idea. Don't get me wrong -- I'm all for learning cloud and mobile tech -- in order to develop for them -- but there are some serious drawbacks in treating the user as a consumer and a renter who never owns anything.

## LibreOffice spell checking

I used to only use VS code for my static site blog posts. I use other editors for different languages, but I like VS Code for web development and markdown. However, it doesn't have the ability to check spelling. Now what I've started to do is to copy the content of my writing into a LibreOffice document and do the old-fashioned spell check on it. I know how to write, it's just an issue of making typos that I don't immediately spot. macOS has phone-esque autocorrect, which can actually be extremely annoying at times. But Windows doesn't really do that. But now my future posts should have fewer mistakes, even when hastily-written.

## Sleep is foundational for productivity

If there's anything I've learned, it's that you can't function well without good sleep. Sleep will make learning, coding, working, and pretty much anything easier. Having less sleep to be awake for more hours is actually counterproductive, because your ability to get things done when you're tired is so much worse. Also, not every hour of the day is equal -- when you're energetic, you can get the most work accomplished. One hour of being very alert and energetic is worth a few hours of working while tired. 

Coffee is good, but not a replacement for sleep. And too much coffee can be bad. I like to drink coffee every single day in the morning, and sometimes again later in the day, but there are some downsides. That being said, I am the most productive after 1-2 cups of coffee. Some people debate whether coffee really makes you more energetic, or if you just feel more energetic compared to when you have a caffeine "crash" a few hours later. But I think that, even if it's not perfect, coffee is better than no coffee -- at least in moderation. 