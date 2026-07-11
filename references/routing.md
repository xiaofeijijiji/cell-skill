# Scientific Routing

Use this guide to construct a minimal, ordered workflow.

## Routing Rules

1. Start from the user's decision or deliverable, not from an available tool.
2. Normalize entities before querying multiple sources.
3. Run independent retrievals in parallel when their outputs do not depend on
   one another.
4. Run dependent stages in sequence and define the handoff schema explicitly.
5. Use the most specific capable workflow for each stage.
6. Avoid invoking multiple tools that provide the same evidence unless
   triangulation or coverage comparison is scientifically useful.

## Common Chains

### Literature To Manuscript

Define claims -> search primary literature -> verify identifiers and dates ->
extract evidence -> assess conflicts and limitations -> draft -> citation audit.

### Raw Data To Figure

Inspect data -> define estimand -> select analysis -> validate assumptions ->
calculate results -> choose visual encoding -> render -> visual and statistical
audit -> export at final dimensions.

### Variant To Mechanism

Normalize variant and genome build -> population frequency -> clinical evidence
-> regulatory and expression evidence -> gene mapping -> protein or pathway
context -> integrated interpretation with evidence tiers.

### Protein To Functional Hypothesis

Normalize accession and isoform -> sequence and annotations -> domains ->
structures -> homologs -> interactions and pathways -> hypothesis -> testable
predictions and limitations.

### Compound To Translational Evidence

Normalize structure and identifiers -> target and assay evidence -> mechanism ->
selectivity -> safety and pharmacology -> clinical trials -> conclusion separated
by preclinical and clinical evidence.

### Paper To Presentation Or Patent

Extract verified claims, methods, figures, and limitations -> identify audience
and purpose -> rebuild narrative -> create artifact -> check factual traceability,
rights, and formatting.

## Escalation Conditions

Request user input when any unresolved choice changes the biological entity,
reference build, cohort, primary endpoint, legal publication rights, clinical
meaning, or irreversible external action. Otherwise proceed with a stated
conservative assumption.
