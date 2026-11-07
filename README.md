# Repolex Knowledge Graph of ansible-collections/skydive

RDF knowledge graph data for [ansible-collections/skydive](https://github.com/ansible-collections/skydive), parsed by [repolex](https://repolex.ai).

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
rlex download ansible-collections/skydive
```

Consult `rlex --help` for other options, including SPARQL queries, HTTP server, and interactive visualization.

## Data structure

All data is stored as gzip-compressed [N-Quads](https://www.w3.org/TR/n-quads/) (`.nq.gz`), a standard RDF format that can be loaded into any triplestore or graph database.

```
.
├── aggregate
│   ├── ast
│   │   └── 21d837f14ca27dfce9fc35843a27b0d962b4da4b
│   │       └── chunk-001.nq.gz
│   └── repolex
│       └── 21d837f14ca27dfce9fc35843a27b0d962b4da4b
│           └── chunk-001.nq.gz
├── blob
│   ├── 06a6f5f537d688f1412d0962d549df728493ef8d.nq.gz
│   ├── 08c2e17b7a9902e3ef0e249e07454a95634b31a5.nq.gz
│   ├── 0c3dae1ecc9dec51e00e67e2b31430b34e98d6bc.nq.gz
│   ├── 121eab6867ba35e57dc7b01a170b2708f81b7b62.nq.gz
│   ├── 172bf5786d1a8805816c0936413c8ee1c1bdf6ed.nq.gz
│   ├── 1aceac0a0c249a11922ec9179b57bd8103716966.nq.gz
│   ├── 238108317b865ff2e1804e2f184df130cecbdda4.nq.gz
│   ├── 3b27d814f4d5d0dd1c45f07204167187bfa019c4.nq.gz
│   ├── 6f0d12b3a5ceb46c71a7004f802a0994bac94d4c.nq.gz
│   ├── 7f697ac770fd6c48209dd08988abb2de0b6c64a3.nq.gz
│   ├── 90d40550bcaa4d5864f570d7ec93cddc941a6efd.nq.gz
│   ├── a9772bea1f6568ee5ddb0c318a980c20204d88ce.nq.gz
│   ├── ba9c980fb86bef62c1cd5c86cd09c6cde80b0cd1.nq.gz
│   ├── c4189e3644b1f1bcb42dd6b84a7505391902d17b.nq.gz
│   ├── e69de29bb2d1d6434b8b29ae775ad8c2e48c5391.nq.gz
│   ├── e750b93dd173ac068378c52d2cbccbe6bdfcf6e8.nq.gz
│   ├── ea1472ec1f38b2d1410951194a02f8fb9f1c820a.nq.gz
│   ├── f288702d2fa16d3cdf0035b15a9fcbc552cd88e7.nq.gz
│   └── f95f3ea6aa30fd1a7309f86fe9960620c93718e3.nq.gz
├── branch
│   └── branch.nq.gz
├── commit
│   └── commit.nq.gz
├── filetree
│   └── 21d837f14ca27dfce9fc35843a27b0d962b4da4b.nq.gz
├── issue
│   └── issue.nq.gz
├── pr
│   └── pr.nq.gz
└── tag
    └── tag.nq.gz

13 directories, 27 files
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

[ansible-collections/skydive](https://github.com/ansible-collections/skydive)

---
*Parsed on 2026-11-07 by [repolex](https://repolex.ai)*
