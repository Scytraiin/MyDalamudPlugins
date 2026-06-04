# Voice Director

`VoiceDirectorV2` is a Dalamud plugin for players who want different cutscene voice languages in different duties without constantly changing that setting by hand.

You pick the duties you care about, choose the voice language you want there, and the plugin restores your usual default everywhere else.

## In game

Open the main window with:

```text
/vodir
```

Open settings directly with:

```text
/vodir config
```

## What this repo includes

This repository contains the plugin source, tests, release notes, and the metadata needed for custom repository distribution. The technical pieces are still here, but they are mainly for maintenance and release work rather than for everyday use.

## Current status

- Current plugin version: `1.6.3`
- Dalamud API target: `15`
- Custom-repo package output: `out/release/latest.zip`

## Preview

![UI preview](https://raw.githubusercontent.com/Scytraiin/VoiceDirectorV2/master/images/preview1.png)

## For development and releases

If you are working on the plugin itself, the main areas are:

- `VoiceDirector/` for the plugin source
- `VoiceDirector.Tests/` for unit tests
- `release-notes/` for release text
- `scyt.repo.json` for custom repository metadata

Local validation is handled through Docker so the workflow stays reproducible:

```bash
docker build -t voice-director-ci .
docker run --rm voice-director-ci
```

To build a release package, mount a valid Dalamud dev folder:

```bash
docker run --rm \
  -v "/path/to/your/15.0.0.2/dev:/dalamud:ro" \
  -v "$PWD/out:/out" \
  voice-director-ci
```

Release preparation still follows the same general flow: update the version, refresh the notes, validate in game, and publish the generated release artifacts plus updated repo metadata.

This project continues the original Voice Director idea for newer FFXIV and Dalamud versions now that the earlier upstream is no longer actively maintained.
