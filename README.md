# Repolex Knowledge Graph of agronholm/httpx-sse

RDF knowledge graph data for [agronholm/httpx-sse](https://github.com/agronholm/httpx-sse), parsed by [repolex](https://repolex.ai).

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
rlex download agronholm/httpx-sse
```

Consult `rlex --help` for other options, including SPARQL queries, HTTP server, and interactive visualization.

## Data structure

All data is stored as gzip-compressed [N-Quads](https://www.w3.org/TR/n-quads/) (`.nq.gz`), a standard RDF format that can be loaded into any triplestore or graph database.

```
.
├── aggregate
│   ├── ast
│   │   └── 643938c805e671fa20adcf314b447f862b77bcda
│   │       └── chunk-001.nq.gz
│   └── repolex
│       └── 643938c805e671fa20adcf314b447f862b77bcda
│           └── chunk-001.nq.gz
├── blob
│   ├── 08e627f6284d8b9b595365f7e28ab7dd4d2175bc.nq.gz
│   ├── 09e0c43d12f5e7f3e6038b1f43d467a094d70250.nq.gz
│   ├── 0f55825e303be27a5f53477dbc6fde1f747cbbea.nq.gz
│   ├── 1947a53afac51b71e665d5299198bd7dbc770cd8.nq.gz
│   ├── 1f6ad81f9eba8c0bd80908609a2f74b4b1097101.nq.gz
│   ├── 256c4c0bf1164f53effab665c8866fadc9abfd21.nq.gz
│   ├── 2dfcd1e393d922712f4d60501288c828eb78c4c4.nq.gz
│   ├── 30b0e7cbb2e3f61f7061695c9bc4d6087b94ca38.nq.gz
│   ├── 36600eb63374cb1f936f4d90a9aa1ad5b5c1fd9f.nq.gz
│   ├── 405f33e98e0e5cfd13d7acd8a88dd467687779a5.nq.gz
│   ├── 4617e41bcd7f57dc0e82b944da0d217b3c368e0d.nq.gz
│   ├── 49139e012b8905b8b421e488415d4e509f1838bc.nq.gz
│   ├── 5580482f3fefe5620609489b3e1682dddde5cdbc.nq.gz
│   ├── 625638ab85e3289a33a254b2cfd69562011ecaee.nq.gz
│   ├── 63c9c90b477220212c30c6b983ee99d4d0b02ffe.nq.gz
│   ├── 67e0a96cc84b6a0fa809c47343f76398acaeb9b1.nq.gz
│   ├── b60cdad8dcf11ff85a9df6d4b1a44c5c5410345d.nq.gz
│   ├── ba0b39ddcd10fa8812e528e4137dcb7e1b1a6e5d.nq.gz
│   ├── cd2c4d287ce86c4e922d56c66423615085892e14.nq.gz
│   ├── d0674c7cfb26768be6be423c0fd73edd07ae88c8.nq.gz
│   ├── d4dc1190f7b02a8c97ab85e4f896787ca39dd9ec.nq.gz
│   └── e69de29bb2d1d6434b8b29ae775ad8c2e48c5391.nq.gz
├── branch
│   └── branch.nq.gz
├── commit
│   └── commit.nq.gz
├── filetree
│   └── 643938c805e671fa20adcf314b447f862b77bcda.nq.gz
└── tag
    └── tag.nq.gz

11 directories, 28 files
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

[agronholm/httpx-sse](https://github.com/agronholm/httpx-sse)

---
*Parsed on 2026-10-11 by [repolex](https://repolex.ai)*
