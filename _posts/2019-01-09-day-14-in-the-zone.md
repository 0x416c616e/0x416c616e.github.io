---
layout: "post"
title: "Day 14: In The Zone"
date:   2019-01-09 8:23:04 -0600
---

## Distractions destroy productivity

Today I'd like to talk about something I've noticed about productivity. It's not specific to today, but in general, the concept of "being in the zone" can really affect how much work you can accomplish. 

Little distractions like phone notifications, meetings, calls, and so on can really take your mind out of your work.

It can take a while to get in the zone, and when you're there, you don't want to leave. When you first get up in the morning, shower, shave, get dressed, and start to code, at first you're not as productive as you can be. You're not only just waking up, maybe still digesting food and figuring out plans for the day, but you might have also just had a conversation with someone, or thought about your commute. 

It takes a while to be fully alert, clear your mind of all distractions, not be hungry or have any other physical needs, and then be left alone to do your work. It takes a significant amount of time to get in the zone, but it doesn't take much at all to take you out of it. Someone asking you for help for something, getting lunch, going to the restroom... there are so many things that can take your mind away from your work. A "15 minute" meeting might actually cost you over an hour of productivity because of the lingering thoughts in your head that make you code more slowly. 

When you finally get in the zone for programming, even if it's only for a few hours in a day, you can get much more accomplished in a short amount of time. 

Then it's late, and you're still in the zone, and you don't want to leave, because you know even 15 minutes of coding in the zone can be more productive than the first hour of the next day because you'll have to reorient yourself and remember all of what you were doing and everything you need to consider. 

## How music helps programming

Some people might think of music as entertainment or a distraction, but I personally find music to be a helpful tool to help me pace myself and also get in the zone, tuning out background noises and other thoughts. When you're thinking about music and programming, there isn't room for much else to go on. Music can also change your emotional state, based on what kind of music it is. 

Some music is very demanding of your attention, with lyrics that make you think about whatever it is the person is talking about. But if you listen to instrumental music, it's a more cerebral experience that won't mess up your thoughts or take you out of the zone.

Basically, background music, like from soundtracks, or just music that otherwise doesn't have any singing/lyrics, actually bolsters my programming ability and concentration, so long as it isn't too intense. 

There are really two categories of music I listen to: music for active listening, and music for passive listening. Active listening distracts you and gets you to fully concentrate on the music. This is good for concerts or leisure, but not so great for getting work done. On the other hand, passive listening music might seem less interesting when you're doing absolutely nothing else and only focusing on the music, but it helps as a background element when you're focusing on something else, such as programming.

## osTicket, Bitnami, and MySQL databases

![osTicket screenshot](/assets/osticket_installation.PNG)

I still haven't fixed osticket just yet (I installed it but there are errors), but I did manage to combine a few online tutorials to come up with this list of commands for an initial setup on Bitnami, this time using a different Bitnami LAMP 5.6 stack instead of the 7.1 version I was using before:

![Bitnami LAMP 5.6](/assets/bitnami_lamp_5_6.PNG)


