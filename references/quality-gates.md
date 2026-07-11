# Scientific Quality Gates

Apply relevant gates before delivery.

## Identity And Provenance

- Confirm species, identifier namespace, isoform, genome build, strand, units,
  sample definition, and source version.
- Preserve source links, accessions, queries, retrieval dates, and transformation
  history.
- Verify that cited sources support the exact nearby claim.

## Data Integrity

- Check shape, types, missingness, duplicates, impossible values, outliers, group
  sizes, exclusions, and unit consistency.
- Confirm joins do not silently duplicate or discard records.
- Keep raw inputs unchanged and make derived data reproducible.

## Statistical Validity

- Match analysis to design, dependence structure, outcome type, and estimand.
- Check assumptions or use robust alternatives.
- Report effect sizes and uncertainty, not only p-values.
- Address multiplicity, confounding, batch effects, censoring, and class
  imbalance when relevant.
- Avoid causal language without a defensible causal design.

## Computational Validity

- Record software and database versions when they affect results.
- Set random seeds where supported.
- Check warnings, convergence, coverage, sample attrition, and edge cases.
- Re-run a minimal reproduction of headline results.

## Visual Validity

- Use an encoding appropriate to the variable types and scientific question.
- Show individual observations for small groups when possible.
- Define error bars, intervals, sample sizes, tests, corrections, and units.
- Avoid misleading axes, unnecessary dual axes, perceptually uneven color maps,
  and decorative effects that alter interpretation.
- Inspect the rendered artifact for clipping, overlap, missing glyphs, legibility,
  grayscale distinction, and panel consistency.

## Writing And Evidence

- Separate results from interpretation and hypothesis.
- Check terminology, numbers, identifiers, and cross-references for consistency.
- Prefer primary sources for factual scientific claims.
- Label preprints, indirect evidence, model predictions, and database assertions.
- State limitations that could change the conclusion.

## Safety And Ethics

- Protect personal, clinical, genomic, and unpublished data.
- Do not infer clinical actionability beyond the available evidence.
- Respect consent, licenses, access restrictions, and source terms.
- Flag dual-use or hazardous experimental details for appropriate handling.

## Delivery Gate

The result is ready only when the requested artifact exists, key claims are
traceable, required checks pass, and any unrun checks are disclosed.
