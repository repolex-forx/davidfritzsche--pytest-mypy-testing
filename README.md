# Repolex Knowledge Graph of davidfritzsche/pytest-mypy-testing

RDF knowledge graph data for [davidfritzsche/pytest-mypy-testing](https://github.com/davidfritzsche/pytest-mypy-testing), parsed by [repolex](https://repolex.ai).

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
rlex download davidfritzsche/pytest-mypy-testing
```

Consult `rlex --help` for other options, including SPARQL queries, HTTP server, and interactive visualization.

## Data structure

All data is stored as gzip-compressed [N-Quads](https://www.w3.org/TR/n-quads/) (`.nq.gz`), a standard RDF format that can be loaded into any triplestore or graph database.

```
.
├── aggregate
│   ├── ast
│   │   └── 0e300ba48cd04fc7f3c215590c5af4033d308be4
│   │       └── chunk-001.nq.gz
│   └── repolex
│       └── 0e300ba48cd04fc7f3c215590c5af4033d308be4
│           └── chunk-001.nq.gz
├── blob
│   ├── 0e588e67699bc77aa671fdf3e306aa809362bb22.nq.gz
│   ├── 0f938dc19f050712fb404acf2cb105bddd10e1b5.nq.gz
│   ├── 204b93da48d02900098ced21c54062ffbff36b9c.nq.gz
│   ├── 280911e719da4c1d05d9bb4361c7269dd1c91ca9.nq.gz
│   ├── 33af129b4219662e6d0c916d59c053f53457574a.nq.gz
│   ├── 353cfde0f0d8b8e15d24a9434e69c8afff488042.nq.gz
│   ├── 4108338f2c670fbb9f23b3e6ce0ac663865dd678.nq.gz
│   ├── 45c98a617bee6cc7b44afa626a1825d963c056c4.nq.gz
│   ├── 4ed90b952240cb872426e64da9e41252cc61ae3e.nq.gz
│   ├── 52ea28d0777926d987712bf07333a4c39d67a2bf.nq.gz
│   ├── 57a0b8af660063310016d847d04fd97f90eca739.nq.gz
│   ├── 6c991f4e58e2962bfa1df88c15f387e063f12418.nq.gz
│   ├── 717561cdae1de8281f81d39a9f4f3e3fd1583c79.nq.gz
│   ├── 7508d691984e7e548e24d4c98d154e16ac09c939.nq.gz
│   ├── 750f943acfd4793acff09f8d5616b42b5f7aa5b8.nq.gz
│   ├── 789dad9518416b859dc54684f8fa95e47827b8fe.nq.gz
│   ├── 8807af1df344be16b2f4c39508aa6bdb0bb0f38f.nq.gz
│   ├── 932b0d466de3764d51060223c31e2dd8c0ad8b42.nq.gz
│   ├── a343ccd4335f66ace3f9a83dfff02212a84ef4f2.nq.gz
│   ├── a83120215e6111ae8841a84e11ee7457fd6fa013.nq.gz
│   ├── c4d7c3dd62143c2b44579d913a1be44b6efe8330.nq.gz
│   ├── d1e59ea3de712e4e1565b21cbc6e926bd972ebfd.nq.gz
│   ├── d5c0e71a0cc2eb7c4a38d44260e1d64447dff509.nq.gz
│   ├── d96714889c9bf62e98c3160a428c3c5ff5d8c2d8.nq.gz
│   ├── dbe71b3811b7329448543860e690a3c06874e515.nq.gz
│   ├── ddf9235c6b3128aea242019921d37e27d4816a69.nq.gz
│   ├── e643261f5ec8c8e8767fb139d9f8112185c3dad4.nq.gz
│   ├── e9cf278311b588b1acf5b4e571016f4655334ac0.nq.gz
│   ├── f3ca40c767b5ffc9683d9a72d12157d1edbe6dc2.nq.gz
│   ├── f95dccd315d33e5ce42c39bb083e272d7a12d02d.nq.gz
│   ├── f97e18ead68cf31b887b9eb3043614342e3e4252.nq.gz
│   └── ff2ecd58d5c1d73f58cb7a362b57b8865d78c7cb.nq.gz
├── branch
│   └── branch.nq.gz
├── commit
│   └── commit.nq.gz
├── filetree
│   └── 0e300ba48cd04fc7f3c215590c5af4033d308be4.nq.gz
├── issue
│   └── issue.nq.gz
├── pr
│   └── pr.nq.gz
└── tag
    └── tag.nq.gz

13 directories, 40 files
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

[davidfritzsche/pytest-mypy-testing](https://github.com/davidfritzsche/pytest-mypy-testing)

---
*Parsed on 2026-11-06 by [repolex](https://repolex.ai)*
