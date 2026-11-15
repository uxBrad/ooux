# JSON Schema Export (optional)

Translate the confirmed Object Map into data structures. Rules:

- One schema per Object. Name = canonical term, PascalCase.
- Attributes become `properties`, ordered by forced rank. Core Content first, Metadata after, tagged with `x-group`.
- `x-rank` carries the forced rank so the hierarchy survives the export.
- Relationships:
  - `1..1` / `0..1` -> `{object}Id` string property (required for `1..1`).
  - `0..*` / `1..*` -> array of ids, `minItems: 1` for `1..*`.
  - Many-to-many -> the join object holds both ids.
- States become an `enum` on a `status` property.
- Do not add fields the model does not contain. List anything you had to assume.

## Template

```json
{
  "$schema": "https://json-schema.org/draft/2020-12/schema",
  "$id": "https://example.com/schemas/ObjectA.json",
  "title": "ObjectA",
  "description": "[Definition from Object Guide]",
  "type": "object",
  "properties": {
    "id": { "type": "string" },
    "name": { "type": "string", "x-group": "core", "x-rank": 1 },
    "summary": { "type": "string", "x-group": "core", "x-rank": 2 },
    "status": {
      "type": "string",
      "enum": ["draft", "submitted", "approved", "archived"],
      "x-group": "metadata",
      "x-rank": 3
    },
    "objectCId": { "type": "string", "description": "belongs to ObjectC (1..1)", "x-group": "metadata", "x-rank": 4 },
    "objectBIds": {
      "type": "array",
      "items": { "type": "string" },
      "description": "has ObjectB (0..*)",
      "x-group": "metadata",
      "x-rank": 5
    }
  },
  "required": ["id", "name", "objectCId"]
}
```