```
cd /opt/bitnami/apache2/htdocs
git clone https://github.com/osTicket/osTicket
cd osTicket
php manage.php deploy --setup /opt/bitnami/apache2/htdocs/osTicket/
cp include/ost-sampleconfig.php include/ost-config.php
chmod 0666 include/ost-config.php
mysql -u root -p
```
(then you're prompted for the password that is on the bitnami login banner, which is randomly-generated and looks like gibberish... if you need to see it again, log out and back in to the bitnami VM to see it again)
Here is an example of the randomly-generated password to look for: https://docs.bitnami.com/images/img/platforms/virtual-machine/app-credentials.png
Then in mysql, do the following:
```
CREATE DATABASE osticket;
GRANT ALL PRIVILEGES ON osticket.* TO 'osticketuser'@'localhost' IDENTIFIED BY 'YOURNEWDATABASEPASSWORDGOESHERE';
FLUSH PRIVILEGES;
exit;
```
Then back to the web interface and set up the osTicket installation with the database info you just entered above.
Then finally:
```
chmod 0644 include/ost-config.php
```

This sequence of steps helped me get farther than the problem I was stuck on previously, but osTicket still has some issues even when doing the above stuff. For example, you can submit a new ticket, but you can't log in to see it. I can't even log in with the admin account I used to set it up. I'm not sure what the problem is, but I posted about it on their forum and I will try and make more progress tomorrow.

I'm not going to attempt to fix everything in a single day. But the important part is chipping away at a problem, slowly but surely, making at least a small amount of progress every single day. When you skip a day or two, it becomes out of sight, out of mind. Then you eventually give up. So I am working towards fixing this issue. I'm also learning more about PHP and MySQL, which I should really learn more about in-depth anyway, because of how ubiquitous they are. 

Admittedly, some of the issues I'm having with osTicket might be because of issues specific to the Bitnami implementation of the LAMP stack. The entire point of using a Bitnami VM is that it's a turnkey solution to let you get a LAMP web server up and running in mere minutes. But if the differences between a Bitnami config and a typical LAMP stack are problematic enough to the point that you need to delve deep and do a lot of troubleshooting and modifications in order to get your app to work within it, isn't that self-defeating? The only point of Bitnami is that it saves you time, but the issues I'm facing here have taken up quite a lot of time thus far. 

I'm kind of thinking about giving up on Bitnami and just setting up a LAMP stack from scratch, with a regular distro like Debian or something. Then I'd learn more about LAMP anyway, instead of thinking of it as some magic stack that I can't interact with or set up myself.

## Trendy modern tech stacks vs. big and uncool stuff with momentum

It's all too easy to get into current trends about what's fashionable to develop for. MEAN stack has a cool sound to it, doesn't it? I did MEAN stack for my CS undergrad web development and databases class. As modern and cool as it is, I can't help but think that it's good to know LAMP as well. If, for nothing else, it will help me learn more about osTicket and web shells (since I'm learning about information security, and PHP shells are a common thing for sites with remote file inclusion vulnerabilities, or sites that let users customize the CMS theme by uploading PHP files, or sites that have unrestricted file upload vulnerabilities that let you inject PHP code in an image upload, for example).

Someone I know got a job doing Django/Python development, but I don't think it's used everywhere, so I should know other things instead of putting all my eggs in one basket. Python is a nice and versatile language, but there are still plenty of legacy projects running PHP regardless. Facebook and Wordpress are still PHP-based, and while it's easy to dismiss them because of the numerous things you can complain about either of them, the fact of the matter is that plenty of people still use LAMP, whether people think it's cool or not.

On the frontend side, it seems like new JavaScript frameworks come and go practically overnight. I've done some vanilla JS stuff and even some things with jQuery, but there are so many other JavaScript libraries and frameworks that I just can't keep up with it all. And why should I? By the time you invest the time and effort it takes to get familiar with someone, it's already deprecated. So sometimes it's best to go with technologies that have better "staying power" rather than things that are here right now but might not have much longevity. 

Nobody thinks Java or PHP are cool, but they are still widely used. I think it's good to learn languages that are hireable, even if you don't like them. I use plenty of different operating systems even if I don't like them all equally, but I know that there will be cases where I either have to develop for it, or support someone who is having an issue with a particular OS. So right now I use Windows 10 and Ubuntu on my desktop, Debian and Ubuntu and CloudLinux on my servers, macOS on my laptop, and iOS and Android on tablets and phones. You need to learn all the widely-used stuff, whether it's a programming language, OS, IDE, or whatever. Getting into obscure niches won't help you. 

## PHP on shared servers

![PHP selector](/assets/php_selector.PNG)

Namecheap servers run a special data center-oriented Linux distro called CloudLinux. They have cPanel and Softaculous installed within them, and they typically run LAMP stuff, but now they've branched out and have support for Node and Python stuff too (though I haven't done that on Namecheap just yet). But one interesting tool in Namecheap's cPanel web dashboard is that you can choose which version of PHP your server runs. This will affect every website you have running on that server. In my case, I have a few Wordpress sites, as well as some sites I've written from scratch.

Because of news about PHP 5.6 no longer getting security support, I decided to upgrade my PHP version.

## The rift between PHP 5.6 and PHP 7.X

Therre is significant fragmentation in PHP, remniscient of Android or Python 2.7 vs 3.X. Some legacy stuff refuses to be updated, despite all the warnings about potential hacking when the security support is discontinued. It's weird to think that you can get hacked because your *programming language* has vulnerabilities rather than your code within it, but that's the case here. It's also the case for old versions of Python that use outdated urllib stuff. Anything over a network needs updates and support. 

