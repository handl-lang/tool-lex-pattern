# engine-lex-pattern

`hnl-engine-lex-pattern` — a data-driven lexer engine that reads
`LexerRuleDef` fragments from a `Language` and tokenizes source text.

An `engine-*` crate: the lex operation implemented generically — rules come
from language data, never from hardcoded token tables.

## Development

```bash
cargo xtask gate        # fmt --check → clippy -D warnings → test → doc
```

`cargo xtask` wraps the repo's `xtask/` crate (`fmt`, `clippy`, `test`, `doc`,
`check`, `gate`); `ci.sh` is the gate entry. Deps resolve from git, so no
sibling checkouts are needed; a plain clone test-runs as-is.

## License

MIT.

## Documentation

<https://handl-lang.github.io/docs/engine-lex-pattern/>
