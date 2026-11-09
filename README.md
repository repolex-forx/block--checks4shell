# Repolex Knowledge Graph of block/checks4shell

RDF knowledge graph data for [block/checks4shell](https://github.com/block/checks4shell), parsed by [repolex](https://repolex.ai).

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
rlex download block/checks4shell
```

Consult `rlex --help` for other options, including SPARQL queries, HTTP server, and interactive visualization.

## Data structure

All data is stored as gzip-compressed [N-Quads](https://www.w3.org/TR/n-quads/) (`.nq.gz`), a standard RDF format that can be loaded into any triplestore or graph database.

```
.
├── aggregate
│   ├── ast
│   │   └── e26559519cb60c2c0e20772990f5c22bba6f6ad0
│   │       └── chunk-001.nq.gz
│   └── repolex
│       └── e26559519cb60c2c0e20772990f5c22bba6f6ad0
│           └── chunk-001.nq.gz
├── blob
│   ├── 0367d2331a2cbfb3dadb43da08affe106a235c28.nq.gz
│   ├── 098e43fed3ac98e6ac05c7ab5e36f13805ce1402.nq.gz
│   ├── 16642d4904de326a047a2bf0cec88c2cae1f6a7f.nq.gz
│   ├── 1bc469e68eb776aa52185c6cbfc5cdcaee837ce3.nq.gz
│   ├── 1d944bf3be593bc9a600693281fd4d756a685456.nq.gz
│   ├── 20412e86b9f4495f10c05ded29d720698d5036fe.nq.gz
│   ├── 2c8368bbca42186780d2aa9d9d77bcbed54c9010.nq.gz
│   ├── 2d9915c5bede9fb8550d74a05ce3c4cd09069bdb.nq.gz
│   ├── 31559b7d115e3c105b328cce9b9dcd9774025061.nq.gz
│   ├── 383f4511d444516caed0fd113ee8a2b640cd2290.nq.gz
│   ├── 46022546bbc0922cfca9e3de6085695dbb0d7f4d.nq.gz
│   ├── 4916d489243c30c3a897bcf3d6db953fd68992b2.nq.gz
│   ├── 4dbe902fc4d0d551e3fff20e9e7505b8cb58a080.nq.gz
│   ├── 53ee7bd5b343d4ea1ecd43936de5f94c1727202f.nq.gz
│   ├── 5b4b5a55abffb957d2f3123c1d15797f3a285f9b.nq.gz
│   ├── 6a5dfb20ad6e39659ea7b70768e9d29d673f4474.nq.gz
│   ├── 6bccf43368fd7c96d9c659562a5142b8b8cb98a1.nq.gz
│   ├── 7275e34eb332140358915fa6798ac5c71aa94e34.nq.gz
│   ├── 840aa29fd64859522f62eac4aeeb114fe956aaab.nq.gz
│   ├── 920e27f0c5ec8503cc83acb14e2cf8a763a9a2b6.nq.gz
│   ├── 982eae2c067bbfe4ef180592913e5d0db80aac2d.nq.gz
│   ├── 9b3b0381570158c5a83f46e338dd1383a1d0af93.nq.gz
│   ├── 9fbbfebb5722757a1b93a15e15baf8ed206e114a.nq.gz
│   ├── a72bd85a919acc8c117d19cddb4bd243f827cc5f.nq.gz
│   ├── a79a163ebb830aef2486482d2a5c72b8dd48e9c5.nq.gz
│   ├── a8a949ebfb24451d55019cd7862bb796da46c663.nq.gz
│   ├── b1cf7372bc3d503602139603fc8e29fd4c6a381b.nq.gz
│   ├── cc17d794d8718ff258b63659cd8931a1cb004e08.nq.gz
│   ├── e889550ba4cbc92a720527042e5f6e7a303bfcbc.nq.gz
│   ├── ee9f74d613e7d2f47144d37be1410297a979bc26.nq.gz
│   ├── f61f87eedd6510c56cd18a94ad4ab77f1aefa114.nq.gz
│   └── fe28214d3352b0ed40820a4999317694c8b1ef57.nq.gz
├── branch
│   └── branch.nq.gz
├── commit
│   └── commit.nq.gz
├── filetree
│   └── e26559519cb60c2c0e20772990f5c22bba6f6ad0.nq.gz
└── tag
    └── tag.nq.gz

11 directories, 38 files
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

[block/checks4shell](https://github.com/block/checks4shell)

---
*Parsed on 2026-11-09 by [repolex](https://repolex.ai)*
