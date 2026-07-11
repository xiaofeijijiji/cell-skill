# Optional Skill Adapters

Adapters extend Cell Skill but do not define its core behavior.

## Discovery

Inspect the current skill catalog and choose by declared description. Do not
assume that a package, vendor, or folder name is installed. Prefer a specialized
adapter when it closely matches a bounded stage such as database retrieval,
sequence analysis, structure search, figure production, document generation, or
literature verification.

## Invocation Contract

1. Read the selected adapter's complete `SKILL.md` before acting.
2. Load only references required for the current stage.
3. Give the adapter a concrete input, expected output, and acceptance criteria.
4. Preserve returned provenance, warnings, and uncertainty.
5. Validate the result with Cell Skill's quality gates.
6. Do not copy adapter instructions into Cell Skill or redistribute adapter
   assets without license permission.

## Composition

Use adapters in a directed chain. Examples:

- retrieval adapter -> analysis adapter -> visualization adapter -> writing
  adapter;
- identifier resolver -> database query -> integrative interpretation;
- document reader -> evidence extractor -> reviewer or presentation workflow.

Avoid circular delegation. One workflow must remain responsible for the final
scientific conclusion and artifact.

## Fallback

If an adapter is unavailable, incompatible, or license-restricted:

- use official APIs or documented command-line tools;
- use established open-source libraries for analysis;
- implement only the task-specific glue needed to connect them;
- disclose reduced coverage or validation limits;
- never fabricate adapter output.
