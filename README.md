# Repolex Knowledge Graph of mattn/go-runewidth

RDF knowledge graph data for [mattn/go-runewidth](https://github.com/mattn/go-runewidth), parsed by [repolex](https://repolex.ai).

> **Note**: This data is experimental and subject to change without notice.

## How to use this data

The easiest way to get started is to install the [rlex](https://github.com/repolex-ai/rlex) query tool:

```bash
cargo install --git https://github.com/repolex-ai/rlex
```

Verify the install:

```bash
rlex --help
```

**rlex is designed to be used primarily by LLMs in a terminal.** Start up your favorite AI assistant and ask it to use rlex. It handles the SPARQL — you just ask questions in plain English.

To load this repo's data:

```bash
rlex download mattn/go-runewidth
```

Consult `rlex --help` for other options, including SPARQL queries, HTTP server, and interactive visualization.

## Data structure

All data is stored as gzip-compressed [N-Quads](https://www.w3.org/TR/n-quads/) (`.nq.gz`), a standard RDF format that can be loaded into any triplestore or graph database.

```
.
├── aggregate
│   ├── ast
│   │   └── 99da42750b5dcb798c068e8f1817cea66a220864
│   │       └── chunk-001.nq.gz
│   └── repolex
│       └── 99da42750b5dcb798c068e8f1817cea66a220864
│           └── chunk-001.nq.gz
├── blob
│   ├── 0acac51a0f254e42e28cf00ef99430856d32f315.nq.gz
│   ├── 2637e3dcb3e983fb0f53987b874aa3993fe1217e.nq.gz
│   ├── 302c3d0c6ebc2444d96d3a5c1db1b179d651348e.nq.gz
│   ├── 3f8d1467a6044103f4033795130f848ebf8c3e51.nq.gz
│   ├── 4976375c9fb882de1c6b71c7136edb1fff72bc04.nq.gz
│   ├── 546543c9b7e6d848818c712ce2ef3c38625625da.nq.gz
│   ├── 5b9ac164683a1115849449d52983c5a593c0a834.nq.gz
│   ├── 75dbfacc4944204ba533cd53e371fc60afda8f6f.nq.gz
│   ├── 81bc90752c7f417e971014cbefbdc4a349d2d232.nq.gz
│   ├── 84b6528dfe914e1e6be7e309cdb1dc7eb6b2cc6f.nq.gz
│   ├── 8890712562f5ec01e90eaf103fdc9eb910cf2628.nq.gz
│   ├── 91b5cef30ebdf08cb6efe669497a96f58c66035d.nq.gz
│   ├── 951500a24d370ec553d8665fbfa0af1fc38cca76.nq.gz
│   ├── 95d9ba548f64e61dbdebcdd03ade396040dc9f23.nq.gz
│   ├── a5aacb019d3500c0d64c6ba7a901fb0c19562884.nq.gz
│   ├── a6898ee7015f413c61d04e329e5c932d123daa34.nq.gz
│   ├── a9efdbde37f7f9850faee95b1bea28af22aadacb.nq.gz
│   ├── b6914dcff6759a235faac1376a04db0d3ba41770.nq.gz
│   ├── c2abbc2db30be0c33b36c274c581c1f28b8a41b8.nq.gz
│   └── ecbaed99ca6b38ed28d5b574fee0f536ab6452ac.nq.gz
├── branch
│   └── branch.nq.gz
├── commit
│   └── commit.nq.gz
├── filetree
│   └── 99da42750b5dcb798c068e8f1817cea66a220864.nq.gz
├── issue
│   └── issue.nq.gz
├── pr
│   └── pr.nq.gz
└── tag
    └── tag.nq.gz

13 directories, 28 files
```

| Directory | What it contains |
|-----------|-----------------|
| `blob/` | Per-file AST graphs, content-addressed by git blob SHA. Each file in the source repo gets its own graph. |
| `aggregate/ast/` | Combined AST graph per parsed commit. Merges all blob graphs for a snapshot of the entire codebase at that point. |
| `aggregate/lsp/` | Language Server Protocol enrichment: resolved symbols, definitions, references, and type information. |
| `aggregate/dataflow/` | Interprocedural data flow edges between functions and modules. |
| `aggregate/repolex/` | Combined graph (AST + LSP + dataflow) per commit. |
| `commit/` | Git commit metadata (author, date, message, parent links). |
| `branch/` | Branch metadata. |
| `tag/` | Tag metadata. |
| `filetree/` | File tree snapshots per commit (which files existed and their blob SHAs). |
| `audit/` | Code architecture and graph audit reports per commit. |

## Source repository

[mattn/go-runewidth](https://github.com/mattn/go-runewidth)

---
*Parsed on 2026-11-10 by [repolex](https://repolex.ai)*
