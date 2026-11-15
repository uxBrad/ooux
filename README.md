# ooux-architect

A Claude skill for practicing Object-Oriented UX (OOUX) with Sophia Prater's ORCA method: Objects, Relationships, Calls to Action, Attributes.

It enforces structure before screens. No wireframes, navigation, or flows until the object model is done.

## Workflow

| Stage | Output | Gate |
|---|---|---|
| 1. Noun foraging | Object list, filtered with the SIP test (Structure, Instances, Purpose) | You confirm the Object List |
| 2. Relationships | Relationship matrix with cardinality, nested objects, orphan flags | You confirm the System Model |
| 3. Calls to Action | CTA matrix by role and object state | Check-in |
| 4. Attributes | Core Content vs Metadata, forced-ranked | Done |

Workflows like Onboarding or Checkout are never objects. The skill converts them to persistent objects (Account, Order) or CTAs.

## Install

Copy the `ooux-architect/` folder into one of:

- `~/.claude/skills/` (all projects)
- `<your-project>/.claude/skills/` (one project)

Then ask Claude to model a domain, or paste requirements or a transcript.

## Contents

```
ooux-architect/
├── SKILL.md
└── references/
    ├── object-guide.md
    ├── relationship-matrix.md
    ├── cta-matrix.md
    ├── object-map.md
    └── json-schema-export.md
```

## Credit

ORCA and OOUX are Sophia V. Prater's methodology. This skill is an independent implementation, not affiliated with or endorsed by her.
