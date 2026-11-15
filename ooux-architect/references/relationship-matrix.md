# Relationship Matrix: [Project / Domain]

Read **row -> column**. Each cell: `verb (cardinality)`. Leave `-` where no relationship exists.
Cardinality: `0..1` optional one, `1..1` exactly one, `0..*` zero or many, `1..*` one or many.

| From \ To | ObjectA | ObjectB | ObjectC |
|---|---|---|---|
| **ObjectA** | n/a | has (0..*) | belongs to (1..1) |
| **ObjectB** | belongs to (1..1) | n/a | - |
| **ObjectC** | has (0..*) | - | n/a |

## Relationship List

| # | From | Verb | To | From side | To side | Nested? | Notes |
|---|---|---|---|---|---|---|---|
| 1 | ObjectA | has | ObjectB | 1..1 | 0..* | Yes, B nests in A | |

## Join Objects Needed (many-to-many)

| Pair | Proposed join object | SIP passed? |
|---|---|---|
| | | |

## Flags

- **Orphans:**
- **Ambiguous connections:**
- **Cycles / redundant paths:**

## Gate 2 Status

- [ ] User confirmed System Model on [date]
