# Preview environments

QA happens on the preview environment for the branch, not on staging.

Every pull request into `develop` gets its own deployed copy of the site with its own database. That copy is where the ticket is reviewed and QA'd. Only once it passes does the work merge. Staging is no longer the QA gate: it is where merged work lands, so by the time a change reaches it, it has already been accepted.

Ideally a ticket has exactly one pull request, so every ticket has a preview to look at and every preview answers a single ticket. Some pull requests have no ticket behind them - refactors, dependency bumps, infrastructure, tidying. Those still get a preview, but they merge on code review alone and do not need QA approval. That is fine and expected. QA approval gates the tickets, not every single PR.

The point of the change is that a ticket is now tested in isolation. Previously everything queued up on staging together, so a failure could belong to any of the changes sitting there and a rejected ticket had to be unpicked from the others. On a preview, the only thing that has changed is the ticket in front of you.

## Getting the link

The URL is posted as a comment on the pull request in GitHub, and takes the form:

```
https://pr-123-app-ozeaon.joseph-400.workers.dev
```

The number is the pull request number. The developer links the pull request from the Monday ticket when they move it into Review + QA, so the ticket is the starting point either way.

It takes roughly seven minutes from the pull request opening for the URL to work.

## Test accounts

|          |                                                                      |
| -------- | -------------------------------------------------------------------- |
| Email    | `alpha@ozeaon.com` through to `tango@ozeaon.com` (the NATO alphabet) |
| Password | `ozeaon-preview`                                                     |

Each preview is seeded with the same fixture: twenty accounts, three organisations, projects, articles, posts, and imagery. That means a known starting state on every ticket, which staging never gave you. Test data you create lives and dies with that preview.

## What this changes for QA

- Test the ticket on its own preview and record the result on the Monday ticket before it merges. A failure goes back to the developer on the same pull request.
- Do not wait for a staging deployment to start QA. The work is testable as soon as the pull request is open.
- The preview is destroyed when the pull request merges or closes. Capture screenshots for anything that needs to live on the ticket.
- If the developer pushes a fix after you have tested, the code updates but the sample data does not. Data-related fixes need the pull request closed and reopened to reseed — ask the developer to confirm they have done that before retesting.

## Two traps

**Previews send real email.** Sign-ups and invitations produce real messages to whatever address is typed. Use a made-up address unless you are specifically testing that an email arrives.

**Uploaded images persist after the preview is destroyed.** Nothing confidential.

## When the preview itself is broken

Empty pages, missing content across the board, or a URL that never appears are build failures, not defects in the ticket. They belong back with the developer rather than in a QA report. Everything else is fair game.
