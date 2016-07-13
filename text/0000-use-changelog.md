- Start Date: 2016-07-13
- RFC PR: (leave this empty)
- Nix Issue: (leave this empty)

# Summary
[summary]: #summary

We use a change log file to document API changes of released versions relative
to their predecessors.

# Motivation
[motivation]: #motivation

Change logs are a common and convenient way to document API changes in a single
location. Being able to easily find notes on breaking changes is particularly
useful.

# Detailed design
[design]: #detailed-design

We follow the conventions laid out in [Keep A CHANGELOG](https://github.com/olivierlacan/keep-a-changelog/tree/18adb5f5be7a898d046f6a4acb93e39dcf40c4ad).

We add a section to CONTRIBUTIONS.md, encouraging contributors to add
appropriate entries to the change log as part of their pull requests.

We add a section to RELEASE_PROCESS.md (which does not exist yet), that tasks
the persons creating a new release with updating CHANGELOG.md appropriately.

We add an initial CHANGELOG.md file.

# Drawbacks
[drawbacks]: #drawbacks

It adds a bit of work to the development process.

# Alternatives
[alternatives]: #alternatives

We could decide not to keep a change log.

# Unresolved questions
[unresolved]: #unresolved-questions

None.
