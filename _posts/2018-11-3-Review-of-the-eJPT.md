#### Review of the eJPT

<p align="center">
<img src="https://drd2shbp62i2h.cloudfront.net/com/assets/images/certification/ejpt_certificate_sm.png"/>
</p>



Endless days and sleepless nights trying to implement the "bleeding edge" of security solutions. It all ends in pain, and the anticipation is blinding as there is no end in sight. Suddenly the week ends, and all is well...but you aren't going to get that sleep back...

That's enough over exaggeration about my work week though, this is a review the eJPT. Although my hectic work week didn't *help* in achieving the eJPT, the eJPT itself didn't cause any harm (phew).



Those of you who follow my social media or YouTube know that I am on track to taking the OSCP. For those of you who fall into that category, you may be wondering, why did I take the eJPT?



In my last blogpost I talked a little about what I do for work now a days in the context of my progress in life and in my projects. Part of my responsibilities as the lead for our infosec operations is also to be a hiring manager for my team. This means I have had to define what it is that I am looking for in candidates who wish to apply for my team.



To me certifications are important, but should never be a damning factor. What I mean by that is having a certification should only help those who have it, but shouldn't necessarily  harm those who don't. As someone communicating to HR departments and potential applicants, that's an easy thing to get wrong. You see, in my eyes, certifications, good ones anyway, are simply continuing education. If someone holds a valuable certification, it makes them stand out among other applicants. So in that regard, if two candidates are equally qualified and well suited for the job, and one has a certification I value while the other doesn't, it is more likely that the certified one will be who I would choose. 



That's what I mean by certifications should only help, but it is not what I meant by they should not harm. What I mean by not causing harm to those who don't, is that they should not be "filtered out" by hiring processes because they don't have a particular certification, this a garbage way to do filtering and gets rid of so many extremely qualified candidates who may not have as much education/certifications as others.



So yes, certifications *should* give you an edge up, it shows you've gone the extra mile to verify your knowledge and hopefully learn more, but they should not be blanket filter.



That being said, I personally value the eLearnSecurity certifications. They are very hands on and I think they prepare those who are certified for an actual job in a much better way than most of the more "theory" based certifications. I also value the Offensive Security certifications as well, hence my journey to the OSCP, so when I see either of these types of certifications in potential candidates, it allows me to ask valuable questions about why they sought out the cert, and what they learned. It also gives me a fair bit of confidence in their technical ability.



The eJPT is one of those certs I am looking for. Personally I have never taken a hands on security cert at all. Up until now 100% of my value instilled in these certifications has come from my colleagues achieving them and finding them valuable. Essentially a value by proxy.



Although I'm no veteran penetration tester with 6 years of experience, I do have a fair amount of professional penetration testing experience. So why would I get the eJPT if I'm clearly not a "junior" level tester?



My desire for achieving this cert was 3 fold:

1. I am expecting it from potential applicants, so I felt a responsibility to vet what I was asking for to ensure quality.
2. I have never taken a hands on security certification of any kind before, so this was a good stepping stone toward the OSCP for me. It was practice with a certification as a reward for doing well.
3. My colleagues did it no problem, so why can't I? (Nice healthy competition)



Since I am more experienced, the eJPT was fairly easy, but I don't believe the difficulty detracted from the quality of the certification in any way. The eJPT is very hands on and offers a very realistic internal penetration testing scenario. Albeit, the scenario is a bit "old", but if you consider all the legacy systems in critical infrastructure or banks, it's still relevant in 2018 (sadly). More than that though, the techniques that are required to be successful are 100% critical in being a good penetration tester, so achieving this certification demonstrates the ability to execute those techniques.



Below I'll describe the exam in as much detail as possible, save for spoilers. I hope that it will be valuable information for those vetting or looking to take the exam themselves.





#### The Exam



The eJPT is multiple choice, and the questions are available as you take the test. This allows you to "test to the questions", which is actually recommended by eLearnSecurity in their documentation. This may *seem* like it would make the exam easier, but that is not necessarily true. If you are unable to execute the techniques required to find the answers in the first place, testing to the questions will NOT help you. All it allows you to really do is, optimize wordlists in the case of password cracking, and verify certain findings. Neither of which are necessary as if you already know the techniques, which you have to execute on anyway, then the material provided is more than enough to find the correct answers on your own.



