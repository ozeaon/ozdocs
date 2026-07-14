# Kanban

Work flows through 13 phases on the OZEAON Tasks board on Monday.

The board is split into two tracks. Columns 1 to 6 are the design track, run by BA, Designer, and PM. Columns 7 to 13 are the dev track, run by Engineering and QA. A design ticket does not move from column 6 into column 7. It is translated. See "How design tickets become dev tickets" below.

## Design track

1. Ready for design. Upcoming next for designers. Written as a feature-level brief, for example "User Dashboard and Settings" or "Educational Resources".
2. Design in progress. Designer working in Figma.
3. Design review. Waiting for Joseph's signoff on visual direction.
4. Specs pending. Designs are signed off. BA and PM write the functional and logic spec against the signed-off design. This may surface small design adjustments, which the designer applies before moving on.
5. Create dev tickets. Specs are written and fully synced with designs. The design ticket is broken down here into the granular dev tickets that will actually be built.
6. Designs are frozen and dev tickets have been created. The design ticket is closed as delivered. It does not move any further.

## Dev track

7. Ready for dev. Developer ticket backlog, whether based on designs or not. This is where the dev tickets created in column 5 land, alongside any purely technical work.
8. Dev in progress.
9. Code review. PR created, ready for review.
10. Deploy queue. PR approved and merged, waiting for deployment.
11. Ready to QA. Code has been merged and deployed.
12. QA. QA in progress.
13. Done.

## How design tickets become dev tickets

A design ticket is broad. Example: "User Dashboard and Settings". It covers a whole area of the product.

A dev ticket is granular. The same area might produce ten or twenty dev tickets. Example: "Add account deletion confirmation modal", "Wire up notification preferences form", "Persist theme choice per user".

The translation happens in column 5, Create Dev Tickets, and it is a joint step between BA, PM, and a dev lead. The output is a set of TOZN-prefixed tickets in Ready for Dev. The parent design ticket is linked from each dev ticket so we can trace back to the original design context.
