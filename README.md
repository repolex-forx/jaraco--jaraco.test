# Repolex Knowledge Graph of jaraco/jaraco.test

RDF knowledge graph data for [jaraco/jaraco.test](https://github.com/jaraco/jaraco.test), parsed by [repolex](https://repolex.ai).

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
rlex download jaraco/jaraco.test
```

Consult `rlex --help` for other options, including SPARQL queries, HTTP server, and interactive visualization.

## Data structure

All data is stored as gzip-compressed [N-Quads](https://www.w3.org/TR/n-quads/) (`.nq.gz`), a standard RDF format that can be loaded into any triplestore or graph database.

```
.
├── aggregate
│   ├── ast
│   │   └── 1cb060970a556ec9688d0dec21737c2cc79f19e1
│   │       └── chunk-001.nq.gz
│   └── repolex
│       └── 1cb060970a556ec9688d0dec21737c2cc79f19e1
│           └── chunk-001.nq.gz
├── blob
│   ├── 10d412f406891b9683f832fcbc134c9bdf4f916e.nq.gz
│   ├── 1f2aa7533b0423a8eb943f6f4ec02498e39581a0.nq.gz
│   ├── 2e3f4dd791a6372b427d618eb0baa8c4dc58e5f0.nq.gz
│   ├── 304196f81e11a168c9894f966e4a617ebf4ed53c.nq.gz
│   ├── 3633d8cfa8855ffa45105598b9c9c795a51a9069.nq.gz
│   ├── 3a4bf6ddc412175b20a925cdc5b3ab5be4329c65.nq.gz
│   ├── 4283ca5f9063de083c89662d88ca70e2f5fdea89.nq.gz
│   ├── 4d096da689e0f46a39a059d080b132ee200dfb41.nq.gz
│   ├── 54c9000ec94341dd65c2053251b85b124017b9b5.nq.gz
│   ├── 54cc8303b22089e12053e552d4e6cb852a865b8a.nq.gz
│   ├── 577e87a793a20e413f7321f4f17ec1eba2ea1962.nq.gz
│   ├── 5bdc232005af9be104a00437ae9bc64417a4c1cc.nq.gz
│   ├── 700235be57c1b2872455c0be5333f59cf568e252.nq.gz
│   ├── 724370638fc188317bbc7dc868f1a571995fd796.nq.gz
│   ├── 74de90e422ee68a4a0397f070d30955e073a7d81.nq.gz
│   ├── 8fa70b0d5097de6c914620e9eeb179e7d1395fee.nq.gz
│   ├── 9a0f3bce1395ae3819030b822e5d9076c85068ea.nq.gz
│   ├── adefeb3df9ea54251c775edbaa6436c67b97f8b6.nq.gz
│   ├── b103b3734a52533c6b5bebe5f0d61c6f0c07d651.nq.gz
│   ├── c8f9deb163cb6d43d32e2b42f7f2564fa4c3180f.nq.gz
│   ├── e05a3d4a2ab888e32952006d8cd380864368db5f.nq.gz
│   ├── e69de29bb2d1d6434b8b29ae775ad8c2e48c5391.nq.gz
│   ├── ef7f254b35b9d8669adb83b1ffa46c509cbb2aaa.nq.gz
│   └── f50dcc5ad40e76393fd9f168c23dd51a5c2de29d.nq.gz
├── branch
│   └── branch.nq.gz
├── commit
│   └── commit.nq.gz
├── filetree
│   └── 1cb060970a556ec9688d0dec21737c2cc79f19e1.nq.gz
├── issue
│   └── issue.nq.gz
├── pr
│   └── pr.nq.gz
└── tag
    └── tag.nq.gz

13 directories, 32 files
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

[jaraco/jaraco.test](https://github.com/jaraco/jaraco.test)

---
*Parsed on 2026-10-20 by [repolex](https://repolex.ai)*
