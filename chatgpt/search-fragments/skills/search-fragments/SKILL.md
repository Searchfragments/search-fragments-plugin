---
name: search-fragments
description: Use when the user half-remembers something they cannot name (a film, show, song, book, research paper, quote, person, place or event), or asks whether something they vaguely recall can be found. Gets a verdict from Search Fragments before answering, so nothing is guessed.
---

# Search Fragments

Search Fragments tells you whether a half-remembered thing can be reached before you answer. Use it instead of guessing.

## When to use it

- The user describes something by its plot, scene, clue or context and cannot name it.
- The user is looking for a research paper or study they only partly remember.
- You are not confident of the answer to such a question. Do not use it for well-known facts you can answer directly.

## How to call it

1. Pass the user's own words to `resolve_fragment`. It runs the quick gate first and only does the full search when needed. (You may call `gate_probe` first yourself; `resolve_fragment` then reuses its pages.)
2. If the quick answer is not what the user meant, call `resolve_fragment` again with `skip_gate: true` to force the full search.

## What to do with each verdict

- ORIGIN_OF_TRUTH (Found, or a quick answer): give the answer and cite the source and quote it came with. If a citation or DOI is included, show it as given.
- PARTIAL_ORIGIN (Leads): show the leads as things to check. Never present a lead as the answer.
- NOT_REACHABLE: say Search Fragments could not place it, and ask for one more detail (a year, a name, a scene). It is not a claim that the thing does not exist.

Never fill a gap with your own guess when the verdict is Leads or Not reachable.

If the user tells you which result was right, send it back with `submit_resolution_feedback` and the `resolution_id`.
