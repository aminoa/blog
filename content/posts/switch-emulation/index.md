---
title: 'Nintendo is killing Switch Emulation via Murky Legal Theory'
date: 2024-10-02T17:07:07-04:00
draft: false
---

*All legal discussion is relevant to the United States only. Please don't use any of this as legal advice. If you find any errors with this article, please send an email to [a@stalereference.com](mailto:a@stalereference.com).*

On October 1st 2024, GDKChan took down the Ryujinx organization from GitHub after contact with Nintendo.

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

Simultaneously to Connectix, Randy Linden (computer programmer who ported Doom to the SNES and Dragon's Lair to the C64) and David Herpolsheimer (marketing with IBM, Kodak, Apple) began work on Connectix  - Notably used dynamic recompilation, allowed for emulation enhancements (improved resolutions, anti-aliasing). bleem! envisioned it could be an easy way for developers to port their PlayStation games to PC. 

Sony disagreed and sued them over copyright infringement over the usage of screenshots for comparative advertising; while the district court ruled in favor of Sony and set up a preliminary injunction against Sony, the appeals court overturned this. The court asserted Bleem as a competitor to Sony and ruled Bleem's use of screenshots was for comparative advertising and thus fair use - *"If sales of Sony consoles drop, it will be due to the Bleem emulator's technical superiority over the PlayStation console, not because Bleem used screen shots to illustrate that comparison"*.

Again, Bleem wins this case but again, Sony continues to sue. Linden goes to Sony. Herpensheimer, disaffected by the loss of the company and his colleagues, leaves the software industry: ["I was ready to build a bunker and fill it with canned food because if this was how the world worked, I didn't want anything to do with it."](https://www.eurogamer.net/the-history-of-bleem)

## Things Aren't So Settled: The Digital Millenium Copyright Act

The EFF highlights the Genesis lacked a license agreement.

Here comes in the DMCA which further complicates things. The DMCA was designed to prevent circumventio n...... There are narrow DMCA exemptions for reverse engineering whcih include ....

Blizzard v. BnetD5: Signing a EULA contract which prohibits reverse engineering of software does apply, thus the programmers waived their rights when they signed the contract. Furthermore, the anti-circumvention provisions of DMCA hold up which limited the possibilities. 

Under [Apple v. Corellium](https://www.copyright.gov/fair-use/summaries/appleinc-corellium-sdfla2020.pdf), Judge Rodney Smith (US District Court for the Southern District of Florida) specifically highlighted that while Apple couldn't issue a summary judgement for the DMCA claim stemming from fair use protections, Corellium wasn't scot-free either; he opinoed that based on prior rulings, there would need to be a balanced approach between Section 1201 and Fair Use. However, Apple and Corellium settled this claim back in 2021 so this question never got resolved.

## Nintendo's Actions against Emulators

- 1999: UltraHLE (emulator, N64) vs. Nintendo (lawsuit threat)
- 2023: Dolphin (emulator, GameCube/Wii) / Valve vs. Nintendo
    - Nintendo's lawyers argue for this.
    - Dolphin's lawyers argue against this
- 2024: Nintendo vs. Yuzu
    - Primary assertions Nintendo made
    - Yuzu settled, didn't rely on 

## Why the Recent Action against Ryujinx is a Big Deal

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