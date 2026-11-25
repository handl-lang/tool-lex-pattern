# Agent guide — tool-lex-pattern

`hnl-tool-lex-pattern` — a data-driven lexer engine that reads
`LexerRuleDef` fragments from a `Language` and tokenizes source text.
Rules come from language data, never from hardcoded token tables.
`publish = false` (git-install only). Rust 2024.

## Layout

| path | role |
| --- | --- |
| `src/lib.rs` | the engine — `LexerRuleDef`-driven tokenizer implementing `hnl-tool-lex` traits |
| `tests/integration.rs` | integration tests |
| `docs/` | engine doc |
| `xtask/`, `workflows/gate.yaml`, `bupha.toml`, `.cargo/` | vendored repo gate + CI wiring |

## Contract

- Deps resolve from git — `handl-language` → `handl-lang/kernel`,
  `hnl-tool-lex` → `handl-lang/tool-lex`, `handl-kit-data-prelude` →
  `handl-lang/host`, all `branch = "main"`.
- All tokenization behavior is data (`LexerRuleDef` in the `Language`);
  adding a token kind is a YAML change, not an engine edit.

## Verification

```bash
cargo xtask gate   # fmt --check → clippy -D warnings → test → doc
```


<!-- myco:agent-awareness -->

## Agent awareness

- Session start / any work discussion: run `myco status --prompt`
  before proposing next steps — know the board first.
- User describes new work → offer to capture it (`myco todo add`,
  `issue new`, `proposal new`). Don't wait to be asked.
- Picking up a task: `myco resume <ID>` is the briefing.
- Wrapping up: `myco handoff <ID>` anything resumable; keep statuses
  honest (claimed → in-progress → blocked/done).

<!-- /myco:agent-awareness -->
