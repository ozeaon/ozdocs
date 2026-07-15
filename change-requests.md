# Change requests

A change request is any change to a feature after column 6, Design Done. This covers design tweaks, spec corrections, dev-initiated changes, and bugs. The same flow applies regardless of who triggers it — designer, developer, Joseph, QA, or BA.

Adjustments made during columns 4 and 5 (Specs Pending, Create Dev Tickets) do not need a change request. That is the point of those columns: BA and PM are writing specs against the design, and small design adjustments to keep the two in sync are expected. Once the ticket reaches Design Done, any further change needs a change request.

Every change request needs a ticket. Discussion in chat does not count as a request and will not be picked up by the dev team. BA owns the change request process end to end: intake, spec updates, coordination with Designer, and confirmation that spec and design are aligned before the ticket returns to Ready for Dev.

## Internal feedback

Joseph and other internal stakeholders send feedback directly to BA/PM. Not to the dev channel, not to designers, not scattered across chat threads. BA/PM triages: what is a bug, what is an improvement, what is out of scope, what is already covered. Only after that triage does anything reach dev or design, and only via a ticket.

The point is to protect the dev and design teams from unstructured, in-flight commentary. If something needs to change, it becomes a ticket. If it does not, it stops with BA/PM. Devs and designers should only ever see filtered, actionable input.

## Bugs

The [bug report form](https://docs.google.com/forms/d/e/1FAIpQLSc3XCR9CQah3jCu-Uw6a-htuVCTXGMmMmYtrG9QQacyI_EhDQ/viewform) is the intake channel for bug reports from users and external testers. It is not the channel for internal team members. Internal bug reports go to BA/PM under the internal feedback flow above.

Bugs raised in dev or design chat will be ignored. This is not a courtesy rule, it is how the dev team keeps the queue coherent.

## Design changes after freeze

Once a ticket reaches Design Done, the developer-facing Figma is the reference for dev. Do not edit it directly.

If a designer wants to change something after freeze, the flow is:

1. Ideation in a playground or draft file. The designer explores the change without touching the developer-facing Figma. Devs can be invited to view the playground for feedback.
2. Signoff on the direction with Joseph.
3. Change request ticket, assigned to BA and Designer.
4. BA updates the spec if the change affects function or logic. If the change is purely visual and the spec already covers behaviour, the BA notes this on the ticket.
5. Designer updates the developer-facing Figma to match the signed-off direction.
6. Ticket moves to Ready for Dev only once spec and design are aligned.

This applies to every change, including ones that feel mechanical. Correcting an avatar component, adjusting a card height, swapping an icon: these all go through the flow above. The developer-facing Figma does not get edited ad-hoc. If it is worth changing, it is worth a ticket.

### Small design changes

Worked example, swapping an icon in the top navigation bar:

1. Designer makes the change in the playground and attaches a screenshot or link to the new version on the ticket.
2. BA reviews and marks the ticket as either **Needs spec update** or **No spec update needed**.
3. BA sign-off. Ticket moves to Ready for Dev.
4. PM sign-off. PM assigns the dev and tags the Designer to permit the developer-facing Figma update.
5. Designer updates the developer-facing Figma.
6. Dev delivers to prod.

## Dev-initiated changes

Two flavours, depending on whether the dev has already made the change or is blocked by a spec/design mismatch.

Dev-notified. The change is small, obvious, and the dev has already made it. They open a change request ticket to record it, BA and Designer update the spec and design to match, no discussion needed. The ticket exists so the docs stay authoritative, not to relitigate the call.

Dev-blocked. The dev spots a spec/design mismatch that stops them from implementing. They open a change request ticket and flag it as blocking. BA owns the decision, syncs with Designer if needed, and unblocks the dev. Same-day turnaround is the default.

In both cases the ticket is the record. No silent edits to spec or design without a ticket, and no PR merged against the spec without a ticket to explain the divergence.

## Post-delivery changes

Once a feature is delivered, the original spec becomes historical documentation of the decision. Future changes are new change requests against the current behaviour.
