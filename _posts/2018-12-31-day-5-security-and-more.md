---
layout: "post"
title: "Day 4: Security and More"
date:   2018-12-31 14:50:01 -0600
---

## Not quite coding, but still important

Today, someone told me about a security issue someone else had. They got malware on their computer. During this conversation, the person I was speaking with demonstrated some misconceptions about malware and security, so I decided to write up a quick article about it in order to teach them about malware and security.

Here's that article, for anyone else who might be interested in learning a thing or two about malware:

---

## A brief primer on malware

### What is malware?

Malware is an umbrella category. It means malicious software. Sometimes people say “virus” when they really mean malware, because viruses are a very uncommon kind of malware. But anti-malware software often calls itself antivirus software because so many people misuse the word virus. A virus is a kind of self-spreading malware, but most malware doesn’t spread itself. All viruses are malware, but not all kinds of malware are viruses.

There are many different kinds of malicious software, some more nefarious than others. Adware puts ads on your computer. Spyware collects information in order to make money (such as stealing usernames, passwords, and credit card numbers). Key loggers record keyboard presses, which can lead to stealing login info. RATs are Remote Access Trojans which can steal info about record your screen. A bot, part of a botnet, is a piece of software that listens for commands from a “command and control” aka C2 server. An important thing to note is that a lot of malware is stealthy. It won’t show itself to you. The only kind of modern malware that makes its presence known is ransomware, which is a kind of malware that encrypts your files and then demands you pay a ransom in order to decrypt them. But ransomware is an outlier in the sense that it lets you know that it’s on your computer. Spyware will try its hardest to remain undetected. It will not make any new windows appear on your computer, and unless you find it with a scan, you will never know about its existence. 

But instead of getting into all the details about irrelevant malware info, the important takeaway here is that many kinds of malware can steal your accounts and your identity in order to commit fraud, which can be very costly and difficult to recover from.

Someone I know once got something called a browser locker, which is malware/a scam that stops you from being able to close your browser and tells you to call “Microsoft Support” which is actually a fake support number that will tell you to install remote access software on your computer and then they pretend to get rid of problems on your computer and charge you money for it. This is somewhat related to another category: fake antivirus software, which will find made-up threats and then ask for you to pay to get rid of them.

### How can you get malware? 

Clicking on a link, opening an email attachment, downloading a program, etc. Yes, even a website in a browser can give you malware. And yes, even word documents and PDFs can be malicious too. Not all documents are malicious, I’m just saying they can be. 

Sometimes, people will trick you into clicking a link, either to open an email attachment or to visit a malicious website. 

Also, sometimes hackers will pretend to be from your bank or some other site or service you use. They might send you something that says they’re from Facebook and you need to click something in order to confirm or secure your account. These kinds of fake messages are called phishing, and they will sometimes tell you to go to a website that looks vaguely similar to the real one, but if you check the domain name, you will see that it’s not right.

### Are only shady websites malicious?

No, legitimate websites can get hacked and then the hacker will make the site serve malware to people who visit it. This is sometimes called a “watering hole attack.” In a similar manner, hackers can sometimes steal your acquaintances’ accounts, and then send links to malware to everyone on that person’s contact list. So if your friend gets hacked, their accounts could be used to send you malicious links or attachments. This is called “reputation hijacking” because you are more likely to trust links from an account that is owned by someone you trust. But keep in mind that a person’s account is not the same as a person.

### How you can protect against getting malware?

It’s very important to install software updates for your operating system (such as Windows 10) and all of the programs you have installed within it (such as Firefox, Chrome, Adobe Reader, and so on). 

### How do you know if you have malware?

The easiest way to find out if you have malware is to run an anti-malware scan, such as with Malwarebytes. However, no anti-malware software is perfect, nor will it ever be. However, sometimes things won’t get detected, but one way you might know you have malware is abnormal resource usage on your computer. If your computer is really slow for no reason, it might be because of malware running on the computer. Keep in mind that I am talking about the speed of your computer, not your internet connection. You can check out your computer’s resource usage by opening the task manager.

Some security exploits make use of bugs in software. If something is very glitchy or crashes a lot, it could be because of hacking, but it might also just be benign. 

### What is data exfiltration?

Data exfiltration is the process of stealing private information from a device and sending it to some remote location, such as a hacker’s server. Some malware will exfiltrate your files, sometimes searching for very specific things instead of stealing everything indiscriminately. This is why you should never store your passwords or financial information in a document on your computer. 

