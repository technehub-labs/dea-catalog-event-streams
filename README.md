# Event / Event Stream

> A discrete state change or stream of changes, published with a topic and schema.

**Layer:** L3 · **Entity:** `EVT` · **Metamodel:** [v2.0.0-alpha](https://github.com/technehub-labs/dea-metamodel)

[![View in Metamodel Explorer](https://img.shields.io/badge/Metamodel%20Explorer-View%20Entity-2C3E50?style=shield)](https://technehub-labs.github.io/metamodel/?entity=EVT)

## Status

This is a **scaffold** repository — created during the Phase 1 metamodel v2 rollout.
Content population is planned for a subsequent phase.

## Entity Definition

| Field | Value |
|-------|-------|
| Entity ID | `dea:entity-evt` |
| Class Alias | `EVT` |
| Layer | `L3` |
| Metamodel Version | v2.0.0-alpha |

## Catalog Structure

```
dea-catalog-event-streams/
├── metamodel-pointer.yaml   ← entity mapping (do not edit manually)
├── entities/
│   └── v1-alpha/          ← catalog entries go here
│       └── README.md
├── schemas/                ← JSON Schema for this entity type
│   └── entity.schema.json
└── .github/
    └── workflows/
        └── ci.yml         ← validates entries against schema
```

## Contributing

See [CONTRIBUTING.md](./CONTRIBUTING.md) and the
[DEA Metamodel](https://github.com/technehub-labs/dea-metamodel) for guidance.
