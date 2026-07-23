# New feature process

How a feature moves from an idea into column 1 of the kanban board. Discovery, in other words.

Every new feature goes through discovery before it appears in [kanban.md](kanban.md) as Ready for Design. The output of discovery is a signed-off BRD, a signed-off design direction, and a team-facing PRD (functional specification). Without all three, the feature does not enter the design track.

Roles in this phase: Joseph (product), Olena (BA/PM), Roman (design).

## 1. BRD

Joseph and Olena write the Business Requirements Document together. It captures the problem, the target users, the goals, and the constraints. It does not describe screens, flows, or components.

The BRD is signed off before any design or spec work begins. It is the anchor for everything that follows.

## 2. Design and spec loop

Once the BRD is signed off, two workstreams start in parallel and feed each other.

- Joseph and Olena work with Roman on UX and UI. Roman explores flows, layouts, and states in Figma. Joseph and Olena feed in constraints from the BRD and push back on decisions where needed.
- Olena writes the team-facing PRD, the functional specification. It captures behaviour, states, transitions, validation, permissions, and side effects. It follows the same split as [documentation-conventions.md](documentation-conventions.md): behaviour lives in the PRD, visuals live in the Figma.

The two loop. A design decision often clarifies a spec question, and a spec question often surfaces a design gap. Expect several passes back and forth before either side is stable.

## 3. Refinement and signoff

The loop closes when:

- Roman has produced proper designs, not exploratory sketches. Suitable for review inside the design track.
- Olena has delivered a refined functional specification aligned with those designs.
- Joseph is satisfied that both reflect the BRD.

At this point discovery is done. The feature is created as a design ticket and enters column 1, Ready for Design, on the kanban board. From there it picks up the flow described in [kanban.md](kanban.md).

## After discovery

Once discovery is done, the BRD, PRD, and designs are the reference for everything downstream. Any change to them follows [change-requests.md](change-requests.md), except while the ticket sits in columns 4 or 5 where small adjustments are expected as spec and design are synced.
