# Repolex Knowledge Graph of samuelcolvin/MacTab

RDF knowledge graph data for [samuelcolvin/MacTab](https://github.com/samuelcolvin/MacTab), parsed by [repolex](https://repolex.ai).

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
rlex download samuelcolvin/MacTab
```

Consult `rlex --help` for other options, including SPARQL queries, HTTP server, and interactive visualization.

## Data structure

All data is stored as gzip-compressed [N-Quads](https://www.w3.org/TR/n-quads/) (`.nq.gz`), a standard RDF format that can be loaded into any triplestore or graph database.

```
.
├── aggregate
│   ├── ast
│   │   └── e03917f2228bb14e4feaf48a32a7b6a180d49544
│   │       └── chunk-001.nq.gz
│   └── repolex
│       └── e03917f2228bb14e4feaf48a32a7b6a180d49544
│           └── chunk-001.nq.gz
├── blob
│   ├── 033f9fb6bb794a0f53825f8c4686ea2ac6082b29.nq.gz
│   ├── 0379f2487fb426201efa78e9950f5bbfab2920ab.nq.gz
│   ├── 0702bbcfc0e8475ce09c6136224771530a2f8b6c.nq.gz
│   ├── 0c844c8c8bc1bb63f4dc45c9520738097f5ad606.nq.gz
│   ├── 19a33d0bf77d8855c48a2f02517370a039846d72.nq.gz
│   ├── 279ce9cba705d19a8de620bad458e6dcf4dfbbb7.nq.gz
│   ├── 310f900092fd8491bf06f6f214dde3f93159b00d.nq.gz
│   ├── 5e9aadbd22df623fd7f02b439bc8775004b2645c.nq.gz
│   ├── 8da6348abf32be6364a569f1b45af9b602bdcc33.nq.gz
│   ├── 97412be1784ab46bda4c07fd81469ec2a5e02049.nq.gz
│   ├── a2172735135f848a6b43ae6e0a146fd80e751056.nq.gz
│   ├── a45f34040e40ae657bea697654391ea4396ed9b5.nq.gz
│   ├── a59935ba9cf28f4db6001b81e1e95c0905e1a616.nq.gz
│   ├── ae83958f2ff0fdd8e4088284e6804c94a1f6c82a.nq.gz
│   ├── b78f64f66d5a2ce4d2b304d26093796cdb4c25c2.nq.gz
│   ├── d8965f262757e4b6e6f07b3e0527eba9bac2adb8.nq.gz
│   ├── de9730c5e9747be215921cae70ef7d5c7b0cc147.nq.gz
│   ├── f36fa0a602d97cdc5cc021b4d636801cafc7aa2b.nq.gz
│   └── f6ee5f5e207e8f5221f8f6b3e478ba92a1201c50.nq.gz
├── branch
│   └── branch.nq.gz
├── commit
│   └── commit.nq.gz
├── filetree
│   └── e03917f2228bb14e4feaf48a32a7b6a180d49544.nq.gz
└── tag
    └── tag.nq.gz

11 directories, 25 files
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

[samuelcolvin/MacTab](https://github.com/samuelcolvin/MacTab)

---
*Parsed on 2026-10-11 by [repolex](https://repolex.ai)*