### What should you do if you get malware?

Reboot into safe mode, then run a Malwarebytes scan to get rid of it. Disconnect your internet connection, because malware can do bad things such as exfiltrating data when you’re still connected to the internet. 

Then, you really need to change all of your passwords and monitor your accounts closely. You might even want to consider cancelling your credit cards and getting new ones, or even doing a credit freeze. If you have lots of accounts and changing everything sounds too daunting, considering using a password manager such as LastPass.

### If I got an Apple computer, would that be immune to malware?

This is a common misconception. I'm writing this on a MacBook right now, and even I know that macOS isn't perfect.

### Is malware only a problem on Microsoft Windows?

No, it’s a problem for every device. Windows, macOS, Linux, iOS, and Android – there is malware for every operating system out there. Apple used to falsely advertise that malware was only a problem for Windows, but there are plenty of mac-specific things too. Security is a concern for every type of device, whether it’s a desktop, laptop, tablet, or phone. In fact, there is even malware for routers now, such as DNSchanger, which will make your router redirect you to fake versions of websites that will steal your login information. 

### Is there a way to make a computer 100% secure?

No, security is never absolute. People want a quick fix, but there is no quick fix. 

### Will anti-malware software find everything?

No, not all malware gets picked up by anti-malware software. That’s why it’s important to be cautious when using a device. Any kind of device that connects to the internet can be potentially hacked or potentially get malware. But being cautious about clicking things can help a lot.

### What is security?

Security is an ongoing process. Security is never perfect and it never will be. Security will be an issue for as long as computers and phones exist. Anyone who says they’ve “solved security” or have something that’s “hack-proof” are either lying or don’t know what they’re talking about.

### Do I have to actively click on something in order to be compromised?

No. There is a category of security issues called “remote code execution” which means that someone can do something to your computer remotely without you even clicking on something. These are less common though, especially when you have a firewall, but it does come up every now and then. This is why software updates are important.

### What is the difference between scheduled scans and realtime protection and why does it matter?

If something gets stopped with realtime protection, that can mean that it was stopped before it ever infected your computer or did anything bad on it (well, hopefully). If something only gets picked up with a scheduled scan, that means it could have done something bad on your computer in the period between when you got it and when it was detected by a scan.

Stopping things in real-time is a proactive approach. Scheduled scans are a reactive approach. Reactive security always lags behind. It’s better than nothing, but it’s not ideal.

### If anti-malware software says something it detects is generic, does that mean it’s safer?

No, it just means they don’t have much information about it.

### What are signatures or IOCs?

Signatures are things like file size, checksum, file name, process name, and so on. These are characteristics of malicious files. IOC means Indicator of Compromise. A scan might use signatures to detect some threats. However, signatures are easily thwarted because cyber criminals can easily change the properties of their malware. Signatures are sometimes also referred to as definitions. You need to update anti-malware software before running it to make sure it has the latest information. 

### What is polymorphic malware and how does it relate to signatures?

Polymorphic malware is slightly different (in terms of file size, name, checksum, etc) while still performing the same malicious tasks. If a criminal sends 1,000 people a polymorphic key logger, no two copies will be exactly the same. That makes it harder to detect. A lot of malware these days is polymorphic. It makes it harder to be detected by traditional signature-based methods of detection.

### What is heuristic analysis?

Heuristic analysis is a kind of scanning that checks things based on their behavior rather than relying on signatures. Most anti-malware these days incorporates a combination of signatures and heuristics. Heuristic analysis is much more effective against polymorphic malware.

### How do you (the person writing this article) know about security and malware?

I’ve read lots of books about hacking and malware, and I’ve also taken an online class called Virtual Hacking Labs. 

### Do cyber criminals get arrested?

Sometimes, but not always. Some hackers live in countries that don’t have extradition treaties with the US, so even if the US asks a country to hand over an accused criminal, their country’s government might not cooperate. 

### Who gets targeted for malware?

It’s not about you as a person. The main motive for hacking and malware is to make money. It’s nothing personal. People in rich countries are targeted more because they are likely to have more money. 

Sometimes, hackers can even automate the process of sending out scam emails, or scanning websites and devices for security issues, using tools like nmap and shodan, for example.

---

## Python

In addition to the malware happenings, I also decided to learn more about Python, using an online Udemy course. I also made the repository for my static site generator [here](https://github.com/0x416c616e/staticsitegenerator), though there isn't much in it just yet. 