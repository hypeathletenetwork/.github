# Contributing

How changes are made, for everyone who works in these repositories.

## Before you start

1.  Find the ticket. Every branch, commit and pull request carries a real ticket
    key. Never invent one.
1.  Look for existing work. Search open pull requests and branches for the key,
    and extend what is there instead of starting a second copy.
1.  Claim the ticket: set yourself as assignee, move it to In Progress and say
    which branch you are using.

## Making the change

- Branch as `HAM-<n>/short-slug`.
- Write commits in Conventional Commits form with the key after the scope, for
  example `fix(chat): HAM-123 refuse an empty message id`.
- Keep a change to what the ticket needs. Do not mix in unrelated refactors.
- Run the repository's lint and tests before you open a pull request.

## Opening the pull request

- Title it `HAM-<n> - Sentence-case summary`.
- Fill in the template. It ends with what you verified and a list of what
  still needs checking, with an owner for each item.
- After it merges, move the ticket on the same day: Ready For QA if it is
  merged but not yet verified, Done only when the checks are finished.

## Secrets and personal data

Never put a secret, a token or personal data in a commit, a pull request, an
issue or a chat. If one gets in, tell the team straight away so it can be
rotated. Deleting the file does not undo it.

## Security problems

Do not open a public issue. See the security policy.
