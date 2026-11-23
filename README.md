# tool-lex-pattern

`hnl-tool-lex-pattern` — a data-driven lexer engine that reads
`LexerRuleDef` fragments from a `Language` and tokenizes source text.

A `tool-*` crate: the lex operation implemented generically — rules come
from language data, never from hardcoded token tables.

## Development

```bash
cargo run --manifest-path xtask/Cargo.toml -- gate   # fmt → clippy → test → doc
```

The repo's `xtask/` crate provides the gate tasks (`fmt`, `clippy`, `test`, `doc`,
`check`, `gate`); `ci.sh` is the gate entry. Deps resolve from git, so no
sibling checkouts are needed; a plain clone test-runs as-is.

## License

MIT.

## Documentation

<https://handl-lang.github.io/docs/tool-lex-pattern/>
