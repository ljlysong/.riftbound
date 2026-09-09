---
title: Unprocessed
---

Staging area for inventory events that haven't been applied to the collection yet. Excluded from the published site (`Unprocessed` is in `quartz.config.yaml`'s `ignorePatterns`) — this folder is a personal workflow tool, not content for visitors.

## The three scenarios

- [[Other/Unprocessed/Sold]] — cards sold for cash. Records live in `content/private/Sold.md` instead (local-only, gitignored) — see that file's note for why.
- [[Traded]] — cards traded away/received.
- [[Pulled]] — cards pulled from opening packs/boxes.

## Workflow

1. Fill in a row whenever one of these happens — no need to touch the big set files (`OGN.md`, `UNL.md`, etc.) yourself.
2. When ready, ask Claude to **"process the Unprocessed folder"**. It will:
   - **Sold**: decrement the sold card's Qty in its set file (and in `Binder.md` if it was a tracked single there).
   - **Traded**: decrement the given card's Qty, increment the received card's Qty, in their respective set files.
   - **Pulled**: increment each pulled card's Qty in its set file, and append a line to the [[Acquisition Log]].
3. Processed rows get cleared back to an empty table (headers only) so the file is ready for the next batch.
