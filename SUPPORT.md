# Support

**Tier:** 3 (the kit itself is maintained at tier 1)
**Maintainer:** @tamnd

The kit is maintained by the engine team and tracks the engine release. The bindings built with it are maintained by their own authors, at tier 3, and each names its own maintainer in its own repository.

What the kit guarantees: the C ABI will not break under you within a major version, the conformance corpus and its runners stay current with the engine, and a binding that publishes a scorecard is listed on the client overview with its score, its tier, its maintainer, and its last-tested engine version. Promotion to tier 2 is a written criterion in Spec/2064g/dx/01-quality-bar.md, not a favour.

Tier definitions are in Spec/2064g/dx/01-quality-bar.md and are published on the client overview page. A tier is a commitment somebody made, so this file names a person rather than a project.

## Where to file

- The FFI declarations, the runners, the template, or the scorecard tool: here.
- A specific community binding: that binding's own repository.
- Query results, error codes, performance, or anything that reproduces through the `zu` CLI: [tamnd/zu](https://github.com/tamnd/zu/issues).
- Documentation and examples: [tamnd/zu-web](https://github.com/tamnd/zu-web/issues).
