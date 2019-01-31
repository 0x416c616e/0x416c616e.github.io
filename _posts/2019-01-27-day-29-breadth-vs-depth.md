---
layout: "post"
title: "Day 29: Breadth vs. depth"
date:   2019-01-27 1:05:38 -0600
---

## More SSG progress

Today I continued to work on my static site generator program.

## Generalist or specialist

I have noticed that, sometimes, my daily #100daysofcode entries might look a little more barren when I put more time into a single topic, like doing a lot of development on my SSG app (which is taking me longer than I thought it would).

## Making the wrong bets on tech

## Using what's "best" vs. using what's popular

## Fly-by-night JavaScript frameworks

## The myth of future-proofing

Nothing is future-proof. Technology comes and goes.

## Fear of missing out and information overload

On social media, some people will continue to waste time -- checking notifications and messages, refreshing pages, logging back into things, and opening multiple browser tabs -- all because they fear missing out on something important. But 

## My social media strategy

Some people will tweet or post about anything and everything. Some people might get the wrong idea and think that I'm all-tech-all-the-time, but in reality, it's just because I choose to exclude certain topics from my social media presence. There's more to my life than technology and software development, but I don't really feel like sharing much about it. Your social media and online reputation aren't just about what you choose to post -- it's also defined by what you choose not to post. 

Some people post about controversial or personal things. I would rather keep it professional. It's good to not post too much information, and also good to not post anything upsetting/offensive. What I post is rather milquetoast, but this is intentional.

My strategy is simple: post about things related to your field of education/work, maybe occasionally some hobby-related stuff (I've posted about my experiences with travel), and don't post too much else. I have no problem with writing about software development, security, tech trends, events where I meet other developers, and things like that. That's because I consider these to be "safe" topics. They don't make me look bad and they're not going to upset people. 

Staying positive is another important aspect of my social media presence. I try to frame things in a positive way. Negativity just makes you look bad. Life isn't always sunshine and roses, but you are doing yourself a disservice if you post too much negativity.

In general, I'd say less is more when it comes to posting on social media. It's not just about building rapport or coming across a certain way, but overdisclosure can lead to problems such as phishing or identity theft if you divulge too much personal information. As someone who is interested in information security, I can't let myself become the target of a scam.

## How secure are your third party dependencies?

On the topic of oversharing and getting phished/scammed, I've always thought about issues of supply chain security. Sure, I use a lot of apps. Sure, I trust a lot of developers who make open source tools. But when you write a program with external libraries/packages, or install browser add-ons, you are trusting not only that the developer is non-malicious, but also that they themselves will have good security hygiene so that they won't get hacked and won't have their developer-related accounts compromised. If they are lax about security, people who take control of their GitHub or app store accounts could release a malicious software update that would give people ransomware, key loggers, RATs, or really anything they want. This is a complicated issue, because some people really need features over security, so they are willing to take slight risks here and there.

The person who developed an app that runs on your device... maybe they got their computer from craigslist, and they have no way of knowing if it has a stealthy UEFI rootkit or MBR rootkit. Maybe one day, they accidentally visited a typo of a domain instead of the real thing, and maybe they had JavaScript enabled (meaning that there is a slim but nonzero chance they got malware from the site). Maybe they buy cheap flash drives online, which could potentially have malicious payloads on them, for things like BadUSB, which can do keyboard emulation to execute commands and wget a remote payload. 

Maybe the developer of an app you use codes in a library or coffee shop, and when they leave their laptop to use the restroom, they don't lock their computer. Maybe someone looks at their keyboard when they type their password. Maybe they write their passwords on sticky notes that can be seen from outside their office window. Maybe they did a livestream and accidentally streamed some private keys. Maybe they accidentally set up their .gitignore file wrong and committed some config files with database credentials in them.

Maybe the person who made an app or website you use doesn't install software updates very often. Perhaps they can't be bothered to disable word macros. Maybe they concentrate more on development and not on software. Maybe one of their projects had a security dependency, but if they updated to the latest version, it broke features, so they rolled back to a previous version. What if they pirate commercial software on their development computer? What if their GitHub password is the same password for their other accounts, and what if they get compromised? Password reuse can lead to account theft. 

What if a developer, whose apps are used by millions of people, uses a cloud-based password manager, and that password manager gets compromised? What if they work remotely, but don't install updates on their router or modem (evne when there are CVEs)? What if they click through certificate warning messages in their browser? 

Maybe someone logs into a public computer and forgets to log out. Maybe they use public wifi at a coffee shop and it turns out that it wasn't trustworthy. Maybe they used a VPN that actually logged everything they did and performed traffic sniffing or MITM attacks. 

What I'm trying to say is that we all rely on a delicate network of software, often barely-functioning, filled with bugs, written by individuals in their pajamas, who are not security experts, and sometimes even get lazy about the security concepts they are aware of. 

Because of this precarious situation, compromises can happen.

So why is this important? Threat modeling and assessing your attack surface. Your attack surface is all of the things you have that can potentially be hacked. Well, the more apps/websites/tools/plugins you use, the more ways you can be hacked. The irony of using more security tools is that the security tools themselves can be compromised, so the more you use, the more likely you are to get breached. 

So what can you do? Well, one simple idea I have is that it's simply easier to not using something than it is to figure out how to secure it. How do you keep Wordpress secure forever? By not using it at all in the first place. If you can get away with not using it, then using fewer things can mean you will be more secure, assuming you don't cut out really important SIEM/IDS/anti-malware stuff. There are some things everyone really should use, and that might sound like it contradicts my point. But I'm saying you should cut down on the number of apps and whatnot that you use, but only within reason, not compromising very important things. But reducing your attack surface is a very important security strategy. 

One way you can reduce the attack surface of your website is to use Static Site Generator instead of a CMS such as Wordpress. And not only that, but it's good to audit the source code too. SSG does not have auto-update functionality built into the program, unless you are using it with git, and then do a ```git pull``` or something. But if you just download the files and use it that way, it will be secure. Then, you can audit the source if you ever want to download a more recent version. If my GitHub account ever got compromised, you could still look at the source code to see if anything is suspicious. 

I made SSG for a few reasons: to make my resume and website look better, to learn more about Python, to make a tool I'd actually use, and to have a secure alternative to Wordpress. 

The reason why a CMS is insecure is because it has all sorts of potentially-hackable software running on your internet-facing server. By contrast, static site generator only runs the software client-side, and generates static HTML that you can upload to any server running a very minimal server stack. 

By not putting something on the internet, it's not remotely hackable. That's the benefit of SSG.

Of course, it's not a magic bullet for security, because you still need to have an underlying server to serve the pages to people, even if they are just static HTML. So you would need to run a Linux server with Apache, or something like that. Then you'd need to have some sort of remote administration, like ssh or maybe even cPanel. So those are all the things on your server that can potentially be hacked, because your server it still remotely-accessible. But just installing updates in Linux and Apache or nginx is much easier than securing all of that stuff on top of a CMS, WP plugins, misconfigurations, etc.

I did quite a few pentesting VM labs through a website/online course called Virtual Hacking Labs, and if a site was running Wordpress, it'd make me happy, because I knew I'd either find a CVE for remote code execution, or somehow get either a local account or remote file inclusion that would allow me to upload a web shell (if you can change the PHP theme, you can upload a web shell). From the web shell, you can establish a revere shell. Then, with the web shell, you can usually get an account like apache. 