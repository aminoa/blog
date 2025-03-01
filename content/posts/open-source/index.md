---
title: 'Notes on Free Software and Open Source'
date: 2025-02-25T16:04:00-04:00
draft: false
summary: Reading I did on Linus Torvalds, the FOSS movement and Richard Stallman
---

## Forward

Last summer, before writing Feature, I wanted to improve my knowledge of the history of open source software. While I initially focused on Linus Torvalds, I broadened my research (mainly reading books/articles but also watching YouTube videos) to focus on the movement as a whole. This post won't be as polished as my previous one; it is more of a research document rather than a regular blog post. Regardless, you may find this fun to read! If you take nothing else from this post, read [For Fun and Profit: A History of the FOSS Revolution (2017, Tozzi)](https://mitpress.mit.edu/9780262551786/for-fun-and-profit/) - it was the best summary of the FOSS movement I've read.

- [Forward](#forward)
- [Book Summaries](#book-summaries)
  - [For Fun and Profit: A History of the FOSS Revolution (Tozzi, 2017)](#for-fun-and-profit-a-history-of-the-foss-revolution-tozzi-2017)
    - [Chapter 1: The Path to Revolution Unix and the Origins of Hacker Culture](#chapter-1-the-path-to-revolution-unix-and-the-origins-of-hacker-culture)
    - [Chapter 2:](#chapter-2)
    - [Chapter 3:](#chapter-3)
    - [Chapter 4:](#chapter-4)
  - [Just for Fun: The Story of an Accidental Revolutionary (Torvalds, 2001)](#just-for-fun-the-story-of-an-accidental-revolutionary-torvalds-2001)
  - [Free Software, Free Society (Stallman, 2002)](#free-software-free-society-stallman-2002)
  - [The Cathedral and the Bazaar (Raymond, 2001)](#the-cathedral-and-the-bazaar-raymond-2001)
  - [(Bonus: Linus' Master of Science Thesis) - Linux: A Portable Operating System (1997)](#bonus-linus-master-of-science-thesis---linux-a-portable-operating-system-1997)
- [Timeline](#timeline)
- [Thoughts](#thoughts)
- [Philosophy of Richard Stallman](#philosophy-of-richard-stallman)

## Book Summaries

***It's telling that most of these books are over 20 years old....***

### For Fun and Profit: A History of the FOSS Revolution ([Tozzi](http://christozzi.com/), 2017)

#### Chapter 1: The Path to Revolution Unix and the Origins of Hacker Culture

Unix, developed by Bell Labs, served as the origin of open source despite starting off as a closed source project - a community sharing and developing source code for fun. Ken Thompson and Dennis Ritchie began developing a Multics OS replacement while working at Bell Labs to run Space Invaders on the [PDP-7](https://en.wikipedia.org/wiki/PDP-7). This involved redeveloping an assembly file system, shell, and processes for the machine -  this became known as Unix [^manpages]; Unix was rewritten in C in 1973 to assist in porting the operating system to other machines. At the time, AT&T (which was the parent company of the Bell Systems and its research subsidiary, Bell Labs) was legally barred from commercially entering the computer industry [^at&tnotes]. AT&T licensed the product and distributed the source code to educational institutions and companies for $20,000.

Unix was not open source but AT&T and the corresponding research institutions pioneered the FOSS ideals that would later coincide with the 'hacker ethic', the social, political, and cultural values of meritocracy, resisting authority, and cherishing interesting problems with computers Specifically, it followed a rolling release model, had open bug reports, allowed other organizations to participate in its development without restrictive licenses, and a growing, rebellious, anti-corporate community spread across Unix user groups and the Unix newsletter. The ideas of academia (sharing of ideas, decentralizing authority, and peer-review) also had a significant influence on FOSS, partly because many of these projects arose from research institutions like MIT and UC Berkeley[^railroadinfo].

#### Chapter 2: 

In 1984, the Bell System was broken up and AT&T now could commercialize Unix (quintupling the price to $100,000) which stifled both Unix and BSD. Binary only distribution became more commonplace (ex. 1983 with IBM), the shift to consumer microcomputers shifted the industry away from research computers like the PDP, and alternatives like BSD were limited [^bsdinfo]. Industry efforts like the standardization focused Open Source Foundation also lacked impact. This decay would change with Richard Stallman's efforts on the GNU project.

Richard Stallman was born in 1953 in NYC. He was weird, autistic and split between two single parent households. While he was at Harvard, he visited the MIT AI Lab and loved the programming within the hacker community; he decided to drop out of MIT PhD later to work at the AI Lab. Multiple incidents within this lab shaped his view on software.

In 1980, there was a Xerox printer that jammed frequently and required someone to monitor the it. To set this up, Stallman went to Harvard to retrieve the source code and modified it to enable that functionality. He later wanted to get the source code for a different printer from Carnegie Mellon University but was denied because of Xerox's NDA, alarming him that proprietary software didn't align with values of sharing, transparency, or collaboration. In 1982, the AI lab programmers began to defect: at first to Lisp Machines, Inc by Richard Greenblatt and then the rest to VC-funded Symbolics which recruited the rest of the programmers. 

After, Stallman announced a free Unix-like OS, GNU, on the net.unix-wizards and net.usoft newsgroups on Usenet[^newsgroups]. Stallman stalled (lol) writing a compiler since adapting preexisting C compilers was challenging, so instead worked on a rewrite of James Gosling's gmacs, or GNU Emacs. Bash, a C compiler, and Unix utilities (like ls and make) were later developed and added. Stallman also began to invest in the legal side of GNU, bearing GPL in 1989 as the largest innovation, a lawyer-friendly copyleft license that could embody FOSS values across any piece of software.

This period also marked the beginning when the corporate support of free software began. Cygnus Solutions, founded in 1989 by GNU Debugger adn GNU Binutils' maintainers John Gilmore, Michael Tiemann, and David Henkel-Wallace, provided support services for free software and would later merged with Red Hat a decade later. By 1988, GNU started receiving donations from HP and Software Research Associates.

There was one wrinkle; by 1990, there still wasn't a kernel. Stallman initally went with the TRIX kernel but switched to CMU's Mach kernel since the TRIX kernel was only written for a Motorola 68000 and Microkernels were considered the future of operating systems but he needed to wait for the AT&T components to be stripped first. A year later, GNU Hurd based on the Mach kernel began development. The "design turned out to be a research project" and requiring cross compatibility didn't help matters. 

GNU was overall successful based on Stallman's leadership (projecting a strong vision of the project, comprimising in areas that mattered, an example being the Library GPL license scaling a back from GPL for the sake of adoption), institutional support, and the legal focus (GPL and Creative Commons). The limited members who participated in the project slowed the growth and the project also didn't focus much on the microcomputers of the 90s. 

#### Chapter 3:

Linus Torvalds was born in Helsinki, Finland in 1969. He was swedish speaking which was quite rare in Finland. He grew up and loved microcomputers though needed the internet to communicate with other developers. His parents, one of them a communist, the other an academic, influenced his software distribution thoughts. 

In 1987, computer scientist Andrew Tanenbaum released Operating Systems: Design and Implementation which discussed operating systems and a unix-like educational and simple OS, MINIX. After Linus purchased the book three years later, he was amazed by MINIX though didn't like the limited functionality (no terminal emulator/remote login, microkernel, or portability/POSIX compliance) and especially the price ($169); in particular, he thought an operating system should be $0 and didn't want financial compensation or donations.

Therefore, he began to rectify this. He developed an assembly terminal emulator, then shifted towards disk/filesystem drivers which slowly pushed him into doing proper operating system development which occurred around 1991. Lack of academic resources or industry support made things harder for Linus; he needed to ask on the MINIX usenet group about POSIX standards, debugged via die-loops and use MINIX (including GNU) utilities. Tannenbaum disagreed with Linus' work, complaining that it was using a monolithic kernel and that it only worked on a 386 (particularly stinging to Linus as that was the only machine he had). He argued back against the microkernel and for it's portability due to the POSIX compliance in what would later be known as the Torvalds-Tannenbaum debate. 

From here, contributors began to add to Linux, with page-to-disk (swapping), X Window graphics, and networking. Linus decided to license the project as GPL despite the fanatical community and indifference to free software principles since he did agree that the license encouraged collaboration. Companies such as Red Hat and SUSE S.A began commercializing the project. 

There was a bit of a fracturing between the Linux and GNU communities. Linux's free spirit of decentralized development with commercial activity contrasted with GNU's more centralized careful approach. Stallman also was very discontent that the entire OS was named 'Linux' rather than 'GNU/Linux', sidelining the ideology of the software in favor of the development methodology as well as the fact that GNU was the majority of the code. Regardless, Linux was able to succeed in part due to the timing (the struggles of Hurd, the BSD lawsuits, the growing internet and email access to send in patches to minimize barriers for contributing), the GPL license, and the free cost of the OS itself.

#### Chapter 4:




### Just for Fun: The Story of an Accidental Revolutionary ([Torvalds](https://en.wikipedia.org/wiki/Linus_Torvalds), 2001)

### Free Software, Free Society ([Stallman](https://www.stallman.org/), 2002)

### The Cathedral and the Bazaar ([Raymond](https://en.wikipedia.org/wiki/Eric_S._Raymond), 2001)

### (Bonus: Linus' Master of Science Thesis) - Linux: A Portable Operating System (1997)

## Timeline

- 1964: Initial development of Multics, a time-sharing OS from MIT, General Electric, and Bell Labs
- 1969: Ken Thompson and Dennis Ritchie begin developing Unix to replace Multics
- 1973: Unix is rewritten in the C programming language
- 1978: Development of BSD, a Unix alternative, begins

- 1983: Richard Stallman launches the GNU project
- 1985: Release of Emacs, the first GNU project
- 1989: Launch of GPLv1 license
- 1991: Linus Torvalds starts the Linux Kernel
- 1994: Ian Murdock, with support of the FSF, launches Debian
- 1994: Red Hat formed

- 1998: Open Source Initiative founded by Raymond
- 1998: Bash rewritten
- 2001: The Cathedral and the Bazaar released
- 2005: Linus creates Git 
- 2008: GitHub founded

## Thoughts

- Tax breaks/financial incentives for developers creating FOSS  
- A development methodology vs. a social movement

## Philosophy of Richard Stallman

- Enveloped in controversies later stalled him  
- His philosophy seems archaic and non feasible even a decade ago  
- His movement has primarily an ethical view, not a technological one
- GNU/Linux debate \- his values are right but there's an advocacy limit before people want to tune you out and RMS has not found his limit  
- Epstein Controversy: Got back on the open source board in 2021, but furthered decline of his influence.

[^manpages]: The first man pages were created in 1971. 

[^at&tnotes]: This restriction stemmed from a 1956 decree from a DOJ lawsuit against AT&T. 

[^railroadinfo]: Both Steven Levy and Eric Raymond point to the MIT Tech Railroad Club as originating the values of cherishing computers, working on interesting problems, a meritocratic place to work, etc. While inspecting the arguments that Steven Levy and Eric Raymond make, Tozzi argues that both of their focus on the MIT Railroad Tech Club is too narrow. General ideas of public accountability, resisting authority and meritocracy are historical values that arose from the French Revolution and the Revolutionary War. The FOSS principles and hackerdom originate more from academia with (fitting that these would also appear in an MIT research lab). The hackers who developed FOSS software were continuing the ideas that formed during Unix. 

[^newsgroups]: Looking at TechTarget, Usenet allowed researchers/academics to share information/ideas via an online discussion forum - it used the Network News Transfer Protocol (NNTP). 

[^lookandfeed]: Battle for ‘Look and Feel’, software patents which could protect the idea/concept behind software, which copyright law didn’t cover  
- 1987: SoftKlone won legal battle over look and feel of its programs  
- 1989: Stallman founded League for Programming Freedom, separate org to combat above issue (GNU promoted it)  
- 1988-95: Apple filed (and eventually lost) lawsuits against HP/Microsoft about look and feel   

[^bsdinfo]: At UC Berkeley, Kevin Bostic led a team to separate BSD code from AT&T Unix to make a free software version. In 1989 and 1991, networking code would be added to BSD but a year later, Unix Systems Labs (the company which took over Unix from AT&T) sued Berkeley System Design (which was founded by Berkeley students part of the Computer Systems Research Group, or CSRG). After AT&T bought 20% of shares in Sun Microsystems in 1987 and collaborated to create Unix System V, a consortion of companies afraid of not being part of the standardization process came together to form the Open Source Foundation, a body which focused Unix standardization (but not FOSS). This body didn't materialize much.