Useful additional Git commands
==============================

Description
-----------

This repository hosts a collection of miscellaneous extra Git commands (in the
form of scripts building mostly on top of Git plumbing commands) that have
proved useful.

Installation
------------

Those scripts are supposed to be made available to your local Git installation
(either by copying them in a location on the `PATH` or by defining
[Git aliases](https://git-scm.com/book/en/v2/Git-Basics-Git-Aliases)) in
order to act as invokable custom Git commands.

Commands
--------

### git-disseminate ###

Usage: `git disseminate [A...B]`

**Finds all non-merged commits in `A` but not in `B`** (that have not been
cherry-picked from `B`, looking for at most 1,000 commits) that contains
`!disseminate!` in their commit message, **and cherry-picks them to the current
branch.**

The `!disseminate!` tag does not need to be at the beginning of a new line and
can appear anywhere in the commit message body (as well as in the subject).

When `git disseminate` is called with no arguments, `A` defaults to `master`
and `B` to the current branch.

### git-gc-all-ferocious ###

Usage: `git gc-all-ferocious`

Performs a **very** aggressive GC! **Beware of data loss!**

See: <https://stackoverflow.com/a/14728706>
