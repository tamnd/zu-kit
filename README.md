# zu binding kit

Everything you need to write a [zu](https://github.com/tamnd/zu) binding for a language that does not have one yet, and to prove that it works.

Nine more languages have real audiences for an embedded graph database and none of them justifies a full-time maintainer. Writing nine bindings badly is worse than writing none, so instead of shipping half-finished bindings the project ships the kit and treats community bindings as first-class consumers of it.

The promise to a tier-3 maintainer is narrow and it is kept: the C ABI will not break under you, the tests that prove your binding correct are provided, your binding is listed in the docs with its score and its tier, and promotion to tier 2 is a written criterion rather than a favour.

## What is in the kit

| Directory | Contents |
|---|---|
| `ffi/` | generated FFI declarations per system: ctypes, cffi, dart:ffi via ffigen, koffi, Ruby fiddle and ffi, Zig `@cImport`, a Swift module map, `Clang.jl`, cpp11, PHP FFI |
| `runners/` | the conformance runner per FFI system; the corpus itself is fetched from the `tamnd/zu` release, never vendored |
| `template/` | a working minimal binding, about 400 lines, written to be copied |
| `REFERENCE.md` | the semantic contract: lifetimes, threading, type mapping, error mapping, the things a binding gets wrong |
| `scorecard.py` | emits the standard scorecard for any binding that runs the corpus |

`libzu` and `zu.h` come from the [tamnd/zu](https://github.com/tamnd/zu) release, prebuilt for every tier-1 platform. The corpus is versioned with the engine and ships as `conformance-<version>.tar.zst`.

## Getting listed

Run the corpus, publish the scorecard, and your binding appears on the clients overview with its score, its tier, its maintainer, and the last engine version it was tested against. A binding that stops passing gets a stale badge automatically, which is both kinder and more honest than a maintainer deciding when to delist someone.

## Status

Pre-1.0 and pre-release. Nothing is published yet. The kit tracks the engine version, so a release here always pairs with the same release of [`tamnd/zu`](https://github.com/tamnd/zu).

## Where things live

| What | Where |
|---|---|
| Engine, Rust SDK, CLI, `zu.h`, conformance corpus | [tamnd/zu](https://github.com/tamnd/zu) |
| Documentation and website | [tamnd/zu-web](https://github.com/tamnd/zu-web) |
| Tier-1 and tier-2 clients | `zu-python`, `zu-node`, `zu-go`, `zu-java`, `zu-c`, `zu-dotnet` |
| This kit | here |

## Specification

Spec/2064g/dx/11-tier-3-languages.md in [tamnd/zu](https://github.com/tamnd/zu). Milestone: DX5 (tamnd/zu#171).

## License

Apache-2.0, same as the engine.
