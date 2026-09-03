# Process

Short reference docs for how work moves through OZEAON.

Read these before raising a change, opening a ticket, or asking why something is not in dev yet.

## Contents

- [kanban.md](kanban.md). The 10-column board on Monday. What each column means, who owns it, and how design work reaches the dev track.
- [change-requests.md](change-requests.md). How to change something that has already been signed off, specced, or shipped. Includes the design change flow and the bug reporting rule.
- [preview-environments.md](preview-environments.md). QA now happens on the pull request's own preview environment rather than on staging. Where the link comes from, the test accounts, and what it changes for QA.
- [documentation-conventions.md](documentation-conventions.md). Where visual detail lives (Figma) versus where behaviour lives (specs), and how the two stay in sync without duplicating each other.

## The one-line version

Spec writing, design ideation, and signoff happen in columns 1 to 6, spec first. It then enters the dev track at column 7, broken into granular dev tickets if it covers an area of the product, or as it stands if it is already a single piece of work. Anything that changes after a ticket reaches Design Done needs a change request. Internal feedback goes to BA/PM, who triage before anything reaches dev or design. External bugs come in via the bug report form.
