# Kanban

Work flows through 10 phases on the OZEAON Tasks board on Monday.

The board is split into two tracks. Columns 1 to 6 are the design track, run by BA, Designer, and PM. Columns 7 to 10 are the dev track, run by Engineering and QA.

<img width="2234" height="612" alt="image" src="https://github.com/user-attachments/assets/57dac624-0b47-400a-aa6f-32d73e83f5cd" />

## Design track

The spec comes first. BA and PM write it, and the designer designs against it.

1. Specs Pending - the entry point for a feature. BA and PM write the functional and logic spec, at feature level, for example "User Dashboard and Settings" or "Educational Resources".
2. Ready for Design - spec is written and the feature is upcoming next for designers.
3. Design in Progress - designer working in Figma against the spec. Design work often surfaces gaps or contradictions in the spec, which BA amends as they go.
4. Design Review - waiting for Joseph's signoff on visual direction.
5. Create Dev Tickets - designs are signed off and fully synced with the spec. The work that will actually be built is put into Ready for Dev from here. A broad design ticket is broken down into granular dev tickets; a narrow one that is already the size of a single piece of work moves across as it is.
6. Design Done - designs are frozen and the dev work exists on the board. Where the design ticket was broken down, it is closed as delivered here and goes no further.

## Dev track

7. Ready for Dev - developer ticket backlog, whether based on designs or not. This is where the dev tickets created in column 5 land, alongside any purely technical work.
8. Dev in Progress - developer building the ticket.
9. Code Review + QA - PR created, code reviewed, and QA'd on the PR's own preview environment, then merged. The ticket stays here for all of it, so review and QA are tracked on the ticket rather than as separate columns. See [preview-environments.md](preview-environments.md).
10. Done - reviewed, QA accepted, and merged.

## Getting from design to dev

Column 5 is a judgement call between BA, PM, and a dev lead: is this ticket already one piece of work, or is it an area of the product?

"Update the icon in the article header" is one piece of work. It moves straight into Ready for Dev.

"User Dashboard and Settings" is an area, and needs breaking into granular tickets - "Add account deletion confirmation modal", "Wire up notification preferences form", "Persist theme choice per user". Each one links back to the parent design ticket so the original design context is traceable.
