---
id: Y0cZsmfUdytwajRGeylMZ
title: CLI
desc: ''
updated: 1632061759277
created: 1631473249667
---

Dendron has a [[CLI|dendron.topic.cli]] command to help with development.

```sh
dendron dev <cmd>

commands related to development of Dendron

Positionals:
  cmd  a command to run
      [string] [required] [choices: "generate_json_schema_from_config", "build",
      "bump_version", "publish", "sync_assets", "prep_plugin", "package_plugin",
                                                               "install_plugin"]

Options:
  --version           Show version number                              [boolean]
  --help              Show help                                        [boolean]
  --wsRoot            location of workspace
  --vault             name of vault
  --quiet             don't print output to stdout
  --upgradeType       how to do upgrade
                              [choices: "major", "minor", "patch", "prerelease"]
  --publish endpoint  where to publish              [choices: "local", "remote"]
```

## Common Options

### upgradeType

What next semver version to upgrade to

## Commands

### generate_json_schema_from_config

Update json schema for `dendron.yml`

### build

Build vsix for a given upgradeType [^upgrade]

### bump_version

Bump up version number for upgradeType [^upgrade]

### publish

Publish packages to npm

```
dendron dev publish 
```

### sync_assets

Re-built static HTML used in plugin

### prep_plugin

Format `package.json` of plugin to make it compatible with `vsce package`


### package_plugin

Equivalent to running the following

```sh
vsce package --yarn
```

### install_plugin

Install latest vsix in all local vscode versions

<!-- Citations -->
[^upgrade]: [[upgradeType|dendron.dev.cli#upgradetype]]
