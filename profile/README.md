<p align="center"><img src="https://raw.githubusercontent.com/go-erasure/brand/main/social/go-erasure.png" alt="go-erasure" width="720"></p>

<h1 align="center">go-erasure</h1>
<p align="center">Pure-Go erasure coding — Reed-Solomon over GF(2^16) and the RozoFS Mojette transform, with go-asmgen SIMD.</p>
<p align="center">[![docs](https://img.shields.io/badge/docs-mkdocs--material-0A6E96?style=flat-square&logo=materialformkdocs&logoColor=white)](https://go-erasure.github.io/docs/) ![repos](https://img.shields.io/badge/repos-2-0079A8?style=flat-square) ![Go](https://img.shields.io/badge/Go-1.26.4-00ADD8?style=flat-square&logo=go&logoColor=white) ![license](https://img.shields.io/badge/license-BSD--3--Clause-0A6E96?style=flat-square)</p>

---

## What is this?

`go-erasure` provides two independent, dependency-free erasure-coding libraries in pure Go:

- **Reed-Solomon** over GF(2¹⁶) — an MDS systematic code (Cauchy generator matrix) in the PAR2-compatible field, with a SPLIT(16,4) SIMD region-multiply on all six 64-bit targets.
- **Mojette transform** — the XOR-only discrete-Radon projection code used by [RozoFS](https://rozofs.github.io/rozofs/master/), with a go-asmgen region-XOR kernel on all six 64-bit SIMD targets.

Both are `CGO_ENABLED=0`, hold 100% test coverage, and keep a scalar oracle that a differential fuzzer checks the SIMD kernels against byte-for-byte on every CI run.

## Repositories (2)

| Module | Kind | What it is | API |
|---|---|---|:--:|
| [`reedsolomon`](https://github.com/go-erasure/reedsolomon) | codec | Reed-Solomon MDS erasure code over GF(2¹⁶) — PAR2-compatible field, SPLIT(16,4) SIMD. | [ref](https://pkg.go.dev/github.com/go-erasure/reedsolomon) |
| [`mojette`](https://github.com/go-erasure/mojette) | codec | Mojette transform (discrete Radon, XOR-only) — the RozoFS erasure code, SIMD on all six 64-bit targets. | [ref](https://pkg.go.dev/github.com/go-erasure/mojette) |

> This list reflects the repos that actually exist in the org.

## Links

- 📖 Docs — <https://go-erasure.github.io/docs/>
- 🌐 Site — <https://go-erasure.github.io/>
- 🎨 Brand assets — <https://github.com/go-erasure/brand>

---
<p align="center"><sub>Branding in <a href="https://github.com/go-erasure/brand">go-erasure/brand</a>.</sub></p>
