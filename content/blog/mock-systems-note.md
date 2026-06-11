+++
title = "Mock Post: Notes on a Tiny Systems Tool"
date = 2026-06-01
description = "A placeholder post with enough structure to exercise the refreshed blog list and article layout."

[taxonomies]
tags = ["mock", "systems", "rust"]
+++

This is a mock post for testing the refreshed blog design. It is intentionally
written like a short engineering note so the typography has realistic paragraph
lengths, links, metadata, and rhythm.

## The Shape of the Tool

The imaginary tool watches a directory, fingerprints files, and prints a compact
summary when something changes. The implementation does not matter here; the
point is to see how ordinary technical prose sits in the article template.

- Keep the watcher loop boring.
- Make the output stable enough to diff.
- Fail loudly when configuration is ambiguous.

> A good command-line tool should make the common path obvious and the failure
> path unmistakable.

## A Small Sketch

```rust
fn summarize(paths: &[PathBuf]) -> usize {
    paths
        .iter()
        .filter(|path| path.extension().is_some())
        .count()
}
```

That gives the code block, list spacing, quote treatment, and section headings
something to render against.
