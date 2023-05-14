---
title: Difference between software architecture and software design
date: 2021-01-24
category: Software Architecture
tags:
  [
    'software architecture',
    'software design',
    'SDLC',
    'information architecture'
  ]
thumbnail: arch.png
author: Suresh Kumar Mukhiya
---

## Abstract

<div class="abstract" style="background-color: #f1f0f0; color: rgba(0, 0, 0, 1); padding: 1rem;font-style: italic;text-align: justify;">
In this article, we are going to discuss several terms associated with software, software architecture and especially the difference between software architecture and software design. Software architecture is the skeleton of the entire system. It is the highest level of abstraction to comprehend how the whole system.  Software design is about detail specifications of individual modules/components and their technical relationships.
</div>

#### Keywords:

Software design, Software architecture, Software system, Software pattern

### Terminology Jungle

I'm not an expert in `Software Engineering` but have been working as a Software Engineer since last ten years. During my PhD, I recently came across several terms that confused me and my entire understanding of the software development paradigm. Let me give you examples:

- Software architecture[<a href="#fn4" id="ref4">4</a>] vs software design
- Software design vs system design
- The software design process vs software development process
- System modelling vs software modelling
- Software architecture vs [information architecture](/posts/2019-10-27--theory-about-information-architecture/theory-about-information-architecture)
- [Software design patterns](/posts/2020-07-29--factory-design-pattern-in-python/factory-design-pattern-in-python) vs software architecture styles
- Software development life cycle (SDLC)[<a href="#fn1" id="ref1">1</a>]

Researchers and book authors used these terms extensively in their manuscripts when explaining any system or software. Some authors distinguished these terms while others used these terms interchangeably. To have a deeper understanding, I tried to consult some of my senior professors. Honestly, I become more confused.

Both as a developer and as a researcher, I wanted to dig more into this. And as any other person would do, I started to `Google`, read blogs, `StackOverflow`, or `hacker news`.

I discovered fascinating and opinionated definitions of software architecture and software design. Not many resources explaining the difference between software architecture and information architecture.

Available resources are minimal and directed towards their understanding. Definitions were ambiguous and lacked discrete difference between these two.

I decided to share this experience with others. If you are reading this post, that means you are on the same path as me.

### System vs Software

First thing first, what is the difference between system and software? Checkout an interesting discussion on Quora about the difference between <a href="https://www.quora.com/What-is-the-difference-between-a-system-and-a-software" rel="nofollow"> system and software.</a>

Wikipedia defines:

<blockquote>
 A system is a group of interacting or interrelated entities that form a unified whole..
</blockquote>

Several books attempt to use this definition, which makes sense. With this definition, we know, a system can be a cultural system, economic system, physical system, biological system and many more. We are not interested in those. A system is a set of hardware, software, people, policies, directives, and others. See the examples given below:

- Water pumping system
- Computer system
- Spacecraft power supply system
- Real time tweet labelling system

From a computer science perspective, the system is a hardware system or a software system or a combination of both. **Software** is a specific term used in the computer science field which defines a collection of executable **programs**. A program is a set of **instructions**.

<p class="tips">
A <em>software</em> is a <em>system</em> but a <em>system</em> might not be a <em>software</em>.
</p>

This is why we refer computer as system. A computer system contains both several hardwares and software. I hope I was able to clear concept. Having understood the difference between system and software, it should be much clear when I say,

- System engineer vs software engineer
- System engineering vs software engineering
- System developer vs software developer
- System tester vs software tester
- System architecture and software architecture

### System Engineer vs Software engineer

A **software engineer** designs and creates engineering specifications for building software programs, and should have broad information systems experience. Software engineers work with QA and hardware engineers to develop testing plans.

A **systems engineer** in IT does the same work as a software engineer in that he or she develops software components. But systems engineering additionally involves specifying, building, maintaining and supporting technical infrastructure. That infrastructure can include the build, test and production environments used to deliver software as a Service, and the systems used to monitor deployed software solutions' performance.

### Software architecture vs software design

Now, back to the main topic. We know what software is. As aforementioned, if you are into software engineering, you will face the term software architecture, and software design repeatedly. What are the main differences between these two terms? The answer to this question is opinion-based.

Here are links that I had bookmarked at the start of my PhD.

- https://stackoverflow.com/questions/704855/software-design-vs-software-architecture
- https://www.geeksforgeeks.org/difference-between-software-design-and-software-architecture
- https://simplicable.com/new/software-design-vs-software-architecture
- https://cybarlab.com/difference-between-software-architecture-and-software-design
- http://jinwolf.tumblr.com/post/6591954772/architectural-patterns-vs-design-patterns

<p class="tips">Software architecture is the skeleton of the entire system. It is the highest level of abstraction to comprehend how the whole system.  Software design is about detail specifications of individual modules/components and their technical relationships. </p>

Wikipedia defines software architecture as:

<blockquote>Software architecture refers to the fundamental structures of a software system and the discipline of creating such structures and systems. Each structure comprises software elements, relations among them, and properties of both elements and relations [<a href="#fn2" id="ref1">2</a>].
</blockquote>

Similarly, software design is defined in Wikipedia as:

<blockquote>Software design is how an agent creates a specification of a software artifact intended to accomplish goals, using a set of primitive components and subject to constraints [<a href="#fn3" id="ref3">3</a>].</blockquote>

I am not sure how clear is these definitions. To simply put, architecture is a bigger picture and design is a smaller picture.

#### Software architecture

Software architecture activities involve a) architecture analysis, b) architecture creation, c) architecture evaluation, d) architecture evolution and e) architecture support such as documentation, communication and others.

