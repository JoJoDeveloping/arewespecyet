+++
title = "Ferroscene"

[extra]

intro = "Ferroscene is a specification that aims to certify Rust for certain safety-critical environments. Read more about what it does, and why we do not consider it a formal specification."

newstag = "ferroscene"
+++

[Ferroscene](https://spec.ferrocene.dev) is a version of the Rust toolchain that is certified for use in certain safety-critical systems, like the software that runs in your car.
In order to be legally certified for such uses, there needs to be a specification of what Rust is supposed to behave like.
The Ferroscene Language Specification (FLS) is that specification.
Thus, it describes (in formal prose) various aspects of Rust's type system and operational semantics.

The Ferroscene spec is a large step towards a specification.
It gives a detailed account of many aspects of the language, and is [sometimes](https://spec.ferrocene.dev/types-and-traits.html#subtyping-and-variance) extremely rigorous.

Unfortunately, the specification does not apply this level of rigor everywhere.
Large parts of Rust are only described in broad terms.
For example, the spec only gives a short, "axiomatic" [account](https://spec.ferrocene.dev/ownership-and-deconstruction.html#references) of borrow checking.
It does not describe how the borrow checker actually works (in terms of an algorithm), and the given rules are written in prose, which makes them abiguous.

The Ferroscene Language Specification has now been [donated](https://rustfoundation.org/media/ferrous-systems-donates-ferrocene-language-specification-to-rust-project/) to the Rust project, to be used as a starting point for Rust's specification.
This means that the FLS might soon be officially "blessed" by the Rust project.

For us, the main problems with the FLS are that it is insufficiently formal, as showcased by the example above; this is coupled to the spec's use of English.
We hope that this will change in future, and indeed the [plan](https://rust-lang.github.io/rfcs/3355-rust-spec.html#questions-deliberately-left-open) for Rust's specification would allow stricter formalisms for important parts, instead of attempting an English prose description.


