# Repolex Knowledge Graph of google-deepmind/Temporal-3D-Pose-Kinetics

RDF knowledge graph data for [google-deepmind/Temporal-3D-Pose-Kinetics](https://github.com/google-deepmind/Temporal-3D-Pose-Kinetics), parsed by [repolex](https://repolex.ai).

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
rlex download google-deepmind/Temporal-3D-Pose-Kinetics
```

Consult `rlex --help` for other options, including SPARQL queries, HTTP server, and interactive visualization.

## Data structure

All data is stored as gzip-compressed [N-Quads](https://www.w3.org/TR/n-quads/) (`.nq.gz`), a standard RDF format that can be loaded into any triplestore or graph database.

```
.
├── aggregate
│   ├── ast
│   │   └── a8369cd9d626fd661ff54eb34e733ea9956b9f86
│   │       └── chunk-001.nq.gz
│   └── repolex
│       └── a8369cd9d626fd661ff54eb34e733ea9956b9f86
│           └── chunk-001.nq.gz
├── blob
│   ├── 261eeb9e9f8b2b4b0d119366dda99c6fd7d35c64.nq.gz
│   ├── 517c4ff9029f96d88a3becb081911dd0684c65fe.nq.gz
│   ├── 648b18edbe27bf94b76387a4ae2c9317ff49cfca.nq.gz
│   ├── 6550a432c3324d73aaad6c74421a3910f272077b.nq.gz
│   └── f0fe9e2d8f59be7c6ddc09f5ed821d80e4aa900a.nq.gz
├── branch
│   └── branch.nq.gz
├── commit
│   └── commit.nq.gz
├── filetree
│   └── a8369cd9d626fd661ff54eb34e733ea9956b9f86.nq.gz
├── issue
│   └── issue.nq.gz
├── pr
│   └── pr.nq.gz
└── tag
    └── tag.nq.gz

13 directories, 13 files
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

[google-deepmind/Temporal-3D-Pose-Kinetics](https://github.com/google-deepmind/Temporal-3D-Pose-Kinetics)

---
*Parsed on 2026-11-06 by [repolex](https://repolex.ai)*
