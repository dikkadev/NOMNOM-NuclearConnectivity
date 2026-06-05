# NuclearConnectivity

Client-side Nuclear Option mod for external integrations, currently Steam Timeline combat markers.

## Install

The easiest way to install and update this mod is with **NOMM**, the Nuclear Option Mod Manager:

- NOMM: https://github.com/Combat787/NOMM
- Latest NOMM download: https://github.com/Combat787/NOMM/releases/latest

You can also install manually from this repository's Releases page. Download the latest `NuclearConnectivity-v*.zip` archive and extract it into your Nuclear Option `BepInEx/plugins/` folder. The archive already contains the plugin folder layout.

## About this repository

This GitHub repository is a release mirror for NOMNOM/NOMM automatic updates. The canonical source code and development history live in the Forgejo monorepo:

- Source: https://forge.dikka.dev/lab/nuclear_option_mods

## Metadata

- NOMNOM id: `dev.dikka.nuclearconnectivity`
- Author: dikkadev
- Tags: QoL, Integration
- Release asset format: one `.zip` per release

## Details

`NuclearConnectivity` is a client-side `Nuclear Option` mod for connectivity and external integration features.

The first implemented slice is Steam Timeline marker support for a few high-value combat events.

## Planned Scope

- external integration hooks for multiple services and tools
- a home for future connectivity-related features guided incrementally
- Discord rich presence is planned later

## Current Features

- optional Steam Timeline integration
- marker on local player aircraft loss
- marker on credited air-to-air kills
- optional marker on credited air-to-ground kills

## Requirements

- `Nuclear Option`
- `BepInEx 5`

## Installation

1. Install BepInEx for `Nuclear Option`.
2. Build or download a release archive.
3. Extract the `NuclearConnectivity` folder into `BepInEx/plugins/`.

The final layout should look like this:

```text
BepInEx/
  plugins/
    NuclearConnectivity/
      NuclearConnectivity.dll
```

## Configuration

Current config file:

- `BepInEx/config/dev.dikka.nuclearconnectivity.cfg`

Current switches:

- `Enable Steam Timeline`
- `Mark Player Death`
- `Mark Air-to-Air Kills`
- `Mark Air-to-Ground Kills`

Implementation notes:

- credited kill markers are sourced from `KillDisplay.DisplayKill`
- local aircraft loss markers are sourced from `Unit.UnitDisabled`

