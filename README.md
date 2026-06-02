# MyDalamudPlugins

This repository is set up as a master/custom Dalamud plugin repository.

The source for each plugin lives in its own folder:

- `FFYIV`
- `VoiceDirectorV2`

The master repository file is [pluginmaster.json](pluginmaster.json). It aggregates the plugin store entries that Dalamud expects and points each plugin at its own GitHub release artifact.

## Release model

Build and release each plugin from its own repository folder and keep its GitHub releases versioned independently.

After a plugin release changes version metadata, update the matching entry in `pluginmaster.json` so the custom repository advertises the new version and release ZIP.

## Using in Dalamud

After this repository is pushed somewhere public, add the raw `pluginmaster.json` URL to Dalamud's Custom Plugin Repositories list.

Example shape:

`https://raw.githubusercontent.com/<owner>/<repo>/<branch>/pluginmaster.json`

## Recommended future improvement

Keeping copied plugin folders here works, but if you want cleaner long-term maintenance, Git submodules are the better fit. They preserve each plugin's own history and release workflow while still giving you one master repository that serves a combined `pluginmaster.json`.
