<!--
Title:  HAM-<n> - Sentence-case summary
Branch: HAM-<n>/short-slug

Write for a reviewer who has not seen the ticket. Keep it short and delete any
section with nothing to say. Never paste a secret, a token or personal data.
-->

## What

One or two sentences on what changes for users or callers.

## Why

The problem, with the Jira link.

## Design decisions

Each non-obvious choice, with the reason and the alternative you rejected.

## Review focus

What is worth blocking on, and what is fine to skim.

## Testing

What you ran, and what you checked by hand.

## CI scope (platform-api only, delete elsewhere)

A platform-api pull request runs only the tests that import the files it
changed. It runs the whole suite on its own for anything outside TypeScript in
`src/` and `tests/` (migrations, config, workflow, setup and data files), for
a deleted file, or when no test imports the change. Draft pull requests skip
the suite until they are ready, or carry the `run-ci` label.

Add the `full-ci` label to force the full suite when a TypeScript-only change
could reach code the tests load without importing it: dynamic imports, routes
or plugins registered at runtime, or helpers and fixtures shared widely.

Pushes to `dev` always run the full suite, and the dev deploy waits on it. If
a pull request passed but breaks `dev`, report it in the team Slack thread.

- [ ] platform-api only: `full-ci` label added if the change could reach code the tests do not import (or N/A).

## QA still to do

Name an owner for each item. There is no separate QA team: whoever opens the
pull request owns checking it, or hands a named person an exact checklist.

- [ ] Check: owner

## Before you open this

- [ ] The title and the branch carry a real ticket key.
- [ ] Lint and tests pass, and any new behaviour has a test.
- [ ] Nothing in the diff is a secret, a token or personal data.
