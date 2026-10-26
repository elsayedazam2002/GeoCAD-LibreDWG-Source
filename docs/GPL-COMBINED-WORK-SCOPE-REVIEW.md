# GeoCAD Bridge / LibreDWG — GPL Combined-Work Scope Review
Date: 2026-10-26
Status: **PRELIMINARY — LEGAL APPROVAL PENDING**
Scope: documentation only; not a legal opinion or permission to release.

## Observed integration (review/libredwg-public-preview-20261026)
- `dist/cad-workspace/index.html` loads `services/dwg-parser.js`.
- `dist/services/dwg-parser.js` dynamically imports `/vendor/libredwg/dist/libredwg-web.js`, calls `LibreDwg.create(wasmDirectory)`, and directly invokes the WASM-backed `dwg_read_data` / `convertEx` interfaces.
- The resulting DXF is processed by `DxfParser` and `GeoCADDxf` in the CAD Workspace pipeline.
- Processing is browser-local. Separate file paths, dynamic import, or separate repositories alone do **not** establish a legally independent program.

## Preliminary license-scope assessment
| Component | Preliminary assessment |
| --- | --- |
| LibreDWG JS/WASM, modifications, corresponding build sources | GPL-3.0 obligations apply to distribution |
| `dist/services/dwg-parser.js` | High combined-work exposure: direct API integration |
| CAD Workspace scripts using this conversion pipeline | Potential combined-work exposure; scope needs dependency-level and legal review |
| Independently usable DXF processing | Review actual coupling and independent licensing before determining scope |
| GIS, BIM, unrelated independent utilities | No automatic inclusion demonstrated by reviewed evidence; assess shared code and bundling |

This assessment does **not** conclude that every CAD Workspace file must be released, or that unrelated site components are covered. It also does **not** certify that only the LibreDWG source is required.

## Public corresponding-source evidence
- Public library-only source prerelease: https://github.com/elsayedazam2002/GeoCAD-LibreDWG-Source/releases/tag/libredwg-0.8.1-source-review
- Archive: https://github.com/elsayedazam2002/GeoCAD-LibreDWG-Source/releases/download/libredwg-0.8.1-source-review/LibreDWG-Source.tar.gz
- Candidate archive SHA-256: `5d5fbd589f45dcf787cdf38cfa68550f97d93cf97b1cb8768365f990d935a25d` (independent download/hash verification of the exact release asset remains pending).
- Deployed patched WASM expected SHA-256: `21fc06724879645e642adaa7fbc1af6904db34b317e3f6c509b2ccf322cfb244`.
- Prior CI rebuild evidence concerns an earlier CI source candidate, not independently the exact published release asset.
- Manifest remains `status: pending`. No legal clearance is implied.

## Closure checklist (without repeating prior functional tests)
1. Map imports, exports, worker calls and shared dependencies from `dwg-parser.js` through the CAD UI, DXF engine and runtime; record which files constitute the possible combined work.
2. Verify complete corresponding source, notices, build/control scripts, and actual public release asset SHA-256.
3. Obtain qualified open-source licensing counsel's written conclusion on the combined-work boundary, distribution duties, and whether any proprietary application sources must be provided.
4. If private-source operation cannot be supported, choose compliant disclosure, a legally independent integration architecture reviewed by counsel, or a permissively licensed/independently developed alternative.
5. Update release approval only after the applicable requirements are satisfied. Preserve the existing runtime and tested behavior until then.

## References
- GNU GPLv3: https://www.gnu.org/licenses/gpl-3.0.en.html
- GNU GPL FAQ (linking, aggregation, and communication between programs): https://www.gnu.org/licenses/gpl-faq.en.html

**No source archive, WASM, application runtime, tests, production branch, or deployed site was changed by this document.**
