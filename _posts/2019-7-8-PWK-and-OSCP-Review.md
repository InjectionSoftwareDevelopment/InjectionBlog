#### PWK and OSCP Review <a name="pwk-oscp-review"></a>

This article is a tale of pain and triumph, with some controversial opinions to *"stir the pot"*!

If you only want to read about the review of the Course, Lab, and Exam, and forgo all of the "story", just click [here](#course-review) (not a phishing link I promise 😉).

If you prefer to listen and look at poorly drawn slides/stick figures you can check out this video version of my review here: [OSCP Journey Part 28.0 (PWK/OSCP Review)](https://youtu.be/zXkLbcDcYiA).

**DISCLAIMER:** 

*The views expressed in this article do not reflect those of my previous, current, or future employers. These views and stories are my own, and I am choosing to share them for the inspiration and entertainment of others.*

*Also, this post, like my many others, may contain some "colorful language". If you are easily offended by this do not proceed, or do, I don't care...*

## Preface <a name="preface"></a>
This PWK/OSCP review should hopefully be a unique one. My goal with this post (and its accompanying video) is to shine a light on a personal experience, a close to a journey if you will, in the most current context of this challenging certification (as of 2019).

Please note, as times change, and as the certification itself changes, this post may not age well. That is totally out of my control, and that is okay. What will carry on is the value I was able to gain from this process and my own personal experiences. I will strive to continue giving that back to the hacking community in more ways than just my OSCP Journey.

Within this post you will find details about my background, why I chose to tackle the OSCP certification, some opinions around my experience, what my experience was like, and ultimately a full review of the course (save for spoilers of course, try harder folks! 😉).

Thank you for reading, I hope this provides value to you!


<p align="center"><img src="https://www.offensive-security.com/wp-content/uploads/2019/10/Group-175@2x-300x270.png"/></p>

## Table of Contents <a name="table-of-contents"></a>
### &nbsp;&nbsp;&nbsp;&nbsp; - [PWK and OSCP Review](#pwk-oscp-review)
### &nbsp;&nbsp;&nbsp;&nbsp; - [Preface](#preface)
### &nbsp;&nbsp;&nbsp;&nbsp; - [Table of Contents](#table-of-contents)
### &nbsp;&nbsp;&nbsp;&nbsp; - [Background](#background)
### &nbsp;&nbsp;&nbsp;&nbsp; - [Why Choose the PWK/OSCP](#why-oscp)
### &nbsp;&nbsp;&nbsp;&nbsp; - [Thoughts and Opinions](#thoughts-and-opinions)
### &nbsp;&nbsp;&nbsp;&nbsp; - [My Journey](#my-journey)
### &nbsp;&nbsp;&nbsp;&nbsp; - [Course Review](#course-review)
### &nbsp;&nbsp;&nbsp;&nbsp; - [Lab Review](#lab-review)
### &nbsp;&nbsp;&nbsp;&nbsp; - [Exam Review](#exam-review)
### &nbsp;&nbsp;&nbsp;&nbsp; - [What's Next?](#what-is-next)
### &nbsp;&nbsp;&nbsp;&nbsp; - [Closing Remarks](#closing-remarks)

## Background <a name="background"></a>


A question often asked of someone who is about to embark on their PWK/OSCP adventure is "what experience do you have?". I have been asked this question in many forms such as:

1. Have you done pen-testing before?
2. How long have you been in infosec?
3. What's your *background*?

When people are asking these questions they are usually trying to gauge one of two things:

1. How prepared THEY are based on how much experience YOU have before THEY take on the challenge.
2. How prepared YOU are based on how much experience THEY **THINK** *YOU* should have before YOU take on the challenge.

I emphasize different details in the above two points for a reason. While people may have similar experience levels, your experience level in your career DOES NOT, and CAN NOT dictate your preparedness for the PWK/OSCP. I have heard all the same stories you likely have up to this point. Senior pen-testers with 15 years of xp failing the OSCP, super 1337 16 years olds crushing it in 6 hours, or most commonly "most people pass it on their second attempt".

There is certainly a true story in all of those tales, but the point here is, that just because I had a certain amount of experience DOES NOT mean that you need the same amount to be successful in your OSCP. What you need is hard work, dedication, and determination. With all that out of the way, let's answer the question, what is my background?

At the time of tackling my OSCP I would consider myself a "mid level" IT professional with around 6 years of general IT experience spanning across several fields. My very first job was essentially a system administrator's assistant for a private school. It was an awesome first gig and I spent nearly 3 years doing it until I was ready to transition to a software development role. While in that job I picked up a lot of cool hardware skills like crimping my own cables, physically building and deploying network equipment, and doing laptop repairs. I also snagged some website development experience and experience managing enterprise APs and some basic Active Directory experience.

I should preface, at this time I was not into infosec/hacking/etc...

I kind of did hacking in my spare time just to learn about WiFi and web based attacks, but I was more into software development and was very good at programming already. I was creating iOS/Android apps right out of highschool as I prepared for college. I was self taught, and making strong strides that helped me excel in my college career. Regardless, the IT Assistant gig was a fantastic first job for 18 year old me, and helped me kick start my career into IT at a young age instead of starting in a more common first job like retail or food service.

From there I took on several Software Development gigs. I landed a job as a Software Developer at a local company where I got to use my mobile app development skills, and did some freelance contracting on the side for a little extra cash. These jobs didn't pay much, but were great and flexible while I pursued my computer science degree.

During this time I met a group of guys who introduced me to Capture the Flag competitions. They convinced me to learn a little more about computer security and hacking, and down the rabbit hole I dove. I started learning about forensics, web app exploitation, cryptography, etc...

By the end of it all I had placed 3rd on a team of 4 in General Electric Ghost Red CTF. I didn't know who mubix was at the time, but one of my greatest achievements still is winning mubix's approval by developing a custom native macOS application to "phish" him into giving up his credentials for a social engineering challenge. Later when I learned it was him, it made this achievement all the more shining in my heart. I note this point not only because it's fun story, but also because mubix is a fantastic resource, and I have learned a lot in relation to this journey from his metasploit minute series, so take note of that if you're taking notes!

After that CTF experience I was hooked, I was no expert by any means but I knew I was sick of software development and I wanted to get paid to do this hacking thing! Poor naive little me...I did get there as you will see, but I had much to learn and many compromises to make!

Somehow I convinced the employer at my Software Development gig to let me do some security work. He let me do some very simple vulnerability assessments, basically identify issues beyond a vulnerability scan, but no shelling boxes. This might seem unordinary, and it is, but I was already doing generic IT work for this company like diagnosing Sharepoint issues for some clients, and setting up networks for others. It was a smaller shop and some times the general Sys Admin/Network folks were all tied up, so they made use of the experience I had from my first gig. In exchange for doing the dirty work I suppose it's only fair they let me dig around for security stuff!

I ended up finding some pretty critical issues, no shells needed! This eventually turned into me contributing some useful WPScan automation to scan our clients' WordPress sites. Each dev, even me, had a set of sites they maintained. No one had any security training so I was able to build some scanning scripts so our devs knew when they needed to patch their sites.

From here I landed an "internship" at another company that eventually led to scholarship opportunity. I use "internship" in quotes because it was a really another part time development job, they just don't normally hire "part time" so they didn't know what to call me. I was off to the races doing development again. However, during my time there I identified some pretty nasty vulnerabilities in some of the applications, and fixed them. Those findings, combined with a few more CTF wins, convinced someone in executive management that I would be far more effective in a dedicated security role.

They tried me out, let me do a few code audits and application penetration tests. I nailed it. They decided when I graduated I'd be promoted to an "Information Security Analyst"... finally a real security job...

Here's the catch, this was for a smaller company who never had a dedicated security practice before. I was tasked to assist executive management in building this out. I had great guidance from the leadership, but even with that, it was a lot of pressure for 22 year old me to essentially be the technical expert on this whole security thing. I did a few more pen-tests, helped design company policy, and learned a shit ton about PCI DSS Compliance. I always found something critical on every engagement I did, which made my management see just how valuable an offensive security practice could be.

Fast forward a year later to now, I'm 23 years old, and I am the manager of the information security team. At this point in my career I've done a dozen or so engagements of various types:

- White box code audits
- Web application pen-testing
- Regular network based pen-testing (internal and external)
- Managing and Validating Third Party engagements

Every single time, I have found something critical and was able to help remediate it. Data compromise, XSS, compromised DCs, etc... all before some criminal did. This feels great...but there was always something missing...

There's a lot more to my background than the above, but I've rambled enough and covered everything that's relevant. Buy me a beer at DEF CON and I'll tell you more stories if ya like.

The outcome of all this is that I have always learned on my own, and done this by myself. I have never had a "pro" to learn from directly, and I have had to carve my own path. This is some serious imposter syndrome stuff, why should anyone believe what I say, I have no professional validation? 

Sure I was providing a ton of value, but does it matter in the context of my career when you look at me on paper? 

Why am I the manager? 

Why didn't they pick someone who knows what they're doing?

Ever since I took on the title of "Information Security Analyst" and obtained my B.S. in Computer Science I had one goal. GET GOOD.

To me this meant an attempt at beating imposter syndrome with some sort of professional validation. This is where the OSCP comes in.


## Why Choose the PWK/OSCP <a name="why-oscp"></a>

As I went through my college career I learned that certifications are fairly common in the information security industry. I actually went after my Security+ paid for by my University around my junior year. I was contributing to and helping lead a lot of the student based security activities. From campus clubs, to competing in CTFs on behalf of the university. They thought I'd be a good candidate to knock out my Security+...they were right...BUT...

I totally failed it, only by a few points, I think 3 to be exact, but still, I failed. I was a bit embarrassed because it's so easy, but all excuses aside, I just didn't prepare for it and it costed me. Doesn't matter who you are, a week to study for a certification for the very first time has a good chance to result in failure. That was me.

I thought Security+ was bullshit anyway. Don't get me wrong, it checks boxes, if you're new to security, go for it! Just don't expect it to make you qualified for a job. It'll help you get it, but probably won't prepare you technically. 

So what certifications exists that will help you perform technically? Well in hindsight, there's a lot of them, however Offensive Security's OSCP stood out as the most prestigious to me.

As a younger student just getting in to CTFs it's a certification I thought I wouldn't have until I was a few years into my security career. However, when it came time to do pen-testing professionally, as I prepared for my shiny new analyst role, I decided to set it as a goal for myself.

I had several peers and pros tell me lots of negative things that struck a sour chord with me. They said:

- I wouldn't be good enough to do pen-testing right away 
- That my job was a joke cause the company was smaller
- That I wouldn't grow the same way at smaller company

These things sting a little. Even the points that had some truth get soured by the negativity. Now I'm a good sport, I can take the punches of my peers, but as someone who is dedicated and passionate to offensive security, I wasn't going to accept that I had to "grind in the SOC" like everyone else.

Jokes on me...I did my grind...I just did it a bit differently! While I did get to do pen-testing right out of the gate, working for a smaller company means you do everything...and I mean EVERYTHING. I was the main DFIR guy, I did policy, compliance, application security, architecture...in some ways the standard SOC grind at a bigger company might have been easier!

The reason you do the SOC grind in a lot of cases is to gain experience on the "other side". Jobs are plentiful in this, at the time of writing, and it's not only a great foot in the door, but will provide you valuable experience as an offensive security professional later on.

So clearly I went the hard route, but when it came time to tell people I don't know that "I do pen-testing", I often bite my tongue. This is because I am totally self taught. I didn't feel like I stood up to any other offensive security professionals in this space.

For me this meant chasing down the OSCP *NOW*, not in 3-5 years. The reality is there is a lot of pretentiousness in the offensive security space. Hell, many people reading this article might think I'm still not worth my salt. This is something that we should combat in this space, but it's really hard to do so as someone with no "street cred". While we should never compromise on talent, skill, or experience, we should also be kind and willing to share knowledge. Maybe that's the hacker in me rather than being *just* a pen-tester, but I felt like the OSCP was my best shot to validate my skills to myself, the community, and to my current and future employers professionally.

The ultimate motivation and desire is to show that "I CAN, and I DID". I did it standing on the shoulders of those who did believe in both me, and in the community.

This may seem like a whole lot of crap to dwell on over a professional certification, but to me this was more than a certification, it was a source of validation.

You may not share this sentiment and that's okay. To you this may just be another professional certification. You don't need a sappy story to justify why you want this cert. The only reason you need to justify chasing it down is that YOU CAN, and YOU WILL!

*P.S. I still don't have that Security+, but I do have some much cooler certs now.* 😉


## Thoughts and Opinions <a name="thoughts-and-opinions"></a>

Let's get a bit *controversial*. As it narrowed down closer to the time to go after the OSCP I started seeing a lot of really negative opinions about it. This was obviously very discouraging as I had been training for over a year, and achieving this was very important to me.

First, cheating was on the rise:

Offensive Security combated this with a proctoring solution. Not all of the Offensive Security certifications are proctored, but the OSCP is one of them. This is due to the large amount of cheating that was being observed. The OSCP is a certification hiring managers usually trust to show that a candidate has the technical skill for a role. Now as a manager, and a security professional, I can tell you, TRUST BUT VERIFY. However, the issue is that verification takes extra work, and if candidate after candidate shows that they have no business holding an OSCP, then filtering on the OSCP becomes unreliable which really devalues the certification.

Fortunately, I think the new proctoring solution really helped curb this. Is it still technically possible to cheat on the OSCP? I mean yeah, but it's possible to cheat on almost any exam. The point is that it is now significantly more difficult. While the proctoring is a bit invasive for the type of exam experience Offensive Security is providing, as someone who desired to obtain the certification, I find the change to be worth it in order for the certification to hold its value.


Second, there was a lot of shouting about how it's an "entry level cert":

You may disagree with me, that's fine, but this is NOT an entry level certification. Not in any way, shape or form. To me, this is a very pretentious view point to hold, and the people expressing it either:

1. Are total jerks, and want to put others down.
2. Don't like certifications at all.
3. Are trying to communicate a sensible point in a very negative way.

For those that are just being pretentious and think you need to be writing totally custom exploits bypassing ASLR, writing custom kernel exploits, and doing back flips through a flaming hula hoop to be a pen-tester, get lost. Your job isn't that hard, and it likely never will be. I know this for a fact, because I DO THAT JOB. Compromising an enterprise requires none of those skills, and likely never will. Quit being an asshole, let people chase their goals. 

Don't get me wrong, offensive security scales, and as you become more advanced you SHOULD tackle and expect to encounter more complex techniques, but that should never be the baseline for an intermediate role at most organizations.

For those who just don't like certifications, that's totally fair. You don't have to, it'd be cool if you were kinder, but this is the internet, and I am not your mom. If someone just doesn't like certifications, don't sit and argue with them, no one wins. Agree to disagree and move on.

Lastly, usually when you hear someone say that "the OSCP is an entry level cert", who is not one of the previous two stereotypes mentioned, they are usually trying to express a very valid opinion, they're just doing an awful job. That opinion is that the OSCP is not enough to get you a penetration testing gig. Basically that solely obtaining your OSCP does not mean you're qualified for an intermediate-senior level offensive security role. This is **TRUE**. The OSCP *alone* is not enough to land you such a role. Most tend to clarify that "the OSCP isn't easy, but it is entry level". This is still misguided in my opinion and is still an awful job communicating the point. As stated above, I believe the primary point these people are trying to communicate is that having an OSCP != being an intermediate or senior level pen-tester.

The OSCP is likely to help you get into a junior pen-testing role, but this really just depends on how much experience you already have. Almost no certification is enough to land you a job on its own. Certifications are not golden tickets, they are there to give you a boost. Obviously your mileage may vary, but this is coming from someone who is a penetration tester and a manager, so I'd like to think my opinion holds some water here.

That being said, the fact that the "OSCP does not mean you're intermediate pen-tester" != "the OSCP is an entry level certification". The OSCP is an intermediate certification. For the sake of argument I want to spell out what the differences are and use other certifications to assist in the classification. Keep in mind, this is just MY opinion. If you don't like it, fine, scream in the comments, but don't get too tied up about it, it's probably a waste of energy 😘.

Offensive Certification Professional Difficulty Classification Examples:

- Entry Level: Pentester+, eJPT
- Intermediate: OSCP, eCPPT
- Advanced: OSCE, OSEE


So let me spell this out a little clearer. For the entry level options, this isn't about how they compare to one another. In my mind Pentester+ is a simple CompTIA cert, where as eJPT is a great hands on experience. This is about where they place you in terms of preparedness for a career. If someone comes to me with an eJPT and no professional experience I can trust that they will do fine in a junior level role, but may need some extra guidance. If someone comes to me with an OSCP and no experience, I can trust that they will also do fine in a junior level role, and probably won't need quite as much guidance. I think the only time where a certification will automatically place you beyond a junior level role with no professional experience is with something like the OSCE or OSEE. Clearly someone with no professional background achieving these on their own has some thick skin. **Trust but verify of course**, but it is my opinion that when you begin talking about the advanced certifications + experience there is some slightly heavier weight for the advanced certs that could assist a potential applicant with less professional experience.

That being said, who is the OSCP really best for then? 

Well in my opinion, someone like myself. The OSCP is a good booster for someone who has a few years in infosec, but needs a little extra push to either help them get over to the offensive side, or help them grow vertically in the offensive side. You see, if a SOC Analyst or a System Administrator with 2-3 years experience snags their OSCP, and wants to become a pen-tester, it is a whole lot easier to place them in an intermediate role. Their prior experience tells you that they have some solid security chops, and the OSCP gives you confidence that they likely know how to pop some boxes. Again this is just my opinion as someone who is a hiring manager, but your mileage may vary.

So no, the OSCP is not an "entry level" certification. The OSCP is very much a challenging intermediate certification. There are "beginner" aspects to it, but keep in mind this is a training course. It's really poor for any training course to not recap some basics. You can't assume people know everything. That said, even in its basics, the PWK does not start you totally from ground zero. You need some decent chops navigating both Windows and Linux based systems or you're gonna have a bad time. While you might think you can go from 0 to pen-tester with the OSCP alone (and maybe you can, good for you!), you generally will need some prior technical know how to optimize your success.

Finally, "try harder" is toxic:

One of the gimmicks with the PWK/OSCP is that you will always be told to "try harder" whenever you ask for help. Some view this as a negative approach and express that those seeking answers and knowledge should receive quality help, not just the phrase "try harder". To some this implies a sort of "fuck off, you're not good enough, figure it out" expression. While I don't disagree, I also didn't see any of this negativity during my PWK/OSCP experience. I had read about it, even seen little flurries of debates on social media about it, but when "rubber met the road" I personally experienced no sort of negativity from the "try harder" mentality.

In fact, what I saw was exactly what those complaining were suggesting instead. Many suggested that instead of "try harder" we should provide good guidance and feedback, and help coerce the proper direction. If someone asks for an answer or is right on top of it then a "try harder" might suffice, but otherwise it is far more valuable to take a more open approach.

Again, I don't disagree, I actually saw exactly this occurring in the PWK Forums. If ever I was stuck, I saw nothing but conversations being had similar to the "Hack the Box" forums. People would discuss their issues, seek validation, and assistance, and rarely was the response flat out "try harder". It was usually "did you enumerate X?", or "did you think to run Y yet?". Which was a far cry from the expectation of "try harder" that everyone hastily claims as the staunch motto.

Don't get me wrong, you are told to "try harder", and it's quite the mantra, but it's not nearly as severe as some make it out to be. That was my experience anyway, I wouldn't get too hung up on it, but just some food for thought based on what I observed.


## My Journey <a name="my-journey"></a>

Most of you reading might know about my OSCP Journey, you can relive core parts of it whenever you like with [this video playlist!](https://www.youtube.com/watch?v=bWM0BCQ5q1o&list=PL9WW-prbqvGzHsGK_OqTyYWbCZjucpInV)

For those that don't, this section is just a quick recap of what I did to prepare for, and execute on my OSCP certification.

1. I spent a little over a year practicing through a curated list of Vulnhub VMs and Hack the Box systems that were deemed "OSCP like". I would record myself going through some of these systems "live" and post them for all to see the mistakes I would make and observe my process. Below I will list out all the lists I used and mark which one's I solved with (Completed). The lists that I referenced are as follows:
	- Vulhub: 
		- (Completed) Kioptrix: 2014 https://www.vulnhub.com/entry/kioptrix-2014-5,62/
		- (Completed) FristiLeaks: 1.3 https://www.vulnhub.com/entry/fristileaks-13,133/
		- (Completed) Stapler: 1 https://www.vulnhub.com/entry/stapler-1,150/
		- VulnOS: 2 https://www.vulnhub.com/entry/vulnos-2,147/
		- (Completed) SickOs: 1.2 https://www.vulnhub.com/entry/sickos-12,144/
		- Brainpan: 1 https://www.vulnhub.com/entry/brainpan-1,51/
		- (Completed) HackLAB: Vulnix https://www.vulnhub.com/entry/hacklab-vulnix,48/
		- /dev/random: scream https://www.vulnhub.com/entry/devrandom-scream,47/
		- pWnOS: 2.0 https://www.vulnhub.com/entry/pwnos-20-pre-release,34/
		- SkyTower: 1 https://www.vulnhub.com/entry/skytower-1,96/
		- Basement: https://www.vulnhub.com/series/dc416,99/ 
	- Hack the Box (all of these can be found by purchasing VIP on https://hackthebox.eu. I'm not being paid for this or anything I just really love this site, it's great resource and tons of fun!):
		- (Completed) Lame
		- brainfuck
		- (Completed) shocker
		- (Completed) bashed
		- (Completed) nibbles
		- beep
		- cronos
		- nineveh
		- (Completed) sense
		- (Completed) solidstate
		- kotarak
		- node
		- valentine
		- (Completed) poison
		- (Completed) sunday
		- tartarsauce
		- Irked
		- (Completed) legacy
		- (Completed) Blue
		- (Completed) Devel
		- (Completed) Optimum
		- (Completed) Bastard
		- (Completed) granny
		- Arctic
		- grandpa
		- silo
		- bounty
		- (Completed) jerry
		- conceal
		- (Completed) Jeeves [Slightly Harder the OSCP]
		- Bart [Slightly Harder the OSCP]
		- Tally [Slightly Harder the OSCP]
		- Active [Slightly Harder the OSCP]
		- Jail [Slightly Harder the OSCP]
		- falafel [Slightly Harder the OSCP]
		- (Completed) DevOops [Slightly Harder the OSCP]
		- Hawk [Slightly Harder the OSCP]
	- Misc:
		- (Completed) Metasploitable 1 https://www.vulnhub.com/entry/metasploitable-1,28/ 
		- (Completed) Metasploitable 2 https://metasploit.help.rapid7.com/docs/metasploitable-2
		- (Completed) Metasploitable 3 https://github.com/rapid7/metasploitable3
2. In addition to practicing "OSCP like" boot2root systems I also practiced public exploit code modification. I spent time learning to do simple exploits like MS08-067 manually all the way to writing some automation and unlocking the mysteries of [MS17-010 with my AutoBlue scripts](https://github.com/3ndG4me/AutoBlue-MS17-010) so that way I didn't need to rely solely on a metasploit module to exploit common vulnerabilities.
3. Practicing pivoting. While the OSCP exam may not require it, the eJPT did and its a crucial skill to know like the back of your hand. During my journey I decided to take on the eJPT first as a taste of a less restricted, easier, but still very hands on offensive security certification. It was a blast and you can read more about it [here](https://injecti0n.org/injection-blog/Review-of-the-eJPT/), but I spent a lot of time in my home lab building out complex pivoting scenarios and using different tools to insure I could always get to my targets!
4. I BUILT A HOME LAB! The best way to learn about a network is to force yourself to build one. I used a lot of my background knowledge in system and network administration and was able to accomplish this "off the dome", so unfortunately I don't have any specific resources to share. That being said, there are some great books and references out there, and googling is part of the process! Grab some dedicated hardware, check out VMWare's ESXi or Proxmox, and google how to build a Windows Domain environment! This is absolutely 100% overkill for the OSCP, but it is AMAZING experience and every offensive security nerd should have a lab anyway, so go do this. Don't have dedicated hardware for those fancy tools? No problem, use trusty old virtualbox, maybe couple it with vagrant for easy management, and go figure it out. Learning it all will be good experience and give you a taste for what mistakes or configuration decisions system/network administrators might make in a real environment.
5. Exploit development. I wasn't super new to binary exploitation basics since I am seasoned CTF player, I was just awful at it. So I decided to throw away everything I thought I knew and go back to basics. This paid off in tremendous dividends as you'll see later on. For this I started off by reading the "Get Good Book" AKA "The Art of Exploitation". I read that amazing book cover to cover, then watched LiveOverflow's binary hacking series, took on some basic challenges from exploit.education, and finally tackled SLMail for some Windows experience:
	- The Art of Exploitation: https://www.amazon.com/Hacking-Art-Exploitation-Jon-Erickson/dp/1593271441
	- LiveOverflow's binary hacking series: [LiveOverflow Binary Hacking Playlist](https://www.youtube.com/watch?v=iyAyN3GFM7A&list=PLhixgUqwRTjxglIswKp9mpkfPNfHkzyeN)
	- exploit.education Protostar: http://exploit.education/protostar/
	- SLMail is commonly known vulnerable Windows application, google it like I did, and good luck!  
6. Take the PWK. The last thing I did in all of this preparation was take the plunge and begin my PWK. I spent a little over a year doing all of the previous items over and over again constantly improving and becoming as good as I possibly could before signing up for my OSCP. The main goal was to be a pro at exploiting systems without any automated tools as a crutch. With dedication, I achieved this. This was key for me because even though many of the tools I'm used to (SQLMap, Metasploit, etc...) are extremely useful in the real world, the fact is they are an arbitrary restriction on the OSCP. Therefore, defaulting to them is a non-option. Also, because I was already doing penetration testing professionally, I had the luxury of conducting real penetration tests in my day to day as well. Obviously I cannot disclose any details from these, but being "in the ring" certainly gave me an edge!

Was a year of training overkill? Yeah...probably, especially since I had a few real engagements under my belt and lots of CTF experience. You likely won't need a whole year to prepare. To me I wanted to really grow, and this was how I did it, by doing so I set out not to "pass the OSCP", but to *CRUSH* it and secure victory and success of my goals!

## Course Review <a name="course-review"></a>

Let's talk about the PWK Course. So when you sign up for the PWK you get 3 things for all that money you (or hopefully your employer!) are/is spending. For starters you will get a packet of PWK course materials. This comes with a PDF filled with tutorials and exercises, and you get a video series that is the video representation of the PDF. You also receive 30, 60, or 90 days of lab time to the PWK lab environment depending on what package you purchased. Finally, you also receive the ability attempt the OSCP exam once. 

Technically speaking, once you give them all the money they asked for, you can dive straight into the exam whenever you like. There is a few weeks lead time when you book it, so you won't be able to take it instantly, but you can totally forgo all the course material and labs if you think you're that uber 1337. I don't recommend this of course, almost no one does, because you're really cheating yourself out of some solid material. You may THINK you know everything there is to know, but let me burst that bubble, YOU DON'T! It's always worth it to go back to basics from someone else's perspective. You never know what you may learn, and there is nothing better than strong fundamentals.


So how is that course material?

Well, simply put, it's awesome!

I can't cover the specifics of it, that's for you to find out once you dive in! What I can say is that Offensive Security takes good care of you. While you will need to go beyond the course material sometimes and "try harder", the material provides a solid foundation for everything you will see in the labs and exam.


Seriously, just stick to the material and you will do great! It's not hand holding, but it provides everything you need to know from their "menacing" buffer overflow requirements, to exploit modification, to metasploit and everything in between. We will talk about the lab report a bit more in the Lab Review section, but do note that you will need to complete the PWK Course exercises in the materials provided in order to receive points for your lab report. That just means be sure to do your homework!

The exercises are good, and force you to get your hands dirty if you're prone to just skimming the packet or watching the videos (I was at first, be sure you go back and do the exercises!).

The last note I'll make is I loved the inclusion of a video series as an alternative way to consume the material. While it did distract me from the exercises at first, I was able to learn a lot more quickly and effectively thanks to the videos. Definitely a thumbs up to Offensive Security for providing that learning option!


## Lab Review <a name="lab-review"></a>

Labs! Over the last year I've seen people rave about the labs, and I've seen people shit on the labs. Let me weigh my grandiose opinion in this debate...they're pretty freaking sweet.

The biggest complaint I've seen is that "they're dated". While I can't describe specific systems I encountered, I can attest that there are older systems in the lab, but I don't think this is a fair point to complain on. The point of the OSCP isn't about if a system is up to date or not, it's about the identification and exploitation of vulnerable systems. Whether the machine is Windows XP or Windows Server 2019 is totally irrelevant. If you can't find and pop a vulnerability on one, you probably can't do so on another. Besides, if you can't pop MS08-067 at all you're a sorry excuse of a pen-tester. And I don't want to hear "but you don't see those in the real world anymore". It may not be common, but YES YOU DO, and you better be able to pop them when you do. 

Need proof? 

Here's some Shodan for ya: https://www.shodan.io/search?query=Windows+Server+2003.

That aside, it should be noted that you can't just go around the labs doing MS08-067 or MS17-010, Offensive Security isn't dumb, they know those are too easy. While some systems might have vulnerabilities like that, most of the time you are more likely to encounter applications or services that are non-standard and have been purposefully installed for you to learn how to enumerate or attack.

That's why it's important to emphasize the Offensive Security is teaching a process here, the age of the boxes is totally irrelevant if you're able to learn the process and consistently get shells.

While I was in the lab I popped 12 systems, which really isn't much, but I had 30 days. I spent 1 week solely on course material, another week in the labs, and my last two weeks going back and doing all the exercises and reporting because I screwed up and accidentally skipped them my first week (I just watched the videos and moved on 😥).

So I popped roughly 2 boxes a night while I was in the lab. Each night I spent around 2-4 hours depending on how difficult a box was, but I was pretty consistently going to bed with 2 systems owned each night by the 4 hour (starting around 8 PM ET going to 12 PM ET each evening). I had 10 full user/root compromises, and 2 user only compromises, one of which was on a "boss box" known as "Pain". Most of the hostnames for the "boss boxes" are common knowledge at this point, but while I may be able to say the name, all I can really say past that is, it was indeed painful...and I never did root it...

What's important here is not the pain I experienced, but rather the success from popping the 10 boxes. You see Offensive Security provides you an opportunity to earn some bonus points on the OSCP exam by turning in a "lab report". This lab report can't just be a quick couple of pages over 3 boxes, no, the lab report has some pretty specific requirements you have to meet to earn those bonus points. You can read about them in the documentation [here](https://support.offensive-security.com/oscp-exam-guide/#section-2-exam-information), but basically the requirements are as follows:

1. Complete all exercises in the course material (unless the exercise is marked that it does not need to be reported on)
2. Gain both user and root access to at least 10 unique systems in the lab (you can do more, but adding more to the report won't help or hurt you)
3. For those 10 systems be sure you show the proof.txt and the ifconfig/ipconfig output in your report

If you do those things, read through the other requirements, and follow the reporting template, you might earn yourself up to 5 bonus points which could be make or break if you're having a rough exam attempt! I safely accomplished the 10 system requirement and was able to take my best shot at a lab report.

Unfortunately by the time I took on my exercises, some of them required lab access which I did not have after 30 days. So as a result, some of my final exercises were missing some key data only obtainable with lab access. I supplemented this by completing the intent of the exercise within my home lab, but I'll never know if that was good enough or not. I strongly advise knocking out the exercises first, and going with more than 30 days of lab time if you have the option to.


All in all, the labs were SO MUCH FUN. Remember, both the lab and exam are meant to be hacked, Offensive Security might throw in a few oddballs, but for the most part everything is very straightforward. Please don't get "straightforward" and "easy" confused. Many systems in the PWK labs can be a challenge, but all in all, they're all very hackable, and as realistic and straightforward as possible. Kudos to Offensive Security here too. My only complaint is I wish I had more lab time, but that's on me!

## Exam Review <a name="exam-review"></a>

Ah the exam, yep...

If you've read up on this, it hasn't changed, still as tough as always. If you have no clue and this is your first time reading about it, let me break it down for you:

- You have 24 hours (technically 23.75 as the VPN cuts off a bit early) to hack into 5 systems.
- After this you have another 24 hours to create and submit an exam report to Offensive Security detailing your findings.

Some have critiqued this as being harsh, unrealistic, or overkill. Personally I enjoyed the challenge (seriously, I've never had fun taking an exam before. The OSCP exam was fun!), but it is very unrealistic to expect someone to be so time constrained in any engagement scenario. The reality is that criminal adversaries take as much time as they need to get the job done, rarely is there a scenario where something is "only up for 24 hours". While it may be a bit silly, it is a challenge, and it's not for everyone. For me it was right up my alley, and I had a blast. I had some Jolt Cola on standby in case I needed to write a magical 0day (btw Jolt helps you find 0days if you didn't know that already), and approached it like a CTF challenge. It was a blast.

Similar to the labs, the exam has been critiqued as "dated". While I cannot discuss what machines were observed in my exam, I can assure you that the exam is certainly NOT dated when compared to the lab. The exam systems are likely going to be unique from student to student, but my experience was that the exam was even more "industry standard" than systems you may see in the lab. That said, the lab systems vary greatly, I saw a little bit of everything in the labs, you're bound to see a little bit of everything in the exam to. If anyone ever expresses this sentiment I'd remind them that the point is the process, not the age of the system. New or old, systems in the lab and exam are vulnerable, and your goal is to figure out what those vulnerabilities are and how to exploit them. I'll leave it at that.

My only critique is that the tool restrictions become extremely arbitrary in the context of the exam. I didn't find a single place where I would've been able to use a canned metasploit exploit even if I wanted to. It's a good thing it's not a crutch I lean on, but if it was I would've failed miserably, because it was a useless crutch for my attempt. I did end up "burning my metasploit lifeline", but it was for no reason other than to get a stable shell and try a few minor things. It is also a bit silly because we should be encouraging the use of such tools for efficiencies in the real world. The lab does teach metasploit in some depth fortunately, but restricting its use, when the exam is designed so the tool isn't even useful, just makes it feel like we are ignoring the other capabilities. While I think it's certainly a fun challenge, I think it's also a bit arbitrary and useless to restrict. Otherwise I have no serious complaints.

While I can't talk about what I saw in the exam, I can give the generic break down, and go over what strategy I used to tackle the exam.

As stated, there are 5 systems to compromise. Each has varying point values, and specific objectives.

1. 25 Points: The "buffer overflow" system. This system is meant to test how well you can write a custom exploit against a custom service that is vulnerable to a basic buffer overflow.
2. 25 Points: Just a generic 25 point system that requires user/root
3. 20 Points: Just a generic 20 point system that requires user/root
4. 20 Points: Just a generic 20 point system that requires user/root
5. 10 Points: Just a generic 10 point system that requires user/root

It's important to note that point values DO NOT indicate difficulty whatsoever.  The systems ALL vary in difficulty, but I think it is reasonable to say that the point values *generally* reflect difficulty. Just don't rely on this or be surprised if the 10 point system is the hardest box you've ever popped in your life when you take your exam. You never know!

My strategy was as follows:

1. Take out the buffer overflow box - 25 points
2. Take out the 20 point boxes - 40 points
3. Take out the 10 point box - 10 points
4. Take out the 25 point box - 25 points


The idea here is that if you really understand the buffer overflow, it can be an extremely easy 25 points. I am someone who has a strong programming background and spent a significant amount of time making sure I could do these like putting butter on toast, so I had the buffer overflow completed within the first 2.5 hours. 25 points on the board!

By the 6 hour mark I had gone for the two 20 pointers, but only gotten user on one. At this point I veered from my initial strategy and went for the 10 point box hoping for an easy feel good root. I got what I was after, 6 hours in I had user on a 20 pointer and root on the 10 pointer. This left me with 45 points (assuming users are worth 10 points).

At about the 7/8 hour mark I had taken out the other 20 point box, this put me at 65 points (again assuming users are worth 10 points). This is enough to pass IF my lab report gets a full 5 bonus points! However, that was a risk I wasn't willing to take. So we pressed on...

Now, at 9 hours in...I think I have passed in terms of points...I have gotten user on the 25 point box which puts me a little north of 75 points. This is all assuming that user shells are worth at least half points for each box. Offensive Security NEVER specifies how many points you get for user, just that you do get points, and it is NOT full points. It was at this point @SoDakHib on twitter reminded me that I need to be sure I passed, no assuming is allowed!

With that...I took a break...thought about my path to priv esc on that 20 point box...and relaxed for a bit...

After my break I came back fresh, and went into exploit development mode. I had decided I knew what to do, and just needed to modify some exploit code to better accomodate my circumstances. At the 12 hour mark, this paid dividends...NT AUTHORITY/SYSTEM in my "whoami" output, and a cheer of victory was undoubtedly observed by my proctor. There we had it, a solid 75 points for sure, plus the user on the 25 point system, and potential lab bonus points had me sitting at a potential 90 points, all of which was more than enough to pass in every case.

Final breakdown was:

- 5/5 user compromise
- 4/5 root/admin compromise

At this point I decided to write up a report for what I had done so I wouldn't have to do so later. Once I completed my report, it was 14 hours in, and I decided to go to sleep. I woke up the next morning two hours before my exam ended just to tackle the root privesc on the 25 point system, because we should always try harder 😉. Unfortunately I didn't get it, but that was a-okay as I was able to complete my exam with confidence and turn in the report I had ready.

Then...the most painful part...waiting for Offensive Security to tell me if I had passed or failed!

When you submit your report they'll confirm receipt of it within a few hours. From there it could take up to 5 business days for them to review your results and inform you about whether or not you have passed. While I was confident I had the points, and I knew my report was good, I still had a sinking feeling as I waited. You see, even if you score perfectly on the exam in terms of popping every box, you can still easily fail by not meeting the reporting requirements. A solid report is just as important as your technical performance during the exam. This is a professional certification after all, your deliverable to the client is important. You can't go in and smash everything and not tell your client how reproduce or fix it. If you do that you're no better than a criminal and your skills provide no value in a professional context.

After days of waiting...and I do mean the full 5 business days...they sure didn't let me relax...

I PASSED!

After my first attempt on the OSCP, I absolutely crushed it. No amount of confidence during the process or my wait could convince me I did, but in hindsight I totally nailed it. My friend @clamsecurity probably gave the best possible advice right before my exam. He said, "Remember...all you're doing is popping boxes, you literally do this all the time, just go pop some boxes."

That's what I did, I went in, and I popped boxes, and I won!


My only remaining advice that is unique to exam prep is to not rely on cross compilation on Kali with mingw. While you do need to learn this, and you can get by just fine, I strongly recommend getting both some Linux and Windows VMs on standby with relevant tools (gcc, Visual Studio, etc...) and varying architectures ready to go to compile exploits. You may see varying architectures and encounter complex vulnerabilities with PoCs that are are hard to cross compile on the 32 bit Kali VM that Offensive Security recommends its students to use. Sometimes it's just easier to load Windows C code into Visual Studio and click build rather than spend time resolving weird mingw compilation errors for an hour or two (especially when you're in a timed exam!). I had to set this up on the fly, but it paid off in the end. You may not need this at all, but it's smart for any pen-tester who is doing any exploit modification or development to emulate the target system as closely as possible prior to exploitation. Just an example of how one may need to go beyond what's taught in the course to succeed.


## What’s Next? <a name="what-is-next"></a>

I have had a few people ask what's next. 

OSCE? 

More Vulnhub VM Videos? 

Where am I going from here?

Well in terms of certifications, at some point I would certainly like to tackle my OSCE, but for now, much like I did while preparing for the OSCP, it's time for me to grow more.

I have a lot of research I am doing that will come to fruition over the next few months, and I have several books I am going to read in order to grow my knowledge. Ultimately my current goal is to grow in both my professional career and just in terms of general knowledge and understanding. I don't feel like I need another certification to validate my skills, I just need to continue to get better until I am ready to take on another challenge, such as the OSCE.

In terms of my videos, I have some awesome ideas for educational content, but they will take me time to build, and honestly may never come to fruition, but that's my next big goal in terms of "YouTube". That being said, I will likely make more box walkthroughs, maybe do some streaming of boxes, CTF write ups, and just show off cool projects I'm working on.

So if you've been following my journey via videos, don't worry, the journey may be over, but I'll keep making new content!

## Closing Remarks <a name="closing-remarks"></a>

To close this out, I want to say thank you for reading this, I hope it taught you something, benefited you in some way, or at least entertained you.

Thank you Offensive Security for inspiring me since I was a younger college student and setting a bar so high that I fought tooth and nail to achieve it! It was truly worth it.

Thank you to everyone who told me I couldn't, because it drove me to grow until now when I can finally tell you, I DID!

Thank you to my current professional leaders David and John for supporting my opportunity to take this challenge on professionally.

Thank you to Chris, Bob, Will, Seth, and Camilla for being supportive on this journey and in life in general.


### Author: 
#### — 3ndG4me (Casey Erdmann)
