# Behringer WING `mdl` Catalog (Validated)

This repo contains a canonical catalog of Behringer WING Remote Protocol `mdl` identifiers, intended for:
- snap/template generators
- OSC tooling
- reverse-engineering and validation workflows

## Files

- `catalog/wing_mdl_catalog_canonical.validated.json`
  - Main machine-readable catalog.
  - Split into `validated_models` and `unvalidated_models`.
  - Each model is tagged with a validation level and a recommendation tier.

## Validation levels

- `doc`: appears explicitly in Behringer WING Remote Protocol PDFs
- `console`: confirmed by loading/saving a snap or observing console UI behavior
- `inferred`: mentioned elsewhere but not proven — do not rely on it for auto snap generation

## How to validate a new `mdl`
1. Load the effect/model on the console.
2. Save a snap: `VALIDATE_<SECTION>_<MDL>.snap`
3. Add it to the repo (optional, as evidence).
4. Move the model from `unvalidated_models` → `validated_models` and tag it.
