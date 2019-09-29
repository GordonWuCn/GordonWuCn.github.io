---
title: 'RUBIK design and implementation'
date: 2018-6-13
permalink: /posts/2018/06/13/blog-post/
tags:
  - Rubik
excerpt: Roadmap of design and implementation of Rubik
---

Initialization of RUBIK
------

After my draft design of abtraction of networking protocol, which made the model 
of abstraction start to unravel, professor Li and I became more serious about 
this project. After analysis, in the way of good design, there are two defects 
about my fist design. First, it is way far to say elegant and has a very high 
learning cost. Since it basically uses a JSON-like format to describe a design, 
users need to understand every key's meaning, which is very counterintuitive to 
describe a thing that is dynamic changing and has stateful meanings. Besides 
hard to learn, the code style design is ugly and hard to catch people's eyeball.
If there are is no intuitive syntax and beatiful code structure, it is very hard 
for coder in networking area to leverage our code. Second, in term of 
implementation, it can be exacting and full of bugs if we program our syntax 
parser, which is very volatile, also hard to support high-level syntax. Due to 
these defects, we switch to use python interpreter, which provides a ready-made 
grammar parser and has tons of virtue in coding, to accomplish our design. And 
we came up with our project name -- Rubik.

Design and implementation
------

Since I was acquainted with backend implementation and had couple of codes 
ready, we put our efforts on syntax design. Same as my first design, using 
python to design the syntax was still exacting and often fall into dilemma. 
However, unlike the first time, professor Li and I can work altogether to 
discuss the ideas, like which syntax is better, how to have a new grammar to 
describe a new abstract. We polished our design about a handred times
(I really mean 100) to find a balance between abstraction and flexibility, 
as I discussed [before]({{ site.url }}/rubik/2017/12/18/RUBIK-Preliminary.html).
This process lasted about 3-4 months, and started to converge at May. In this 
design, we can describe standard TCP protcol, including buffer reordering, 
retransmission detection and window control, in less than 100 lines of code. 
Speaking of implementation, it is fairly easier than designing part -- by 
leveraging python AST library, we basically can manipulate python code in our 
will. Our fine-grained idea is aimed at publishing on NSDI. And our RUBIK code 
will be open-sourced when the paper is accepted to NSDI.

Thought during design and implementation
------

Compared with my first design, this formal design is even more exacting and 
intensive, since in my first design, I only worked myself and I did not need to
discuss and presuade other whether a specific design is good. However, when 
cooperating with professor Li, though tired and worrisome, it really came out a
work that is fantastic, providing users with tons of good features and syntax to
work on abstraction of a networking protocol. Introspecting myself and 
retrospecting the whole process of design and cooperation 
with professor Li, I summarized point of virtues that facilitate our project 
and keep on right track. 

First, professor Li and I keep very frequent and fluent communication, which is 
crucial in a group. In designing such difficult and abstractive thing, obstacle 
and stagnation were encountered very frequently. Moreover, if team member cannot
keep the information flow smoothly and swiftly, the situation can deteriorate. 
However, professor Li and I always exchange the difficulty we meet in design and 
implementation and, though impediments do not decrease, can figure out ways to 
solve our problems. Besides solving problems, communication brings us 
unremitting confidence, which is our fuel to sustain when encountering tons of 
diffculty and seems never end. Sometimes it is very frustrating when 
encountering problems that seems impossible to solve. However, talking with 
other and inspired by other's intelligence can make me solve quickly and give 
me confidence that our team is invincible and no problem can beat us. 

Second, professor Li and I have very intensive discussions about our design, 
which is different from the first point, since communication contains 
everthing but discussion on design solve our academic problems. Since, the 
design is very complicated, human brain is tend to idle, when encountering such 
sophisticated system. However, when two people are exchange their opoinions 
about this design, brain is runing very fast without rest. For example, it 
is very common that there is a new syntax that I cannot find a good way to 
devise and it can last about 2-3 days. However, when I discuss my problem and my
primary thought with professor Li, as discussion going on, my brain works very 
fast in order to come up with reasons to defend my thought or question his 
thought. And as intensive process progresses, new thoughts and revisions
inspired by our discussion and defence come up and we will finally have a 
satisfied solution about the problem, which takes time much less than the time when
I think the question myself. From these intense discussions, I realized 
that it is very helpful to discuss with others about the problems and it will 
be solved in short time. In addition, when discussing to others, please let all
voice and idea flow on the discussion. **"Discussion is not to convince others 
to accept your point of view, but to exchange opinion for a better answer"**. 
This quote really helps when I want to dominate the discussion.

Third, I am patient and unperturbed when encounting problems and has unremitting
passion on this project. So does professor Li. It is very usual that when being 
in a team working on a project, team meets a problem, but the attitude to the
problem is crucial. Especially when team members stuck into a problem that seems
unsolvable, if I can be patient and unflappable and still work on that 
problems, which is a action that signal my teammates that we are still confident
on solving this problem. On the other hand, if I start to be upset and complain 
about my teammates, situation can be even worse and team solidarity can break 
up. The latter is very common in failed projects. However, professor Li and I 
never have touched the edge of collapsing. I always believe that no problem is 
unsolvable, it is just I did not take enough efforts and spend enough time. 
Besides unflappablility, I has my passion on this project, which give me 
incessant energy to solve continous incoming problems. It is very frustrated 
and tired to notice that there are still problems on the way when I just solved 
one. However, when I was a freshman in computer science, it always came into my 
mind that it would be such a achievement that I could build my own compiler. 
Therefore, the sense of achievement offers me tons of fuel to propel me focusing on 
RUBIK design and implementation.