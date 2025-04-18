+++
template = "home.html"

[extra]
answer = "No, sadly 😢"
+++

Rust does not (yet) have a formal specification. There are various projects aiming to formalize various parts of Rust, but these are mostly working independently.

## What about Ferroscene?

We do not consider the [Ferroscene Language Specification](/topics/ferroscene), which specifies a subset of Rust, a _formal_ specification. Ferroscene has been certified for use in certain safety critical environments, which is very cool! But the Ferrroscene specification is still written in [English prose](/topics/englishprose), and it is not suitable for rigorous applications of formal methods. It is also unofficial, since it is not maintained by a Rust team.

## What do you mean by _formal?_

By a formal specification, we mean a mathematical definition of (parts of) Rust. Such a mathematical definition must be unambiguous, leave nothing undefined, and should be written using formal language.  
History [has shown](https://dl.acm.org/doi/10.1145/2908080.2908081) that specifications in [prose](/topics/englishprose), like the C standard, tend to be ambiguous, to leave many things unclear, and thus give rise to conflicting interpretations and incompatible tools.

## Why do we need a formal specification?

Rust promises a lot of guarantees, notably memory and thread safety. But does Rust actually deliver? Can you write a safe Rust program breaking these guarantees? Ignoring compiler bugs, the answer is no, _hopefully_.  
Instead of merely hoping this, we would like to formally prove this. This requires a precise, formal, mathematical description of what Rust programs are, what they do, and what is checked by e.g. the borrow checker—in other words, a formal specification of Rust.  
Further, there is a growing variety of tools consuming Rust, like [gccrs](https://blog.rust-lang.org/2024/11/07/gccrs-an-alternative-compiler-for-rust/) or formal verification tools. A formal specification ensures that all these tools agree on what Rust code means, which is currently not the case.

## So, what has been formalized?

Currently, there are several loosely connected groups formalizing various parts of Rust. For example, people are working on the operational semantics, the borrow checker, or the trait system. We have a [vision](/topics/vision) for how this can all be connected, but putting this into practice is very hard.