#### Terms associated with software architecture:

Here are the lists of terms associated with software architecture. Explaining each of them is beyond the scope of this article. However, I will try to give a short definitions of each terms that are easier to remember. Official definitions of these terms are one Google search away.

- **Software architecture description**: It includes structural diagrams, behavioural diagrams, documentations and other artifacts used to communicate and analyse software architecture. Common mechanisms of architecture descriptions are:
  - Software architecture description languages (ADL): I will leave you with [WikiPedia links to discover more](https://en.wikipedia.org/wiki/Architecture_description_language).
  - [Software architecture viewpoints](https://en.wikipedia.org/wiki/View_model). Commonly used viewpoints include functional viewpoints, logical viewpoints, information/data viewpoints, module viewpoints, requirements viewpoints, security viewpoints and others.
  - [Software architecture frameworks](https://en.wikipedia.org/wiki/Architecture_framework). This is an interesting and new topic for me. I will try to write a separate blog post for this topic. Commonly mentioned software architecture frameworks include TOGAF, 4+1 view model, MODAF and others.
- [Software architecture styles and patterns](https://en.wikipedia.org/wiki/Architectural_pattern) An architectural pattern is a general, reusable solution to a commonly occurring problem in software architecture within a given context. Architectural patterns are documented as software design patterns. Architectural styles are reusable 'packages' of design decisions and constraints that are applied to an architecture to induce chosen desirable qualities.

### Software design

Software design involves low-level component and algorithm design of a high level software architecture. During software design process, software designers attempts to achieve **software quality attributes** such as compatibility, extensibility, modularity, fault-tolerance, maintainability, reliability, robustness, security, usability, performance, portability and scalability.

- Software design defines the detailed properties.
- Software design is more about on individual module/component.
- How we are building is software design. In software architecture, we are building skeleton/structure of the software system.

During software design process we answer following questions:

- What are the responsibilities of each modules/components?
- What can module X do and what it can not do?
- Which design patterns can be used?
- UML diagrams, flowcharts, simple wireframes for specific modules.

Two essential concepts about software design are a) design patterns, and b) principles and practices.

<p class="warning">
Do not confuse <em>software architecture</em> with <em>information architecture</em>. I have written a separate posts about <a href="/posts/2019-10-27--theory-about-information-architecture/theory-about-information-architecture">information architecture and associated terms.</a>.
</p>

#### Design patterns

During software designing phase, a software designer uses a design pattern. A design pattern is the re-usable form of a solution to a design problem. There are several types of software design patterns, such as:

- **Creational design patterns**: Abstract factory, builder, dependency injection, factory method, lazy initialization, multiton, object pool, prototype, and singleton.
- **Structural design patterns**: Adapter, bridge, composite, facade, flyweight, front controller, marker, module, proxy, twin, and others.
- **Behavioural design patterns**: Blackboard, chain of responsibility, command, interpreter, strategy, visitor, and others.
- **Concurrency design patterns**: Lock, Reactor, Scheduler, Thread pool and others.

<p class="note">
<a href="/posts/2020-07-29--factory-design-pattern-in-python/factory-design-pattern-in-python">In this article</a>, we will discuss about design patterns in brief and discuss one of the creational design pattern named as Factory Method Design Pattern.
</p>

#### Principles and practices

Software designers are expected to software design principles and practices. There are several standard principles and practices. I can not cover each of them here. However, I have a `TODO` list in my backlog to write on the topic. Commonly mentioned principles includes:

- SOLID refers to Single Responsibility, Open Closed, Liskov substitution, Interface Segregation and Dependency Inversion Principles.
- Orthogonal software
- Minimising complexity
- Code refactoring
- Future proofreading
- Overengineering
- Design for sale
- Code smell
- There is more than one way to do it.

Well, well, well! Too many technical terms. One technical term to explain another word. This practice is the reason why I found technical documentation very confusing and hard to read. I hope to use simple words to describe these terms and how they fit into the broad picture. Before I wrap up, I would like to mention that there are some opinion-based definitions mentioned in this post. The descriptions are explained based on my understanding and research for the last ten years in the software industry. Validity or reference to the definitions is cited where ever applicable. Happy researching and learning. Keep tuned in for the next post.

### References

1. <span id="fn1"></span>Ruparelia, Nayan B. "Software development lifecycle models." ACM SIGSOFT Software Engineering Notes 35.3 (2010): 8-13. <a href="#ref1" title="Jump back to footnote 2 in the text.">↩</a>
2. <span id="fn2"></span>Ralph, P. and Wand, Y. (2009). A proposal for a formal definition of the design concept. In Lyytinen, K., Loucopoulos, P., Mylopoulos, J., and Robinson, W., editors, Design Requirements Workshop (LNBIP 14), pp. 103–136. Springer-Verlag, p. 109 doi:10.1007/978-3-540-92966-6_6 <a href="#ref2" title="Jump back">↩</a>
3. <span id="fn3"></span>Clements, Paul; Felix Bachmann; Len Bass; David Garlan; James Ivers; Reed Little; Paulo Merson; Robert Nord; Judith Stafford (2010). Documenting Software Architectures: Views and Beyond, Second Edition. Boston: Addison-Wesley. ISBN 978-0-321-55268-6.<a href="#ref3" title="Jump back">↩</a>
4. <span id="fn4"></span>Bass, Len, Paul Clements, and Rick Kazman. Software architecture in practice. Addison-Wesley Professional, 2003.<a href="#ref4" title="Jump back">↩</a>
