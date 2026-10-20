+++
title = 'Guidance and Advice for Game Boy Emulation'
date = 2026-10-12T20:41:05-04:00
draft = true
+++

This is some brief guidance I would have liked to read before I built my emulator. I am by no means an expert, but I've spent enough time developing Dot Matrix where I can provide a few[^few] easy[^easy] steps[^steps].

I've wanted to write a Game Boy emulator for around 8 years. Back in high school, I opened the [Pan Docs](https://gbdev.io/pandocs/), but I lacked motivation. In sophomore year of college, I wrote an incomplete [CHIP-8 interpreter](https://github.com/aminoa/chip8) which ran on 1970s microcomputers. I started my [C++ Game Boy emulator](https://github.com/aminoa/dot-matrix) in July 2023 since I didn't have an internship; I slowly built up the CPU and got it to pass Blargg's CPU tests and started on background rendering before tabling the project. I decided to restart the project again in Rust, to improve my knowledge of the language and to finish off the emulator, which can be found here: [dot-matrix-rs](https://github.com/aminoa/dot-matrix-rs). 

## CPU

- Has 8 registers, an ime 
- GB ROM has a large instruction set

The Game Boy itself has a boot ROM which initializes some registers and displays the Nintendo logo but I didn't bother emulating that.

A Game Boy ROM consists of interrupt vectors, a header, and instructions which command the hardware. 

- It has a clock that runs at ~4.19 MHz.
- 8 KiB of Work RAM and VRAM

## Audio

- Interpreter 

- What is an interpreter? Fetch decode execute

- Instruction set (z80)
  - Different types of instructions 
- Show images/mermaid diagrams of fetch-execute-decode loop
- Here's a hexdump of instructions
- Mapping


- Interrupts (various types)
  
## Memory Management

- How 
- How does the hardware work? 
- Not enough storage or RAM
- We need to be able to "bank" more storage/RAM

- Cart accessible

## Joypad

- How does button selection work

## PPU

- Four modes
- Three types of objects rendered during a scanline pass
  - Background
  - Window
  - Objects
- Scrolling

## APU

- How does an audio wave work?
  - Based on an APU register counting up
- Length counter
- Four different channels (two square channels, wave, noise)
- Frame sequencer

- Implementing in Rust

## Savestates

- Dumping CPU, PPU, MMU, and cart objects into file
- Loading deserializes said objects and sets them back to the current running emulator state
- There's a standard GB savestate format but I didn't follow that

## Advice

I'm not as negative as I was in my previous GB emulation post, where I expressed dismay at my progress, since it's challenging to know the proper pace for projects and smart design decisions when going through what was initially a "learning" project. It was extremely educational though in that way.

- You should cheat when building an emulator. Obviously don't AI generate the entire emulator, but reading emulator source code and using AI selectively is important
  - I felt self-conscious about this, but when working on new, unexplored systems, you won't have this option, so you should take advantage of this.
  - I've seen some people online write you can just use the pandocs but I found that challenging, I definitely looked at my share of source code, blog posts, and AI snippets.
- Build an emulator in a language you know well. Writing in Rust was fun, but in retrospect, I would have stuck with my [C++ emulator](github.com/aminoa/dot-matrix) and saw it.
- I didn't complete my [CHIP-8 emulator](https://github.com/aminoa/chip8), but spending more time here would have been good
  - Also, for prospective emudevs, I've linked this before but [VeloCity666's comment here](https://www.reddit.com/r/EmuDev/comments/8ve8lu/comment/e1muyme/?context=3) rings true: you don't need to work your way up to newer systems. Once you finish CHIP-8, you can move onto another system.
  - Writing any emulator is a massive time commitment, and the Game Boy is highly emulated. I don't regret writing this emulator, but opportunity cost is something is worth considering.

I'm tempted to say no, but I won't have a good answer for a couple years still. I feel sure that, after writing a *good* CHIP-8 emulator, most emudevs can move on and start contributing to existing emulators. There's a lot of menial work that comes with emulating an entire system (lots of repeated CPU instructions for ex, parts of audio channels had similarish behavior, etc.). 

## AI

- The way I used AI altered; early usage was tab autocomplete (mainly for filling out CPU instructions);
- Tutor method: 
  - First via writing my own PPU implementation and then asking Claude for corrections about my implementation (though this displayed too much code)
  - Then creating an output style (where it could write Rust audio code but not Game Boy APU code; it could however provide spec information on the APU)
- In general, 
- I also used Claude to help me fix an audio bug (which compared my emulator state to Same Boy's).

I did not approach this emulator purely from specs. Early on, I was reading other emudev's source code and using LLMs to help with either figuring out next steps or generating UI/controller code (though I did vet the code so that it would fit in with the project). I find that reading source code helps get a better grasp on the design taste of an individual developer. LLMs were useful in terms of generating boilerplate code or helping point out errors in some of my original functions (ex. MBCs). 

I also debugged an issue with Pokemon Blue after trying to do some print debugging, by throwing Claude at it (which compared SameBoy logs to my emulator) and was able to catch the issue (a missing write after no matches).

## Sources

- https://www.ign.com/articles/2009/07/27/ign-presents-the-history-of-game-boy
- https://gamrconnect.vgchartz.com/thread/246545/gameboy-total-lt-sales-breakdown/1/
- https://en.wikipedia.org/wiki/Von_Neumann_architecture#History

[^few]: Many.
[^easy]: Mileage may vary.
[^steps]: Don't need to follow in order directly. 


[^ghrepos] This is a weird metric to use; "homelab" has 29.8k repos; "todo app" has 518k repos; "RAG chatbot" has 49k repos; "emulator" as a whole as 88k repos (but this includes terminal emulators/other unrelated projects).
[^pandocsrant] The Pan Docs are not fully complete (though useful), but there's many resources to explore here.
[^blockers]: I was curious about this, so I ran a Claude Deep Research on the repos that surfaced from "game boy emulator".
