---
layout: "post"
title: "Day 18: Static Site Generator"
date:   2019-01-16 9:13:12 -0600
---

## We meet again

Hello and welcome to another blog post featuring my progress with programming and quasi-Feynman-esque learning, as well as assorted vignettes and scatterbrain musings on a multitude of tangentially-related tech topics!

## I hope today will be even a fraction as productive as yesterday

I got so much done yesterday. I think a combination of coffee and genuine interest in the subject really helps.

I was also, for the most part, distraction-free. I left my phone far away, on silent and in do not disturb mode, ignoring social media except for Youtube programming tutorials. 

I was really able to stay in the zone, as I've described previously, by warming up and then sticking with my work for most of the day. Minutes of interruptions can ruin hours of productivity.

That being said, taking short breaks every now and then can help. I like to listen to music or do light reading for my breaks. But social media, videos, etc. can wreck your progress. Part of being productive isn't just about what you're doing, but it's also about what you're *not* doing. You're not putting distractions in your head. If you do, you will be thinking about funny cat videos or your friend's latest tweet or selfie on Instagram rather than the code you're working on. 

## JSON validation

[Here](https://jsonlint.com/) is a cool JSON validation tool I came across. It's really neat, especially if you're a beginner!

## Plans for today

I plan on finishing my static site generator (the command line version of it), and then migrating my site (alans100daysofcode.com) from Jekyll over to my own tool, which I will call SSG for now. I'm really not good at naming things, but oh well. 

Now, I might encounter time-consuming issues with the above goals, and they are my top priority. But if I am able to finish those things with time to spare, here are some other things I want to do:

**UPDATE:** as it turns out, the static site generator still has a lot more progress to go before it's really finished. I havevn't even managed to finish the command line version of it, and I didn't even start on the GUI stuff yet. It might take me a few more days to finish even the command line version. Then I want to learn tkinter and make a GUI for it. But maybe the GUI version can be a separate python script, so that people can still use the command line version if they prefer. Some people prefer cli to GUI. And a CLI program can be used with another program to programmatically do something, like you make an app that uses the command line version to auto update a site, or something like that.

## Goal for a future day

- Rewrite my resume in LaTeX. Same basic information and layout, just in TeX instead. It's been a while since I used it. I used it a lot for writing math formulas when I took some math classes in the past, but I've probably forgotten more than a thing or two in the months I haven't been using it. Not onlt that, but LaTeX math is just a small subsection of what you can do in LaTeX, and I have yet to use it for anything other than equations/formulas.
- Convert Saint Louis Software to SSG, at least for the blog section. I might have to slightly customize the SSG project specifically for this site, because it's a little different than the original use-case for SSG. The rest of the pages on the site do not have SSG stuff, nor will SSG delete them or otherwise mess with them. This can be a project for another day though.


## Wordpress API coolness

I just learned that my Wordpress websites have an API built-in, thanks to the CMS. I didn't need to lift a finger, it's already there. A future project I might want to do is to make an Android app that makes use of the Wordpress API for one of the websites I've made thus far, in order to fetch data from it. Or perhaps my planned Support Network STL app can simply fetch JSON data from a Wordpress API on a shared server of mine. I have some extra capacity so it wouldn't be too hard to set up just another Wordpress add-on domain. The power of a mobile app is better performance and a more native experience, but using the JSON/REST API means you can just get data from your web app instead of doing everything differently from scratch. In fact, you could have a single API on your website and then separate Android and iOS apps, written in Java and Swift respectively, that do things differently, but still interact with the API in some way anyway.

Here is an example of a website I've made, and how it has an API:
[https://smartfinancialresearch.com/wp-json/](https://smartfinancialresearch.com/wp-json/)


## The medium is the message

A decade ago, I might've written this stuff as a book rather blogging or using Twitter. But times have changed. People point out JK Rowling as a successful author, but times are different now. Would she have been as successful if she wrote and published her books in 2019? Absolutely not! I love to read, but you have to understand that people do way more than just read books now. Netflix and social media take up a lot of people's time, for better or for worse. The idea of the long-form blog is also kind of dying, but it's still more relevant than print media. e-books are okay, but they're still books. 

## The shelf life of tech skills

What I'm saying is you have to be aware of what's going on around you rather than just what you yourself want. That's not just about being an author vs. being a Youtuber, blogger, or podcaster, but this same idea applies to programming as well. Perhaps 20 years ago, you would've been a C++ programmer. 10 years ago, you'd be fine only learning PHP for web development. Today? Doesn't make sense to ignore full stack web development with modern languages and platforms like Django or Node. You don't get to pick and choose the circumstances of the world during your lifetime. You don't get to choose when you were born. And you can't afford to play the "I was born in the wrong generation" card either. A very important aspect of programming is keeping up with everyone else.

10 years from now, my suggestions about programming languages and tools will be obsolete, because there will be new things. But by then, I'll have updated my opinions and recommendations anyway because of taking in new information and adapting over time. Some things are slow-moving, but a lot of tech really does pop up quickly, and you need to strike when the iron is hot sometimes -- before consensus agreement on when something is worth doing. So I encourage people to explore new things, play around with stuff, even if you're not going to dedicate all your time to it. Do new things. Don't ever stop learning new tools and languages and ways of thinking.

Windows 10 desktops might become the new Commodore Amigas. Android or iOS might become the new Symbian. Instagram might become the new MySpace. Java might become the new COBOL. And that's perfectly fine, just as long as you've switched to something newer before it completely went under. Learn to recognize when something is declining. Cut your losses instead of being wedded to your previous skills. 

It's all too easy to look at the present and wrongly think that things will be like this forever. As if tech giants haven't come and gone in the past. Look at the history of Silicon Valley. Huge players crash and burn both quickly and irrevocably. It has happened, it still happens, and it will continue to happen. 

I used to memorize old and oudated computer knowledge when I was studying for the CompTIA A+ exam, which I never ended up paying to take the exam for. I did learn a lot about computers, but a lot of the specific facts they wanted you to memorized were useless. 

A lot of my older tech skills are like that. Cisco IOS isn't the hottest skill to have either these days, but I certainly agonized over it when I was in community college. I wouldn't be afraid to eventually let go of these old skills and focus on what's more immediate and important. Things that are here today and will continue to be here tomorrow. Staying power. 

## Avoid the trap of buzzword-driven development

While I did just ramble on about how outdated tech skills should be given up in favor of more relevant and hirable skills for things people currently use (which is a never-ending process, by the way), don't be the kind of developer who buys too much into short-lived fads based around cool-sounding buzzwords. It's good to know modern things, but don't follow it overzealously. 

RESTful APIs are cool, but don't put them everywhere just because they sound cool and new. Machine learning and neural networks are also cool, but shoehorning them into a project where they don't below -- just so you can have more buzzwords for marketing -- doesn't make much sense. Cloud is good, but not everything should be in public, shared hypervisors. Hyperconverged infrastructure is a good concept, but don't obsess over it to the point of ignoring everything else. Containers and orchestration are cool concepts too, but sometimes you need to admit that a project really doesn't need it. Use the right tool for the right job. Don't try to cram all the newest buzzwords into a single project just becaues you can. Use things in moderation and where appropriate.

This might sound hypocritical, considering my previous blog post mentioning how I will sometimes add an unnecessary feature into a personal project just so that I can learn it. But that's not what I'm referring to here. Sometimes you need to make semi-useless personal projects just to get experience with somethnig. But that kind of thing shouldn't happen for meaningful work-related projects, unless it'll never make it to production and you're just treating it as job training.

## Other stuff I did today

Fixed some issues in random repos, deleted and merged some useless repos (or ones with separate projects that can all be lumped into the same project for a single repo), opened new issues on projects so I won't forget what needs to change for them, archived some repos, etc. I basically cleaned up my GitHub profile so that you are more likely to see my good repos instead of just misc junk learning stuff. I have a lot of cool apps and websites on my GitHub account, but also some less-impressive educational repos. 

## Take a look at my best software

My top 6 pinned repos are just ones I want to work on (so they're not out of sight, out of mind), not my most impressive ones. I'd say my best repos are [Saint Louis Software](https://github.com/0x416c616e/saintlouissoftware), [EZcrypt](https://github.com/0x416c616e/ezcrypt), [FileHider](https://github.com/0x416c616e/filehider), [Static Site Generator](https://github.com/0x416c616e/staticsitegenerator), [2D RPG Game Engine](https://github.com/0x416c616e/2drpggamengine), [Road Warrior](https://github.com/0x416c616e/roadwarrior, and [amp](https://github.com/0x416c616e/amp).

