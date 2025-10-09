+++
title = '6 weeks at the Recurse Center'
date = 2025-10-08T15:51:55-04:00
draft = false
+++

I don't remember how I first learned about the [Recurse Center](https://www.recurse.com/), but I heard about it while at NYU, and I knew I wanted to do it once I had more time. I graduated in September 2024[^intern] and signed my job offer at Affirm in December, so I had about 6 months before my job started. I initially [applied](https://github.com/aminoa/rc-app/tree/main/attempt-one) in late October 2024 for the Winter 2 batch, but I failed the second round. I [reapplied](https://github.com/aminoa/rc-app/tree/main/attempt-two) in March 2025 and got into the Summer 1 batch.

It's a programmer's retreat, so there isn't a structured curriculum. Instead, it's up to you and your batchmates to coordinate to create weekly group sessions on different topics or to work on projects. However, a group of motivated software engineers on sabbatical[^demographic] end up creating structure: we had weekly events on Wednesday and Thursday to either display a cool hobby or a programming project. There were consistent creative coding jams on Wednesday and Game Dev discussions on Thursday. cs336 lectures on Friday, AI papers (probably the hardest to keep up with), and Zero to Hero review sessions on Monday. I was open to almost anything except anything related to infrastructure[^noinfra].

## Why did I apply?

To be surrounded by people who find computers fascinating. My favorite thing about RC was the people. I met so many interesting people across tons of different disciplines, career trajectories (tenured big tech employees, startup founders, non-tech people trying to break in, college students), backgrounds, and interests[^friends]; they highly motivated me to work on different projects though I admittedly also got distracted because of them (I'd say that's a good problem). It reminds me most of [BUGS at NYU](https://bugsnyu.com), but the scale at RC is much larger. This is probably the biggest selling point of RC and is why I would highly recommend doing an in-person batch.

## What did I do

I primarily honed in on ML courses during my batch. The ML group that formed around [cs336: Language Modeling from Scratch](https://stanford-cs336.github.io/spring2025/) was very motivating. We went through about 5 lectures; the first two were straightforward (history of neural nets, tokenizers, pytorch refresher), but lecture 3 was challenging (went over the transformer architecture but heavily dove into pieces that have changed like norms and embeddings), lecture 4 was straightforward (mixture of experts wasn't too hard conceptually, specialized subnetworks with gates), and lecture 5 (my favorite, talking about GPUs, its hardware, and multiple tricks[^gputricks] used to optimize computation). I plan to work through the corresponding assignments. Going through the AI papers was also a challenge (since it was easy to miss context); I tried going through "Attention is All You Need" (2017), "RoFormer: Enhanced Transformer with Rotary Position Embedding" (2023), and "FlashAttention: Fast and Memory-Efficient Exact Attention with IO-Awareness" (2022). Finally, there was [Karpathy's Zero to Hero](https://karpathy.ai/zero-to-hero.html) ML course, but I was too occupied to invest much time despite it being very well done.

I attended many of the creative coding and game development meetings, which I found fun to cool off from the more technical sessions ([collaborative ant simulation game](https://editor.p5js.org/kim.a.elise/sketches/Ixo0PS_GV)). I also tried working on personal projects (focused a bit on getting QEMU-iOS to build, but sadly, it did not cooperate), but I mostly sidelined them since I found so many new things to work on. There was an offshoot of the linguistics group which played [Chaants of Senaar](https://store.steampowered.com/app/1931770/Chants_of_Sennaar/), and while I didn't participate in the main linguistics group, the group play was great[^otherevents].

## What didn't I do (or finish)

I ended up looking at a ton of new things briefly that I also couldn't explore much. Here's a list:

- Hardware Escape Room
- Distributed Systems Group (MapReduce and Raft Implementations)
- Writing a C Compiler
- Vulkan Tutorial
- Godot Game Development
- Writing a native Java application on the 3ds[^3dsjava]
- [Transformer Circuits](https://transformer-circuits.pub/)
- OpenPBX

## "Never Graduate"

The [Community](community.recurse.com) forum is a hidden gem: I actually found my sublease in NY on it, and community members sell their stuff for cheap (I was tempted by an NSO N64 Wireless Controller). The RC Zulip is still useful after graduating even though I don't check it frequently; you can discover many interesting NYC events on there and there's an active alumni channel.[^unrelated]

RC was a ton of fun, and it felt very bittersweet to finish my batch, but I hope to take a bit of a break before I reapply so I can grow more as an engineer. I can see my limitations quite clearly (I can get sidetracked by new ideas, sometimes I can get in a rut and have a hard time coming up with a novel approach to a foreign problem, and I still struggle to commit to larger tasks), which I hope to work on. I'll apply again around 2030 and hopefully in a full-batch :)

[^intern]: I finished my last semester in May 2024 but I did an internship at Qualcomm over the summer.
[^demographic]: There were some college graduates but I would guess it skewed mid-20s to early 30s.
[^noinfra]: a) It's too much of a time sink, especially with home kubernetes cluster, and b) I was going to start at Affirm right after so I thought it wouldn't be the best use of my time.
[^gputricks]: quantization, fusing operators since memory access is a bottleneck, in a similar vein recomputating activations to avoid memory access, memory coalescing, many more
[^3dsjava]: Yes, the 3DS uses an ARM-11 dual-core CPU (32-bit ARMv6 ISA) and it supports [Jazelle](https://en.wikipedia.org/wiki/Jazelle), an ARM extension, for native Java bytecode execution. There is actually a project [here](https://github.com/aspargas2/advent-of-code-2023/tree/main/day01-jazelle) which uses this mode to solve an AOC problem. I learnt about this through the [Copetti](https://www.copetti.org/writings/consoles/nintendo-3ds/) architecture article.
[^unrelated]: This is the first small post. To reduce friction, I'm planning on writing more in the future though there will occasionally be really big posts (like my last two)!
[^friends]: I also felt it was easy to make friends at the hub (I only did a half batch, so I'm sure you make a few more in a full-batch).
[^otherevents]: Other notable one-off events included using [GNU Radio](https://www.gnuradio.org/) and ricing show-and-tell.
