- Start Date: 2022-10-05
- RFC PR: (leave this empty)
- Nix Issue: (leave this empty)

# Summary
[summary]: #summary

Add the following targets as tier 3 supported platforms:
  * `aarch64-unknown-linux-musl`
  * `arm-unknown-linux-musleabihf`
  * `armv7-unknown-linux-musleabihf`
  * `powerpc-unknown-linux-musl`
  * `powerpc64-unknown-linux-musl`
  * `riscv64gc-unknown-linux-musl`
  * `s390x-unknown-linux-musl`

# Motivation
[motivation]: #motivation

The listed targets are used by Alpine Linux for supported architectures (Alpine
creates its own targets, but they are based on the listed ones), except the ones
already supported in nix (`x86_64-unknown-linux-musl`, `i686-unknown-linux-musl`),
and `powerpc64le-unknown-linux-musl`, which is not supported by the libc crate.

Nix failures to compile block at least 10 packages from getting built
for s390x and/or riscv64 architectures, my quick GitLab search for "nix crate" shows.
This should help to monitor potential changes in nix for breaking these architectures.

# Detailed design
[design]: #detailed-design

N/A

# Drawbacks
[drawbacks]: #drawbacks

Possibly increased needed maintainership time. However, failing tier 3 CI
should not be blocking code from inclusion.

# Alternatives
[alternatives]: #alternatives

No new targets.

# Unresolved questions
[unresolved]: #unresolved-questions

N/A
