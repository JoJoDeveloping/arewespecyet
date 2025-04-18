+++
title = "English prose"

[extra]

intro = "Many specifications are written in English prose, and this is bad."
+++

When you read this website, you will find that a common complaint about some specification efforts is that they are carried out in "English prose."
We are of the opinion that this is not sufficient for _truly_ specifying a language, for several reasons.

The first problem is that writing specs in a human language makes it very easy to accidentally introduce ambiguities.
It is possible to use terms without a definition, it is possible to define things that are ambiguous, and more worringly, it is possible to use a term that one thinks has a sound definition, but then other people disagree on what precisely this term means.

The next problem is that the particular style of English makes it quite hard to give a top-down view of the language to be specified.
Things that are important for the large-scale shape of the language, like the shape of memory or of values, might only be described piecemeal.
While such a specification is technically unambiguous, it is hard to navigate and makes it easy to overlook things.
Understanding such a specification requires training in "rules-lawyering," which makes the specification needlessly inaccessible.

The C standard is a famous example of a specification written in English prose that has all the issues above.
This has lead to many different variations of C, and it is common to ignore parts of the specification that one does not like.
Ambiguities in key parts of the specification have resulted in misunderstandings, so that even tools that try to follow the standard end up disagreeing in important parts.

This leads us to the true problem with written specifications, namely that they require humans to interpret them.
If the spec was truly unambiguous, it should be understandable by a computer.
There should be a way of testing programs for conformance with the specification that does not require someone to read and interpret several hundred pages of rules.
In other words, the specification should be _executable_ and machine-readable.

This leads us to the [vision](/topics/vision) for the specification: executable, easy to understand, readable for machines and humans alike.
