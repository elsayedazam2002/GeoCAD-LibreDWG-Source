# GeoCAD LibreDWG Source

Public source-delivery repository for the patched LibreDWG WebAssembly component used in GeoCAD Bridge. **This repository is not the source code of the GeoCAD Bridge application.**

## Publication status

**Review candidate — NOT YET A VERIFIED CORRESPONDING-SOURCE RELEASE.** The precise uploaded source archive must still be independently rebuilt and checked against the distributed WASM. Do not claim GPL compliance is complete based solely on this repository being public.

## What belongs here

- LibreDWG upstream source and its applicable copyright/license notices
- GeoCAD-specific patches to LibreDWG
- Build instructions, toolchain pinning, and any necessary build/supporting files
- SHA-256 digests for the precise source distribution and deployed WASM

Do **not** upload GeoCAD Bridge application source, UI, secrets or unrelated internal files.

## Candidate and verification

A source archive was prepared separately for review. It has not yet been published as a verified release asset in this repository. The targeted distributed WASM SHA-256 is:

`21fc06724879645e642adaa7fbc1af6904db34b317e3f6c509b2ccf322cfb244`

An earlier GitHub Actions run reproduced that WASM from **its own** extracted source archive, not yet conclusively from the later user-provided candidate. Until exact-archive reproducibility, legal completeness, and publicly accessible source delivery are confirmed, this is a staging documentation repository.

## License and scope

Upstream LibreDWG license and third-party notices must be carried through unmodified as applicable. Making LibreDWG's source available does **not** alone determine whether additional GeoCAD Bridge application code is subject to GPL obligations; that depends on how the components form and are distributed as a combined work. Obtain a qualified legal review.

## Main application

This repository is intentionally separate from the GeoCAD Bridge application repository. No application source is included here.
