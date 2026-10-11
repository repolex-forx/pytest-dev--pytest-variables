# Repolex Knowledge Graph of pytest-dev/pytest-variables

RDF knowledge graph data for [pytest-dev/pytest-variables](https://github.com/pytest-dev/pytest-variables), parsed by [repolex](https://repolex.ai).

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
rlex download pytest-dev/pytest-variables
```

Consult `rlex --help` for other options, including SPARQL queries, HTTP server, and interactive visualization.

## Data structure

All data is stored as gzip-compressed [N-Quads](https://www.w3.org/TR/n-quads/) (`.nq.gz`), a standard RDF format that can be loaded into any triplestore or graph database.

```
.
├── aggregate
│   ├── ast
│   │   └── 0a5b11e474a006e068e7c386b70ce5c36aa5c4ed
│   │       └── chunk-001.nq.gz
│   └── repolex
│       └── 0a5b11e474a006e068e7c386b70ce5c36aa5c4ed
│           └── chunk-001.nq.gz
├── blob
│   ├── 18e7e7822604d8fa15c46c9ec245a941817ac997.nq.gz
│   ├── 21ec1d4b7451acdcd94a9ae0ffd9faab63ec3a85.nq.gz
│   ├── 31c9122e4a189e0e391a03ee2ae5b826f3c5c72b.nq.gz
│   ├── 3941c2ccae4c89688193a40895b9a669d6da1422.nq.gz
│   ├── 41dc2327f1698b99dd397a84f47b9596d0a516b5.nq.gz
│   ├── 438272e0e20a3dbbe9edec7939969dc23189969e.nq.gz
│   ├── 6194d21a0df430da02b22690571c117c125545b5.nq.gz
│   ├── 897bc91819b44a027ad54f3f05d508a41bc38288.nq.gz
│   ├── 912ee4a6964f9d3e8bf1198fb5078dbb8aa85335.nq.gz
│   ├── b615121f8916931de9f87dfc9f37e10338c66f3c.nq.gz
│   ├── c36595fa82228e9cb5a3b8d350c8c25fd1ad7277.nq.gz
│   ├── cdedfa89b16d36dfd6f66809b9a07ae8ec9e817f.nq.gz
│   ├── e69de29bb2d1d6434b8b29ae775ad8c2e48c5391.nq.gz
│   └── efc99b7f0bb514321a18e2147c17b8ad4498aa61.nq.gz
├── branch
│   └── branch.nq.gz
├── commit
│   └── commit.nq.gz
├── filetree
│   └── 0a5b11e474a006e068e7c386b70ce5c36aa5c4ed.nq.gz
├── issue
│   └── issue.nq.gz
├── pr
│   └── pr.nq.gz
└── tag
    └── tag.nq.gz

13 directories, 22 files
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

[pytest-dev/pytest-variables](https://github.com/pytest-dev/pytest-variables)

---
*Parsed on 2026-10-11 by [repolex](https://repolex.ai)*
