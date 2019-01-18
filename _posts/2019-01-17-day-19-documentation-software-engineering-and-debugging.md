---
layout: "post"
title: "Day 19: Documentation Software Engineering, and Debugging"
date:   2019-01-17 23:34:45 -0600
---

## Don't just write code, write documentation too!

What's immediately obvious to you, as the developer, will not be immediately obvious to the people tryinh to use it. I recently wrote a TON of documentation explainnig what my static site generator is, what it can (or I guess *will*) do, how you can use it, etc.

I painstakingly explained each of the directories and files, and the general methodology for using it and what it does when you use it. That's also in addition to the more beginner-friendly plain English explanations that basically just say that you can use it to make websites, don't have to code in order to use it, and you need to have Python installed on your computer in order for it to run.

I will eventually have to separate out the more in-depth technical documentation from the friendlier easy stuff, but for now, I put it all in the readme.md file. Check out the SSG repo [here](https://github.com/0x416c616e/staticsitegenerator).

If your program has bad documentation and is difficult to install or use, people will just use a similar app that is easier. People take the path of least resistance. Everyone is busy. Everyone has things to do. Nobody wants to spend unnecessary time learning a complicated thing when they can just use something simpler instead. 

## Software engineering

Writing documentation really forced me to flesh out my kind of vague ideas about the app. I made a sample project folder called example, within the projects subdirectory, and you can see that 


## Adding dependency and usage information in READMEs

Today, I added basic info and instructions for using my software. For example, I listed the specific versions of Java to use my old Java programs with, and mentioned how to run them using ```java -jar filename.jar```.

## ConEmu

I switched from Git Bash to ConEmu today. At first, I researched something called cmder, which was recommended by some people online. however, it was glitchy for me, because I use vim in a terminal, even though I also use IDEs. It seemed to work fine for most things, but vim didn't work right, so I switched to ConEmu instead, which works just fine for everything I need to do. I also chose to use Git Bash as my shell for ConEmu.

The main 2 advantages of ConEmu over regular Git Bash or PowerShell is the customization ability and that you can split the screen into multiple terminals, kind of like tmux or screen, but easier to use, and with the ability to the use the mouse to resize things.

## Agile development

While tools are good and all, I have been trying to learn more about agile and devops, which says that individuals and interactions are more important than processes and tools, among other things. It also says working software is better than comprehensive documentation. That's great and all, but at the same time, that doesn't mean I shouldn't write documentation, or that I shouldn't learn new tools. Yes, ultimately time and deadlines are more important than features, and agile sprints are good in that regard. Some of it seems like vague and nebulous fluff, but I am trying to learn it anyway. A lot of places incorporate pseudo-agile into their development workflow, but somehow a lot of agile reminds me of the "no true Scotsman" argument. If you're not doing XYZ, you're not doing real agile! Weird gatekeeping. But at the end of the day, as long as you have a more time- and -people-oriented alternative to waterfall, it can't be that bad, right? Trello, kanban, sprints, devops, trying to bridge the gaps between IT and development, and even security (DevSecOps). It sounds good. Testing, continuous integration, automation, build servers, processes, essential features vs. wishlist features, etc.

I read an Audible audiobook version of The Phoenix Project a while ago, and it was interesting. Agile seems useful, but also overhyped in some ways. I will learn and observe things without necessarily having to follow everything to the letter. I do like the time-oriented nature, and the idea that it's okay to adapt based on sprints and whatnot instead of only having an initial plan and then having to stick to it the entire time.

But as I wrote about previously, don't fall for buzzword-driven development. Agile is great and all, but even if your company has cool things like RESTful APIs, scalable microservices architecture, devops, agile, etc... at the end of the day, if your software isn't good, then none of these hyped up labels really matter. As Linus Torvalds once said, "Talk is cheap. Show me the code."

## No one is an island

At the end of the day, soft skills are probably more important than technical skills. Software is made by teams of people, not individuals. The ability to effectively communicate and work collaboratively is hugely important for software development. So all the coding in the world won't do you any good if you can't work well in a team. That's why open source projects and social media are good practice for beginners -- online open source projects on GitHub allow people to collaborate on projects together, even with people in different areas, with different schedules and skills. 

Technology is ultimately about people. People make tech. People use tech. It's not all about bits and bytes, CPU registers and data structures. To think of technology as some cold, logical, mechanical concept is wrong, because people are involved in every step of developing software and hardware. 

## Schema validation/enforcement

Because my static site generator deals with JSON a lot, I figured it would be good to create schemas and validate files to make sure they have the right keys and values. I got this idea because of a web development and databases class I took at SIUE a while ago that went over MongoDB, Mongoose, and schemas. I don't really remember all of it now, but I do remember that you can make sure data is structured properly.

There is a python JSON schema validation package called jsonschema. It can be installed with ```pip install jsonschema```. I had to add it to my list of dependencies for the project.

For regular json usage in Python, you'd use ```import json```, but that's just for regular usage, not validation.

In order to use jsonschema after installing it, you have to add this to your project:



Here is an example JSON object that you might want to validate:



```
{
    "name": "PyCon Sweden",
    "location": [
        59.320393,
        18.0670063
    ]
}
```

And here is the schema for validating it:

```
{
    "type": "object",
    "properties": {
        "name": {"type": "string"},
        "location": {
            "type": "array",
            "description": ""
        }
    }
}
```

I sort of understand it, but it can be tedious to write manually. Instead, being the lazy programmer that I am, I took the path of least resistance and googled it, and came across a site that can automatically generate a schema based on your schema input. You want to provide valid JSON and make sure that's really what you want. Then it will generate a schema you can store as a validator object in python jsonschema. 

Is it really lazy, or perhaps efficient? Maybe a bit of both. Rather than sovling the entire problem by myself, I looked for other people's solutions. I do that sometimes. I know cargo cult programming is bad, so I don't engage in that. I try to avoid copying and pasting from Stack Overflow, instead using it more as a way to be steered in the right direction, perhaps looking at API documentation or something like that. 

## Modularity

Instead of having everything inside of a single main function, I broke a lot of my generator.py stuff into separate functions, though I have had some issues. It's been a rocky day as far as development goes. I am making progress on the program but there have been some frustrating issues. 

## Debugging is the bane of my existence

I was working on my generator.py program and had some scoping issues, so I then applied some bad code on top of it and it made it even more confusing and difficult to solve. 

I tried adding both command line switches and a while loop numbered input() list for using the program for either opening an existing project or creating a new one. Because of the fact that there were two different ways to either make a new project or open an existing one, there had to be checks to make sure you wouldn't end up doing the same thing twice. I had issues with variable scope for a string that was 

Programming is empowering and makes you feel like the smartest person in the world when things go as planned. But when there's a difficult-to-diagnose issue, it really gets you down. But on the bright side, the only way to get better with debugging and refactoring is to get more experience with it. 

## Scaling back feature ideas

I was originally planning on doing a TON of stuff for this project, but today's debugging was really draining on me, and it was for such a small part of the overall project too, so if I want to go with as many feature ideas as I originally planned, it could take me WEEKS of programming and debugging everything to get it all right. I don't want to spend that long finishing this project, since a lot of it is already done. I just want to get a fully-functional static site generator, even if it doesn't have dozens of extra bells and whistles. 

Yesterday, I was really excited and happy about this project, so I created way too many issues on GitHub for suggesting new features to make. Now, I closed a lot of those issues so that I won't have tons of technical debt.

## Current status of my static site generator program

- Frontend web templates are finished (HTML/CSS/JS) for all the different kinds of pages
- Project structure/design is finished -- I have finished the basic *design*, but I still haven't finished all the *implementation*
- Command line arguments for opening or creating a new project are finished
- Numbered options menus are mostly finished, at least for the display part, though maybe not for functionality
- JSON stuff has been started

Stuff left to do:
- Design pagination algorithm -- use test thing first before the real deal
- Finish fleshing out JSON file structures
- Finish JSON schema and validation
- Practice writing JSON to the practice template file 
- Delete unnecessary test/practice files
- Consider creating a regeneration module instead of putting it in generator.py because it's getting pretty big and messy, modularity is better
- Finish functionality for making, deleting, and editing files
- Add functionality to all menus, submenus, and all their final items
- Use regex to valid project names and also check if project folders are there or not
- Make it so that creating a new project copies all the project template files (the formerly example project directory)
- Lots of other stuff!
- Figure out how to add jsonschema files to the project (I don't want to rely on the user independently installing it)
- Learning more about os.path.*, such as and os.path.join() to make OS-independent paths to different files and directories. macOS and Linux are pretty similar about paths, but Windows is different. That can complicate things. I try to use relative paths for things, but I might need to do os module stuff just to be on the safe side to not break multi-platform functionality.
- Probably forgetting some other things

You think something like "take user input, store it into JSON, then combine with a template to make static pages" sounds simple, but then you look into all the little details, and you realize your app idea takes much longer than you had initially anticipated.

Will I still add a GUI to this program? I'm not sure, it might be difficult to replace the current text-based stuff with a graphical program. I would have to convert a lot of things over. It would really be a different program at that point. Maybe I can make a separate repository for it (graphical static site generator?).

My next project after this will not be the full stack IT ticketing system. It will be the simple text-based game I mentioned. The reason why I want to do that is because I want to have a project that will make it easy to implement classes, interfaces, and a lot of other Python programmnig language features I haven't used in this project. This project used a lot of user input, input validation, file IO, functions, and things like that. But there is much more to a programming language than that.