# Resources for learning more about compilers

Here we have a few more resources about learning how compilers work and
what happens to code _after_ the compiler runs — that is, how does a CPU actually _execute_ machine code?


# How machine code works

For a gentle introduction to machine code, David Murray, [The 8-Bit
Guy][8bit], has a good primer for the [6502]:

<iframe width="560" height="315" src="https://www.youtube-nocookie.com/embed/HWpi9n2H3kE" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>

[8bit]: https://www.the8bitguy.com/

For a more in-depth treatment, I recommend Ben Eater's videos. They are excellent, go into a technical detail yet remain relatively accessible.

Here are a couple of videos that compare C code to 6502 machine code,
and show how a CPU actually interprets machine code.

<iframe width="560" height="315" src="https://www.youtube-nocookie.com/embed/yOyaJXpAYZQ" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>

<iframe width="560" height="315" src="https://www.youtube-nocookie.com/embed/yl8vPW5hydQ" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>

[6502]: https://en.wikipedia.org/wiki/MOS_Technology_6502

<aside>
Why do all these videos focus on the 6502? It's a processor that was
used in classic computers like the Apple II, the Commodore 64, the
Nintendo Entertainment System (NES), and many others. Relatively
speaking, it's a simple processor—in fact, the entire processor can be
simulated in your browser, wire-for-wire, transistor for transistor at
[Visual 6502][V6502]. With just over 3,510 transistors, it is feasible
to understand what each part of the processor does in detail; compare
that to today's processors with billions of transistors!
</aside>

[V6502]: http://www.visual6502.org/JSSim/

If you want an explanation of how transistors and electronics can be
built up to implement logic, I recommend the series Crash Course
Computer Science:

<iframe width="560" height="315" src="https://www.youtube-nocookie.com/embed/gI-qXk7XojA" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>

# More about compilers

Want to write your own compiler or interpreter? I recommend [Crafting
Interpreters][crafting] by Robert “munificentbob” Nystrom. It's free,
but you can buy a print copy! I highly recommend it.

The classic book on compiler construction is “[Compilers: Principles,
Techniques, and Tools][dragon]” by Alfred Aho, Monica Lam, Ravi Sethi, and
Jeffrey Ullman. It's often known as the “Dragon Book” due to often
depicting compiler construction as a dragon on the cover of its various
editions. This is usually your textbook for a compiler construction
class.

# Interpreters

In our presentation, we explained how a compiler converts source code to
machine code. Some languages, like Python are _interpreted_. As far as
the implementation is concerned, much of the steps are the same. For
example, in CPython (the default Python implementation), the Python code
is compiled to _bytecode_. Here is a presentation I did that describes
how bytecode is executed. I even live-coded a small Python interpreter in
Python, which is wild:

<iframe width="560" height="315"
src="https://www.youtube-nocookie.com/embed/5yqUTJuFuUk?start=431"
title="YouTube video player" frameborder="0" allow="accelerometer;
autoplay; clipboard-write; encrypted-media; gyroscope;
picture-in-picture" calledallowfullscreen></iframe>

[crafting]: https://craftinginterpreters.com/
[dragon]: https://en.wikipedia.org/wiki/Compilers:_Principles,_Techniques,_and_Tools

# Why are they called “compilers”?

I _strongly_ recommend reading “[The education of
a computer][hopper1952]” by Grace Murray Hopper. This is the 1952 paper
that _invents the compiler_. Grace Hopper's “compiling routine of type
A” worked by compiling (in the conventional sense) a collection of
_subroutines_ into one larger _routine_. The subroutines were taken from
a _library_ of routines. This programming system was not a programming
language in the way we recognize it now, but it set the groundwork for
Murray's later [FLOW-MATIC][] programming language which was the basis
of the [COBOL][] programming language, which is (shockingly!) still used
to this day.

[hopper1952]: https://dl.acm.org/doi/10.1145/609784.609818
[FLOW-MATIC]: https://en.wikipedia.org/wiki/FLOW-MATIC
[COBOL]: https://en.wikipedia.org/wiki/COBOL
