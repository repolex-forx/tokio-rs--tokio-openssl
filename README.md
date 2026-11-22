# Repolex Knowledge Graph of tokio-rs/tokio-openssl

RDF knowledge graph data for [tokio-rs/tokio-openssl](https://github.com/tokio-rs/tokio-openssl), parsed by [repolex](https://repolex.ai).

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
rlex download tokio-rs/tokio-openssl
```

Consult `rlex --help` for other options, including SPARQL queries, HTTP server, and interactive visualization.

## Data structure

All data is stored as gzip-compressed [N-Quads](https://www.w3.org/TR/n-quads/) (`.nq.gz`), a standard RDF format that can be loaded into any triplestore or graph database.

```
.
├── aggregate
│   ├── ast
│   │   └── 70edf385ad3a2f4efe58fa6077a511da7379c0d0
│   │       └── chunk-001.nq.gz
│   ├── lsp
│   │   └── 70edf385ad3a2f4efe58fa6077a511da7379c0d0.nq.gz
│   └── repolex
│       └── 70edf385ad3a2f4efe58fa6077a511da7379c0d0
│           └── chunk-001.nq.gz
├── blob
│   ├── 03814ae8d961b386b6e808ba81b7b3a9171b169f.nq.gz
│   ├── 1332f8eb5d96f1551077bd11558a8805cbb8f9f1.nq.gz
│   ├── 2a6afc5662644809a8c3371fa37a75d46b2a7d11.nq.gz
│   ├── 2d08323d3fa3425ce6dc6d2f6ae569eddae41fd2.nq.gz
│   ├── 312f4a5d9ff2c650fb953c379069faad8d2c0e25.nq.gz
│   ├── 47ff62f6048de75d6bde3dc511ff978e3a3a79d2.nq.gz
│   ├── 51bdf5f9499f32e09cb7cd3f30f4a7c3f0822695.nq.gz
│   ├── 58f1020aa32af9235b7e142116c10cd404775db2.nq.gz
│   ├── 662540bd90189dd738435c3ad0e9a8685f7891d1.nq.gz
│   ├── 85d6c4d1449beeaae2c7feb0adfdac3cebe197ce.nq.gz
│   ├── 93255d1f5981fbaac5d040592b5371835c89f526.nq.gz
│   ├── 9b18b5810d8378e01ece57093da0ecc57a26da51.nq.gz
│   └── d5a3b639700b48049af7d02342ed471fc6957c17.nq.gz
├── branch
│   └── branch.nq.gz
├── commit
│   └── commit.nq.gz
├── dep
│   └── 70edf385ad3a2f4efe58fa6077a511da7379c0d0.nq.gz
├── filetree
│   └── 70edf385ad3a2f4efe58fa6077a511da7379c0d0.nq.gz
├── issue
│   └── issue.nq.gz
├── pr
│   └── pr.nq.gz
└── tag
    └── tag.nq.gz

15 directories, 23 files
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

[tokio-rs/tokio-openssl](https://github.com/tokio-rs/tokio-openssl)

---
*Parsed on 2026-11-22 by [repolex](https://repolex.ai)*
