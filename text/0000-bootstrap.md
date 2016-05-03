- Start Date: 2016-05-01
- RFC PR: (leave this empty)

# Summary
[summary]: #summary

Implement a lightweight RFC process for the nix project.

# Motivation
[motivation]: #motivation

Development on nix has been going well over the last few months. For the most
part, adding APIs and working out how to adapt them to be more Rust-friendly
has worked really well. However, there are some tougher design choices where
there's been stagnation. Some examples:

- string handling in nix (https://github.com/nix-rust/nix/issues/221)
- the future of nix, including crate organization
  (https://github.com/nix-rust/nix/issues/190)

The RFC process gives a place to discuss and document major design
decisions. This provides readers with both the final decision in a clean form
and the discussion that lead up to it.

We have already created a [conventions document][conventions] to help newcomers
to the library understand how nix approaches its APIs. Larger additions to that
document would also go through the RFC process.

[conventions]: https://github.com/nix-rust/nix/blob/master/CONVENTIONS.md


# Detailed design
[design]: #detailed-design

*The contents of this section will make up the bulk of the RFC repository's
README after this RFC is accepted.*

The nix RFC process is modelled after [the one Rust uses][rust-rfc-process] but
adjusted to be lighter weight. Credit for the lightness also goes to the
[intermezzOS project's RFC process][intermezzos-rfcs].

[rust-rfc-process]: https://github.com/rust-lang/rfcs#what-the-process-is
[intermezzos-rfcs]: https://github.com/intermezzOS/rfcs

To initially discuss a topic, open an issue on [the RFC repo][nix-rfcs]. We’ll
discuss things in those issues.

[nix-rfcs]: https://github.com/nix-rust/rfcs

When a proposal is ready to be made, submit a pull request adding a new file in
the `text` directory. More detailed steps:
  - Fork the RFC repo http://github.com/nix-rust/rfcs
  - Copy `0000-template.md` to `text/0000-my-rfc-name.md` (where `my-rfc-name`
    is descriptive. don't assign an RFC number yet).
  - Fill in the RFC, and open the pull request

We’ll discuss things in the PR, and then either merge or not. The RFC text will
likely change as we discuss it; those changes should be added to the PR as
additional commits without squashing or rebasing to keep a record of the them.


# Drawbacks
[drawbacks]: #drawbacks

It adds some process where there was none.

# Alternatives
[alternatives]: #alternatives

## No process

We could continue as we have. This has already resulted in some stagnant areas
where we need to make a decision to move forward. 

## More process

We could instead opt for a heavier process. It is most likely not warranted for
the size of the project.

# Unresolved questions
[unresolved]: #unresolved-questions

What sections should be in the template? The same as in this RFC?
