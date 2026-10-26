# GPL-3.0 compliance scope review — open decision record

This document is a review checklist, **not a legal approval**. Publishing LibreDWG source is necessary but may not be sufficient for distributing the browser-integrated component.

## Confirmed facts

- The LibreDWG source candidate is published as a public GitHub prerelease asset.
- The source delivery repository is separate from the private GeoCAD Bridge application repository.
- The deployed component is a patched LibreDWG WebAssembly/JavaScript runtime, identified by the SHA-256 in [SOURCE-STATUS.md](SOURCE-STATUS.md).
- Existing CI evidence supports a byte-for-byte rebuild from an extracted source archive; the precise published asset was not the subject of that recorded rebuild.

## Questions for qualified GPL review

1. Identify the license version and copyright notices of every LibreDWG and linked third-party component in the shipped JS/WASM distribution.
2. Determine whether GeoCAD Bridge's interaction with the GPL-covered WASM/JS runtime creates a single combined work or independent works, based on actual module boundaries, calls, and distribution.
3. If a combined work, assess the obligation to license and provide corresponding source for covered application portions; **do not assume that keeping the main repository private avoids GPL obligations**.
4. Confirm that the public source bundle includes all necessary patches, scripts, build inputs and applicable notices to recreate the shipped covered component.
5. Make a conspicuous source/license link available alongside the browser-delivered runtime, and retain attribution.
6. Check the precise version of the source bundle, JS glue, WASM, and runtime distributed on each deployment.

## Release gate

- Source archive publication: **DONE (prerelease)**
- Existing technical rebuild evidence: **RECORDED (limited to prior CI archive)**
- Legal determination for application integration: **OPEN**
- GPL compliance sign-off: **OPEN**
- Production deployment: **NOT AUTHORIZED BY THIS DOCUMENT**

No source code from the GeoCAD Bridge application is included in this repository.
