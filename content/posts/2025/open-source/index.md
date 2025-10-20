---
title: 'Reading on the Free Software and Open Source Movement'
date: 2025-02-25T16:04:00-04:00
draft: false
summary: Reading I did on Linus Torvalds, the FOSS movement and Richard Stallman
---

*Photo credit to [Faces of Open Source](https://www.facesofopensource.com/linus-torvalds/). If you take nothing else from this post, read [For Fun and Profit: A History of the FOSS Revolution (2017, Tozzi)](https://mitpress.mit.edu/9780262551786/for-fun-and-profit/) and take a look at the timeline and maybe my forwards for the books.*

Edit 03-13-2025: Added footnote on Red Hat, added more contributors for Creative Commons to timeline based on Sachin's notes.

Last summer, before writing Feature, I wanted to improve my knowledge of the history of open source software. While I primarily focused on Linus Torvalds, I broadened my research (reading books/articles and watching YouTube videos) to focus on the movement as a whole. This post won't be as polished as my previous one; it is more of a research document rather than a regular blog post, but it may be fun to skim through!

## Table of Contents

- [Table of Contents](#table-of-contents)
- [Timeline](#timeline)
- [Book Summaries](#book-summaries)
  - [For Fun and Profit: A History of the FOSS Revolution (Tozzi, 2017)](#for-fun-and-profit-a-history-of-the-foss-revolution-tozzi-2017)
    - [*Forward*](#forward)
    - [Chapter 1: The Path to Revolution Unix and the Origins of Hacker Culture](#chapter-1-the-path-to-revolution-unix-and-the-origins-of-hacker-culture)
    - [Chapter 2: Inventing the FOSS Revolution Hacker Crisis, GNU, and the Free Software Foundation](#chapter-2-inventing-the-foss-revolution-hacker-crisis-gnu-and-the-free-software-foundation)
    - [Chapter 3: A Kernel of Hope](#chapter-3-a-kernel-of-hope)
    - [Chapter 4: The Moderate FOSS Revolution](#chapter-4-the-moderate-foss-revolution)
    - [Chapter 5: The FOSS Revolutionary Wars](#chapter-5-the-foss-revolutionary-wars)
    - [Chapter 6: Ending the FOSS Revolution?](#chapter-6-ending-the-foss-revolution)
  - [Just for Fun: The Story of an Accidental Revolutionary (Torvalds, 2002)](#just-for-fun-the-story-of-an-accidental-revolutionary-torvalds-2002)
    - [*Forward*](#forward-1)
    - [Birth of a Nerd](#birth-of-a-nerd)
    - [Birth of an Operating System](#birth-of-an-operating-system)
    - [King of the Ball](#king-of-the-ball)
    - [End Sections](#end-sections)
  - [Free Software, Free Society (Stallman, 2002)](#free-software-free-society-stallman-2002)
    - [*Forward*](#forward-2)
    - [Part 1: GNU Project/Free Software](#part-1-gnu-projectfree-software)
    - [Part 2: What's in a Name?](#part-2-whats-in-a-name)
    - [Part 3: Copyright and Injustice](#part-3-copyright-and-injustice)
    - [Part 4: Software Patents: Dangers to Programmers](#part-4-software-patents-dangers-to-programmers)
    - [Part 5: Free Software Licensing](#part-5-free-software-licensing)
    - [Part 6: Traps and Challenges](#part-6-traps-and-challenges)
    - [Part 7: Value Community and Your Freedom](#part-7-value-community-and-your-freedom)
  - [The Cathedral and the Bazaar (Raymond, 2001)](#the-cathedral-and-the-bazaar-raymond-2001)
    - [*Forward*](#forward-3)
    - [A Brief History of Hackerdom](#a-brief-history-of-hackerdom)
    - [The Cathedral and the Bazaar](#the-cathedral-and-the-bazaar)
    - [Homesteading the Noosphere](#homesteading-the-noosphere)
  - [Bonus!: Linus' Master of Science Thesis - Linux: A Portable Operating System (1997)](#bonus-linus-master-of-science-thesis---linux-a-portable-operating-system-1997)
    - [*Forward*](#forward-4)
    - [0. Intro](#0-intro)
    - [1. Linux Design/Implementation](#1-linux-designimplementation)
    - [2. Compatibility](#2-compatibility)
    - [3. Software Interface Portability](#3-software-interface-portability)
    - [4. Hardware Portability Issues](#4-hardware-portability-issues)
- [Articles, Talks, and Interviews with Linus Torvalds](#articles-talks-and-interviews-with-linus-torvalds)
  - [*Forward*](#forward-5)
  - [DebConf 14: Q\&A with Linus Torvalds (2014)](#debconf-14-qa-with-linus-torvalds-2014)
  - [TED Talk: The mind behind Linux (2016)](#ted-talk-the-mind-behind-linux-2016)
  - [Aalto Talk (2012)](#aalto-talk-2012)
  - [BBC Article (2012)](#bbc-article-2012)
  - [Linux Foundation Interview with Dirk Hohndel (2024)](#linux-foundation-interview-with-dirk-hohndel-2024)
  - [New Yorker Article (2018)](#new-yorker-article-2018)
- [Thoughts](#thoughts)
- [Other Sources](#other-sources)

## Timeline

The Research/Pre-Microcomputer Era:

- 1964: Initial development of Multics, a time-sharing OS from MIT, General Electric, and Bell Labs
- 1969: Department of Defense creates ARPAnet
- 1969: Ken Thompson and Dennis Ritchie begin developing Unix to replace Multics
- 1973: Unix is rewritten in the C programming language
- 1978: First release of BSD, a Unix alternative
- 1981: Symbolics hires members from the MIT AI Lab, decline of FS movement

The GNU Era:

- 1983: Richard Stallman launches the GNU project
- 1984: X Window development starts (graphical backend) 
- 1985: Release of Emacs, the first GNU project
- 1985: Stallman starts the Free Software Foundation
- 1989: Launch of GPLv1 license
- 1990: Tim Berners-Lee created the World Wide Web
- 1991: Linus Torvalds starts the Linux Kernel
- 1992: Tanenbaum-Torvalds debate (on comp.os.minix usenet group)

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
- 2001: Creative Commons created by Lawrence Lessig, Eric Eldrid, Hal Abelson, and Aaron Swartz

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

*It's telling that most of these books are over 20 years old....*

### For Fun and Profit: A History of the FOSS Revolution ([Tozzi](http://christozzi.com/), 2017)

#### *Forward*

This book did a really good job at not just giving a summary of the FOSS movement but doing analysis of previous summarizations of FOSS/open source as well as attempting to contextualize many of these figures. It isn't the most in-depth for Linus Torvalds or Richard Stallman but it is benefitted on not zooming in too much on one particular figure; furthermore, it is (semi?.... ok almost a decade old wow) recent so it covers more ground that most articles/books on the subject. It starts off in Bell Labs with Unix, progressing into GNU and the movement tha† Stallman kicked off, then heading into Torvalds' kernel and how the combined GNU/Linux system was adopted by companies and mainstreamed over the coming decades. 

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

GNU was overall successful based on Stallman's leadership (projecting a strong vision of the project, comprimising in areas that mattered, an example being the Library GPL license scaling a back from GPL for the sake of adoption), institutional support, and the legal focus (GPL and Creative Commons) [^lookandfeel]. The limited members who participated in the project slowed the growth and the project also didn't focus much on the microcomputers of the 90s. 

#### Chapter 3: A Kernel of Hope

Linus Torvalds was born in Helsinki, Finland in 1969. He was swedish speaking kid (rare in Finland) and grew up loving microcomputers; however, while having strong research for Europe, Finland was disconnected from the a lot of the work being done in the United States and Britain, meaning that Linus needed to order parts to ship them home and use the internet to communicate with other developers. 

In 1987, computer scientist Andrew Tanenbaum released Operating Systems: Design and Implementation which discussed operating systems and a unix-like educational and simple OS, MINIX. After Linus purchased the book three years later, he was amazed by MINIX though didn't like the limited functionality (no terminal emulator/remote login, microkernel, or portability/POSIX compliance) and especially the price ($169); in particular, he thought an operating system should be $0 and didn't want financial compensation or donations. His parents, one of them a communist, the other an academic, influenced his software distribution thoughts. 

Therefore, he began to rectify this. He developed an assembly terminal emulator, then shifted towards disk/filesystem drivers which slowly pushed him into doing proper operating system development which occurred around 1991. Lack of academic resources or industry support made things harder for Linus; he needed to ask on the MINIX usenet group about POSIX standards, debugged via die-loops and use MINIX (including GNU) utilities. Tanenbaum disagreed with Linus' work, complaining that it was using a monolithic kernel and that it only worked on a 386 (particularly stinging to Linus as that was the only machine he had). He argued back against the microkernel and for it's portability due to the POSIX compliance in what would later be known as the Torvalds-Tanenbaum debate. 

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

Microsoft took multiple actions to attempt to stifle FOSS. First, they promoted the "shared source" model to let Microsoft keeps its IP rights while sharing the source to select partners, though this ended up not working out. Second, they backed the SCO Group which filed a lawsuit against IBM and other companies claiming that some of the Unix code was from the System V OS they released; Torvalds and other open source developers thought the company was just spreading fear about Linux rather than having genuine claims of copyright infringement. The lawsuit against Novell failed in 2007 and SCO Group would file for bankruptcy. Third, Microsoft backed a thesis by Kenneth Brown in 2004, "Samizdat: And Other Issues Regarding the 'Source' of Open Source Code", which argued that Torvalds copied directly from the MINIX kernel based on its complexity, criticized open source based on the fact that the origins of the code aren't known for sure, and argued that the GPL license is bad for the economy. The argument of copying was countered directly by Tanenbaum and further criticized by Stallman and Ritchie. 

The failure by Microsoft to stop open source showed the persistence that FOSS software had through legal precedent and the strong corporate backing. At the same time, the ideas of free software that Stallman highlighted started fading away with minimal backing from companies.

#### Chapter 6: Ending the FOSS Revolution?

At the turn of the millennium, FOSS was dominant in the server/developer space but in the decades to come, open source software came into consumer electronics as well. Microsoft collaborated more with Canonical (the creator of Ubuntu) and Google would create Android and Chromebooks (running a linux distro, ChromeOS). This isn't a complete shift on FOSS software; instead, the philosophy for these companies have shifted to using open source software in conjunction with their own proprietary software (for example, websites hosted on Microsoft Azure) as a means of reducing engineering effort. 

Android, initially created by Andy Rubin and Rich Miner as a camera software company, was acquired by Google in 2005 and set to develop a mobile OS to counter iOS; it notably used a Linux kernel and based on Google's efforts on promoting and distributing the OS was able to capture 90% of the mobile market share. However, Google didn't want to link Android to Linux or open source (the kernel was GPL licensed and the rest of the OS Apache licensed).

Canonical and Ubuntu were created in 2004 by Mark Shuttleworth in order to create a free accessible distribution. While supporting GNU developers, he found them too ideological and incorporated proprietary components in Ubuntu such as binary blobs[^redhatbinaryblob]. Ubuntu would conquer the server space (being the second most popular distribution) and get to 40 million desktop users[^ubuntupopularity]. The reactions were expected: Torvalds praised it for the ease of usability whereas Stallman criticized it for collecting user data for Canonical's marketing efforts. 

The trend of using FOSS software while still limiting user control continued through the 2000s/2010s. Cloud computing provided FOSS software online (such as Rackspace's OpenStack in 2010 to create standards for object storage) and this trend was viewed unfavorably by Stallman as it took away control from the user while taking their data. Embedded devices (such as TVs, thermostats, etc.) also starting using FOSS software but attempted to limit the ability to modify the free software on the device (also known as Tivoization, which was the motivating reasons for GPLv3).

The ideas of FOSS did spread outside of just software as well. Creative Commons, created by Lawrence Lessig, was a license inspired by Stallman and the GPL license which pushed scientific research/educational resources to be open. Wikipedia would be a notable adopter for the CC-SA license as well as following the 'bazaar' style of development with user contributions. Currently, the FOSS community is geographically spread across the world though predominantly white and male, which can be partly attributed to access to education/computers as well as FOSS leaders either being indifferent (Torvalds) or negative (Raymond) on the issue. 

I've been using the word FOSS but really the free software portion isn't relevant anymore; the loss of ideals has disappointed hackers/FOSS enthusiasts though they do get along more with those in the open source camp. Open source software itself has prospered and as new computing methods/standards come into play, so will the goals of FOSS adapt.

### Just for Fun: The Story of an Accidental Revolutionary ([Torvalds](https://en.wikipedia.org/wiki/Linus_Torvalds), 2002)

#### *Forward*

You get to see inside Linus' mind on many of the events that are covered and it was contrary to my preconceptions of him; instead of being a practical minded open source advocate, he's an engineer fascinated with the craft who likes to give back and provide the infrastructure for greater projects; I was initially slightly disappointed when I found that he minimally explored open source ideas from an ethical point of view (he did talk about it a little, mentioning how it can prevent hoarding). With that being said, I realize that free software focuses more on that rather than open source. I did appreciate him talking more about his personal life (upbringing, finding a house, many houses in Finland have saunas, his parents/sister, etc). One more caveat: the book dates itself, especially towards the end but from what I've read from him, I don't think he's radically changed his mind on most topics here.

#### Birth of a Nerd

Linus Torvalds was born in 1969 in Finland to two journalists who emigrated from Sweden. He grew up in a dysfunctional family as a odd-looking socially awkward kid who was smart academically and often went to his mom's or dad's place after his parents divorced. In Finland[^finlandball], it's a more quiet culture that prioritizes education (also he points out that its common for homes to have sauna rooms). The first highlight of his life was his morfar (grandfather on mom's side) buying him a Commodore VIC-20 (Linus viewed the computers he received as different highlights for his life). He would write out tons of programs, typing the example programs, then trying to read programs that were in English computer magazines including a morse code program. Linus would often stick himself away in his room with a computer for hours on end, even when his dad wanted him to get a new hobby. When he joined the University of Helsinki, he was one of the only students to major in computers and joined Spektrum, a social club for guys in hard sciences, though he put university on hold temporarily to do military service for 11 months.

#### Birth of an Operating System

A year before he started college in 1988, Linus purchased and upgraded Sinclair QL with extra RAM and used the EEPROM to include his self-written compiler and editor and began to work on writing video game clones (such as pac-man). He then read Tanenbaum's Operating System book which was the catalyst that led Linus to take a C and Unix class and learn more about Unix. He also obtained the limited MINIX teaching OS and he started modifying it to add a terminal emulator (using two threads, one for the display and the other for the keyboard) using the GNU C compiler.

Linus enjoyed being able to create his own world with his own constructed rules, analogizing it to physics. He also enjoyed the ability to get your code to work regardless of what computing environment it was in. After developing the terminal, he used it to log into the university computer to read emails and look at the MINIX news group discussions. However, Linus also wanted to download and upload things which would be quite challenging but, not having a heavy courseload and minimal social obligations, led him to implement filesystem driver functionality, shifting his work into a full operating system. However, to complete it, he worked to add POSIX standards[^posixsunmanual]. Ari Lemke, a TA at Helsinki, to set up the FTP directory to host "Linux" which he got by combining "Linus" and "Unix". Linus set up his kernel to boot the bash shell and worked on reimplementing the syscalls that were needed to make it work. Once this was complete, he was able to compile other programs (like ls and cp). He moved his shell work to a new partition on his drive, Linux. In 1991, he posted again to the comp.os.minix newsgroup,accnouncing that he was beginning work on a new operating system. 

Later, when he attempted to dial back into the internet, he accidentally dialed onto his Minix hard disk, leading him to switch to Linux. At this point, other people began using the OS and for the first time, Linus addressed a German's user request for page-to-disk, which motivated many other users to switch. Despite the growing usage, Linus didn't want compensation (despite his university loans and his mom working). He partly associates his viewpoint based on his work being built off the work of others, needing user feedback to improve his OS, and Finnish culture being much more against greed[^nickeintermission], going as far as to have a not-for-sale copyright license. However, he viewed the GPL license as a brilliant tool and, also somewhat influenced by a speech by Stallman, led to his decision to use the GPL license [^linusgplthoughts]. 

In 1992, Tannebaum wrote a post lamenting the Linux Kernel was using a monolithic approach (saying "among the people who design operating systems, the debate is essentially over. Microkernels have won") and that it wasn't portable. Linus, worried of his social standing in the online community was under threat by Tanenbaum's comments, harshly countered stating that unlike Minix, Linus was freely and right now available (even if a microkernel may theoretically be better), doesn't even do the microkernel design well (with multithreading issues), and that the his adherence to the POSIX API provided portability. 

That same year, he was a teaching assistant for the swedish language CS classes and three years later, he would be promoted to a research assistant which was doing Linux development work. Linus felt Linux become a big deal once the X Window System was ported to Linux, which added graphical capabilites. From a development leadership perspective, he took a laid back approach, allowing maintainers focus on the parts that they were most interested in and letting Linus stay low level. Linux continued to grow online too with the comp.os.linux user group grew to within the top 5 most popular newsgroups. He didn't have much of a life outside of Linux besides university obligations and reading emails, though he didn't mind. In 1993, while a TA for the Intro to to Computer Sciences, he instructed his students for homework to send him an email. Tove sent him a message asking him to a date and Linus agreed; they would later marry.

Version 1.0 of Linux releases in 1994 and Linus gives his first televised talk at the University of Helsinki with his parents and Tove in the audience[^linusfirsttalk]. 

#### King of the Ball

The growing interest in Linux gets him more corporate invitations: Novell, a networking company, invites him to California to talk about their desktop which was the first time Linus traveled to the states. A year later, he spoke at DECUS and got a DEC Alpha machine (RISC-based) which he used to port Linux to a new architecture. In 2000, he got to meet Steve Jobs (co-founder of Apple) and Avie Tevanian (principle designer/engineer on Mach microkernel while at CMU which served as the foundation of NeXTSTEP and macOS). He already disliked the kernel due to poor performance and large complexity. He was confounded that Steve was trying to sell him on supporting Apple with its kernel being open source when the rest of the OS was not and emphasizing the want for macOS to take more marketshare from Windows, which Linus didn't care about either. 

Despite continuing to lead development of Linux, Linus still worked for about 6 years in industry[^linusintel]. In 1996, Linus joined Transmeta, an x86 CPU company, despite worries from the Linux community about the company being funded by Microsoft. The year after, he finished his master's thesis and, during the same weekend, would have his first daughter (he would have two more over the coming months). In 1999, Red Hat and VA Linux IPOd and the shares in these companies made Linus a millionare.

Linus became the poster boy of Linux[^tuxorigin] and felt discontent with the portrayals the media had of Linux vs. Microsoft or the idealists vs. the pragmatists as oversimplified. He believed in commercial interests for Linux providing an alternative to Windows and was also comprimising when it came to Transmeta, working on proprietary software there, without beliving that he'd sellout. He dislikes the idea of people preaching or imposing their world views on others and dislike how dogmatic free software advocates can be such as Stallman complaining about software not using the GPL license. Linus' view is straightforward: it provides a development philosphy that can lead to good technology and prevents hoarding from competitors. Reflecting on the development, a part of Linus feels that he would have been overwhelmed early on if he thought through the logistical challenges of supporting all his users, though he highlights his insulation from the actual spread of Linux, which was happening across IT departments. 

#### End Sections 

(*These sections halt the auto/biography and instead Linus muses on different subjects. I'll be more selective on what I include and I'll speak from also my perspective as relevant.*)

The Amusement Ride Ahead: Linus makes a couple of when predictions on the future of computing and got a lot of hits. He predicted correctly the operating system will not be a big deal (which browsers helped with), that phones will take over as a hub for other devices (partly true), and they'll all be running Linux (Android did win most of the marketshare). His most incorrect prediction but also most fascinating was that he thought Sony would trojan-horse the PlayStation 2 into being a general computing device that would serve as a hub for other devices; that prediction is wrong but [Sony](https://en.wikipedia.org/wiki/Linux_for_PlayStation_2) [tried](https://en.wikipedia.org/wiki/OtherOS).

Why Open Source Makes Sense: Linus points out that he often has external discussions with businesses since they find that open sourcing their products may be risky (since they are giving up control). With that said, he does try to maintain his neutrality.

The Meaning of Life 2: I didn't include the first Meaning of Life section since it's repeated. Linus argues that people are motivated by survival, then social motivation, then entertainment and then says that Linux plays a role in his (and for community members) social motivation and entertainment.

### Free Software, Free Society ([Stallman](https://www.stallman.org/), 2002)

#### *Forward*

This was a drag. I was initially captivated by the way that Stallman laid out his ethical principles for software and how companies promoted proprietary software that restricted the user's freedoms; it was a breath of fresh air from the (mostly) development focus I read from "Just for Fun". But then it keeps going. And going. And keeps repeating the same points over and over, almost as if I'm listening to a proselytizer. It's just too much content and tries to address too many topics at once, with little effort to segment the topics properly. This book was constructed from many essays Richard Stallman wrote but it really should have been rewritten and edited to be more concise.

#### Part 1: GNU Project/Free Software 

Free Software Overview:

"Free software" is defined as the freedoms to run, study, redistribute copies and redistribute modified versions - the user controls the program rather than the program controlling the user. You should be able to run the modified software in place of the original software and there should be few limits on usage or modification. Despite the name, you can still charge for free software (and provide prebuilt binaries and the source code). In fact, it's important as it brings in development funds[^sourcepricelimit]. 

The "free" refers to the freedoms the user has (unlike "open source"). The software can be subject to distribution rules (ex. requiring an alternate form of distribution[^deltaappstore] as long as it doesn't substantially limit your freedom) or be subject to government export regulations. While not necessary, it is good for the software (such as GNU/Linux distros) to push users and prioritize interoperability with other free software. On the low-level software side, while the BIOS should be free, past that it's excusable since modern computer firmware below that isn't open. Free hardware isn't possible as it isn't feasible for a user to apply modified circuit/chip designs to their own machine. 

A Brief History of the GNU Project:

Back in 1971, the MIT AI Lab hackers wrote software for the PDP-11 but a decade later, that community of tinkers began to decline when some of them formed Symbolics and hired some of the AI labs. The lab put in more restrictive, modern computers (VAX, 68020) and the labs ethics now became software companies get to have power over users, only the functionality matters (ignoring the type of society that results from that), and that there is no usable software with company oversight. Feeling alarmed by the trend, Stallman set out to create a POSIX-compliant, free operating system for hackers: the GNU system. The announcement was put out on the net.unix-wizards and net.usoft newsgroups in 1983.

The GNU system's goal was to create a complete GNU system (C library, bash, gcc, etc.) to replace Unix and fill in the gaps of proprietary software. The first program Stallman started on was GCC (originally borrowing Tanenbaum's compiler, then attempting to rewrite a Pastel compiler to support C, then starting a new compiler from scratch) which ended up releasing in 1987. The first released GNU program was Emacs which released in 1985 as an alternative for vi/ed and was distributed in the mail for $150 for non-internet users. With Emacs came the GNU General Public License (GPL)[^librarygpl] which embodied the free software principles above. Stallman founded the Free Software Foundation charity that same year, getting profits from sold GNU software, source codes/manuals, and later members' dues. 

The GNU project was coming into fruition component by component by the 90s and was almost done by 1990 but was still waiting on the GNU kernel (GNU Hurd) due to difficulties of the microkernel architecture (debugging was particularly challenging between the individual servers sending messages to each other). A year later, Linus Torvalds released the Linux kernel which, when it became free in 1992, was combined to form GNU/Linux.

Challenges that arose included secret hardware that needed to be reverse engineered, non-free libraries (such as KDE) that required free replacements (GNOME), software patents which restricted some features like LZW compressions or MP3 playback, developing good documentation, and emphasizing the philosophy of freedom rather than the business utility.

Institutional Use of Free Software:

Proprietary software allows spying (telemetry), restrictions, censoring, and backdooring [^sass]. The state should also avoid these harms as its goal is to ensure freedom and the wellbeing of people; it should distribute free software (including their websites/file servers), not require nonfree programs, and ban computers within that require proprietary software. The government should also incentivize free software by pushing manufacturers to not require proprietary software, providing tax breaks for free software developers, and preventing tax writeoffs for manufacturers who donate their software to schools. In a similar way, schools should push their values of cooperation and freedom by using free software to allow gifted students to dive deeper into the software they use.

#### Part 2: What's in a Name?

Saying only "Linux" and not "GNU/Linux" obscures the history of free software[^othersoftwarecategories]. Linux is associated with businesses and company-developed nonfree software whereas GNU is associated with the ideology. Once Linus developed his kernel, he used it with the GNU system so his contribution, which comprised 3% of the OS, was similar to others such as Donald Knuth who created TeX. The integration of the kernel was substantial work and the FSF has to maintain a free version of Linux as well since Linux contains some proprietary binary blobs.

Open source associates itself with practicality rather than morality, or a development methodology vs. a social movement - the naming is also flawed in that it sounds like looking at source code. While not the enemy, they should be highlighted separately as the priorities are different. Open source advocates are more likely to be ok with proprietary software that can have negative consequences for the user (such as DRM). Finally, insulting names for proprietary software can be used to bring in humor and clarify what side you're on. 

#### Part 3: Copyright and Injustice

In the constitution, copyright has minimal focus, not seen as a required right but more so a necessary temporary incentive. There is often the argument of “striking a balance between publishers and consumers” which is the wrong interpretation since the benefit lies with consumers using copyrighted works and any benefit that publishers have should be in pushing that interest (incentivizing publishers to create more work by giving away some of the freedom of the readers).

Stallman argues for 10 years of copyright (which is how long a work lasts), though he notes that different types of work should have different lengths of time for protection (ex. points out that scientific articles shouldn't be paywalled). He also notes that while copyright was more suited during the age of the printing press (mainly preventing unauthorized book copying from other publishers), they are now used against individual users and their usage is tightly controlled.  

#### Part 4: Software Patents: Dangers to Programmers

*The rest of the sections were skimmed through so I have fewer notes on them.*

Patents are a monopoly on an idea that lasts around 20 years and software patents (which cover program algorithms, file formats) shouldn't exist, denying users the freedom to use their computers/software as they wish. According to a 2004 study \- Linux itself possibly violates 283 patents

#### Part 5: Free Software Licensing

The GPL license was created in 1989 to keep derivatives of software free and allow universal access to source code. Version 2 (released in 1991) was created with software patents in mind, explicitly writing that if the parties are subject to other legal agreements, the licensee is unable to distribute their software. The LGPL license was created for the GNU C library to allow it to be linked to other software if the library itself was made available. Version 3 (released in 2007) was created to address the issue of Tivoization (where hardware vendors would prevent users from inserting modified versions of the free software), provide restriction adding for compatibility with other free licenses and strengthening the patent requirements.

An interesting business model that comes up is selling exceptions of their software; in other words, a company provides a free version of their software but sells their software under a less restrictive license for companies to use.

#### Part 6: Traps and Challenges

*This section highlights a couple of the challenges that companies/users are going through with free software; these parts relate to JavaScript and gaming on Linux. There were more but they were either repeats of above or weren't too interesting to me to note down. I also don't agree with some of what RMS is saying but still wrote it down here.*

Most large JS programs nowadays are obfuscated/compacted and the real source isn’t provided and would not be considered free. To define nontrivial JavaScript, it would be any script that loads an external script, makes an AJAX request, uses dynamic constructs, or obfuscates its code (ex. non string literals with Obj.create()).

Valve is supporting Steam on Linux which is good in boosting adoption of GNU/Linux but bad in terms of having users use nonfree software. You can still have commercial games and the art doesn’t need to be free, but proprietary games should be avoided. 

#### Part 7: Value Community and Your Freedom

While compromise is important (ex. patent sections of GPLv3 or LGPL), the values of freedom should not be forgotten and including nonfree software in GNU/Linux (such as Flash) is contrary to the goals of the free software movement. Advocacy of free software is necessary to push people off of proprietary software.

### The Cathedral and the Bazaar ([Raymond](https://en.wikipedia.org/wiki/Eric_S._Raymond), 2001)

#### *Forward*

This book was interesting in the steps outlined on how open source is a development boon compared to proprietary software and the more sociological lens it uses when analyzing open source developers. With that being said, I find that, especially from a business perspective, a lot of his view holds up less; while there are contributors who will be motivated, a lot of the work (for example on the Linux kernel) is be done by employees of large businesses rather than dozens of individually motivated people. Maybe for smaller projects his analysis holds up more but once a project grows large enough, there needs to be some sort of sponsorship/backing for development to be sustainable (in general). With that being said, the text did have a significant influence in getting Netscape to open source their browser so the impact is definitely there.

#### A Brief History of Hackerdom

From 1945 to 1970ish, there was a culture of scientific computing, often with physicists or engineers. The early hacker culture started in 1961 when MIT got the DEC PDP-1 and it became a favorite for the Tech Railroad Club, where members would write programs; these people would form the MIT AI Lab. In 1969, ARPAnet, an experiment by DOD, would connect universities, labs, and defense contractors together.

With the release of the PDP-10 (1971), MIT created an ITS (Incompatible Timesharing System), a time shared operating system (which gives each user a small time slice to use the operating system) for their own software instead of using DEC's, which Raymond points to as kickstarting the culture that led to Emacs and GNU. In 1969, Ken Thompson made Unix at Bell Labs after working on ill-fabled Multics time sharing OS; Dennis Ritchie made C for Unix and in 1978, unix was rewritten in C. Unix was portable, easy to use, and included networking features, UUCP, that allowed remote execution of commands and transfers of files/emails/usenet (distributed discussion system). The latter led to usenet bulletin boards.

In the 1980s, the microcomputer communities took off. DEC stopping work on the PDP-10, killing ITS and Stallman started his Unix replacement and the FSF. The debate became Berkeley (BSD) Unix vs the proprietary AT&T Unix. By the beginning of the 1990s, MS-DOS and Mac hackers separate from Unix, commercial Unix was failing with high prices, and FSF failing to build out Hurd. In 1991 though, Linus Torvalds starts Linux kernel, notably avoids the cathedral method of a small tight-knit group of devs (BSD, GNU), but instead adopting the bazaar method of using many volunteers across internet. This method for developing Linux synergized Growth of ISPs and invention of world wide web.

#### The Cathedral and the Bazaar

Eric Raymond originally thought development would be cathedral-like, carefully constructed by specific people but after he saw Linux, he realized the bazaar-like approach, with different ideas/agendas coalescing into a kernel. Now he connects it to Fetchmail, an open source mail retrieval program he wrote, laying out lessons for creating good open source software:

- 1\) All good software comes by scratching a developer’s personal itch  
  - There is a higher quality standard.
- 2\) Good programmers know what to write. Great ones know what to rewrite (and reuse)  
  - Eric added onto fetchpop instead of writing a new POP client.
- 3\) Plan to throw one away; You Will, Anyhow  
  - Eric switched to more mature client popclient and was ready to start over. 
- 4\) If you have the right attitude, interesting problems will find you  
  - Carl Harris lost interest in maintenance so handed the project over to Eric.
- 5\) When you lose interest in a program, your last duty is to hand it off to a competent successor  
- 6\) Treating your users as co-developers is your least-hassle route to rapid code improvement and effective debugging  
  - With the source, users can be hackers and this is how Linux innovated via its development philosophy more than the kernel itself.
- 7\) Release Early, Release Often, And Listen to Your Customers  
  - Linus incorporated user-feedback and would release sometimes more than once a day, leveraging collaborators. Seeing constant improvements/changes will get the users' egos satisfied/curiosity driven.
- 8\) Given a large enough beta-tester and co-developer base, almost every problem will be characterized quickly and the fix obvious to someone. In other words, “*Given enough eyeballs, all bugs are shallow*” - Linus’ Law.
  - Both parts (finding and fixing the problem) happen rapidly.
- 9\) Smart data structures and dumb code works a lot better than the other way around  
- 10\) If you treat beta testers as if they're your most valuable resource, they will respond by becoming your most valuable resource.
- 11\) The next best thing from good ideas is recognizing good ideas from your users. Sometimes the latter is better.  
  - A user sent idea to use SMTP port for local mail delivery agent.
- 12\) Often the most striking and innovating solutions come from realizing your concept of the problem was wrong 
  - Eric ended up removing all mail delivery except for SMTP.
- 13\) Perfection (in design) is achieved not when there is nothing more to add but when there’s nothing to take away
- 14\) Good tool is intendedly useful, a great tool is unintendedly useful too  
- 15\) For gateway software, don’t modify/delete data stream info unless requested by the user  
- 16\) Syntactic sugar can be good for simple non-turing languages  
- 17\) Don’t do security by obscurity
- 18\) To solve an interesting problem, find a problem interesting to you  
- 19\) Provided development coordinator has communications \>= internet and leads without coercion, more people is better  

Software product management in open source is self-organizing, self-motivated with thorough self-review via personal enjoyment which beats standard corporate projects. Open source can also maintain sustained development for one goal similar to proprietary software. Multiple factors facilitated the bazaar style of development: the growth of cheap internet to remove access barrier and connecting selfish ends of hackers (ego) to  the difficult ends of cooperation.

#### Homesteading the Noosphere

*This essay is a social analysis of open source communities.*

Open source culture influenced by zealotry (commitment to method itself) and commercial hostility (strongly against supporting corporations). The FSF exerted that cultural energy with its zealousness and anti-commercial sentiments (though RMS denies second charge). The pragmatists work/develop open source tools but also use commercial software, only being moderately anti-commercial (mainly against tech giants) and don't buy into everything the FSF says. Linus represents the 'pragmatists', looking favorably on commercial linux distros  

The meaning of ‘ownership’ for an open source software is the person who the community recognizes as the one with right to distribute modified versions. A project is acquired when founding a new one, transferring an existing project, or picking up a deserted project. These practices have been consistently followed, encouraging public accountability/retaining commit history. 

Gift culture means that social status based on giving away compared to exchange culture (the free market) or a command hierarchy (a family, government, etc.). ‘Hackers’ fall under this with them gathering prestige and cooperation based on their work. Good gift qualities include extending the ‘noosphere’ rather than duplicating work, commit to hard/boring work (debugging, docs), and extending used features over creating novel unused features. Despite relying on ego for building, there is a taboo against ego-driven behavior, with a culture of humility instead (constrasting this with the flamboyant 'warez' community). There is also a emphasis on meritocracy and creators (ex. Torvalds, Larry Wall) don’t want a cult of personality.

In terms of project structures (characterized as lockean property where individuals have claims to property from a community to minimize friction/maximize cooperation), the simplest is one maintainer, the second is benevolent-dictator with maintainers, and the last is a voting committee (ex. Apache).

*I didn't finish this book so my notes stop here.*

### Bonus!: Linus' Master of Science Thesis - [Linux: A Portable Operating System](https://www.cs.helsinki.fi/petri/index_files/linus.pdf) (1997)

#### *Forward*

I didn't need to read this at all lol, but I was curious what I'd get here. Linus is quite verbose when describing the different challenges he faced while writing the kernel but that's to be expected from a masters thesis. There is a mega emphasis on portability and especially using the Linux kernel machine to assist in abstracting the software interface, hardware interface, memory management (separate page tables for code that can be shared and code that's arch dependent), etc. He didn't talk about how he created page-to-disk sadly (or swapping as known today). Also note that Linus did emphasize that a lot of the kernel code (and all the GNU code) came from the outside in the acknowledgements.

#### 0. Intro

The most important goal of the Linux Kernel was portability (both in terms of hardware, working on different CPU architectures, and software, being compatible with different operating systems). A mechanism to aid this is the Linux kernel virtual machine - it provides two layers: one between the kernel and userspace (exposed at syscalls) and one between the kernel and the hardware (provided via drivers). The rest of the paper sections will go over different design challenges and solutions.

#### 1. Linux Design/Implementation

Linux doesn't use a microkernel (splitting the kernel into chunks) due to performance issues. Also, as the kernel is open source, it can be configured to add or remove specific features at compile-time. 

#### 2. Compatibility

The design for achieving compatibility was ensuring UNIX compatibility which limits the userland-kernel interface. 

The standardized Linux components across architectures include process handling, memory management, a file system, network access, drivers (each divided into its own folder), and the virtual machine implementation. For each separate hardware architecture, inline assembly can map any VM semantics onto the hardware to minimize performance loss.

#### 3. Software Interface Portability

This is constrained by adhering to the POSIX interface [^personalities].

#### 4. Hardware Portability Issues

While a C compiler does provide cross platform compilation, there are still a host of issues. First are data issues: consistent data sizes are important for networking and file systems so a types header file is required for some platforms. Byte alignment (or an object being stored at an address that's a multiple of 8/4/etc.) is assumed with a trap handler to catch exceptions. Byte order uses functions to convert between big-endian and little-endian.

Memory management must be fast and simple, even without hardware standards. Modern CPUs have a feature known as a Translation Lookaside Buffer (TLB) which shows recent translations of virtual memory to physical memory but the method of handling virtual memory translation varies across the system architecture [^morememorymanagement]. To solve this incongruity, the Linux kernel uses the kernel vm to split memory management into (at least) two page tables, with one dedicated to the kernel VM and the other to the architecture-specific CPU. The TLB and the page tables must be kept in sync.

Cache coherency (syncing multiple processor caches) is also required [^instructionvsdatacache]. For multiprocessor handling, atomicity is provided for kernel data structures via kernel locks. Finally, device drivers (which comprise half of the kernel) provide I/O abstraction though the PCI standard is helping cut down on the work.

## Articles, Talks, and Interviews with Linus Torvalds

### *Forward*

As these notes are on YouTube videos or articles, they are going to be a bit more disjointed that the book summaries above; with that being said, there can be interesting information about Linus's thoughts on the development of the Linux kernel, talking about open source, the way he talks/treats others, etc. I cut a lot of notes because they either repeat information or aren't that interesting.

### DebConf 14: [Q\&A with Linus Torvalds](https://www.youtube.com/watch?v=7SofmXIYvGM) (2014)	

- Distribution? He wants an easy distribution since he's not good at managing systems.
- "Year of the Linux Desktop": Chromebooks help, the main issue being application packaging which is difficult to solve since they require many packages and can't rely on the system. Valve will help standardize this.
- Kernel's hard rule: DON'T BREAK USERSPACE. 
- Inflammatory language: he doesn't care. He cares about the technology and dislikes political correctness (saying that the culture he grew up in was more abrasive *probably referring to his family* and that he has thick skin). With open source, you can more easily find the people you like but you need to earn respect.
- GPL: v3 undermined it, v2 was more straightforward in giving source and getting changes back whereas v3 further restricts on it can be used on your device. Linus purposefully kept the license to be v2 and disliked how sneaky the FSF was for GPLv3. Specifically, he was told that the tivoization clause could be invalidated which was dishonest so he doesn't want to have anything to do with the FSF (with some people there too extreme/crazy). Linus doesn't care about Tivoization since he argues that that is the right of the manufacturer even if he doesn't like it. 

### [TED Talk: The mind behind Linux](https://www.youtube.com/watch?v=o8NPllzkFhE) (2016)

- Linus' home office is comprimsed of plain light green walls that limits stimulation, a silent computer, and a cat. He is alone and enjoys programming (he doesn't like people but he likes his computer).
- A friend at Helsinki introduced Linus to open source licenses (*he mentioned in different contexts that it was a talk by Stallamn that taught him about licenses*). While he worried initially about his work being take aadvantage, the revelation was getting feedback from others.
- Git: there was about 1000 people involved in every release every 2 months. The goal was to replace CVS to improve its scalability. 
- His main qualities are his stuborness and persistence.
- He doesn't relate to other's feelings which is something he feels bad about but points to the fact that open source lets you pick who you want to work with, though he does acknowlege that you need warm people to welcome you into the project and also have a good user interface, but he's more concerned on the engineering side.
- Linus doesn't see himself as a visionary but a strong engineer: again, it's perspiration (Edison) rather than being a visionary (Tesla).

### [Aalto Talk](httpdds://youtu.be/MShbP3OpASA) (2012)

- Commercial: Linus likes easy availability of Linux from commercial interests even after he was initially nervous (but they help with QA/UI work). He enjoys staying on the engineering side even he doesn't do much programming anymore, but mostly communication.
- For the desktop: most consumers don’t want to install an OS so you need preinstalls  
- Kernel dev community runs very deep; if he dies, things will continue.
- Academia: Linus loves abstract CS at University of Helsinki, but didn’t continue with academia because he hates papers. If you can’t see beginning to end, then it isn’t fun On the contrary, he loves startups (Transmeta) with early technical development but loses interest when the focuses shifts to the IPO. For startups generally, he believes in adding a special edge on a boring open source base.
- Nvidia, fuck you  
- Believes in specialization (not every child should do programming), but everyone should get the possibility to tinker with computers  
- Execution is more important than vision: genius is 99% perspiration and 1% inspiration; sign of passion is someone who can solve all the problems with ideas but he believes in hard work and passion
- He doesn’t game but wants gaming platforms to be more open though he understands razer blade approach of consoles. There are not a lot of good open source games, so there would need to be a different mindset for that.

### [BBC Article](https://www.bbc.com/news/technology-18419231) (2012)

- Open source is based on selfish motives, even if not necessarily for financial reward (pleasure of tinkering and wants to get more people into that).
- As kernel has gotten more complex, it has become more difficult to get into development, but there’s no shortage of developers. 
- Linus is glad that Microsoft doesn’t see Linux as the enemy.

### [Linux Foundation Interview](https://www.youtube.com/watch?v=cPvRIWXNgaM) with Dirk Hohndel (2024)

- RISC-V: even when doing open hardware, hardware people are different than software people as there is a big gulf between verilog/kernel and software devevelopers. Furtheremore, it's making the same mistakes that ARM/x86 did.
- XZ situation: Open source relies on trust which can be violated so it's an open problem on figuring out when its violated. 
- AI/LLMs: he doesn’t want to part of the hype, but finds it interesting and is optimistic about AI to find bugs as a tool since kernel tools can be hard to use  

### [New Yorker Article](https://www.newyorker.com/science/elements/after-years-of-abusive-e-mails-the-creator-of-linux-steps-aside) (2018)

- Linus is known as “Benevolent dictator for life” for Linux and reviews every line of code merged
- He temporarily stepped away and apologized after getting questions about his conduct from the New Yorker
- In 2013, he was very against buying into what he saw as "the fake politeness, the lying, the office politics and backstabbing, the passive aggressiveness, and the buzzwords. Because THAT is what ‘acting professionally’ results in: people resort to all kinds of really nasty things because they are forced to act out their normal urges in unnatural ways."
- Sharp, a former kernel developer, said that he doesn't discriminate with this language and despite her suggestion against negative feedback without abusive language, Torvalds thinks the stakes are higher than being polite.
- Aurora, another former kernel developer, noted that the aggressive communication created a leadership model of being an asshole (leading to a sexist environment).
- Torvalds had an unenforced general Code of Conflict in 2015 though later in 2018 a new Code of Conflict was created.

## Thoughts

- Stallman highlights tax breaks/financial incentives for developers creating FOSS, which sounds interesting
- Key difference: "A development methodology vs. a social movement" - the open source initiative really does cover the ideas Stallman advocated for, but there is definitely a de-emphasis on the moral ideas
- His philosophy seems archaic and non feasible even a decade ago - almost all modern software will connect to a cloud service and the rise of AI tooling has only accelerated that change.
- Speaking of AI, the [Open Source AI Definition from the OSI](https://opensource.org/ai/open-source-ai-definition) focuses on open source machine learning systems, highlighting data access (where to obtain the data, how its labeled, processed), the code for training/running the system, and the weight parameters for models. 
- The Free Software Foundation's (and Stallman's) message feels outdated and not providing a realistic go-to action for its supporters to take. I get that the organizations influence was naturally going to decline as the open source movement grew and splintered on their own. With that being said, the FSF is unique in its specific advocacy and there needs to be a change in the organization for it to make its message more actionable and modern. The EFF is a good modern example of what a digital advocacy group should be, especially with very direct call to actions.
- Torvalds didn't come across as the 'open source' leader - this tracks with what Raymond stated that most of these FOSS leaders would rather be humble - he is laid-back on many FOSS issues and doesn't go too deep into advocacy on open source. He's probably content with his role on being the leader of the kernel - it's a bit disappointing. 
- RMS' controverisal comments hurt his standing in the FOSS community (especially on the Jeffrey Epstein scandal about the actions of MIT professor Marvin Minsky though he partially apologized in 2021 when coming back to the FSF board); while some of RMS' statements were mischaracterized, he made some [damning](https://drewdevault.com/2023/11/25/2023-11-26-RMS-on-sex.html) statements.
- Linus used Bitkeeper; he says that open source is the only right way to do software but to use the best tool for the job.

## Other Sources

- [The story behind Open Source Software, Saumo Pal](https://www.btw.so/blog/history-of-open-source-software/)
- [StackOverflow - What are operating-system personalities?](https://stackoverflow.com/questions/52136857/what-are-operating-system-personalities)
- [Wikipedia - Avie Tevanian](https://en.wikipedia.org/wiki/Avie_Tevanian)

[^manpages]: The first man pages were created in 1971. 

[^at&tnotes]: This restriction stemmed from a 1956 decree from a DOJ lawsuit against AT&T. 

[^railroadinfo]: Both Steven Levy and Eric Raymond point to the MIT Tech Railroad Club as originating the values of cherishing computers, working on interesting problems, a meritocratic place to work, etc. While inspecting the arguments that Steven Levy and Eric Raymond make, Tozzi argues that both of their focus on the MIT Railroad Tech Club is too narrow. General ideas of public accountability, resisting authority and meritocracy are historical values that arose from the French Revolution and the Revolutionary War. The FOSS principles and hackerdom originate more from academia with (fitting that these would also appear in an MIT research lab). The hackers who developed FOSS software were continuing the ideas that formed during Unix. 

[^newsgroups]: Looking at TechTarget, Usenet allowed researchers/academics to share information/ideas via an online discussion forum - it used the Network News Transfer Protocol (NNTP). 

[^lookandfeel]: There was a battle for ‘Look and Feel’ where software patents which could protect the idea/concept behind software. In 1989, Stallman founded League for Programming Freedom, a separate organization to combat above issue (GNU promoted it)  and by in 1995: Apple lost lawsuits against HP/Microsoft about look and feel.

[^bsdinfo]: At UC Berkeley, Kevin Bostic led a team to separate BSD code from AT&T Unix to make a free software version. In 1989 and 1991, networking code would be added to BSD but a year later, Unix Systems Labs (the company which took over Unix from AT&T) sued Berkeley System Design (which was founded by Berkeley students part of the Computer Systems Research Group, or CSRG). After AT&T bought 20% of shares in Sun Microsystems in 1987 and collaborated to create Unix System V, a consortion of companies afraid of not being part of the standardization process came together to form the Open Source Foundation, a body which focused Unix standardization (but not FOSS). This body didn't materialize much.

[^gnomeinfo]: GTK developed in conjunction with GIMP. The pressure on Troll Technology caused them to relicense first to the Q Public License and later to GPL in 2000. Victory for FOSS; even if ‘open source camp’ would be ok with Q Public License, showed that compromise wasn’t necessary  

[^moreapacheinfo]: Notably project didn’t follow ‘Benevolent Dictator’ but allowed multiple developers to directly control code. Apache Group also initiated Jakarta (1999), developing programs based on Java, and incorporated into Apache Software Foundation to develop Apache HTTP Server and other projects. Would later host nearly 300 FOSS projects (including Hadoop/Cassandra).

[^randomapple]: Apple in 2001 worked on creating OS X based on a mach kernel and BSD components. There was animosity towards Apple from Linus: Jobs tried bringing Torvalds over by emphasizing Mach base despite closed Mac layer and Torvalds also disliked his assuming attitude that he cared about Apple’s market share. Stallman was more unenthusiastic about Jobs: despises restrictions Apple products have to prevent them from installing software of their won choice

[^moreopenvsfoss]: Eric Raymond's hypothesis of the anti-commercial idealists of free software vs. the pragmatic open source developers was inaccurate in some ways. Stallman supported corporations developing software and was compromising in some ways (for example, the LGPL license).  

[^netscapeinfo]: Raymond’s notion of Linus’ Law (more devs minimizes bugs) and the development methodology and analogy he drew of the cathedral and the bazaar was quite novel compared to Brook’s Law. This utilitarian appeal over ideology as well as recognizing previous FOSS work moved Netscape executives to open source their code (1998). Netscape also looked to the community when picking a license (not finding BSD/GPL appropriate) and this led to the Netscape Public License and Mozilla Public License (for code after open sourcing); while FOSS leaders viewed this positively, few developers improved Netscape and the project faltered until 2003 when AOL (owner of Netscape) reduced support for Mozilla; a setback but one the open source community could push through.  

[^ubuntupopularity]: Shuttleworth argues that Ubuntu focus on usability, commercial backing, and willingness to ignore factions of its userbase contributed to its popularity.   

[^personalities]: There was also the idea of operating system 'personalities' which was the idea that the same platform may have multiple interface abstractions (besides just POSIX). (As seen on the man page, "Linux supports different execution domains, or personalities, for each process... among other things tell Linux how to map signal numbers into signal actions". While popular in the 90s, the rise of virtualization killed this idea).

[^morememorymanagement]: Operating system page tables handle translating virtual addresses to physical addresses since processes are given the illusion of a continuous address space and need to have a mechanism to translate the addresses.  Different CPUs have different methods for handling virtual memory (such as using page table trees (or multiple levels of page tables), a hash table, or even no architecture-specified page tables). 

[^instructionvsdatacache]: Instruction caches are handled by invalidating stale cache entries (if there's an update in one CPU or core, the other CPUs or cores marks their cache entries as stale) while data cache coherency is more complex. 

[^posixsunmanual]: While he asked for them in 1991 on the comp.os.minix newsgroup, nobody responded so Linus initially used the SunOS documentation owned by the university. 

[^nickeintermission]: Linus preferred receiving postcards acknowledging his work. Also Nicke, Linus' dad, said that his communist politics led to Linus being teased so Linus wanted to diassociate from his dad's political views, though Tozzi argues that his views did influence Linus Torvalds.

[^linusgplthoughts]: However, Linus states that he is not a GPL-freak and doesn't think all software should be GPLd, but rather should be up to the creator of the software to decide the appropriate license.

[^linusfirsttalk]: It was not his first talk; in 1993, Linus gave his first public talk at the Netherlands Unix User Group. 

[^tuxorigin]: The origins of the penguin design are disputed. Tove says she inspired Linus whereas Linus says he got the idea from two high ranking Linux developers. Regardless, Tux was support to look cheerful (Torvalds sees the cheeriness as Tux drinking beer and having great sex) and distinctive. Larry Ewing drew the mascot.

[^linusintel]: He wanted to intern at Intel but had visa issues so he continued to stay in Helsinki.

[^finlandball]: Linus was later invited to Finland's "President's Ball" (or Independence Day Reception).

[^deltaappstore]: This is interesting since that means free software (not sure about GPLv3 yet) does allow preventing distribution on certain platforms, so what's done here, preventing using the Delta code on the app store, is (probably) kosher: https://github.com/rileytestut/Delta/blob/main/README.md

[^librarygpl]: GNU Library GPL (used with GNU C Library) was a special copyleft exception that allows linking of proprietary software. Since the C library was generic in preventing usage with non-free systems, that would discourage the use of that library so it's a necessary comprimise to ensure that GCC is used further.

[^sass]: Software as a service enables all of these harms and also risks locking yourself into a network.

[^sourcepricelimit]: There is one exception: the GPL license requires source code provided so if only a binary is provided, there’s a price limit for the source.

[^othersoftwarecategories]: There is also noncopylefted free software, also known as public domain software. In terms of nonfree software, this can include software that prevents redistribution and freeware/shareware.

[^redhatbinaryblob]: Edit: Red Hat's distributions (CentOS, Fedora) also included non-free firmware - credit to Sachin.