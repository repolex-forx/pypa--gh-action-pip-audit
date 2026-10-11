# Repolex Knowledge Graph of pypa/gh-action-pip-audit

RDF knowledge graph data for [pypa/gh-action-pip-audit](https://github.com/pypa/gh-action-pip-audit), parsed by [repolex](https://repolex.ai).

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
rlex download pypa/gh-action-pip-audit
```

Consult `rlex --help` for other options, including SPARQL queries, HTTP server, and interactive visualization.

## Data structure

All data is stored as gzip-compressed [N-Quads](https://www.w3.org/TR/n-quads/) (`.nq.gz`), a standard RDF format that can be loaded into any triplestore or graph database.

```
.
├── aggregate
│   ├── ast
│   │   └── fb241f581674a1bb995061d62504857a9ea4b69e
│   │       └── chunk-001.nq.gz
│   └── repolex
│       └── fb241f581674a1bb995061d62504857a9ea4b69e
│           └── chunk-001.nq.gz
├── blob
│   ├── 12ce5e7375f8ea5e4334bc154542520cc3f5f24b.nq.gz
│   ├── 22b2cb204efb3500a304f45de117ace5dc3423ca.nq.gz
│   ├── 3c4bc7b3253fb9e43a9afa73ebe32ffc8a1d3cdc.nq.gz
│   ├── 461396ba1d34b0f96ea3538de6afda27033b7289.nq.gz
│   ├── 4ca9cedb3156d59b90697aba49f0323ff86c46ac.nq.gz
│   ├── 546e8fe026b6f5789591fd204c56be530ea64395.nq.gz
│   ├── 567f80efe05eb32650f804bf3c0343111bc37789.nq.gz
│   ├── 594d2e4d564f6234bc09880f9e328f2b4d9a1844.nq.gz
│   ├── 6c05a614d2f4784a9ff578692eae7e5c706a12d6.nq.gz
│   ├── 77fd0ac52c253ae7723da9859da54a5ab16eaf88.nq.gz
│   ├── a0c2200f6787515e6de1d7bef3db1332f52d907a.nq.gz
│   ├── a46d96ecfb918c6a6f0556b78cb0f57050f593ca.nq.gz
│   ├── bdaab25d58d7ca2d84eec304db26abf8fea059a8.nq.gz
│   ├── c83f9139af7215ecb9d72e97291e74e59bd95427.nq.gz
│   ├── cdde0cc29508df0d7d28882167cdca0e962d5d9f.nq.gz
│   ├── d50ac0acb61ecb5c1e07320ffb61028025a554a0.nq.gz
│   ├── e4d8a82395c6e7e46634250ce1cfbb1ac2c1e807.nq.gz
│   ├── e69de29bb2d1d6434b8b29ae775ad8c2e48c5391.nq.gz
│   ├── f086aa46b82189ebfb4f39d207a4316aa34ee758.nq.gz
│   ├── f433b1a53f5b830a205fd2df78e2b34974656c7b.nq.gz
│   ├── f6064e3435f4d20918057b887db711ee1bfb0df8.nq.gz
│   ├── f931fc5ed32215e78b6819416d6001c75d3c527a.nq.gz
│   └── ff27519a166c04752a75347522fe9570354e7d37.nq.gz
├── branch
│   └── branch.nq.gz
├── commit
│   └── commit.nq.gz
├── filetree
│   └── fb241f581674a1bb995061d62504857a9ea4b69e.nq.gz
├── issue
│   └── issue.nq.gz
├── pr
│   └── pr.nq.gz
└── tag
    └── tag.nq.gz

13 directories, 31 files
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

[pypa/gh-action-pip-audit](https://github.com/pypa/gh-action-pip-audit)

---
*Parsed on 2026-10-11 by [repolex](https://repolex.ai)*