When Python made big changes from 2 to 3, you needed to make some changes in order to support the newer version, or so I've heard. I only started using Python 3, so I never dealt with whatever differences were in Python 2. But many people are naturally change-averse, and didn't want to embrace the new version and its syntactic sugar and whatnot. But over time, it really made sense to jump ship, even if you weren't the biggest fan. Differences in syntax are one thing, but security is always important, and that will take precedent over pretty much everything else.

Android is another fragmentation offender. So many phones never get updates, so what we end up with is people using old versions of the phone OS that can't handle the latest SDK versions, so it makes sense for developers to intentionally limit their development to older API levels in order to ensure that their apps can run on as many devices as possible. I might not like some of Apple's decisions, but at least they get updates right. Fragmentation is never a good thing.

## Wordpress works on PHP 7.2, but not 7.3

![SFR website error](/assets/sfr_error.PNG)

When I upgraded my servers from 5.6 to 7.0, Wordpress gave me warning messages about how PHP 7.0 isn't secure and that I need to update it. So within cPanel on my CloudLinux Namecheap server, I used the PHP version selector tool to update to PHP 7.3. I hit save and thought nothing of it for a while.

![Jetpack email about downtime](/assets/jetpack_email.PNG)

Then I got an email from Jetpack Monitor notifying me that my site was down. So I checked it out myself, and sure enough, neither of my Wordpress sites on that server were accessible anymore. I got 500 internal server errors. 

![PHP 7.2](/assets/php_7_2.PNG)

So I downgraded to PHP 7.2 and now it works just fine.

## Wordpress updates and why I dislike CMSes

The reason why I'm learning Python and making plans for a static site generator is that, let's face it, CMSes like Wordpress can be annoying. You have to update Wordpress itself, the themes, the plugins, and the underlying server software. But if you update PHP to the newest version, it can break your site. So you have to tread carefully, and there is an awful lot of maintenance required, if you're not doing some sort of managed WP hosting. There are lots of security issues that can arise with Wordpress, not just with Wordpress itself, but sometimes plugins can be insecure or even malicious. All this for essentially static content is a waste. 

That's where static site generators like Jekyll come into play. But my experiences with Jekyll (what this website is currently using as of the time of writing this (but maybe not after that)) have been less than stellar. It's okay once you get it up and running, but it has weird dependency issues and is overly-complicated for something that is billed as an alternative to making your own site from scratch. 

My annoying experiences with Wordpress, PHP, and Jekyll/Ruby are precisely why I am dedicated to making this Python static site generator. I will use no extra dependencies aside from Python and Qt. I will only use the Python standard library to achieve all of this. This way, all you have to install is Python, and it should work on Windows, macOS, and Linux, without any platform-specific modifications. 

## cPanel 2FA

![cPanel 2FA](/assets/cpanel_2fa.PNG)

I enabled 2-factor authentication on one of my 2 public-facing web servers. I had 2FA on the other one already. Now both of my online web servers are properly secure. My ESXi hypervisor is not publicly available on the internet though. I don't think it'd be wise to put a PHP 5.6 server on the internet in this day and age, even if osTicket requires it. I use Google Authenticator on my phone for 2FA, as opposed to less secure SMS-based 2FA.

## More Python exercises

I really like the Python Crash Course book, because unlike other books I've read about programming, it gives you short and easy exercises to complete after every new concept it covers. In one Java textbook I had during my freshman year, it featured huge projects for the user to complete, which weren't assigned for homework, so I just never did any of them. They were too demanding of your time. Meanwhile, another entry-level Python book I read didn't really have you doing much at all. Python Crash Course's exercises are good because they demonstrate concepts but don't take too long to complete.

## p4merge

![p4merge](/assets/p4merge.PNG)

I learned about diff and merge stuff today. I set up a tool called p4merge instead of using the default vimdiff tool. This is useful for git.

## Hotfixes, best practices, and technical debt

