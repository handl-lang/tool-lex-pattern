# Explanation

## Why this crate exists

Hand-written lexers put grammar knowledge in Rust, so every language variant
needs a fork. Reading the rules from data keeps one engine for all languages and
makes grammar reviewable as data.

## Where it sits

This crate belongs to the `tool-*` family. Plugins, kits and hosts reach it
through the kit's operation slot, so the engine can be swapped without touching a
language definition.

See the [reference](/tool-lex-pattern/reference/) for the API and the
[how-to guides](/tool-lex-pattern/how-to/) for tasks.
