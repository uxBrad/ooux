# Object Map: [Project / Domain]

Confirmed after Gate 2. This is the system model, not a sitemap.

## Diagram

```mermaid
erDiagram
    ObjectA ||--o{ ObjectB : "has"
    ObjectB }o--|| ObjectC : "belongs to"
    ObjectA }o--o{ ObjectC : "relates to"

    ObjectA {
        string name "Core 1"
        string summary "Core 2"
        date createdAt "Meta"
        string status "Meta"
    }
```

Cardinality notation: `||` exactly one, `o|` zero or one, `}o` zero or many, `}|` one or many.

## Optional: Class Diagram View

```mermaid
classDiagram
    class ObjectA {
        +name
        +summary
        +status
        create()
        update()
        archive()
    }
    ObjectA "1" --> "0..*" ObjectB : has
```

## Summary Table

| Object | Definition | Nested in | Key relationships | Top 3 attributes | Key CTAs |
|---|---|---|---|---|---|
| | | | | | |
