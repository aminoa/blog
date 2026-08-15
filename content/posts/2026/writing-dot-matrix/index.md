+++
title = 'Writing Dot Matrix'
date = 2026-06-28T20:41:05-04:00
draft = true
+++

I've recently finished working on my Game Boy emulator, [dot-matrix-rs](https://github.com/aminoa/dot-matrix-rs). I've spent about 3 years working on this emulator on and off, through two languages and multiple refactors. When I wrote my last article, I was disappointed by my progress and lamented the time I worked on it. While there are multiple bugs and unimplemented features, I feel content with its final state. Feel free to try it at [gb.aneeshmaganti.com](https://gb.aneeshmaganti.com).

This is not the most comprehensive guide to the GB but it serves as a good recap[^pandocsrant] of the hardware and its implementation, the design decisions and challenges I went through, and reflections. I'll break things down so this shouldn't require background reading. 

Emulation is important both in terms of software interopability and preservation. CHIP-8 is the recommended starting point, but the Game Boy is the smallest non-toy platform. It was conceptualized by Gunpei Yokoi after the release of the Game & Watch, to take console gaming on the go. It was devloped by him and Satoru Okadu at Nintendo R&D1 and released in 1989, using primitive hardware to be price competitive: a 4.19MHz Sharp SM83 CPU (similar to a Z80) with a 160x144 LCD display. The release of various games including Tetris, Super Mario Land, Metroid II, and Pokémon Red and Blue pushed sales of the handheld to 118 million units.

While The Game Boy is one of the most emulated consoles (1.7k repos on GH)[^ghrepos], it's deceptively simple, even as a handheld from the late 80s[^blockers]. I was drawn to the handheld from my interest in chiptunes and to its breadth of documentation.

## What's a computer?


## Building an Interpreter


## CPU



- What is an interrpeter?
- Instruction set (z80)

## PPU

- Four modes
- OAM
- Scrolling

## APU

- Four different channels
- Frame sequencer

## Missing from my emulator?

- More MBCs
- Some broken interrupts 
- Link cable
- GBC (lol)

I hope you've enjoyed reading this post. 

- Writing a JIT
- Future consoles 
- Continuing to write on this blog more

## Finishing off

I did not approach this emulator purely from specs. Early on, I was reading other emudev's source code and using LLMs to help with either figuring out next steps or generating UI/controller code (though I did vet the code so that it would fit in with the project). I find that reading source code helps get a better grasp on the design taste of an individual developer. LLMs were useful in terms of generating boilerplate code or helping point out errors in some of my original functions (ex. MBCs). 

I used Claude (Opus 4.8/5/Fable) to port dot-matrix-rs to the web via Trunk; I put some effort into making the design appeal to my tastes[^sidecodevibecode] but I had little interest in focusing on this. 

## Dot Matrix Development History

Back in high school, I looked at the Pan Docs and thought "this is cool, I should make a Game Boy emulator!". I lacked motivated to start on the project then.

I started working on the original version of this emulator [back in 2023](https://github.com/aminoa/dot-matrix/commit/74ca135e0c849be81867247a4571604625e45cd5). 

Fast forward to sophomore year of college (August 2022) and I became interested in emudev again. I followed the classic advice and worked on a [chip8 emulator](https://github.com/aminoa/chip8). CHIP-8 isn't a game console, but rather an interpreter that ran on multiple 70s computers; it's extremely primitive which is why Reddit/other online forums recommend it as tutorial for learning emulator development. My project was basic but I managed to emulate the CPU opcodes and get garbled graphics. 

I started reading more into the Game Boy hardware as part of a BUGS open source event I hosted (April 2023); in the presentation, I gave a technical overview of the Game Boy hardware [^bugsevent] and then made a simple [practical demo](https://github.com/BUGS-NYU/gbemu-demo) where I purposefully broke `adc` and `and` and had the students try to fix it. As part of the presentation prep, I wrote a basic disassembler.

I started my [C++ Game Boy emulator](https://github.com/aminoa/dot-matrix) during the summer (July 2023) since I didn't have an internship. My C++ knowledge was limited at the time but I slowly built up the CPU and got it to pass Blargg's CPU tests. I later ended up on working on the background rendering code.

## Regrets

I aired these out in this [post](https://stalereference.com/posts/2025/gb/) from 8 months ago...[previouspost]. This project took a long time to complete (I really do think this will be the last major update for this emulator). Funny enough, I was frustrated with it taking 2 years when it will soon be 4 years since I initially had an idea for working on this project; granted, I only committed on and off, with a lot of time being spent with school/work/hobbies/etc. 

This was a massive time commitment, and it was for a system that is highly emulated. However, I think a significant value of the project came from being able to construct and iterate on a mental model for the hardware and being able to fill in gaps.

## Sources

- https://www.ign.com/articles/2009/07/27/ign-presents-the-history-of-game-boy
- https://gamrconnect.vgchartz.com/thread/246545/gameboy-total-lt-sales-breakdown/1/

[^ghrepos] This is a weird metric to use; "homelab" has 29.8k repos; "todo app" has 518k repos; "RAG chatbot" has 49k repos; "emulator" as a whole as 88k repos (but this includes terminal emulators/other unrelated projects).
[^pandocsrant] The Pan Docs are not fully complete (though useful), but there's many resources to explore here.
[^bugsevent] It was absurb in retrospect to give a presentation with this little context of the hardware (and not a lot of sleep), but I don't regret it. It was fun to expose this side of computing to students who may not interface with systems like this.
[previouspost] I wrote I finished my emulator, probably to serve as a stopping point, but the state of that emulator always ticked me off. I put a bit of time into trying to write out the graphics rendering for the emulator but considering many big games still didn't load, I was always unhappy with its state. It's a bit funny in retrospect that I was pretty close, if I just implemented MBCs, since my graphics rendering was already pretty good.
[^sidecodevibecode]: I dislike the default Claude website styling outputs, especially the "retro-tech" ones. I prompted until it looked clean.
[^blockers]: I was curious about this, so I ran a Claude Deep Research on the repos that surfaced from "game boy emulator".
