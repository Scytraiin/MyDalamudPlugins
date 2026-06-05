# MyDalamudPlugins

This repo is a lightweight hub for your personal Dalamud plugins and the custom repository metadata that makes them easy to install.

## What lives here

- [pluginmaster.json](pluginmaster.json) as the file Dalamud reads for the custom repository listing.
- `VoiceDirectorV2` as a symlink to `../VoiceDirectorV2`
- `LootInfoPlugin` as a symlink to `../../FFYIV`

## Working style

Make code changes in the real plugin repositories:

- `../VoiceDirectorV2`
- `../../FFYIV`

This hub stays useful for:

- quickly jumping to the plugin repos from one place
- maintaining [pluginmaster.json](pluginmaster.json)
- publishing or checking the custom repo layout

## Local safety

When this repo was converted into a hub, the old in-repo plugin copies were moved into `.local-backups/` and ignored by git so nothing was lost during the migration.

## Using this repo in Dalamud

Once this repository is published somewhere public, add the raw `pluginmaster.json` URL to Dalamud's Custom Plugin Repositories list.

Example format:

`https://raw.githubusercontent.com/<owner>/<repo>/<branch>/pluginmaster.json`
