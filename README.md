# SENTRY VLDB Release Packages

This repository stores the current SENTRY VLDB release packages prepared for
review and archival transfer.

## Contents

- `packages/SENTRY_VLDB_compile_package_20260801_234139.zip`:
  latest compile package, including `main.pdf`, LaTeX source, references, and
  paper figures.
- `packages/SENTRY_VLDB_artifact.zip`:
  reproducibility artifact package, including experiment scripts, generated
  results, plotting code, manifests, and the source summary files required by
  `artifact/run_all.sh`.
- `packages/SENTRY_VLDB_artifact.zip.sha256`:
  SHA-256 sidecar for `SENTRY_VLDB_artifact.zip`.
- `packages/sentry-toy_code_package_20260801_222115.zip`:
  DuckDB-backed toy validation code package.

## Verification

The packages were checked before upload:

- the toy code package installs in a clean virtual environment;
- `pytest -q` passes with 5 tests;
- the toy smoke reproduction completes with `overall: PASS`;
- the artifact package SHA-256 sidecar matches the uploaded artifact zip;
- the artifact manifest has no missing or mismatched files;
- the artifact rebuild script completes successfully;
- package text and file names were checked for non-English project-local text.

Additional checksums are recorded in `checksums.sha256`.

## Notes

The repository is intentionally package-oriented. The release archives preserve
their internal structure and should be unpacked before running their respective
README instructions.
