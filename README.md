# Repolex Knowledge Graph of jupyterhub/nbgitpuller-downloader-plugins

RDF knowledge graph data for [jupyterhub/nbgitpuller-downloader-plugins](https://github.com/jupyterhub/nbgitpuller-downloader-plugins), parsed by [repolex](https://repolex.ai).

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
rlex download jupyterhub/nbgitpuller-downloader-plugins
```

Consult `rlex --help` for other options, including SPARQL queries, HTTP server, and interactive visualization.

## Data structure

All data is stored as gzip-compressed [N-Quads](https://www.w3.org/TR/n-quads/) (`.nq.gz`), a standard RDF format that can be loaded into any triplestore or graph database.

```
.
├── aggregate
│   ├── ast
│   │   └── 646857507fb21a6f2a7222bdd7610d7184492e69
│   │       └── chunk-001.nq.gz
│   └── repolex
│       └── 646857507fb21a6f2a7222bdd7610d7184492e69
│           └── chunk-001.nq.gz
├── blob
│   ├── 07de284aa5c45f56b69ca6f605edf72a14785b99.nq.gz
│   ├── 16c0a2dc7cfe809fc46ada6e217807e9e947fd74.nq.gz
│   ├── 26d33521af10bcc7fd8cea344038eaaeb78d0ef5.nq.gz
│   ├── 28e96eb8868e25b6bdfe1e0cf41d217bc51917f2.nq.gz
│   ├── 35eb1ddfbbc029bcab630581847471d7f238ec53.nq.gz
│   ├── 57b6edd85910542d9dd652c19eb7aa13555d43e6.nq.gz
│   ├── 797acea53eb091cf5b30518802c3073f544adeed.nq.gz
│   ├── 7b94b0afbc388eec12eb6e6e3b258f470dc0f3a0.nq.gz
│   ├── 85038ffb9a98a95270c95ef454a5ecac8e3233b8.nq.gz
│   ├── 8e435da93deb7bff843097ef72c7532c09311cf5.nq.gz
│   ├── acdac2128db953cbed26f7cb09a59ae72225ea37.nq.gz
│   ├── afcccda6f6ddbad63658017ed0029f00ad1bf644.nq.gz
│   ├── b6e47617de110dea7ca47e087ff1347cc2646eda.nq.gz
│   ├── cb3ba6b477778abda9e0e329461bbcb371995cc3.nq.gz
│   ├── cff5a070b3b33531640254ebfc52ba790c059d6a.nq.gz
│   ├── d2519cf9694ef79be260fab54c91920f8e86f6d4.nq.gz
│   ├── d6ebd4805981b8400db3e3291c74a743fef9a824.nq.gz
│   ├── d7f8cc531039cae3cad6fdf1d85eed18bcf5a17c.nq.gz
│   ├── e69de29bb2d1d6434b8b29ae775ad8c2e48c5391.nq.gz
│   ├── eb3da73e150c2a0c41507521fccd3fbe36c8d7de.nq.gz
│   └── ebf93a188ec102494c9b9ab2dcc67f6bdbd19c8e.nq.gz
├── branch
│   └── branch.nq.gz
├── commit
│   └── commit.nq.gz
├── filetree
│   └── 646857507fb21a6f2a7222bdd7610d7184492e69.nq.gz
├── issue
│   └── issue.nq.gz
├── pr
│   └── pr.nq.gz
└── tag
    └── tag.nq.gz

13 directories, 29 files
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

[jupyterhub/nbgitpuller-downloader-plugins](https://github.com/jupyterhub/nbgitpuller-downloader-plugins)

---
*Parsed on 2026-10-21 by [repolex](https://repolex.ai)*
