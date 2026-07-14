# Kanban

Work flows through 13 phases on the OZEAON Tasks board on Monday.

The board is split into two tracks. Columns 1 to 6 are the design track, run by BA, Designer, and PM. Columns 7 to 13 are the dev track, run by Engineering and QA. A design ticket does not move from column 6 into column 7. It is translated. See "How design tickets become dev tickets" below.

## Design track

<img width="1650" height="498" alt="image" src="https://github.com/user-attachments/assets/71df42ad-f98d-4853-8547-3241ea30e9d7" />

1. Ready for Design - upcoming next for designers. Written as a feature-level brief, for example "User Dashboard and Settings" or "Educational Resources".
2. Design in Progress - designer working in Figma.
3. Design Review - waiting for Joseph's signoff on visual direction.
4. Specs Pending - designs are signed off. BA and PM write the functional and logic spec against the signed-off design. This may surface small design adjustments, which the designer applies before moving on.
5. Create Dev Tickets - specs are written and fully synced with designs. The design ticket is broken down here into the granular dev tickets that will actually be built.
6. Design Done - designs are frozen and dev tickets have been created. The design ticket is closed as delivered. It does not move any further.

## Dev track

<img width="1649" height="691" alt="image" src="https://github.com/user-attachments/assets/9ac3766a-3dd6-4672-805e-bd418666a29f" />

7. Ready for Dev - developer ticket backlog, whether based on designs or not. This is where the dev tickets created in column 5 land, alongside any purely technical work.
8. Dev In Progress.
9. Code Review - PR created, ready for review.
10. Deploy Queue - PR approved and merged, waiting for deployment.
11. Ready to QA - code has been merged and deployed.
12. QA - QA in progress.
13. Done.

## How design tickets become dev tickets

A design ticket is broad. Example: "User Dashboard and Settings". It covers a whole area of the product.

A dev ticket is granular. The same area might produce ten or twenty dev tickets. Example: "Add account deletion confirmation modal", "Wire up notification preferences form", "Persist theme choice per user".

The translation happens in column 5, Create Dev Tickets, and it is a joint step between BA, PM, and a dev lead. The output is a set of TOZN-prefixed tickets in Ready for Dev. The parent design ticket is linked from each dev ticket so we can trace back to the original design context.