It does give some help however. For example, if you only found 8 boxes on the network, but 8 is not a multiple choice option, that gives a fantastic hint that you should enumerate the environment more.



So what techniques are needed to pass the eJPT?

1. Good fundamental [penetration testing methodolgy](https://www.google.com/search?biw=1922&bih=859&tbm=isch&sa=1&ei=UiveW4yIOcKt_QaUkLnwBw&q=pentesting+methodology+sans&oq=pentesting+methodology+sans&gs_l=img.3...6699.7968..8072...0.0..0.59.261.5......0....1..gws-wiz-img.......0i30j0i24.fqYIuDg1VCY#imgrc=kQ0DpGuB2A4gJM:)
2. Enumerate, EnUmerAtE, ENUMERATE!
   1. This means be familiar with nmap, netdiscover, metasploit scanners, sqlmap, gobuster, <insert other scanner/enumeration tool here>. Especially nmap, nmap will always be your best friend forever.
3. Know how to exploit services, and also know how to use services
   1. Metasploit usage is allowed, so if you are brand new, familiarity with the Metasploit Framework goes a long way. More importantly you should understand how to interact with services normally. You may be expected to interact with a SQL database of some sort, or an ftp server. You need to be sure you know how to do those things so you do not get tripped up by fundamentals.
4. Web Exploitation
   1. SQL Injection
      1. SQLMap is allowed, and is great to get the job done quick, but you better know how to do it manually too, or you WILL miss a few things.
   2. Cross Site Scripting (XSS)
5. PIVOTING!!!
   1. This exam relies heavy on understanding how to pivot, if you can't pivot you won't get far.
6. Password Craking
   1. Familiarize yourself with hashcat and john the ripper, you will need them
7. Brute Forcing
   1. hydra is your friend, but if that doesn't work, a little python scripting goes a long way!



The exam scenario itself drops you into an internal penetration test for a client. The scenario defines the rules of engagement, read this carefully as some things, such as brute forcing on a particular network, may NOT be allowed. This document will also provide you with a starting IP to ping, and from there you can use that information to discover more host on the network you've been dropped into.



Past that, there's not much more information I can give, its all about actually conducting the penetration test from there. Once you've compromised a host on the network you're on, you should hopefully be able to use that as a pivot point to the next network. I have no idea if the exam/scenario is different each time or not, so all of that information is hopefully generalized enough to be helpful every time.



When I took the exam the following information was true in regards to how long you have, and what it takes to pass:

1. You have 3 days, from the time you click the start button to complete the exam
2. In some cases I believe you get a free retake if you submit within the 3 days, but don't quote me on that
3. You must answer 15 questions (75%) to pass



I don't remember my exact score personally, since I did kind of breeze though it, but I think it was around and 86%. That just serves as a reminder to those who are experienced to not get too cocky, I should have gotten a perfect score, but instead I wanted to act like an ass and thought I was too good. Always be as humble as possible, you are never too good to do things correctly.



That brings me to my last point, experienced, or not, do NOT underestimate the time commitment it takes to complete this exam. It took me 3 hours to "pass", but I continued on for another 2 hours for a total of 5 hours straight. If you are not experienced, it will likely take you even longer than that, and that is OK!



You have 3 days for a reason, use as much time as you need, don't rush! This is a realistic penetration testing engagement, they take time. It doesn't matter how experienced or good you are, if you are doing this exam correctly, it will take you at least 3 hours in my opinion. If you are just truly kick ass and running through, you can probably own the whole network in about an hour or so, but if you are recording information and doing everything as if it were a real penetration test, and not just "popping boxes" it will take some time no matter who you are.



With all of that said, I hope I have provided a helpful and informative review of the eJPT. I intend to take my eCPPT next, and then my OSCP soon after. I will of course provide reviews for those as well. In the mean time, if you are considering the eJPT, go for it! It is great experience for all skill levels, and honestly...it's just really fun.



My favorite part is the challenge of being graded on how well you can hack. So proving my metal even in an "easier" exam is just as fun as any CTF. Do keep in mind that it is penetration test, and not a CTF, but that doesn't mean it can't be fun!



Thanks eLearnSecurity for a solid certification, and a fun exam experience, I'll be back!



— 3ndG4me (Casey Erdmann)
