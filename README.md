# Epicollect5 Schemas

Canonical JSON Schemas shared across Epicollect5 repositories.

The schemas use [JSON Schema Draft 2020-12](https://json-schema.org/draft/2020-12). Each schema has its own version in its `$id` under `https://epicollect.net/schemas/`. There is no shared schema-set version: repositories can depend on and update only the schemas they use.

## Schemas

| File                               | Describes                                    |
|------------------------------------|----------------------------------------------|
| `project.schema.json`              | Epicollect5 project definition and mapping   |
| `entry-payload.schema.json`        | Entry upload payloads                        |
| `branch-entry-payload.schema.json` | Branch entry upload payloads                 |
| `file-entry-payload.schema.json`   | JSON data carried with file uploads          |
| `delete-entry-payload.schema.json` | Single-entry deletion payloads               |
| `entry-data.schema.json`           | Normalized entry data stored by the platform |
| `geo-json-data.schema.json`        | GeoJSON location data stored by the platform |

## Versioning

Version each schema independently using semantic versions in its `$id`. When changing a schema contract, update that schema's version according to the compatibility impact. Keep the schema change and its `$id` update together in the same pull request.

A schema's content must not change without a corresponding version change. Consumers should track the schema files they use and pin each to the version in its `$id`. They can then check for updates and vendor schemas independently.
