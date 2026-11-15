# CTA Matrix: [Project / Domain]

## Roles

| Role | Description | Source |
|---|---|---|
| | | stated / ASSUMPTION |

## CTAs by Object

Legend: Y = allowed, O = own items only, - = not allowed.

### [ObjectName]

States: [Draft -> Submitted -> Approved -> Archived]

| CTA | Type | Role 1 | Role 2 | Role 3 | Precondition (state) | Resulting state | Side effects on other objects |
|---|---|---|---|---|---|---|---|
| Create | CRUD | | | | none | Draft | |
| Read | CRUD | | | | | | |
| Update | CRUD | | | | Draft | | |
| Delete | CRUD | | | | Draft | removed | cascades to: |
| [Domain action] | Domain | | | | | | |

## Flags

- CTAs no role can perform:
- Roles with no CTAs:
- Destructive CTAs without precondition or recovery:
- CTAs that span multiple objects (candidate for a new object?):
