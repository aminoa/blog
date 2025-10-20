+++
title = 'Reflections on writing a Game Boy emulator'
date = 2025-10-19T20:37:21-04:00
draft = false
+++

## Thoughts

I've recently finished[^finishing] my [Game Boy emulator](https://github.com/aminoa/dot-matrix-rs), based on a C++ emulator I started a couple of years ago. I felt compelled to rewrite it in Rust, partly as a way to learn the language, but also to finish what I started (my previous [emulator](https://github.com/aminoa/dot-matrix/) was incomplete and broken). This post won't be technical ([there](https://gbdev.io/pandocs/) [are](https://github.com/gbdev/awesome-gbdev?tab=readme-ov-file#emulator-development) plenty of resources for that[^rustemuguide]), but more reflective.

The project took me a bit [over 2 years](https://github.com/aminoa/dot-matrix/commit/74ca135e0c849be81867247a4571604625e45cd5), and in retrospect, I would have taken a less perfectionist way of writing my emulator. Instead of spending a large amount of time to pass Blargg's CPU tests, it would have been better to try to get Tetris running and displaying on the screen. To illustrate this, after writing a disassembler, I could have checked what opcodes the game used, then developed a CPU emulator that only emulated those opcodes. Then, I would have written a very inaccurate graphics renderer that looped over the Game Boy display and displayed the background tile data. I could mock the joypad inputs to alternate start to get into gameplay. From here, I could rewrite my graphics renderer to be scanline-based and then go back to implement window/object rendering and proper joypad support. I could move on to other games from here to further improve the emulator. This sounds really hacky and bad, but I also would have finished this project in **6 months instead of 2 years** (obviously working on the project on-and-off).

I don't regret my time spent, since it is the largest personal project I've worked on and also pushed my knowledge of emulators much more than the Chip-8 did. Still, I likely would have tackled similarly interesting problems contributing to pre-existing emulators or trying to take a crack at a non-emulated system. [You don't need to work your way up to newer systems](https://www.reddit.com/r/EmuDev/comments/8ve8lu/comment/e1muyme/?context=3).

On an unrelated note, when I was first developing the dot-matrix-c++, I tried not to reference other emulators to avoid "cheating", but you learn a lot referencing other code, especially since I switched languages. Rust didn't change my emulator architecture much; I used Rc<RefCell<X>> for many components to match how I wrote dot-matrix in C++, though there is a performance penalty, which is why you'll see most other emulators take different approaches.


## Closing

Despite the negative tone of this post, I did enjoy developing the emulator, and I was super excited finally getting my joypad working on it to be able to interact with these games; It's impressive how complex even this piece of 1999 hardware can be. 

{{< video src="dot-matrix-rs-reel.mp4" width="600" >}}

[^finishing]: You can't finish an emulator but I wrote enough of the graphics system to be happy to table the project.
[^rustemuguide]: I wish I knew this existed: https://aquova.net/emudev/gb/
