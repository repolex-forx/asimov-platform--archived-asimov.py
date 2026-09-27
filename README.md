# Repolex Knowledge Graph of asimov-platform/archived-asimov.py

RDF knowledge graph data for [asimov-platform/archived-asimov.py](https://github.com/asimov-platform/archived-asimov.py), parsed by [repolex](https://repolex.ai).

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
rlex download asimov-platform/archived-asimov.py
```

Consult `rlex --help` for other options, including SPARQL queries, HTTP server, and interactive visualization.

## Data structure

All data is stored as gzip-compressed [N-Quads](https://www.w3.org/TR/n-quads/) (`.nq.gz`), a standard RDF format that can be loaded into any triplestore or graph database.

```
.
├── aggregate
│   ├── ast
│   │   └── b058535a14de6b810854d1159783aaf677244101
│   │       └── chunk-001.nq.gz
│   ├── lsp
│   │   └── b058535a14de6b810854d1159783aaf677244101.nq.gz
│   └── repolex
│       └── b058535a14de6b810854d1159783aaf677244101
│           └── chunk-001.nq.gz
├── blob
│   ├── 05f5ceba7ca44502bbcd4cc2884e435881af7793.nq.gz
│   ├── 13edb27f8341a15f7ef6805243c5be8572913129.nq.gz
│   ├── 34a763932bd213a5c9e6b939611e7a97dbef75d7.nq.gz
│   ├── 41edf27105a7f60ef7211bc55a2628bc2e26bcf4.nq.gz
│   ├── 4679b9d5d5a7adba696dc17822a836ebe4f35f5c.nq.gz
│   ├── 52f8d94647b9b2baa73cb937d82797be4d05bb58.nq.gz
│   ├── 6324d401a069f4020efcf0ff07442724b52f47c2.nq.gz
│   ├── a38ace0fbaab348ee98b54bc1037156bbc00cf2f.nq.gz
│   ├── afb2df71e00aa626901f8ac7f05bf579bd09464e.nq.gz
│   ├── c2a0ef8eedb7c785d3d5265fe5757698e0b381e6.nq.gz
│   ├── e3e57a8ce4ccbf74759a6df8fa4a3980ff1c9209.nq.gz
│   ├── e67ce52c43e0f5b22f922f0fa6419202657fd698.nq.gz
│   ├── e69de29bb2d1d6434b8b29ae775ad8c2e48c5391.nq.gz
│   ├── e9df000eddd61c7033a60d16a8428969795e8c3b.nq.gz
│   ├── ec27f902e6600754b84be014144e97a01fa608f2.nq.gz
│   ├── ee4d9362508d63f9e156fe9ee1b11ebc1a3e86d6.nq.gz
│   ├── ef22050c52c61b7ce03ecdcb6c54d605ae07b278.nq.gz
│   ├── efb98088164f5786b17e83ed384971fc3c74f93c.nq.gz
│   └── ff26d8884f3e5606f3a5aad41b0afee7be21e877.nq.gz
├── branch
│   └── branch.nq.gz
├── commit
│   └── commit.nq.gz
├── dep
│   └── b058535a14de6b810854d1159783aaf677244101.nq.gz
├── filetree
│   └── b058535a14de6b810854d1159783aaf677244101.nq.gz
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

[asimov-platform/archived-asimov.py](https://github.com/asimov-platform/archived-asimov.py)

---
*Parsed on 2026-09-27 by [repolex](https://repolex.ai)*
