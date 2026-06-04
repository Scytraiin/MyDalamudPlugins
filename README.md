# MyDalamudPlugins

This repo is the home for a small collection of personal Dalamud plugins and the custom repository metadata that makes them easy to install.

It is meant to be a simple publishing hub rather than a deep technical reference. Each plugin keeps its own folder, release assets, and notes, while this repository ties them together for custom repo use.

## What lives here

- `VoiceDirectorV2` for duty-based cutscene voice switching.
- `LootInfoPlugin` for the loot-history plugin work in this collection.
- [pluginmaster.json](pluginmaster.json) as the file Dalamud reads for the custom repository listing.

## Using this repo in Dalamud

Once this repository is published somewhere public, add the raw `pluginmaster.json` URL to Dalamud's Custom Plugin Repositories list.

Example format:

`https://raw.githubusercontent.com/<owner>/<repo>/<branch>/pluginmaster.json`

## For maintainers

Most day-to-day work happens inside the individual plugin folders. When a plugin version changes, its matching entry in `pluginmaster.json` should be updated so the custom repository points at the correct release artifact.

If this collection grows a lot over time, moving plugin folders to submodules would make long-term maintenance cleaner, but the current layout is intentionally straightforward and easy to work with.
