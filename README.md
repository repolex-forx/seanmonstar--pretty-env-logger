# Repolex Knowledge Graph of seanmonstar/pretty-env-logger

RDF knowledge graph data for [seanmonstar/pretty-env-logger](https://github.com/seanmonstar/pretty-env-logger), parsed by [repolex](https://repolex.ai).

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
rlex download seanmonstar/pretty-env-logger
```

Consult `rlex --help` for other options, including SPARQL queries, HTTP server, and interactive visualization.

## Data structure

All data is stored as gzip-compressed [N-Quads](https://www.w3.org/TR/n-quads/) (`.nq.gz`), a standard RDF format that can be loaded into any triplestore or graph database.

```
.
├── aggregate
│   ├── ast
│   │   └── 0e238400e18649415dc710c025e99c009a1bb744
│   │       └── chunk-001.nq.gz
│   ├── lsp
│   │   └── 0e238400e18649415dc710c025e99c009a1bb744.nq.gz
│   └── repolex
│       └── 0e238400e18649415dc710c025e99c009a1bb744
│           └── chunk-001.nq.gz
├── blob
│   ├── 05e610cb0be428c2b59accdd01d098a32a48a475.nq.gz
│   ├── 11070b56e586f8486814aefea281e3bdad605902.nq.gz
│   ├── 13b5b360fb517284e9722da2f0a110b69ad2039b.nq.gz
│   ├── 162f75e785a3cf2a88d8a492374111418b89c70b.nq.gz
│   ├── 16fe87b06e802f094b3fbb0894b137bca2b16ef1.nq.gz
│   ├── 1e6475984645b2833382ab977f937271a7d44b98.nq.gz
│   ├── 2bca22631dfe4e498e2102351506d0b8ea79fa8d.nq.gz
│   ├── 5636075d3b248dccab37eed6a7aa00ffe0d5d95a.nq.gz
│   ├── 5745ebdec9fb2465e427117d1ad37470109a39f8.nq.gz
│   ├── 6b0a21a3ed9b3903de50333452da813cac4eefde.nq.gz
│   ├── 860d4d10d78aac6dd6d9cc6333075f91664e8b79.nq.gz
│   ├── 9345c792e139d9104e5758758514c8313146be7f.nq.gz
│   ├── a9d37c560c6ab8d4afbf47eda643e8c42e857716.nq.gz
│   ├── d822cd56f8b53a3b74590fbf19563ec10e6c6f9f.nq.gz
│   ├── f85e24833b7bdeea7b7010796958164f5159a4f2.nq.gz
│   └── fdc2d3905a6dd86c7e51aff25fd4bc27b09f9985.nq.gz
├── branch
│   └── branch.nq.gz
├── commit
│   └── commit.nq.gz
├── dep
│   └── 0e238400e18649415dc710c025e99c009a1bb744.nq.gz
├── filetree
│   └── 0e238400e18649415dc710c025e99c009a1bb744.nq.gz
├── issue
│   └── issue.nq.gz
├── pr
│   └── pr.nq.gz
└── tag
    └── tag.nq.gz

15 directories, 26 files
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

[seanmonstar/pretty-env-logger](https://github.com/seanmonstar/pretty-env-logger)

---
*Parsed on 2026-11-22 by [repolex](https://repolex.ai)*
