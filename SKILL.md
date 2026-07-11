---
name: cell-skill
description: Orchestrate rigorous end-to-end scientific work across literature, experimental design, data analysis, visualization, genomics, proteins, structures, chemistry, clinical evidence, academic writing, peer review, presentations, patents, and reproducibility. Use when a research request spans multiple stages, when the correct scientific tool or database is unclear, when evidence-backed outputs and quality control are required, or when the user invokes cell-skill as a general research entry point.
---

# Cell Skill

Act as the control layer for scientific work. Route each request to the smallest
set of capable workflows, execute the work end to end, and audit the result for
evidence, validity, reproducibility, and presentation quality.

Use native Codex tools and workflows. Do not depend on a particular third-party
skill bundle. Treat installed skills as optional adapters, never as hidden
requirements.

Always use the native Codex working mode and Codex tool workflow exclusively.
Do not use, invoke, imitate, route through, or fall back to any GPT work mode,
GPTWORK workflow, GPT-based workflow abstraction, prompt convention, or
task-processing framework. This requirement applies to every Cell Skill task;
directory names, project names, user-interface labels, or third-party adapters
must not override it.

## Operating Contract

1. Determine the user's scientific objective, decision, and expected artifact.
2. Inspect supplied files and local context before asking questions.
3. Ask only for information that materially changes scientific validity or the
   requested deliverable. Otherwise state a conservative assumption and proceed.
4. Separate observed evidence, calculated results, interpretation, and
   speculation. Never present one category as another.
5. Prefer primary sources, official databases, documented APIs, and established
   analysis libraries. Record access dates when live sources are used.
6. Preserve identifiers, units, genome builds, species, assay types, sample
   definitions, and statistical estimands throughout the workflow.
7. Do not fabricate citations, measurements, methods, database records, or tool
   output. Mark unavailable evidence and unresolved uncertainty explicitly.
8. Complete verification before delivery. Report checks that could not run.

## Route The Task

Read [references/routing.md](references/routing.md) when the request crosses
domains or the correct workflow is unclear.

Classify the work into one or more lanes:

- Evidence: literature discovery, source retrieval, citation verification,
  evidence synthesis, or claim auditing.
- Data: profiling, cleaning, statistics, modeling, omics analysis, or
  reproducible computation.
- Biology: genes, variants, sequences, proteins, structures, pathways,
  ontologies, expression, or regulatory evidence.
- Chemistry and medicine: compounds, targets, assays, pharmacology, safety,
  clinical trials, or clinical interpretation.
- Communication: figures, manuscripts, reviews, revision letters, proposals,
  slides, patents, data statements, or experiment records.

Use multiple lanes only when each produces a necessary input for the next. Keep
one lane in charge of the final artifact.

## Execute The Workflow

### 1. Frame

Write an internal task specification containing:

- research question or claim;
- target entity, population, system, or dataset;
- requested output and audience;
- constraints, acceptance criteria, and uncertainty tolerance;
- required provenance and reproducibility level.

Resolve ambiguous biological identifiers before analysis. Preserve the original
user input alongside normalized identifiers.

### 2. Inspect

For local data, inspect schema, dimensions, missingness, duplicates, ranges,
units, group sizes, distributions, and obvious integrity problems. For source
material, inspect metadata, version, date, and completeness. Do not select a
method or chart before understanding the input.

### 3. Design

Choose methods based on the scientific question and data-generating process.
Define comparisons, controls, covariates, endpoints, statistical assumptions,
multiple-testing handling, and sensitivity analyses where relevant.

When several valid approaches exist, choose a default and briefly state why.
Surface alternatives only when their tradeoffs could change the conclusion.

### 4. Acquire

Retrieve only the evidence and data needed for the question. Prefer stable IDs
and machine-readable endpoints. Capture source name, query or accession, version
or build, retrieval date, and transformation history.

Use credentials only through approved secret-handling mechanisms. Respect source
licenses, access rules, rate limits, privacy requirements, and consent limits.

### 5. Analyze

Use established libraries and domain tools for core scientific algorithms.
Validate inputs before execution and inspect outputs for convergence, coverage,
sample loss, impossible values, and method-specific failure indicators.

Keep raw inputs immutable. Make transformations traceable. Set seeds for
stochastic methods when supported. Prefer scripts or notebooks that can recreate
reported results over undocumented manual operations.

### 6. Interpret

Tie each conclusion to a result or source. Distinguish association from
causation, statistical significance from practical importance, and absence of
evidence from evidence of absence. Discuss limitations that could plausibly
change the conclusion rather than listing generic caveats.

### 7. Communicate

Match the artifact to its audience and venue. For figures, expose distributions,
sample sizes, uncertainty definitions, units, and relevant statistical methods.
For prose, maintain claim-evidence alignment and consistent terminology. For
slides, preserve the reasoning chain rather than copying manuscript paragraphs.

### 8. Verify

Read [references/quality-gates.md](references/quality-gates.md) and apply every
gate relevant to the task. Re-run focused checks after corrections. Do not claim
completion when a required validation remains unresolved.

## Use Optional Adapters

Read [references/adapters.md](references/adapters.md) before invoking installed
skills. Discover available capabilities from the current environment rather than
assuming fixed package names.

Load an adapter's complete `SKILL.md` before using it. Delegate only the bounded
stage it is designed to perform, then apply Cell Skill's provenance and quality
gates to the returned artifact. If no suitable adapter exists, execute the same
stage directly with available tools and established libraries.

## Deliver

Provide the requested artifact first. Then summarize:

- the answer or principal result;
- evidence and methods supporting it;
- material assumptions and limitations;
- files created and checks completed;
- unresolved items that require new data, authority, or user choice.

Keep intermediate implementation details out of the final response unless they
are needed for reproducibility or troubleshooting.
