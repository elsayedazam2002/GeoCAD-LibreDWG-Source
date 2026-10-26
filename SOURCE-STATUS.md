# LibreDWG public source delivery status

## Public release

- Release: https://github.com/elsayedazam2002/GeoCAD-LibreDWG-Source/releases/tag/libredwg-0.8.1-source-review
- Source archive: https://github.com/elsayedazam2002/GeoCAD-LibreDWG-Source/releases/download/libredwg-0.8.1-source-review/LibreDWG-Source.tar.gz
- GitHub release asset size: 28,107,546 bytes (uploaded; prerelease)
- Local candidate SHA-256: `5d5fbd589f45dcf787cdf38cfa68550f97d93cf97b1cb8768365f990d935a25d`
- Target distributed WASM SHA-256: `21fc06724879645e642adaa7fbc1af6904db34b317e3f6c509b2ccf322cfb244`
- Pinned upstream commit: `53137eeb1fe54e400bfd77a7ad8e21bc373cc998`
- Toolchain: Emscripten `6.0.13`

## Evidence and scope

The source archive is publicly attached to a GitHub prerelease; it is no longer accurate to say it is not hosted. Prior GitHub Actions run https://github.com/elsayedazam2002/GeoCAD-Bridge/actions/runs/40197501101 successfully rebuilt its **own extracted source archive** and matched the target WASM byte-for-byte. This record does not assert a fresh build of the precise published release asset. No repeat of previous tests is required for this documentation update.

The candidate archive contains upstream source, patch, build script, and license notices as previously inspected. This is a review candidate, not a legal opinion or final GPL sign-off.

## GPL review items

1. Confirm the complete corresponding source and build/install scripts for the exact distributed LibreDWG binary, including applicable third-party licenses.
2. Evaluate how the browser application links to and distributes the GPL-covered WebAssembly/JavaScript runtime, including whether other application modules form a combined work and whether further source disclosure is required.
3. Ensure appropriate license/copyright notices and a discoverable source link accompany the distributed runtime.
4. Do not describe this prerelease as certified GPL compliant without qualified legal review.

**Production release remains NO-GO pending legal scope review and release sign-off.** This repository intentionally excludes GeoCAD Bridge application code.