As I wrote about in a previous entry, my desktop's power supply was very poorly designed: it's silent most of the time because it turns its fan off unless it gets too hot, and then it turns the fan on full speed. This means that, most of the time, my computer is completely silent, because I have quiet fans, a fan controller, and a case with sound-dampening material. So for the most part, I can code without any interruptions. But once you do anything power-intensive, such as watching a video tutorial or compiling code, or running a virtual machine, it increases power, which increases the PSU load, causing it to get hotter, which means it turns the fan on -- very loudly, too. A little bit of constant noise is no big deal, but it's really distracting when it's silent most of the time and loud every now and then. 

I could just buy a new ATX PSU altogether, but that would be more expensive and then I'd have to spend a lot of time redoing all the cable management in my computer, which I'd rather avoid if at all possible, considering all the effort I put into routing all cables behind the motherboard tray and cleaning things up with a lot of zip ties. So I came up with an imperfect solution that still works: putting intake and exhaust fans on the outside of the case, lining up with the intake and exhaust vents of the power supply. I got a board that allows me to use a barrel-jack AC adapter with DC computer fans, which I did. Now I have two 120mm fans, so the power supply stays cool. 

![fan board](/assets/psu_fan_fix1.jpg)

Because it's hard to mount fans on the outside of a case, I duct-taped them to the case to keep them from moving. And because one of the fans was making a grinding sound because of the way I taped it, I had to use some cardboard to correct the position so it wouldn't make the annoying noise anymore. 

![PSU fan fix](/assets/psu_fan_fix2.jpg)

So it's a very inelegant solution that gets the job done. I could call this a temporary fix, or a hotfix, but there have been many of these so-called temporary fixes I've implemented that end up becoming permanent. This isn't really ideal, and to apply this to coding, sometimes a hack-y patch on top of bad code can fix a problem temporarily, but it makes maintainability and extensibility difficult. But sometimes, you really need to fix something then and there. Then you can refactor it later... or in all likelihood, just leave it as is. This is a bad practice that I try to avoid with my coding, but it admittedly happens every now and then.

But sometimes an inelegant solution is better than none at all. I've known people who put things off because they're waiting for the perfect time to do it. Going to the gym to start lifting weights, for example. If you're waiting for a perfect time to do something, you might just end up putting it off forever. When compared to not doing anything at all, my quick-and-dirty power supply fix is definitely better than not doing anything at all. 

Could it be better? Sure. But it could also be worse -- not fixing it all is definitely worse. Sometimes people have unrealistic expectations about things, especially when you consider time limitations. Software is limited by deadlines, and when you don't want to put a ton of time (and potentially money) into something, you have to be inventive about things that get the job done well enough, even if it's not necessarily a best practice. 

I'm all about best practices for code, like documentation and commenting things, making functions and classes modular and fully encapsulating rather than writing spaghetti code or cargo cult copy-and-paste-from-Stack-Overflow-and-hope-it-works programming (which I try to avoid), and things like that. As someone (whose name escapes me) once said, perfect is the enemy of good. If you want to do something perfectly, that's going to stop you from doing a good job, because doing something perfectly -- the *one right way* -- might take way too much time, and it'd be a really daunting task.

I've heard some people say they can't learn coding because they're "not a tech person" or they can't study computer science because they're "bad at math" and other such nonsense. What they're saying is they have these imagined prerequisite conditions in their head that have to occur before they can just start doing what they want to do. They're thinking about doing things *the right way* rather than just jumping right in and doing it.

If a good way to write a quick program takes you a few hours, and *the right way* to write it takes 20 more, which is really better? Of course, conversely, doing something quickly and poorly, which saves you time in the short-term, can create a lot of headaches in the future, thereby eliminating any imagined time savings. Technical debt. Any sort of "fast" method of doing something that accumulates technical debt isn't fast at all. 

My power supply hotfix doesn't really create much technical debt. At most, it would take me a couple minutes to remove the fans, then all it'd take is the normal amount of effort to replace the power supply and do all the cabling again. In this case, doing a simple cost-benefit analysis shows it's worth doing because there is a lot to gain by adding the fans, and the cost of time for removing the fans is pretty much negligible. Not all hotfixes are like that though.

I guess that was really long-winded, but what I'm trying to say is that the way you program has to be conscious of how long something will take to implement. Time management is a crucial aspect of programming -- whether it's big O notation for an algorithm, or basing your coding sprint around meeting a certain deadline so you can ship a product. Time is hugely important for coding, but that includes the time required for implementing future features and maintaining the current codebase. 