---
layout:      post
title:       My (different) OSCP review + Exam experience
author:      Raaqim Mohammed
tags: 		 netsec
subtitle:  	 Not the traditional OSCP review, if you're going for the exam read on!
description: Not the traditional OSCP review, if you're going for the exam read on!
date:        '2017-07-26 21:00:00 +1000'
---

# My (different) OSCP review

Normally this is the part where I'd mention how I tried and succeeded in getting my OSCP with a riveting tale of success and victory... I could do that (got 90/100 points from my estimation) but so many others have done it... So instead I'll focus on the part **no-one** likes talking about - the failing the first time part. Yes it happens - more often than what people would like to admit.


## Why do I/We/You fail the first time

The first time I failed I knew exactly why I did. I was coming in thinking "OK, I've heard how hard this is going to be, gotta try the crazy stuff, it's not going to be obvious, probably have to discover a 0day or two, report going to be 200+ pages" - don't overthink it! Remember, the OSCP is the "Introductory" (for lack of better word) certification from Offensive Security. There's still the OSCE and (if you really want to get deep into Windows exploitation) OSEE. 

It's not that crazy (yet) - just go through the methodology and steps of pentesting (I'll use the Penetration Testing Execution Standard (PTES) here but check your materials given to you for a simpler one)

   * Pre-engagement Interactions
   * Intelligence Gathering (i.e. Enumeration)
   * Threat Modeling
   * Vulnerability Analysis
   * Exploitation
   * Post Exploitation
   * Reporting

What step are you struggling at? In that step what are you missing? For example in Enumerating did you really do every bit of enumeration you can? Do you have a checklist? Did you use all the right parameters and settings? **Is there another way to do what you're trying to do?** Shells can be unreliable - did you make extras? Are your notes organised - you did scan this machine right? I recommend using Scrivener - it's a nice way to keep your notes organised. And make sure you do your notes as you go along - and take all the screenshots you need in the way you were told to! It'd be pretty sad to fail because you forgot to take them...

![Scrivener snapshot](https://raaqim.me/img/scrivener_snapshot.png)

You can even sync it to Dropbox, and auto create backups so if your machine crashes during the report stage you don't lose everything! Or if Windows decides now is the best time to reset your machine after Automatically Updating (see tmsteen's review below).

Another thing to point out is that you really should understand what you're running and why. This is especially true when using one of those "Pentesting Cheat Sheets" and you're trying for hours why one command won't work... but your OS is completely different than the assumed one on the sheet. Or running Windows commands on a Linux box (don't laugh, when you have terminal windows left and right it can happen).

A good command to run before starting (on Kali) is -

{% highlight bash %}
script exam_x.log
{% endhighlight %}
   
Where x is the machine's IP or any sort of unique identifier you want.

Just make sure to 

{% highlight bash %}
exit
{% endhighlight %}

So the log is saved... otherwise you did it all for nothing!

## Think outside the box... but don't forget to look inside!

While you'll likely be pushed to your limits (and further) don't neglect to pick at the obvious. Now having said that you do have some restrictions in the exam - and have a limited use of a tool - so a good idea is to save it until the end - but not too late! Pace yourself - rotate between the machines. As tempting as it is to go for the easy wins first go for the 'harder' ones instead since you need the 70 points to pass - and to prevent yourself wasting valuable time. And now with the changes to the exam you can't simply rely on the 10 bonus points (now 5) to pull you through - I personally think that was a good change.

And tools can't do everything - sometimes you just have to get your hands dirty and manually do it yourself! 


## My exam (Round 2) experience

This time around was much easier now that I had my head on straight. I focused on following the methodology more closely and tried the obvious steps first. Everything turned out fine now that I wasn't trying to overcomplicate things - by the 18th hour I had enough points to pass, 20th hour reached 90 and then had dinner, relaxed and tried for the last 10 which I couldn't get sadly. I was far more relaxed and less anxious this time around. 

