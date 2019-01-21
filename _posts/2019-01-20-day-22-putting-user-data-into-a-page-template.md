---
layout: "post"
title: "Day 22: Putting User Data into a Page Template"
date:   2019-01-20 11:38:00 -0600
---

## Today's highlights

I learned more about programming, SQL, the singleton design pattern, Python features, etc. I also made a mockup of putting article content into the layout template for a website page.  

## Random programming learning

I learned about a wide variety of programming topics today, at least at an entry level. Many were new concepts for me, but a couple were just review. You not only have to learn new programming/CS concepts, but you need to make sure you don't forget old ones. I took calculus a while ago and I've already forgotten a lot of basic stuff like derivation and integration, along with a lot of rote memorization stuff like trig functions.

Here's some stuff I learned about today: mutexes (which reminds me of token ring networking), semaphores, Python global interpreter lock (GIL), neural networks, atomic database transactions vs. eventual consistency, overengineering code, deadlock, processes and threads, address spaces, message queues, interprocess communication, remote procedure calls, generic methods, regular expressions, antipatterns, Python classes/objects/instantiation, naming conventions, type casting, continue, break, pass, Python datetime module, dynamic typing, hash tables, programming interview tips, database sharding, distributed databases, vertical vs. horizontal scaling, and one type of design pattern (singleton).

## Design patterns

Just like with doing one SQL chapter per day, and some Python and git stuff, I am also going to learn one design pattern per day now.

Today, I learned about the singleton design pattern. A singleton class is a class that can only have a single instance for it. A way to implement the singleton design pattern in Java is as follows:
```Java
class SingletonClass {
    static SingletonClass singleObject = new SingletonClass();
    private SingletonClass() {
        // Private constructor
    }
    public static SingletonClass getInstance() {
        return singleObject;
    }

}
```

Then, in your driver class (Main or whatever), you'd do something like this in order to access the singleton:

```
SingletonClass object1 = SingletonClass.getInstance();
```

Even if you try to create a second SingletonClass object, you will really just have multiple references to the same instance of SingletonClass.

The next design pattern I will learn is the factory.

## Finally finished my first overly-simplified static HTML article test

My Static Site Generator app is intended to get article input from the user, which is then stored in JSON files -- some keep track of the contents of the articles (which have separate keys for the different pieces of content within a single article), and there is also some stuff related to some special stuff, like the site title, social media links, about page, etc. And there is also a more complicated thing for showing article previews that you can click on, limited to 5 articles per page. I will have to write a pagination algorithm at some point. 

Today, I have a simple version of the program with a skeleton structure for projects, some basic JSON stuff, and a couple incomplete command line arguments for opening an existing project or making a new one. The project supports multiple static sites in the same projects folder. After opening a project or making a new one, there will eventually be an initial setup script.

The project has features that are very similar to a content management system, except that this is all done client-side rather than server-side, and it uses JSON files instead of a database, and it also lacks any sort of login system. But this makes it simpler and reduces attack surface on a site because 

As you can clearly see, there are basically a lot of small things that go into making this bigger program. So because I can break up the big app into tiny pieces, I will build each piece at a time, and make sure it works well with the rest of what I have. I currently work on separate test and feature branches before merging back into master. I currently don't use the official unittest module, but I do manual testing of my own, and I will write tests in the future. But for today, I am doing a very simple mockup of what a bigger feature will be.

Development for this program has been slightly delayed because I am learning Python while I make this program. That's the entire point of this project: to learn a programming language through experience rather than just doing the simple and boring exercises in some books and online video courses, which will only teach you basic stuff and doesn't really involve version control or problem-solving or algorithm design. Or debugging, for that matter.

There are tons of extra things to finish in this app, but today I am at least starting to work on one portion of it.

Update: I didn't end up doing the full thing I described. I only made it get user input and then skip the pagination stuff and then just do find and replace and put the stuff into the placeholders in an output directory. But I was successful with this small thing.

The reason why I am able to succeed with relatively complex projects is by only doing a small thing at a time, and building on that small progress. You aren't going to make the entire app all in one go.

I was watching an interview question example video on Youtube, and the difference between me and the person who was doing the algorithm question is that they wrote a lot of code and hesitated to run it. I make tiny changes, build/run, and change it all the time. I commit and branch code very often. Don't do too much all at once. Take many small steps instead of only a couple big ones. If you get a compiler error or even a runtime problem, or even a logic error that is harder to diagnose, you will know what is probably the culprit because you only changed a small amount of things. This is better than doing lots of changes, encountering an error, and then having lots of different possibilities for what's the issue. 

The more progress I make on things like this, the more confident I become in my programming ability. 

That being said, I had a list of like a dozen apps I wanted to make, and this is just one of them. Yet here it is, almost a quarter of the way through, and all I made so far was EZcrypt and I'm not even done with my second project yet (Static Site Generator). I thought I'd have like 5 projects done by now. I guess not.

But then again, I'm learning things I didn't expect to learn. And I'm doing more than making programs. I also learned Python, more advanced git and GitHub stuff, Jekyll, made a website (I  guess that might count as a third project so far), started to learn design patterns, and I'm learning SQL now too. So what I've really learned is that things will take longer than you think they will, so you can't just say "well I'll finish it all in a couple days" because the problems will be more complicated than you might think. When I say problems, I don't just mean bugs in code. I mean having to think hard about how to break up a program, or how to design algorithms. The pagination algorithm I have to develop isn't something as simple as a sorting algorithm. I have to come up with it on my own. And that's not the only thing I have to do. But at least I've created all the separate menus and project stub files (unfinished markers of what I will make in the future -- I do this for so many projects). 

