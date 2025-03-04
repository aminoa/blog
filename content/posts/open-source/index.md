---
title: 'Notes on Free Software and Open Source'
date: 2025-02-25T16:04:00-04:00
draft: false
summary: Reading I did on Linus Torvalds, the FOSS movement and Richard Stallman
---

# Forward

*If you take nothing else from this post, read [For Fun and Profit: A History of the FOSS Revolution (2017, Tozzi)](https://mitpress.mit.edu/9780262551786/for-fun-and-profit/) and take a look at the timeline.*

Last summer, before writing Feature, I wanted to improve my knowledge of the history of open source software. While I primarily focused on Linus Torvalds, I broadened my research (reading books/articles and watching YouTube videos) to focus on the movement as a whole. This post won't be as polished as my previous one; it is more of a research document rather than a regular blog post, but it may be fun to skim through!

## Table of Contents

- [Forward](#forward)
  - [Table of Contents](#table-of-contents)
  - [Timeline](#timeline)
  - [Book Summaries](#book-summaries)
    - [For Fun and Profit: A History of the FOSS Revolution (Tozzi, 2017)](#for-fun-and-profit-a-history-of-the-foss-revolution-tozzi-2017)
      - [Chapter 1: The Path to Revolution Unix and the Origins of Hacker Culture](#chapter-1-the-path-to-revolution-unix-and-the-origins-of-hacker-culture)
      - [Chapter 2: Inventing the FOSS Revolution Hacker Crisis, GNU, and the Free Software Foundation](#chapter-2-inventing-the-foss-revolution-hacker-crisis-gnu-and-the-free-software-foundation)
      - [Chapter 3: A Kernel of Hope](#chapter-3-a-kernel-of-hope)
      - [Chapter 4: The Moderate FOSS Revolution](#chapter-4-the-moderate-foss-revolution)
      - [Chapter 5: The FOSS Revolutionary Wars](#chapter-5-the-foss-revolutionary-wars)
      - [Chapter 6: Ending the FOSS Revolution?](#chapter-6-ending-the-foss-revolution)
    - [Just for Fun: The Story of an Accidental Revolutionary (Torvalds, 2002)](#just-for-fun-the-story-of-an-accidental-revolutionary-torvalds-2002)
    - [Free Software, Free Society (Stallman, 2002)](#free-software-free-society-stallman-2002)
    - [The Cathedral and the Bazaar (Raymond, 2001)](#the-cathedral-and-the-bazaar-raymond-2001)
    - [Bonus!: Linus' Master of Science Thesis - Linux: A Portable Operating System (1997)](#bonus-linus-master-of-science-thesis---linux-a-portable-operating-system-1997)
      - [0. Intro](#0-intro)
      - [1. Linux Design/Implementation](#1-linux-designimplementation)
      - [2. Compatibility](#2-compatibility)
      - [3. Software Interface Portability](#3-software-interface-portability)
      - [4. Hardware Portability Issues](#4-hardware-portability-issues)
  - [Thoughts](#thoughts)
  - [Philosophy of Richard Stallman](#philosophy-of-richard-stallman)
  - [Footnotes](#footnotes)
  - [Other Sources:](#other-sources)

## Timeline

The Research/Pre-Microcomputer Era:

- 1964: Initial development of Multics, a time-sharing OS from MIT, General Electric, and Bell Labs
- 1969: Ken Thompson and Dennis Ritchie begin developing Unix to replace Multics
- 1973: Unix is rewritten in the C programming language
- 1978: First release of BSD, a Unix alternative

The GNU Era:

- 1983: Richard Stallman launches the GNU project
- 1984: X Window development starts (graphical backend) 
- 1985: Release of Emacs, the first GNU project
- 1989: Launch of GPLv1 license
- 1990: Tim Berners-Lee created the World Wide Web
- 1991: Linus Torvalds starts the Linux Kernel

The Year of the Linux Server Era:

- 1994: Ian Murdock, with support of the FSF, launches Debian
- 1994: PHP Language created
- 1994: Red Hat formed
- 1996: MySQL releases, completing the LAMP stack
- 1997: First essay of the 'The Cathedral and the Bazaar' releases
- 1998: Release of KDE 
- 1998: Open Source Initiative founded by Raymond (Open Source camp invited, not Stallman)
- 1998: Netscape Navigator open sourced
- 1998: Microsoft "Halloween Documents" leaked
- 1999: Release of GNOME
- 2001: Lawrence Lessig creates Creative Commons

The Open Source/Corporate Integration Era:

- 2004: Ubuntu founded by Mark Shuttleworth
- 2005: Linus creates Git 
- 2008: Google releases the First version of Android
- 2008: GitHub founded
- 2010: OpenStack (cloud computing platform) created by Rackspace and NASA
- 2011: Google releases the Chromebook
- 2015: Microsoft adds the 'Windows Subsystem for Linux' to their OS
- 2018: Microsoft acquires Github for $7.5 billion
- 2019: IBM acquires Red Hat


## Book Summaries

***It's telling that most of these books are over 20 years old....***

### For Fun and Profit: A History of the FOSS Revolution ([Tozzi](http://christozzi.com/), 2017)

#### Chapter 1: The Path to Revolution Unix and the Origins of Hacker Culture

Unix, developed by Bell Labs, served as the origin of open source despite starting off as a closed source project - a community sharing and developing source code for fun. Ken Thompson and Dennis Ritchie began developing a Multics OS replacement while working at Bell Labs to run Space Invaders on the [PDP-7](https://en.wikipedia.org/wiki/PDP-7). This involved redeveloping an assembly file system, shell, and processes for the machine -  this became known as Unix [^manpages]; Unix was rewritten in C in 1973 to assist in porting the operating system to other machines. At the time, AT&T (which was the parent company of the Bell Systems and its research subsidiary, Bell Labs) was legally barred from commercially entering the computer industry [^at&tnotes]. AT&T licensed the product and distributed the source code to educational institutions and companies for $20,000.

Unix was not open source but AT&T and the corresponding research institutions pioneered the FOSS ideals that would later coincide with the 'hacker ethic', the social, political, and cultural values of meritocracy, resisting authority, and cherishing interesting problems with computers Specifically, it followed a rolling release model, had open bug reports, allowed other organizations to participate in its development without restrictive licenses, and a growing, rebellious, anti-corporate community spread across Unix user groups and the Unix newsletter. The ideas of academia (sharing of ideas, decentralizing authority, and peer-review) also had a significant influence on FOSS, partly because many of these projects arose from research institutions like MIT and UC Berkeley[^railroadinfo].

#### Chapter 2: Inventing the FOSS Revolution Hacker Crisis, GNU, and the Free Software Foundation

In 1984, the Bell System was broken up and AT&T now could commercialize Unix (quintupling the price to $100,000) which stifled both Unix and BSD. Binary only distribution became more commonplace (ex. 1983 with IBM), the shift to consumer microcomputers shifted the industry away from research computers like the PDP, and alternatives like BSD were limited [^bsdinfo]. Industry efforts like the standardization focused Open Source Foundation also lacked impact. This decay would change with Richard Stallman's efforts on the GNU project.

Richard Stallman was born in 1953 in NYC. He was weird, autistic and split between two single parent households. While he was at Harvard, he visited the MIT AI Lab and loved the programming within the hacker community; he decided to drop out of MIT PhD later to work at the AI Lab. Multiple incidents within this lab shaped his view on software.

In 1980, there was a Xerox printer that jammed frequently and required someone to monitor the it. To set this up, Stallman went to Harvard to retrieve the source code and modified it to enable that functionality. He later wanted to get the source code for a different printer from Carnegie Mellon University but was denied because of Xerox's NDA, alarming him that proprietary software didn't align with values of sharing, transparency, or collaboration. In 1982, the AI lab programmers began to defect: at first to Lisp Machines, Inc by Richard Greenblatt and then the rest to VC-funded Symbolics which recruited the rest of the programmers. 

After, Stallman announced a free Unix-like OS, GNU, on the net.unix-wizards and net.usoft newsgroups on Usenet[^newsgroups]. Stallman stalled (lol) writing a compiler since adapting preexisting C compilers was challenging, so instead worked on a rewrite of James Gosling's gmacs, or GNU Emacs. Bash, a C compiler, and Unix utilities (like ls and make) were later developed and added. Stallman also began to invest in the legal side of GNU, bearing GPL in 1989 as the largest innovation, a lawyer-friendly copyleft license that could embody FOSS values across any piece of software.

This period also marked the beginning when the corporate support of free software began. Cygnus Solutions, founded in 1989 by GNU Debugger adn GNU Binutils' maintainers John Gilmore, Michael Tiemann, and David Henkel-Wallace, provided support services for free software and would later merged with Red Hat a decade later. By 1988, GNU started receiving donations from HP and Software Research Associates.

There was one wrinkle; by 1990, there still wasn't a kernel. Stallman initally went with the TRIX kernel but switched to CMU's Mach kernel since the TRIX kernel was only written for a Motorola 68000 and Microkernels were considered the future of operating systems but he needed to wait for the AT&T components to be stripped first. A year later, GNU Hurd based on the Mach kernel began development. The "design turned out to be a research project" and requiring cross compatibility didn't help matters. 

GNU was overall successful based on Stallman's leadership (projecting a strong vision of the project, comprimising in areas that mattered, an example being the Library GPL license scaling a back from GPL for the sake of adoption), institutional support, and the legal focus (GPL and Creative Commons). The limited members who participated in the project slowed the growth and the project also didn't focus much on the microcomputers of the 90s. 

#### Chapter 3: A Kernel of Hope

Linus Torvalds was born in Helsinki, Finland in 1969. He was swedish speaking kid (rare in Finland) and grew up loving microcomputers; however, while having strong research for Europe, Finland was disconnected from the a lot of the work being done in the United States and Britain, meaning that Linus needed to order parts to ship them home and use the internet to communicate with other developers. 

In 1987, computer scientist Andrew Tanenbaum released Operating Systems: Design and Implementation which discussed operating systems and a unix-like educational and simple OS, MINIX. After Linus purchased the book three years later, he was amazed by MINIX though didn't like the limited functionality (no terminal emulator/remote login, microkernel, or portability/POSIX compliance) and especially the price ($169); in particular, he thought an operating system should be $0 and didn't want financial compensation or donations. His parents, one of them a communist, the other an academic, influenced his software distribution thoughts. 

Therefore, he began to rectify this. He developed an assembly terminal emulator, then shifted towards disk/filesystem drivers which slowly pushed him into doing proper operating system development which occurred around 1991. Lack of academic resources or industry support made things harder for Linus; he needed to ask on the MINIX usenet group about POSIX standards, debugged via die-loops and use MINIX (including GNU) utilities. Tannenbaum disagreed with Linus' work, complaining that it was using a monolithic kernel and that it only worked on a 386 (particularly stinging to Linus as that was the only machine he had). He argued back against the microkernel and for it's portability due to the POSIX compliance in what would later be known as the Torvalds-Tannenbaum debate. 

From here, contributors began to add to Linux, with page-to-disk (swapping), X Window graphics, and networking. Linus decided to license the project as GPL despite the fanatical community and indifference to free software principles since he did agree that the license encouraged collaboration. Companies such as Red Hat and SUSE S.A began commercializing the project. 

There was a bit of a fracturing between the Linux and GNU communities. Linux's free spirit of decentralized development with commercial activity contrasted with GNU's more centralized careful approach. Stallman also was very discontent that the entire OS was named 'Linux' rather than 'GNU/Linux', sidelining the ideology of the software in favor of the development methodology as well as the fact that GNU was the majority of the code. Regardless, Linux was able to succeed in part due to the timing (the struggles of Hurd, the BSD lawsuits, the growing internet and email access to send in patches to minimize barriers for contributing), the GPL license, and the free cost of the OS itself.

#### Chapter 4: The Moderate FOSS Revolution

Distributions of Linux with GNU utilities start to release: Slackware in 1993, Red Hat and Debian in 1994. Throughout the 90s, multiple BSD distros released (such as NetBSD, FreeBSD, and OpenBSD), those these were much smaller in market share compared to Linux.

The Linux desktop began to strive for ease of use and accessibility, starting all the way back with the initial development of X Window in 1984 at MIT which GNU adopted in 1987. Leveraging X Window, Matthias Ettrich created KDE to improve the desktop and create a common UI standard though it used QT, at the time a proprietary library. In response, Miguel de Icaza and Federico Mena created GNOME, a completely free desktop environment, which used GTK+ instead[^gnomeinfo]. Other notable programs created during this innovative time in the 90s include OpenOffice (2000, later forked into LibreOffice after Oracle acquired Sun Microsystems), Thunderbird (2003), and Wine (1993).

Arguably Linux's greatest breakthrough though was in the server space. After Tim Berners-Lee created the world wide web by joining hypertext with the internet and designing and implementing a corresponding web browser and web server. He released the standard into the public domain and so development on more web servers came about. Notably, a group at University of Illinois worked on the NCSA HTTPd server but after Netscape poached Rob McCool (the lead developer), other developers formed the Apache group and working on a replacement web server, the Apache Web Server, which released in 1995 under the Apache license [^moreapacheinfo]. Tailored open source software came to form the LAMP stack (Linux, Apache, MySQL server (released in 1996) and PHP/Perl/Python) which cemented the open source setup as de-facto for web servers.

Linux became a greater player within business. Red Hat, founded in 1995 by Bob Young and Mark Ewing, developed and open sourced their free Linux distribution but earned revenue on certifying Linux across enterprise standards as well as provide support services; it went public in 1999. VA Linux was founded in 1993 and focused more on selling Linux on pre-installed computers and was able to grow quickly, receiving investments from Sequoia Capital and Intel, and also went public in 1999 - that company later declined due to the dot-com bubble and further competition in the computer market. IBM began to sell the Apache Web Server and invested $1,000,000 in Linux in 2000 to act as a counterweight against Microsoft [^randomapple].

#### Chapter 5: The FOSS Revolutionary Wars

There would be two major tensions that would occur during the late 90s/early 2000s. One would be the civil war that would occur from the emergence of two very similar but on closer inspection separate movements: the "open source" (Linux/Torvalds) and the "free software" (Stallman) movements. The second would be external: Microsoft, which used its influence to try and quash the proliferation of open source software and standards.

What was the split between the open source and free software movements? The fracture started with Stallman's failure to rebrand Linux as GNU/Linux and the split development methodologies between GNU's centralized ("cathedral") approach vs. Linux's distributed ("bazaar") approach. Open source became the corporate friendly term that emphasized the development model (which companies like Netscape when open sourcing its browser), upsetting Stallman who thought that the morals of software use were being deemphasized. Torvalds for his perspective who enjoyed the engineering behind open source software and found Stallman to be divisive and too black and white. The free software movement gradually began to decay over the next couple of decades [^moreopenvsfoss].

The second major battle came between the entire FOSS community and Microsoft. Raymond's essay "The Cathedral and the Bazaar" helped push executives at Netscape to open source their browser[^netscapeinfo] and this got Microsoft's attention. As revealed in the "Halloween Documents" that were leaked to Eric Raymond, Microsoft began to fear FOSS software and devised a strategy to squash it: "Embrace, Extend and Extinguish"; this involved creating proprietary extensions to existing open standards to create a lock-in (this was done with Internet Explorer with ActiveX and Microsoft Office's proprietary format). They were primarily afraid of FOSS software taking over the server market and to a much lesser extent desktop Linux distros and wanted to employ the EEE strategy.

Microsoft took multiple actions to attempt to stifle FOSS. First, they promoted the "shared source" model to let Microsoft keeps its IP rights while sharing the source to select partners, though this ended up not working out. Second, they backed the SCO Group which filed a lawsuit against IBM and other companies claiming that some of the Unix code was from the System V OS they released; Torvalds and other open source developers thought the company was just spreading fear about Linux rather than having genuine claims of copyright infringement. The lawsuit against Novell failed in 2007 and SCO Group would file for bankruptcy. Third, Microsoft backed a thesis by Kenneth Brown in 2004, "Samizdat: And Other Issues Regarding the 'Source' of Open Source Code", which argued that Torvalds copied directly from the MINIX kernel based on its complexity, criticized open source based on the fact that the origins of the code aren't known for sure, and argued that the GPL license is bad for the economy. The argument of copying was countered directly by Tannenbaum and further criticized by Stallman and Ritchie. 

The failure by Microsoft to stop open source showed the persistence that FOSS software had through legal precedent and the strong corporate backing. At the same time, the ideas of free software that Stallman highlighted started fading away with minimal backing from companies.

#### Chapter 6: Ending the FOSS Revolution?

At the turn of the millennium, FOSS was dominant in the server/developer space but in the decades to come, open source software came into consumer electronics as well. Microsoft collaborated more with Canonical (the creator of Ubuntu) and Google would create Android and Chromebooks (running a linux distro, ChromeOS). This isn't a complete shift on FOSS software; instead, the philosophy for these companies have shifted to using open source software in conjunction with their own proprietary software (for example, websites hosted on Microsoft Azure) as a means of reducing engineering effort. 

Android, initially created by Andy Rubin and Rich Miner as a camera software company, was acquired by Google in 2005 and set to develop a mobile OS to counter iOS; it notably used a Linux kernel and based on Google's efforts on promoting and distributing the OS was able to capture 90% of the mobile market share. However, Google didn't want to link Android to Linux or open source (the kernel was GPL licensed and the rest of the OS Apache licensed).

Canonical and Ubuntu were created in 2004 by Mark Shuttleworth in order to create a free accessible distribution. While supporting GNU developers, he found them too ideological and incorporated proprietary components in Ubuntu such as binary blobs. Ubuntu would conquer the server space (being the second most popular distribution) and get to 40 million desktop users[^ubuntupopularity]. The reactions were expected: Torvalds praised it for the ease of usability whereas Stallman criticized it for collecting user data for Canonical's marketing efforts. 

The trend of using FOSS software while still limiting user control continued through the 2000s/2010s. Cloud computing provided FOSS software online (such as Rackspace's OpenStack in 2010 to create standards for object storage) and this trend was viewed unfavorably by Stallman as it took away control from the user while taking their data. Embedded devices (such as TVs, thermostats, etc.) also starting using FOSS software but attempted to limit the ability to modify the free software on the device (also known as Tivoization, which was the motivating reasons for GPLv3).

The ideas of FOSS did spread outside of just software as well. Creative Commons, created by Lawrence Lessig, was a license inspired by Stallman and the GPL license which pushed scientific research/educational resources to be open. Wikipedia would be a notable adopter for the CC-SA license as well as following the 'bazaar' style of development with user contributions. Currently, the FOSS community is geographically spread across the world though predominantly white and male, which can be partly attributed to access to education/computers as well as FOSS leaders either being indifferent (Torvalds) or negative (Raymond) on the issue. 

I've been using the word FOSS but really the free software portion isn't relevant anymore; the loss of ideals has disappointed hackers/FOSS enthusiasts though they do get along more with those in the open source camp. Open source software itself has prospered and as new computing methods/standards come into play, so will the goals of FOSS adapt.

### Just for Fun: The Story of an Accidental Revolutionary ([Torvalds](https://en.wikipedia.org/wiki/Linus_Torvalds), 2002)

### Free Software, Free Society ([Stallman](https://www.stallman.org/), 2002)

### The Cathedral and the Bazaar ([Raymond](https://en.wikipedia.org/wiki/Eric_S._Raymond), 2001)

### Bonus!: Linus' Master of Science Thesis - [Linux: A Portable Operating System](https://www.cs.helsinki.fi/petri/index_files/linus.pdf) (1997)

#### 0. Intro

The most important goal of the Linux Kernel was portability (both in terms of hardware, working on different CPU architectures, and software, with software being compatible with different operating systems). One of the most important concepts was the Linux kernel virtual machine - it provides two layers: one between the kernel and userspace (exposed at syscalls) and one between the kernel and the hardware (provided via drivers). The rest of the paper sections will go over different design challenges and solutions.

#### 1. Linux Design/Implementation

Linux doesn't use a microkernel (splitting the kernel into chunks) due to performance issues. Also, as the kernel is open source, instead of relying on one fixed binary, the Linux kernel can be configured to add or remove specific features at compile-time. More design goals will include simplicity, efficiency and of course, compatibility.

#### 2. Compatibility

The design for achieving compatibility was ensuring UNIX compatibility which limits the userland-kernel interface. 

Linux components included process handling, memory management, a file system, network access, drivers (each divided into its own folder), and the virtual machine implementation. For each separate hardware architecture, inline assembly can map any VM semantics onto the hardware to minimize performance loss.

#### 3. Software Interface Portability

Again, this is constrained by the POSIX interface.

There was also the idea of operating system 'personalities' which was the idea that the same platform may have multiple interface abstractions (besides just POSIX). (As seen on the man page, "Linux supports different execution domains, or personalities, for each process... among other things tell Linux how to map signal numbers into signal actions". While popular in the 90s, the rise of virtualization killed this idea).

#### 4. Hardware Portability Issues

While a C compiler does provide cross platform compilation, there are a host of issues that come after. First are the issues that come with data. Consistent data sizes are important for networking and file systems so a types header file is required for some platforms. To handle byte alignment (or an object being stored at an address that's a multiple of 8/4/etc.), the kernel will assume alignment and then use a trap handler to handle exceptions. Byte order is handled with functions to convert between big-endian and little-endian.

Memory management must be fast and simple, even without hardware standards. CPUs have a feature known as a Translation Lookaside Buffer (TLB) which shows recent translations of virtual memory to physical memory. Operating system page tables handle translating virtual addresses to physical addresses since processes are given the illusion of a continuous address space and need to have a mechanism to translate the addresses.   Different CPUs have different methods for handling virtual memory (such as using page table trees (or multiple levels of page tables), a hash table, or even no architecture-specified page tables). 

The strategy the Linux kernel uses is to use the linux kernel virtul machine as the intermediary. The memory management to the Linux kernel VM is the same across platforms, with architecture-specific code after. This requires page tables of the kernel VM and physical memory and they and the TLB need to be kept in sync. 

Speaking of CPU caches, cache coherency (syncing of multiple processor caches) is also required. Instruction caches are handled by invalidating stale cache entries during memory management while data cache coherency is more complex and not handled with shared shared memory maps. For multiprocessor handling, atomicity is provided for kernel data structures via kernel locks.

Finally, device drivers (which comprimise half of the kernel) provide I/O abstraction though the PCI standard is helping cut down on the work.

## Thoughts

- Stallman highlights tax breaks/financial incentives for developers creating FOSS, which sounds interesting
- Key difference: "A development methodology vs. a social movement" - the open source initiative really does cover the ideas Stallman advocated for, but there is definitely a de-emphasis on the moral ideas
- His philosophy seems archaic and non feasible even a decade ago - almost all modern software will connect to a cloud service and the rise of AI tooling has only accelerated that change.
- Speaking of AI, the [Open Source AI Definition from the OSI](https://opensource.org/ai/open-source-ai-definition) focuses on open source machine learning systems, highlighting data access (where to obtain the data, how its labeled, processed), the code for training/running the system, and the weight parameters for models. 

## Philosophy of Richard Stallman

- Enveloped in controversies later stalled him  
- GNU/Linux debate \- his values are right but there's an advocacy limit before people want to tune you out and RMS has not found his limit  
- Epstein Controversy: Got back on the open source board in 2021, but furthered decline of his influence.

## Footnotes

[^manpages]: The first man pages were created in 1971. 

[^at&tnotes]: This restriction stemmed from a 1956 decree from a DOJ lawsuit against AT&T. 

[^railroadinfo]: Both Steven Levy and Eric Raymond point to the MIT Tech Railroad Club as originating the values of cherishing computers, working on interesting problems, a meritocratic place to work, etc. While inspecting the arguments that Steven Levy and Eric Raymond make, Tozzi argues that both of their focus on the MIT Railroad Tech Club is too narrow. General ideas of public accountability, resisting authority and meritocracy are historical values that arose from the French Revolution and the Revolutionary War. The FOSS principles and hackerdom originate more from academia with (fitting that these would also appear in an MIT research lab). The hackers who developed FOSS software were continuing the ideas that formed during Unix. 

[^newsgroups]: Looking at TechTarget, Usenet allowed researchers/academics to share information/ideas via an online discussion forum - it used the Network News Transfer Protocol (NNTP). 

[^lookandfeed]: Battle for ‘Look and Feel’, software patents which could protect the idea/concept behind software, which copyright law didn’t cover  
- 1987: SoftKlone won legal battle over look and feel of its programs  
- 1989: Stallman founded League for Programming Freedom, separate org to combat above issue (GNU promoted it)  
- 1988-95: Apple filed (and eventually lost) lawsuits against HP/Microsoft about look and feel   

[^bsdinfo]: At UC Berkeley, Kevin Bostic led a team to separate BSD code from AT&T Unix to make a free software version. In 1989 and 1991, networking code would be added to BSD but a year later, Unix Systems Labs (the company which took over Unix from AT&T) sued Berkeley System Design (which was founded by Berkeley students part of the Computer Systems Research Group, or CSRG). After AT&T bought 20% of shares in Sun Microsystems in 1987 and collaborated to create Unix System V, a consortion of companies afraid of not being part of the standardization process came together to form the Open Source Foundation, a body which focused Unix standardization (but not FOSS). This body didn't materialize much.

[^gnomeinfo]: GTK developed in conjunction with GIMP. The pressure on Troll Technology caused them to relicense first to the Q Public License and later to GPL in 2000. Victory for FOSS; even if ‘open source camp’ would be ok with Q Public License, showed that compromise wasn’t necessary  

[^moreapacheinfo]: Notably project didn’t follow ‘Benevolent Dictator’ but allowed multiple developers to directly control code. Apache Group also initiated Jakarta (1999), developing programs based on Java, and incorporated into Apache Software Foundation to develop Apache HTTP Server and other projects. Would later host nearly 300 FOSS projects (including Hadoop/Cassandra).

[^randomapple]: Apple in 2001 worked on creating OS X based on a mach kernel and BSD components. There was animosity towards Apple from Linus: Jobs tried bringing Torvalds over by emphasizing Mach base despite closed Mac layer and Torvalds also disliked his assuming attitude that he cared about Apple’s market share. Stallman was more unenthusiastic about Jobs: despises restrictions Apple products have to prevent them from installing software of their won choice

[^moreopenvsfoss]: Eric Raymond's hypothesis of the anti-commercial idealists of free software vs. the pragmatic open source developers was inaccurate in some ways. Stallman supported corporations developing software and was compromising in some ways (for example, the LGPL license).  

[^netscapeinfo]: Raymond’s notion of Linus’ Law (more devs minimizes bugs) and the development methodology and analogy he drew of the cathedral and the bazaar was quite novel compared to Brook’s Law. This utilitarian appeal over ideology as well as recognizing previous FOSS work moved Netscape executives to open source their code (1998). Netscape also looked to the community when picking a license (not finding BSD/GPL appropriate) and this led to the Netscape Public License and Mozilla Public License (for code after open sourcing); while FOSS leaders viewed this positively, few developers improved Netscape and the project faltered until 2003 when AOL (owner of Netscape) reduced support for Mozilla; a setback but one the open source community could push through.  

[^ubuntupopularity]: Shuttleworth argues that Ubuntu focus on usability, commercial backing, and willingness to ignore factions of its userbase contributed to its popularity.   

## Other Sources:

- [The story behind Open Source Software, Saumo Pal](https://www.btw.so/blog/history-of-open-source-software/)
- [StackOverflow - What are operating-system personalities?](https://stackoverflow.com/questions/52136857/what-are-operating-system-personalities)