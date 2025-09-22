+++
title = "Vision"

[extra]

intro = "What we hope the spec will look like."
+++

We hope that our specification will be _executable_, _machine-readable_, and _easy to understand for humans_.
We have already outlined several problems with the approach of writing specification in [English prose](/topics/englishprose).

By _executable_, we mean that the specification should (as far as possible) be presented as a program that can check potential Rust code for conformance with the specification.
This would ensure that tools consuming Rust can be easily checked for conformance, for example by using differential testing.
It ensures that the specification can be probed on examples, to explore how different corner cases should be understood.
It ensures that the specification can be tested, to ensure that it matches our intuitive understanding.
It also ensures that the specification is coherent, since implementing the spec forces the authors to make everything explicit, ensuring that everything fits together.

By _machine-readable_, we mean that the specification should be understandable by other computer programs.
This allows the spec to be imported into other tools that consume Rust, ensuring that they are correct _by construction_.
It also allows the spec to be imported into e.g. computer-checked theorem provers, so that it can be formally proven that Rust actually achieves its guarantees of memory and thread safety.
Machine-checked tools can also check the specification for more basic properties.
Already the goal of a machine-readable specification ensures that it is unambiguous, since it forces all concepts to be properly defined.

Of course, the specification is not made for machines, but for humans, so it should also be _easy to understand for humans_.
There are several things to consider here.
First, we argue that to some extent, formality increases readability.
Most languages already use BNFs to specify their language's syntax, and it seems hard to imagine how the same clarity could be achieved if one were limited to natural language.
Similarly, we hope that other formalisms can make the specification easier to understand, if the formalism is sufficiently explained.
Additionally, since the spec is human-readable, a formal description could concievably be translated into a more human-readable form.
Such a derived English presentation of the rules of a formalism can be included in the specification, even if it is not the authoritative root source, if it is necessary for clarity.

Beyond that, we also argue that an executable specification is much easier to approach, compared to a large document of complicated English sentences.
It can be probed on small example programs, to explore the semantics interactively.
The target audience of the specification, Rust programmers, are used to reading code, whereas many are not native English speakers.

## How realistic is this?

This is not a pipe dream!
In fact, WebAssembly already has [a specification](https://dl.acm.org/doi/10.1145/3656440) that ticks all the boxes here:
It has a machine-readable specification at its foundation, and an English prose specification is generated from that; ensuring the spec is easily readable while avoiding all the pitfalls laid out above.
The specification is written "as a program," so it is naturally executable.

Rust could have the same.
