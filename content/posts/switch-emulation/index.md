---
title: 'Nintendo is killing Switch Emulation via Murky Legal Theory'
date: 2024-10-02T17:07:07-04:00
draft: false
---

*All legal discussion is relevant to the United States only. Please don't use any of this as legal advice. If you find any errors with this article, please send an email to [a@stalereference.com](mailto:a@stalereference.com).*

On October 1st 2024, GDKChan took down the Ryujinx organization from GitHub after contact with Nintendo.

As you will see, emulation and reverse engineering law are intertwined legally. 

(Show notice of Yuzu site image)

## Table of Contents
- [Table of Contents](#table-of-contents)
- [Why is Switch Emulation Development Important?](#why-is-switch-emulation-development-important)
- [History Time! Sega, Sony, and Establishing Fair Use via Reverse Engineering](#history-time-sega-sony-and-establishing-fair-use-via-reverse-engineering)
  - [1992: Sega vs. Accolade, (Lawsuit)](#1992-sega-vs-accolade-lawsuit)
  - [2000: Sony vs. Connectix, (Lawsuit)](#2000-sony-vs-connectix-lawsuit)
  - [2000: Sony vs. Bleem!, (Lawsuit)](#2000-sony-vs-bleem-lawsuit)
- [Things Aren't So Settled: The Digital Millenium Copyright Act](#things-arent-so-settled-the-digital-millenium-copyright-act)
- [Nintendo's Actions against Emulators](#nintendos-actions-against-emulators)
- [Why the Recent Action against Ryujinx is a Big Deal](#why-the-recent-action-against-ryujinx-is-a-big-deal)
- [What can be done?](#what-can-be-done)

## Why is Switch Emulation Development Important?

- 1) Short term benefit: Users should have a right for interopability
- 2) Long term benefit: You can't wait until a product is done to start emulation development 
    - a) Switch emulation isn't finished 
    - b) Imagine interest in Wii U emulation now that the console is finished - if Nintendo took this action against Exzap, would there be any interest in emulating the failed Nintendo console?

- Furthermore, I'll argue that preserving the legality of emulation is of utmost value, in regard to the principles of interopability and of preservation
- Nintendo is sidestepping legal precedent and enforce a culture of fear

## History Time! Sega, Sony, and Establishing Fair Use via Reverse Engineering 

### 1992: [Sega vs. Accolade](https://www.copyright.gov/fair-use/summaries/segaenters-accolade-9thcir1992.pdf), ([Lawsuit](https://casetext.com/case/sega-enterprises-ltd-v-accolade-inc-2))

This lawsuit ended up being one of the most impactful for codifying reversing engineering for functional elements as a fair use defense for copyright infringement. In 1998, Sega released the Sega Genesis and required third party devs pay a licensing fee and exclusively publish for Sega. In 1990, Sega released the Genesis III and implementing the TMSS (Trademark Security System): initialization code that checked for the letters "SEGA" before allowing a cartridge to run.

Game development company Accolade, wanting to avoid the exclusivity agreement, first reverse engineered three Genesis cartridges by decompiling them and wrote a specification manual that contained the Genesis-compatible requirements. As a result, Accolade added this code to their own self-published games. When the Genesis III released, Accolade added the TMSS code as a header file for all its games. 

In 1991, Sega pursued legal action against Accolade for trademark infringement, unfair competition, and copyright infringement; Accolade argued that its use constituted fair use. The district court sided with Sega so Accolade appealed to the 9th circuit. The appeals court agreed with Accolade's claim of fair use:

- Trademark infringement: the "SEGA" trademark can't be used to limit competition
- Copyright infringement: TMSS file was substantially smaller than original game content and there's public benefit to compete with Sega; furthermore, the TMSS contains functional elements, 
  
The Ninth Circuit reversed preliminary injunction and ruled Accolade's decompilation fair use; disassembly of a copyrighted work is fair use if necessary to get access to functional elements of the work.

### 2000: [Sony vs. Connectix](https://www.copyright.gov/fair-use/summaries/sony-connectix-9thcir2000.pdf), ([Lawsuit](https://caselaw.findlaw.com/court/us-9th-circuit/1452245.html))

In 1994, Sony released the PlayStation in Japan and, [based on a cheap price, 3D graphics, a strong game library, and adolescent marketing](https://expertbeacon.com/why-did-the-ps1-do-so-well/), sold over 100 million systems. Four years later in San Mateo, California, [Aaron Giles](https://aarongiles.com/) at Connectix started working on the Virtual Game Station (VGS), an emulator to run PlayStation games on Mac hardware. Giles and Eric Traut initally showed Sony the product but Sony refused to license its BIOS. Therefore, Connectix engineers reversed engineered the BIOS by extracting it from the Sony chip and observed how it interacted with the VGS. In 1999, it was shown at Macworld Expo. 

{{< youtube 3OqMcqRI-xA >}}

Sony, with support from Nintendo, Sega and 3dfx, filed a lawsuit based on claims of copyright infringement and trademark tarnishment. The District Court sided with Sony and issued a preliminary injunction again Connectix, but the Ninth Circuit Court of Appeals reversed both claims and lifted the injunction after showing that Connectix's use of the BIOS was legal. Despite this, the cost of continuous litigation led Connectix to settle and hand over its code to Sony. 

Some highlights from the suit:

1) **Emulation is taken as legal**: "Software engineers designing a product that must be compatible with a copyrighted product frequently must “reverse engineer” the copyrighted product to gain access to the functional elements of the copyrighted product."
2) **Connectix is a valid competitor to the PlayStation**: As discussed in the potential market impact for fair use, "Sony understandably seeks control over the market for devices that play games Sony produces or licenses. The copyright law, however, does not confer such a monopoly".
3) **Connectix copying the BIOS for the purposes of reverse engineering is legal**: as stated in factor 1 for fair use, it's necessary to get access the unprotected/functional elements of Sony's hardware.

### 2000: [Sony vs. Bleem!](https://www.copyright.gov/fair-use/summaries/sonycomputer-bleem-9thcir2000.pdf), ([Lawsuit](https://casetext.com/case/sony-computer-entertainment-america-v-bleem))

Simultaneously to Connectix being developed, Randy Linden (computer programmer who ported Doom to the SNES and Dragon's Lair to the C64) and David Herpolsheimer (marketing with IBM, Kodak, Apple) began work on Connectix. With PC-exclusive enhancements (improved resolutions, anti-aliasing), bleem! envisioned it could be an easy way for developers to port their PlayStation games to PC. 

Sony disagreed and sued them over copyright infringement over the usage of screenshots for comparative advertising; while the district court ruled in favor of Sony and set up a preliminary injunction against Sony, the appeals court overturned this. The court asserted Bleem as a competitor to Sony and ruled Bleem's use of screenshots was for comparative advertising and thus fair use - *"If sales of Sony consoles drop, it will be due to the Bleem emulator's technical superiority over the PlayStation console, not because Bleem used screen shots to illustrate that comparison"*.

Again, Bleem wins this case but again, Sony continues to sue. Linden goes to Sony. Herpensheimer, disaffected by the loss of the company and his colleagues, leaves the software industry: ["I was ready to build a bunker and fill it with canned food because if this was how the world worked, I didn't want anything to do with it."](https://www.eurogamer.net/the-history-of-bleem)

## Things Aren't So Settled: The Digital Millenium Copyright Act

So reading this so far, you probably think reverse engineering for the purposes of creating an emulator is a slam dunk. Unfortunately, things will get more complicated. In 1998, the Digital Millennium Copyright Act (DMCA) was passed; while there were three main provisions, Section 1201 (anti-circumvention) is most relevant; it prevents circumvention of technological protection measures and trafficking tools primarily designed to aid this. However, there is a specific exemption for reverse engineering: 

Section F: *"...circumvent a technological measure... for the sole purpose of identifying and analyzing those elements of the program that are necessary to achieve interoperability of an independently created computer program with other programs".*

There are few cases that focus on the DMCA interopability exemption, fewer that went to trial, and almost none relevant to emulation.

- In [Davidson Associates v. Jung](https://casetext.com/case/davidson-associates-v-jung), as pointed out in the [EFF's discussion on the legality of reverse engineering](https://www.eff.org/issues/coders/reverse-engineering-faq), Blizzard's EULA waived the fair use rights of the developers and BnetD allowing non-genuine software to operate made the exemption invalid.
- In [Apple v. Corellium](https://www.copyright.gov/fair-use/summaries/appleinc-corellium-sdfla2020.pdf) (Corellium created virtualization software for the iPhone), Judge Rodney Smith threw out the copyright infringement claims but didn't issue a summary judgement for Apple's DMCA claim; he opinoed that based on prior rulings, there would need to be a balanced approach between Section 1201 and Fair Use, [much to the charaign of the EFF](https://www.eff.org/deeplinks/2021/02/section-1201s-harm-security-research-shown-mixed-decision-corellium-case). However, Apple and Corellium settled the DMCA claim back in 2021 so this question never got resolved.

The limited number of cases on DMCA interopability makes it hard to know how court would balance copyright and fair use and the DMCA and its exemptions. 

## Nintendo's Actions against Emulators

Nintendo has negatively spoken out and taken actions against emulators ever since Nintendo threatened legal action against UltraHLE, an Nintendo 64 emulator, in 1999. Nintendo previously had a [webpage](https://archive.ph/aTJpk#selection-975.0-975.37) where it discussed game emulation and ROMs; case in point, it states the *"introduction of emulators created to play illegally copied Nintendo software represents the greatest threat to date to the intellectual property rights of video game developers"*. They later updated the webpage 
- 2023: Dolphin (emulator, GameCube/Wii) / Valve vs. Nintendo
    - Nintendo's lawyers argue for this.
    - Dolphin's lawyers argue against this

In 2024, Nintendo broke new ground by filing a lawsuit against an emulator (Yuzu which emulates the Nintendo Switch) for the first time.
    - Primary assertions Nintendo made
    - Yuzu settled, didn't rely on

## Why the Recent Action against Ryujinx is a Big Deal

Hopefully with the context, it should be how this.

- Solidifies the idea of open source not being a method of protecting against legal action
- Shows the issue wasn't Yuzu specific but rather emulating modern platforms 

As seen on Reddit:

- Switch emulation shouldn't go under cover
- Emulation developers and advocated should be respected (ex. KD-11) 
- Emulators should **not** hold off on advertising themselves, being funded via Patreon, showing screenshots/video announcements/etc.
- "Fuck Nintendo" - this feels nice to say but this accomplishes little to nothing.

Respond to Moon Channel video:



## What can be done?

- Legal defense funding
    - Ideally also legally support from organizations such as the EFF or the Software Preservation Group (network)
    - This is especially important for emulators for recent systems (ex. [ShadPS4](https://github.com/shadps4-emu/shadPS4))
    - This would slow down development but would prevent a large corportation from steamrolling an emulator later in its life

- Legislation clarifying anti-circumvention bypass for software being allowed for the purposes of software interopability (rather than relying on legal precedent)
    - This could potentially be done via a DMCA exemption though those have expiration dates
    - Make it harder for Nintendo or another copyright to cite the DMCA in litigation
    - Ideally this would involve collaborating with larger software rights organizations such as the EFF or the Software Preservation Network

- Precautions for Future Emulators
    - Obvious but don't hint at/discuss piracy, especially from lead developers (Nintendo specifically cited a Yuzu maintainer noting that their users probably pirate Switch firmware in their lawsuit)

Sources:

- [Legal Status of Emulation, Emulation General Wiki](https://emulation.gametechwiki.com/index.php/Legal_status_of_emulation)
- [The history of bleem!, Eurogamer](https://www.eurogamer.net/the-history-of-bleem)
- [Programming War Stories: Connectix, Aaron Giles Personal **Website**](https://aarongiles.com/programming/war-connectix/)
- [DMCA - Copyright.org](https://www.copyright.gov/dmca/)
- [DMCA - Cornell Legal Information Institute](https://www.law.cornell.edu/uscode/text/17/1201)