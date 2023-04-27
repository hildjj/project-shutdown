## Crate shutdown process

Rust offers several improvements on library management. In addition to the [General project shutdown](shutdown-steps.md), the following steps are advised.

- [ ] file an "unmaintained" advisory with the [RustSec Advisory DB](https://github.com/RustSec/advisory-db/) (see [Advisory format](https://github.com/RustSec/advisory-db/#advisory-format) for details). This will cause your package to be flagged by `cargo audit`.

- [ ] Publish a version of your now deprecated crate to `crates.io` with the README indicating when the crate will no longer be maintained, as well as any potential mitigation steps that customers may wish to take.
