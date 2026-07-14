# Change requests

A change request is any change to a feature after column 6, "designs are frozen and dev tickets have been created". This covers design tweaks, spec corrections, dev-initiated changes, and bugs.

Adjustments made during columns 4 and 5 (specs pending, create dev tickets) do not need a change request. That is the point of those columns: BA and PM are writing specs against the design, and small design adjustments to keep the two in sync are expected. Once the design is frozen at column 6, any further change needs a ticket.

Every change request needs a ticket. Discussion in chat does not count as a request and will not be picked up by the dev team.

## Bugs

Bugs go through the bug report form. Bugs raised in chat will be ignored. This is not a courtesy rule, it is how the dev team keeps the queue coherent. If a bug is urgent, mark it Critical on the form.

## Design changes after freeze

Once designs are frozen at column 6, the developer-facing Figma is the reference for dev. Do not edit it directly.

If a designer wants to change something after freeze, the flow is:

1. Ideation in a playground or draft file. The designer explores the change without touching the developer-facing Figma. Devs can be invited to view the playground for feedback.
2. Signoff on the direction with Joseph.
3. Change request ticket, assigned to BA and Designer.
4. BA updates the spec if the change affects function or logic. If the change is purely visual and the spec already covers behaviour, the BA notes this on the ticket.
5. Designer updates the developer-facing Figma to match the signed-off direction.
6. Ticket moves to Ready for Dev only once spec and design are aligned.

This applies to every change, including ones that feel mechanical. Correcting an avatar component, adjusting a card height, swapping an icon: these all go through the flow above. The developer-facing Figma does not get edited ad-hoc. If it is worth changing, it is worth a ticket.

## Dev-initiated changes

If a developer discovers during implementation that a spec or design needs to change, they raise a change request the same way. They do not silently edit the spec or the design. They do not merge a PR that diverges from the spec.

If the change is small and blocking, the dev can flag it in the ticket, ping BA and Designer, and get a same-day decision. The decision still gets recorded on a ticket, even if the ticket is opened after the fix.

## Post-delivery changes

Once a feature is delivered, the original spec becomes historical documentation of the decision. Future changes are new change requests against the current behaviour.
