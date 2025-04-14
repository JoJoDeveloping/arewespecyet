+++
title = "Rust Verification Tools"

[extra]

intro = "Read this to learn more about what is verification, which tools there are for Rust, and why they rely on a formal specification."

newstag = "verification"
+++

A verification tool aims to prove that programs satisfy properties like "the program never panics."
Verification tools can be used to prove such properties even for unsafe code, for which Rust makes no guarantees.
These tools also prove much more specific properties than what safe Rust provides by default.
For example, they could prove that `Vec::sort` actually sorts the vector.

Verification tools are often separated between automatic and interactive verification.
An automatic verifier is often faster and easier to use, but an interactive verifier tends to be more powerful.

There are several verification tools for Rust, all with different features.
Currently, all these tools need to figure out themselves what are the formal semantics of Rust, in order to reason about the Rust programs given to them.
With a formal specification for Rust, it could be ensured that these tools all agree on what Rust means.
