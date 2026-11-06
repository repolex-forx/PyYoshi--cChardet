# Repolex Knowledge Graph of PyYoshi/cChardet

RDF knowledge graph data for [PyYoshi/cChardet](https://github.com/PyYoshi/cChardet), parsed by [repolex](https://repolex.ai).

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
rlex download PyYoshi/cChardet
```

Consult `rlex --help` for other options, including SPARQL queries, HTTP server, and interactive visualization.

## Data structure

All data is stored as gzip-compressed [N-Quads](https://www.w3.org/TR/n-quads/) (`.nq.gz`), a standard RDF format that can be loaded into any triplestore or graph database.

```
.
├── aggregate
│   ├── ast
│   │   └── be7279b765e1cf76002040dc36908b32a6f51c1e
│   │       └── chunk-001.nq.gz
│   └── repolex
│       └── be7279b765e1cf76002040dc36908b32a6f51c1e
│           └── chunk-001.nq.gz
├── blob
│   ├── 223c5f666932a3127ede7391f87ae4258a66f779.nq.gz
│   ├── 29e7b32b7094cc1280a759f8241a1c61eccff8d5.nq.gz
│   ├── 3b26fae8bb153fc19a6a8e14c8014853ac4cb3db.nq.gz
│   ├── 414a2e10c59d774d4a15f39596c1881eeeb5864c.nq.gz
│   ├── 45f4fb27f30a63cc50772df6439e9d8b938e6714.nq.gz
│   ├── 47d974bfea412bc2461ba40a12651223aa4c8ac2.nq.gz
│   ├── 4b19d45849a4a5bd6c1ebd2624692a327f90515b.nq.gz
│   ├── 5b548c9f1c7ebe0ed40d800928dd0e03f1fbfd4f.nq.gz
│   ├── 79c33616e4253eb9cb80142d65b6d83f6997596d.nq.gz
│   ├── 7c35697a1702e0597aee73a89e85c469782267b1.nq.gz
│   ├── 852bd5a94fecfdc63546aa47bcbcd54eedc42857.nq.gz
│   ├── 86461c039f35122277e1d8e59b09f37827cb6109.nq.gz
│   ├── 884abab10b4c4fe15498603e4cf807f906327952.nq.gz
│   ├── 88ede49fe5f6b905d13bcc0a1ac37df901623437.nq.gz
│   ├── 890b7a1efbc084d04acd52d9b3340a0c6d2d232d.nq.gz
│   ├── 8b137891791fe96927ad78e64b0aad7bded08bdc.nq.gz
│   ├── 92fb3f855762e1a895dc9240a2fc821cb14364d3.nq.gz
│   ├── 93a848f9688291c7b2172cf99f133675225ad282.nq.gz
│   ├── 9fc44214565d8559c8779771e958922a4d18da36.nq.gz
│   ├── a2233509180b1fe3b9f2a18c2488eb729d2f2bed.nq.gz
│   ├── a3e0fd8dfdea088466f872bfd95d77daf08f930d.nq.gz
│   ├── aaaaadd6e9bf5cc7c87a8711f2a8c476420a1449.nq.gz
│   ├── b03fdc65e0e86d220f57b923e4eaf729084bf1b9.nq.gz
│   ├── b6334208fb377ad7c433f1fe6e47fdf39f5873aa.nq.gz
│   ├── b65691a8c1ce7cd19c41e6880243c08b01144eda.nq.gz
│   ├── bb2c9e2f5f389066b5cea002ff64adc02682e393.nq.gz
│   ├── c5fa5af140310d74b8603c643ecd1ee94d618281.nq.gz
│   ├── cb90056498dbc45f368e2d03c871ba09b0225609.nq.gz
│   ├── ce4b73e443ae21a3fb32fa5062e74ac90633e847.nq.gz
│   ├── cf54b698c713a491ad652bad5ba8b462eaf8ab2a.nq.gz
│   ├── d09b2b122d49b9cd05b7cdc35908a94a628aefe7.nq.gz
│   ├── d5370eead4afa26bd996bb86739763d7be1e3559.nq.gz
│   ├── dbf115bbd8b06ef136017a92d2e0e8f860cb049f.nq.gz
│   ├── debd070be4d955473d4b588c7947b1021078cf20.nq.gz
│   ├── e4c3bba9170e602967e320aab645b53edbbf425b.nq.gz
│   ├── e69de29bb2d1d6434b8b29ae775ad8c2e48c5391.nq.gz
│   ├── e9a778912f5a726a50e97090bdfa5f08a3f61fbf.nq.gz
│   ├── ef8803c1cba928149aa3bd6987316f70963bb309.nq.gz
│   ├── f07d9642d1b2df996dbb9911ddd31ae8b7de4bdf.nq.gz
│   ├── f7ed4141807f6a4940504fb7db738b9348019861.nq.gz
│   └── fc3984fe38fe74e0fcd581df42c19f9964a98296.nq.gz
├── branch
│   └── branch.nq.gz
├── commit
│   └── commit.nq.gz
├── filetree
│   └── be7279b765e1cf76002040dc36908b32a6f51c1e.nq.gz
├── issue
│   └── issue.nq.gz
├── pr
│   └── pr.nq.gz
└── tag
    └── tag.nq.gz

13 directories, 49 files
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

[PyYoshi/cChardet](https://github.com/PyYoshi/cChardet)

---
*Parsed on 2026-11-06 by [repolex](https://repolex.ai)*