The real horror began when I had to do my report - luckily I had prefilled in parts of the template (such as name etc.) beforehand otherwise things would've ended badly. It was harder since I had to go to University the same day - missed my station stop since I was too engrossed doing the report itself! Luckily I had completed it in time and submitted it with minutes to spare.

The main key here for the report is that if you have enough notes and have all the stuff needed as per the exam guide you'll be fine. Now if you didn't collect enough stuff earlier you'll be stuffed here - so **Ensure you collect the proof as required as per the exam**.


## Good exercise to try (better with a friend)

Get a nice, clean Windows VM (XP, 7, 8, 10 etc. the OS isn't too important as long as it's Windows). Once it's installed have a browse around - check the folders, remember the names, the layout. Run through your enumeration 'remotely' (i.e. Nmap and co. the VM), then locally (as a standard user, then as an Administrator). See what commands you can run, and can't as the different users. Dig through everything.

Then, I'm assuming you have a Windows machine that you use day-to-day for this next part (not a machine you use for work). Well guess what - you're going to test your own system today! Run through the same exercise as above - if you only have an Administrator account - create a user account. You'll be surprised with what you find on your own machine. You'll also start noticing what's not normally on a machine that you probably assume is on a standard deployment. I guarantee you'll end up surprised with what you find.

After you've done and documented everything - ask a friend to try it too - even better if they're gotten the OSCP and see what they uncover. 

Repeat the exercise with Linux as well.

This whole exercise is designed to get you to stop assuming things and instead develop the ability to detect things that aren't normally there, and what files would be interesting to look into.


## Some interesting places to have a look to find others in your shoes

[The netsecstudent subreddit](https://www.reddit.com/r/netsecstudents/)

[The oscp subreddit - not affiliated with Offensive Security in any way but a subreddit by redditors](https://www.reddit.com/r/oscp/)

[Techexam's Security Certifications Subforum](http://www.techexams.net/forums/security-certifications/)


## Some more traditional OSCP reviews

[PrimalSecurity's review - the one everyone has read (and if you haven't you should!)](http://www.primalsecurity.net/0x2-course-review-penetration-testing-with-kali-linux-oscp/)

[The definition of "Try Harder" is right here](https://localhost.exposed/path-to-oscp/)

[Tulpa's review - has a very recent prep guide for OSCE as well](https://tulpa-security.com/2016/09/11/review-oscp-and-pwk/)

[InfoSecJim's Review - nice vulnhub recommendations too](https://www.jimwilbur.com/2017/07/oscp-review/)

[tmsteen's Review - and his pre-Exam shock](https://ratil.life/try-harder-the-journey-to-my-oscp/)

[OSCP Review and tips](https://hackmethod.com/oscp-review-tips/) (I'd avoid using Sn1per - don't risk accidentally having an autopwn happen and ruining your entire exam)


## Some great resources for the exam, and the OSCP in general

[Transferring Files from Linux to Windows (post-exploitation)](https://blog.ropnop.com/transferring-files-from-kali-to-windows/)

[Favourite Buffer Overflow Tutorial I've seen - very clear](https://www.nccgroup.trust/au/about-us/newsroom-and-events/blogs/2016/june/writing-exploits-for-win32-systems-from-scratch/)

[Jollyfrog's tale on getting the OSCP](http://www.techexams.net/forums/security-certifications/110760-oscp-jollyfrogs-tale.html)

[A different Windows privilege escalation post than Fuzzysecurity](https://www.toshellandback.com/2015/11/24/ms-priv-esc/)

[g0tmi1k's Linux privilege escalation post - still my favourite](https://blog.g0tmi1k.com/2011/08/basic-linux-privilege-escalation/)

[Place to sign-up to begin your journey](https://www.offensive-security.com/information-security-training/penetration-testing-training-kali-linux/)

[The most important site you'll be visiting the most in those 48 hours (yep even for the report)](https://google.com)

And above all else just remember when you're 18 hours into the Exam and thinking of giving up -


![Try Harder!](https://raaqim.me/img/tryharder.png)

