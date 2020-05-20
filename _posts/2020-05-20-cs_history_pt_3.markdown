---
layout: post
title:      "CS History pt. 3"
date:       2020-05-20 15:07:40 -0400
permalink:  cs_history_pt_3
---


![](https://res.cloudinary.com/practicaldev/image/fetch/s--Kz3vF8t6--/c_imagga_scale,f_auto,fl_progressive,h_420,q_auto,w_1000/https://dev-to-uploads.s3.amazonaws.com/i/9izzha5m89w2iy3olpxg.jpeg)

**Early Programming**

Last week we talked about early computers and the first programmable electronic computer - the Colossus Mark 1 designed by Tommy Flowers in 1943. We also talked about how one form of early programming was done by writing programs in pseudo-code and then translating it into binary machine code, 1’s and 0’s, which people got tired of pretty quickly. Today I wanted to discuss some other forms of early programming that helped alleviate some deficiencies of programming languages that came before them. In 1944, Dr. Grace Hopper was one of the first programmers on the Harvard Mark 1. She programmed it using punched paper tape that looked something like this:

![](https://professoreugene.files.wordpress.com/2012/04/punched-tape-5-hole-pd.jpg)

When the computer read the tape, a hole represented a one and a solid a zero. Since all data is represented at it's base in binary, or a 1 or 0, that's how a punch tape contained data. In the late 1940s, programmers developed things like mnemonics, operands and assemblers! Assemblers were reusable helper programs that read in text-based instructions and *assembled* them into the corresponding binary instructions automatically. Since it wasn't very easy to program using punch tape, Hopper went on to design a language called Arithmetic Language Version 0 (A-0) that made programming much easier. This allowed them to write instructions that were more human-readable, for example, instead of a bunch of confusing 1's and 0's, they could write:
```
MOV [ESI+EAX], CL    ;Move the contents of CL into the byte at address ESI+EAX
```

Not long after, IBM released Fortran which was the first high-level programming language and pretty much dominated early programming. One huge drawback to Fortran was that it could only be run on IBM computers. Grace Hopper wanted a way for a language to be able to run across several different machines rather than just one so she served as a technical consultant to the commitee that gave us COBOL(Common Business-Oriented Language) that could do just that. 

**We Have It Much Easier Than Early Programmers**

Eventually all of these new ideas by all of these smart people led to the hundreds of programming languages we have today, giving us a few new ones each decade. 

![](https://image.slidesharecdn.com/dprogramminglanguage-josa-151025113752-lva1-app6891/95/d-programming-language-6-638.jpg?cb=1445773142)

They allow us to write very high-level code and abstract away all of the things under the hood that we don't necessarily need to worry about. Now, you can whip up a basic website in an hour or build an awesome application that handles all of your real estate or stock trading needs in a week if you really needed to. What used to take years and years can now be done in seconds.

![](https://meme.xyz/uploads/posts/t/l-43556-efficiency-is-just-smart-laziness.jpg)

**This weeks tasks**

I'm not sure what we will cover on next week's blog but I will do my best to make it something interesting/helpful. For the rest of this week, I will be working on my AWS certification, coding, networking and looking for positions to apply to. The AWS course has been a little harder than I anticipated and is requiring lots of time and studying but it's been a great experience so far. I'm excited to be learning so much and to soon be able to have it on my resume. Yesterday, I was able to complete the JPMorgan Software Engineering Virtual Experience which was a great opportunity to learn new skills. I really enjoyed getting to see what kinds of things JPMorgan developers might work on and getting to solve problems in languages I haven’t had much experience with. It was cool to jump in and be able to get the hang of python syntax and think about stocks and trading in a new way. As always, I'd love to connect via [Twitter](https://twitter.com/nicalopezdev) and [LinkedIn](https://www.linkedin.com/in/veronicalopezdev/). I just moved to Denver and would be thrilled to meet more people in the area and in the tech industry. Happy Coding! 

Peace, 

Nica


Sources: 

https://en.wikipedia.org/wiki/Assembly_language

https://history-computer.com/ModernComputer/Software/FirstCompiler.html

https://www.ibm.com/ibm/history/ibm100/us/en/icons/fortran/

https://en.wikipedia.org/wiki/Grace_Hopper#COBOL