There are really 4 main parts to my programming: 
1. Learning -- might involve google, official documentation, Wikipedia, Stack Overflow, books, Reddit, Youtube tutorials, and/or Udemy. Sometimes, I will get distracted and start learning random programming concepts that are interesting or useful, but not completely related to what I was first searching for. I've heard people call this "going down the rabbit hole" when you're researching a topic. 
2. Designing/figuring out what to do -- a lot of this just involves thinking. I'm not usually coding during this time. Sometimes I make diagrams or pictures, or just write text notes. I will often make mockups that are not the end product. Also, keep in mind that a design might not be all-inclusive. I might have a design for a small portion of the program. Sometimes, I look to inspiration from other people. Other times, I actually want to do it all on my own. It can help me feel smarter and more accomplished when I do it on my own. I don't like cargo cult programming. Some people say you really shouldn't reinvent the wheel or solve problems that have already been solved, and I agree to some extent and even say things like that. But sometimes, I see a problem as an opportunity for learning and growth. If I solve it myself, I won't have to rely on google or something in the future. I am proud that I am designing a lot of aspects of Static Site Generator on my own, even if perhaps there is a better way to do some things. But I am also learning stuff about MVC architecture and implementing small pieces here and there for it.
3. Actually implementing the design I thought about. This can sometimes involve sub-steps, where I make a dummy program or dummy function/module before doing the real deal. Then, if the mock implementation works, I try to do it for real. This step does not involve writing the entire program from start to finish. It is merely the implementation for a single feature or bugfix.
4. Fixing bugs (if any). My least favorite part of developing software, but it's necessary. Of course, I'd prefer that my initial implementation attempts in the previous step work out, but that is not always the case. Sometimes, there are issues with unit testing -- issues with the new feature itself. Other times, you encounter issues with regression testing. The individual feature you added is fine in complete isolation, but when you add it to the main project, it doesn't play nicely with the existing code you have. That's not good. Sometimes you get syntax errors, which are easy. Most of the time, you get runtime errors, which at least give you some sort of message. You can handle them with exceptions and display or log stuff when needed. Then you can either read documentation and try to figure it out yourself, or google the exception or other error to see what other people encountered and what they did to try and fix it. The hardest of all are logic errors, because it's not a syntax or compile-time issue, not something that raises an exception, and it's only an issue because the code doesn't do what you want it to, but it's not actually wrong in terms of doing what the programming language is allowed to do. Maybe an image size is wrong, or perhaps your data is not being acted on correctly. These more complicated issues can be very time-consuming and frustrating. I often use print statements to show the status of things during runtime, but I've also used debuggers, and I will try to use debuggers more in the future. I get the basic ideas of breakpoints, step, step into, continue, etc. But old habits die hard. I am actively working on it though. Also, with my new knowledge of unittest and the logger modules in Python, I will be better-equipped to figure out what happened or what went wrong -- in a much more advanced way than my older print() strategy.

## SQL: Advanced data filtering with the use of multiple WHERE clauses

I didn't end up getting to this after all today. I will do it on January 21st.

## The way I read books has changed

I used to read textbooks and try to make sense of things only using the explanations in the books. By the way, I'm referring to tech-centric self-learning books, or textbooks. Not novels. But anyway, if there is a sub-heading in a chapter that I don't understand, I will just look it up on Youtube or even Udemy. But usually I look on Youtube for very specific topics (examples: 'Python logger module', or 'Java singleton design pattern'), whereas Udemy is better for more general stuff that can be structured as an entire course (Python, GitHub, Java).

I've found that this is a much easier way for me to learn. Why? Perhaps a textbook has a good layout. It technically covers all the topics it needs to. The most useful thing about a textbook is how it *enumerates* useful topics for you, and puts them in an order that makes sense. But programming tutorials on Youtube (or sometimes other sources) are almost like mini-lectures, because they show the topic and how you use it. Reading might be good for other fields, and I do like to read books. I'm not the kind of person who only watches movies or TV (in fact, I pretty much never do). But it's hard to use your imagination to envision what it is that the author is describing, especially for technical books where the person writing it has a background in computer science or IT rather than English. Tech books are often good in terms of their technical content, but not that great in terms of writing ability. 

Many people who write or contribute to tech-oriented books know what they're talking about, but they don't always know how to help other people understand it. The other thing is that, for really new tech topics, sometimes there will be a brand new e-book that's out, but it was put together in a kind of rushed way, because time-to-market is important for really new tech. Old-school book publishing takes too long for programming fads. So while the topics listed and code examples might be correct, it can be hard to get through. These kinds of books are generally extremely dense and it takes many times more effort to get through a programming-related book than a novel you can read cover to cover. So breaking it up with visual learning examples, which are often explained in a simpler and better way, are a good complement -- but not a substitute -- for books and courses. 

The other issue is that of specialization. Sometimes, the best Youtube tutorial will be made by someone who has only made a few videos. They're not a "Youtuber" per se, not someone who makes videos at a regular schedule. These people are usually very genuine and are often experts on very niche programming topics. They upload the video about it because they are very good at that particular thing. Not always true, but it's the case some of the time. On the other hand, a textbook covers a massive range of subjects, so there might be parts even the author isn't great at. It's the same with professors teaching a class. There was a C++ class I took, which was generally okay, but when we covered file IO, I asked about appending to a file rather than overwriting it, and the professor didn't know, because C++ wasn't their favorite language, so they were more familiar with other ones instead. But I could just look it up online. 