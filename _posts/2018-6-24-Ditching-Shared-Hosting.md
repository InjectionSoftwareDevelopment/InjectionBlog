#### Ditching Shared Hosting

I always have at least 10-15 "projects" going on at any given time. After all, idle hands are the devils workshop. 
However, despite the number of projects that I have going on at any given time, I find myself to be idle more often than I would have thought.

Most of my projects are the open source projects you see on my github repos for both [Injection](https://github.com/InjectionSoftwareDevelopment) and [3ndG4me](https://github.com/3ndG4me).
I'm maintaining several projects there, as well as a few closed source projects for some cool games 'n stuff that are on the hush hush (assuming I ever start real development on them).

However, what's not tracked via github would be things like infrastrucutre upgrades, home electronics projects, and security research/studying.

So in this blog post I just wanted to talk about some of the infrastructure changes that I plan to conduct over the next few months.

As far as infrastructure is concerned...injecti0n.org really doesn't require all that much horsepower...for now...

At the moment however, injecti0n.org is just a simple website that can but run on an apache server anywhere on the internet.
There really isn't a whole lot to it, in fact for the past 6 years it has always been a static html website with only the look changing over the years.
Anytime I wanted to update the projects section on the site I had to go manually write new HTML in to the desired page. It was gross and not very fun, but the site was simple and that's all I really *needed*.

Now flash back to about a month ago, I upgraded injecti0n.org by rewriting it in ReactJS. I did this because I already had experience in AngularJS, and I wanted to learn something relevant to my current job.
At my work we are moving towards using ReactJS as a frontend technology for the applications we write. Being that I am the security brat over there, it is in my best interest to really learn this technology so I can help our developers in the event they write shitty code that leads to some ugly vulnerabilities (which is inevitable of course).

ReactJS is really neat, it allowed me to build my entire website (which normally took me about a week) in a matter of hours. Now granted I didn't have to start from scratch in regards to assets like CSS, images, and text content, so that did speed up the process significantly.
However, what would have normally taken me days was the new dynamic content features that I wanted to add in. I was so sick of writing static HTML and resizing assets for promotion everytime I released a new project.
So now, I craft a neat little JSON payload format, and with the help of reacts super reusable code, and the github API I was able to construct an elegant solution that allows me to never touch my website code unless I am adding a major feature or making visual updates.

It only took me a short weekend to learn ReactJS, so that weekend has really paid off in terms of productivity for my development projects 
(Yes really, just read the damn documentation it's really easy if you've been programming for awhile. If you watch tutorials on youtube, then you risk being led down a dark rabbit hole. I know, I tried...).

On top of that I started making use of github pages more. I'm using it now to run this new blog set up that you're reading this article on. 

Then it hit me...if I can run a blog on github pages, can I run a react site on it?
<p align="center">
<img src="https://i.imgflip.com/2ctii4.jpg"/>
</p>

Currently I pay monthly for shared hosting via rubberduck hosting. It's extremely cheap! Like $1.50 a month cheap (I pay $3.00 for more storage since I use to host downloads there).
So I'm not really getting away from costs, in fact I am looking into moving my domain over to Google's services which is considerably more expensive at around $13 a month.
The reason for considering moving to github pages is mostly for preparation for bigger and better infrastructure so that I can do more heavy duty things in the future and not hurt my main website in the process.

This shift makes it easier to maintain the core website in a LOT of ways:

1. Deployments are too easy: 
    - Since switching to react, whenever I build the static files I have to login to an ftp or cpanel or 
	whatever have you, and upload each file and replace its current running copy. This takes longer than desired and if anything goes 
	wrong during this process then the site could appear to be broken and steer away newcomers or maybe even expose vulnerabilities. 
	I do not like doing things this way and it is time to stop. I could write a neat-o little deployment script, but it would very much be a hack and another item to maintain.
	With github pages however, react let's you very simply integrate a deployment process right into your build steps. This will automatically push a build to your github pages repo whenever you run you build and deploy scripts with npm.
	This makes life so much easier in the world of deployments.
2. No mainting SSL certs for the core site:
    - Recently my shared hosting provider has switched to [Let's Encrypt](https://letsencrypt.org/) which does make things considerably easier when it comes to managing SSL certs.
		    In fact they have automated the process so that anytime you add a new sub-domain a cert is auto generated, and all certs auto-renew on their own. That is awesome and I have loved that they have provided that with their service, but with github pages, I don't even have to worry about that. All github pages sites are already secured with TLS/SSL and github maintains those certs. A very minor thing compared to the build/deployment point, but a nice thing nonetheless.
3. No more LAMP stack:
    - Ah the trusty old LAMP stack...in the earlier days I did some funky php proxy stuff to handle scraping information for services for apps like Acuity. It was really hacky, but it worked, and having the ability to run PHP on my shared hosting made things pretty dynamic. This meant that if I really really wanted to I could right full stack applicaitons using PHP and MySQL the good old fashioned way. However, there is no need for my portfolio site to be a full stack application, and any other application I may want to write I feel should have separation from the core site and use whatever technology that I see fit to implement it in. With github pages hosting the core site, I am free to stand up VPS's and point sub domains wherever all without ever affecting the core site in any way shape or form. Pretty bitchin' if you ask me.

So why on earth would I NEED to do any of this? Well in the future I would like to potentially use CTFd to run my own fun CTF competitions. While I was in university I competed in many CTFs and even got the chance to write challenges for CTFs hosted by my school and its security club. I love being on both sides of creating and competing in CTFs, so I'd like to have the option to explore that creative outlet.

Infrastructure flexibility is another key purpose, I'm paying more to get more and not be tied down. Ideally, much like the ability to run CTFd, I'd like to be able to stand up VPS's whenever I like and point new domains/sub domains at them as needed. This can be great for C3 on pentests, PoC security research, and various other reasons. It's the flexibility that is appealing to me. I can technically achieve this now with my current hosting, but I honestly don't want any of those things managed from the same place. It's a separation of duties principle really.

So that's kinda where all this is going. I want to expand the horizons of what resources I have at my disposal to do more!

Right now my friend Nathan is assisting me in debugging issues with gh-pages and react, he was the main inspiration for this realization so shoutout to that guy check out is github [here](https://github.com/gibsonnathan).

Once we get that ball rolling, I'll slowly be making the changes I need to get off of my current hosting solution and be ready for `the future`.

Also as far as projects go, my next objective is to tackle [OpenVPNConnect](https://github.com/InjectionSoftwareDevelopment/OpenVPNConnect). I have had a few issues opened up by a community member on that repo, and since [seb](https://github.com/sebkinne) over at [Hak5](https://www.hak5.org/) has recently updates the WiFi Pineapple firmware it's about time I update my module!

I'll have another blog post out here once I release that so stay tuned.

Til next time!

&mdash; 3ndG4me (Casey Erdmann)
