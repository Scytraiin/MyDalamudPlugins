# External API Ideas

This file is intentionally local-only and is not meant to be committed.

## Garland Tools / Duty Loot Tables

- Add a future zone or duty browser that shows expected drops for the current duty.
- Keep this separate from the core loot-history flow so the plugin remains useful offline.

## Universalis / Market Data

- Enrich known items with recent sale price, demand, or trading volume.
- Use this only as optional value-add data for farming sessions.

## Remote Item Metadata Fallback

- Consider a remote fallback only if local item-sheet lookup proves insufficient.
- Keep local game-sheet resolution as the default and preferred path.

## General Rule

- External APIs should remain optional, cached, and clearly separated from the core local tracking flow.
- The plugin should continue to work fully for loot capture, rolls, grouping, history, and overview stats without any network dependency.
