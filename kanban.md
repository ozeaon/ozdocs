# Kanban

Work flows through 10 phases on the OZEAON Tasks board on Monday.

The board is split into two tracks. Columns 1 to 6 are the design track, run by BA, Designer, and PM. Columns 7 to 10 are the dev track, run by Engineering and QA.

## Design track

<img width="1650" height="498" alt="image" src="https://github.com/user-attachments/assets/71df42ad-f98d-4853-8547-3241ea30e9d7" />

1. Ready for Design - upcoming next for designers. Written as a feature-level brief, for example "User Dashboard and Settings" or "Educational Resources".
2. Design in Progress - designer working in Figma.
3. Design Review - waiting for Joseph's signoff on visual direction.
4. Specs Pending - designs are signed off. BA and PM write the functional and logic spec against the signed-off design. This may surface small design adjustments, which the designer applies before moving on.
5. Create Dev Tickets - specs are written and fully synced with designs. The work that will actually be built is put into Ready for Dev from here. A broad design ticket is broken down into granular dev tickets; a narrow one that is already the size of a single piece of work moves across as it is.
6. Design Done - designs are frozen and the dev work exists on the board. Where the design ticket was broken down, it is closed as delivered here and goes no further.

## Dev track

<img width="1649" height="691" alt="image" src="https://github.com/user-attachments/assets/9ac3766a-3dd6-4672-805e-bd418666a29f" />

7. Ready for Dev - developer ticket backlog, whether based on designs or not. This is where the dev tickets created in column 5 land, alongside any purely technical work.
8. Dev in Progress - developer building the ticket.
9. Review + QA - PR created, code reviewed, and QA'd on the PR's own preview environment, then merged. The ticket stays here for all of it, so review and QA are tracked on the ticket rather than as separate columns. See [preview-environments.md](preview-environments.md).
10. Done - reviewed, QA accepted, and merged.

## Getting from design to dev

Column 5 is a judgement call between BA, PM, and a dev lead: is this ticket already one piece of work, or is it an area of the product?

"Update the icon in the article header" is one piece of work. It moves straight into Ready for Dev.

"User Dashboard and Settings" is an area, and needs breaking into granular tickets - "Add account deletion confirmation modal", "Wire up notification preferences form", "Persist theme choice per user". Each one links back to the parent design ticket so the original design context is traceable.
