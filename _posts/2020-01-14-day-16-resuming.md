---
layout: "post"
title: "Day 15: Resuming"
date:   2019-01-14 3:42:36 -0600
---

# Back after some interruptions

I was sick for a little while, so I didn't really do much coding then. I won't count those days towards the 100 days.

# More Python Crash Course

Today, I finished chapter 4, and also did chapters 5-7. Also updated my log and website here. A couple days of being out of the loop is bad, so I'm getting back into the swing of things.

One issue I have with a lot of Python learning resources I'm looking up is that they assume you've never programmed before, so they spend way too much time going over basic concepts. It's really boring. I wish there were more programming books aimed at people that already know a couple programming languages and just want a quick way to get up to speed with the language without going over the basics of programming and OOP paradigm stuff that I've already learned. 

I have also decided that I will be writing my own ticketing system instead of using osTicket. It will be a good first full stack web development project for Python/Django/SQLite. 

## Static site generator

I am still working on the static site generator project. Not only am I learning more about Python still, but I am also doing more mockups and planning about what the program will be like.

I am also starting on a command line version of the program rather than starting out with the GUI version. I will add the GUI stuff later.

### First part of the static site generator: page templates

Before getting into how the program can take user input or user-specified files to generate pages and articles based on what they want, I first had to create some barebones templates for pages. They will have the user's content added in later. The first version will be command line (and also rely on either text files or JSON files), and future versions will have a GUI.

![static generator screenshot 1](/assets/static_generator_screenshot1.PNG)

It's actually based on an old version of a different website I was making. I wanted to turn it into a CMS for a site, but then I realized that a CMS is pretty complicated, so I decided to make a static site, and that's what I eventually turned into [Saint Louis Software's site](https://saintlouissoftware.com). However, this is an older and simple version of that. It is only intended for single-user, single-category blogs, and with a single "about" page. I've made a lot of websites with Wordpress, and this is like a very simple blog with only one category and not many extra static pages. I could potentially add those kinds of extra features in the future (the ability to add more categories or pages), but for the time being I'm just making it simple so that the progress on the project can go faster. Then, once I have a working simple project, I can add more to it. But not until I get it working right first. 

![static generator screenshot 2](/assets/static_generator_screenshot2.PNG)

For now, here are some screenshots of what the basic site looks like. There isn't much to it just yet, but this makes it easier to figure out how I want to make it. For the time being, I have a simple idea of copying template files, and then finding and replacing text based on the user's files. 

![static generator screenshot 3](/assets/static_generator_screenshot3.PNG)

Pagination might be tricky, and would require deleting some things on the main template page if the number of articles isn't disible by 5. Like if you have 8 articles, you would have one page with 5 articles and then a second page with 3, meaning you'd have to delete 2 of the extra article placeholders.

![static generator screenshot 4](/assets/static_generator_screenshot4.PNG)

I will also make it so that it re-generates the pages every time because the order of articles changes. If you have 5 articles, that's enough for one page. I arbitrarily decided on 5 articles per page. So if you add a new article, that's a 6th article, and then the 2nd page has the 1st article, and everything else essentially gets pushed down 1 and the new article is the 5th (top) article on page 1 (index.html). This issue of moving pages around and deleting and re-doing things, and copying stuff from templates and all, will be a little confusing at first, but I know I can do it. 

![static generator screenshot 5](/assets/static_generator_screenshot5.PNG)

I am eventually going to migrate this site over to my static site generator once it's in more of a working state. That should motivate me to work on it and improve it. 