# Repolex Knowledge Graph of piccolo-orm/asgi_server_performance

RDF knowledge graph data for [piccolo-orm/asgi_server_performance](https://github.com/piccolo-orm/asgi_server_performance), parsed by [repolex](https://repolex.ai).

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
rlex download piccolo-orm/asgi_server_performance
```

Consult `rlex --help` for other options, including SPARQL queries, HTTP server, and interactive visualization.

## Data structure

All data is stored as gzip-compressed [N-Quads](https://www.w3.org/TR/n-quads/) (`.nq.gz`), a standard RDF format that can be loaded into any triplestore or graph database.

```
.
├── aggregate
│   ├── ast
│   │   └── 05b0f9707ce7c3acbe39fb3a45c0b2c24b364100
│   │       └── chunk-001.nq.gz
│   └── repolex
│       └── 05b0f9707ce7c3acbe39fb3a45c0b2c24b364100
│           └── chunk-001.nq.gz
├── blob
│   ├── 0221707cd44b4882afc1b8e28ff39e4b42cc5cdc.nq.gz
│   ├── 063a8a6c04c3841e956af1f60aa8e79087815e61.nq.gz
│   ├── 3dd8a9f9435e3ec7d42a4e457c9cd7346bfedd5c.nq.gz
│   ├── 4a61cb2b3113cffce307c4cc19df84650106e98d.nq.gz
│   ├── 62e02d5ad23675d75b9dce0cd3aab52245df9b66.nq.gz
│   ├── 8fe2f94cc26274e7d66fad834d0aa26548fa6772.nq.gz
│   ├── 94a76dd85a98fd5d93ed2120bc6c633aad205fa3.nq.gz
│   ├── b13f7b335b1d6526927798d0067b753c55eca7cf.nq.gz
│   ├── b268446b5208b39cfd86079578ce6b341e1e67bc.nq.gz
│   ├── e49b154999ef4beaf3bb5ea2fb3a87df59176f2f.nq.gz
│   ├── ea11954be5501799009f149fb26b8292ab965ec6.nq.gz
│   ├── efa2d343f3e911ea472d497022e361dad819efed.nq.gz
│   ├── efcec5e7165631b243058b561481f86eae259c50.nq.gz
│   └── f185bba7733ce0cedef1a50490b26377aaed22b1.nq.gz
├── branch
│   └── branch.nq.gz
├── commit
│   └── commit.nq.gz
├── filetree
│   └── 05b0f9707ce7c3acbe39fb3a45c0b2c24b364100.nq.gz
├── pr
│   └── pr.nq.gz
└── tag
    └── tag.nq.gz

12 directories, 21 files
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

[piccolo-orm/asgi_server_performance](https://github.com/piccolo-orm/asgi_server_performance)

---
*Parsed on 2026-10-20 by [repolex](https://repolex.ai)*
