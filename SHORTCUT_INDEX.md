# Image Shortcuts - Recipe Index

This file is a retrieval index, not a recipe source. The complete recipes remain in `SHORTCUTS.md`.

## Purpose

Use this file to locate the exact section in `SHORTCUTS.md` before executing a shortcut. Never use this index as a substitute for the recipe itself.

## Shortcuts

| Shortcut | Exact section in `SHORTCUTS.md` |
|---|---|
| `/linkedin` | `## /linkedin` |
| `/lovestory` | `## /lovestory` |
| `/myclothes` | `## /myclothes` |
| `/underwearcampaign` | `## /underwearcampaign` |
| `/paparazzi` | `## /paparazzi` |
| `/cinematic` | `## /cinematic` |
| `/action` | `## /action` |
| `/anime` | `## /anime` |
| `/instagram` | `## /instagram` |
| `/carousel` | `## /carousel` |
| `/avatar` | `## /avatar` |
| `/travel` | `## /travel` |
| `/product` | `## /product` |
| `/car` | `## /car` |
| `/food` | `## /food` |
| `/website` | `## /website` |

## Retrieval protocol

1. Resolve the user's explicit shortcut, or infer the best matching shortcut from the user's request.
2. Find the exact shortcut in this index.
3. Retrieve the corresponding complete section from `SHORTCUTS.md`, from that `## /shortcut` heading through the content immediately before the next `## /...` heading.
4. Verify that the complete section was retrieved. A truncated excerpt, partial file response, or search snippet is not sufficient.
5. Apply the entire retrieved recipe to the user's request and source image.
6. User-specific instructions override generic recipe decisions where they conflict.
7. If the recipe cannot be retrieved completely, retrieve it again. Do not silently replace it with a generic prompt.

## Important

`SHORTCUTS.md` is the only source of truth for shortcut recipes. This index exists only to make exact retrieval reliable and scalable as the library grows.
