+++
title = 'QEMU-iOS Rewrite Progress'
date = 2026-06-08T00:00:00Z
draft = false
+++

This is going to be a quick update post. I'm in the process of attempting to revive [QEMU-iOS](https://github.com/devos50/qemu-ios), an iPod Touch 1G/2G emulator by Martijn de Vos; it is about 4 years old at this point and seems to be unmaintained[^1].  I've wanted to work on a rewrite of QEMU-iOS for about [4 years](https://github.com/devos50/qemu-ios/issues/17) at this point but it has been on the back burner. Last year I [tried](https://github.com/devos50/qemu-ios/issues/243) several hours to build the original project and run it locally, but I was getting segfaults (in retrospect, maybe I could have traced it better). A couple months ago, I threw Claude at it and it was able to write a small patch and get the project to boot again. I've been itching to work on a large emulation project so it was either this or contributing to [Inferno](https://github.com/ChefKissInc/Inferno). However, since QEMU-iOS is unmaintained, I thought it would be more worthwhile focusing on this project and as a bonus, early iPods are simpler than modern iPhones. QEMU is a mature open source emulation project and TCG is a fast JIT; however, to have more flexibility when writing this emulator and to better familiarize myself with the system overall, I decided to forgo QEMU[^2][^3]. 

## Why not release?

I'm getting close to booting Springboot, but even when I reach this state, I don't plan on releasing the source for now. While my opinion on this could evolve, for important projects I work on, I always want to have some contextual understanding of most of the core emulation code I write and be able to rearchitect it as I feel is appropriate. I've been using Claude to generate a test suite against the original QEMU-iOS project, which it can then use to assist itself when writing the current emulator; this is, in my opinion, a great way to use LLMs since it removes a lot of busywork. However, once the author is divorced from their code's architecture, I suspect it will be challenging to vet the quality of code contributions or even evaluate their own code. This doesn't matter as much for non-core emulation code (such as UI code) since that code is going to be more boilerplate anyway[^4].

## Sidenote

I got motivated back into working on my Game Boy emulator (it never ends)! I did a simple refactor recently, but I hope to build out its debugger and maybe even the APU if I get the time (but I'm fairly busy nowadays, so it's hard to say).

[^1]: There was a [blog post](https://devos50.github.io/blog/2022/ipod-touch-qemu/) written here, a [37C3 talk](https://media.ccc.de/v/37c3-11871-breathing_life_into_legacy_an_open-source_emulator_of_legacy_apple_devices) here, and a [FOSDEM talk](https://archive.fosdem.org/2024/schedule/event/fosdem-2024-2826-breathing-life-into-legacy-an-open-source-emulator-of-legacy-apple-devices/) here.
[^2]: AFAIK the only prominent game emulator using QEMU is [xemu](https://xemu.app)
[^3]: Using Claude, I initially attempted to gradually migrate off QEMU using Unicorn but I was getting memory access issues so I ended up just generating an ARMv6 interpreter instead.
[^4]: Somewhat unrelated but here are AI contribution guidelines from [RPCS3](https://github.com/RPCS3/rpcs3/commit/c0b358003f813e28d7902cd65251c3506847619a) and [Dolphin](https://github.com/dolphin-emu/dolphin/blob/master/Contributing.md#genai)
