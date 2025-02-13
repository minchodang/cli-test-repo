cli-practice
=================

A new CLI generated with oclif


[![oclif](https://img.shields.io/badge/cli-oclif-brightgreen.svg)](https://oclif.io)
[![Version](https://img.shields.io/npm/v/cli-practice.svg)](https://npmjs.org/package/cli-practice)
[![Downloads/week](https://img.shields.io/npm/dw/cli-practice.svg)](https://npmjs.org/package/cli-practice)


<!-- toc -->
* [Usage](#usage)
* [Commands](#commands)
<!-- tocstop -->
# Usage
<!-- usage -->
```sh-session
$ npm install -g cli-practice
$ cli-practice COMMAND
running command...
$ cli-practice (--version)
cli-practice/0.0.0 darwin-arm64 node-v20.10.0
$ cli-practice --help [COMMAND]
USAGE
  $ cli-practice COMMAND
...
```
<!-- usagestop -->
# Commands
<!-- commands -->
* [`cli-practice hello PERSON`](#cli-practice-hello-person)
* [`cli-practice hello world`](#cli-practice-hello-world)
* [`cli-practice help [COMMAND]`](#cli-practice-help-command)
* [`cli-practice plugins`](#cli-practice-plugins)
* [`cli-practice plugins add PLUGIN`](#cli-practice-plugins-add-plugin)
* [`cli-practice plugins:inspect PLUGIN...`](#cli-practice-pluginsinspect-plugin)
* [`cli-practice plugins install PLUGIN`](#cli-practice-plugins-install-plugin)
* [`cli-practice plugins link PATH`](#cli-practice-plugins-link-path)
* [`cli-practice plugins remove [PLUGIN]`](#cli-practice-plugins-remove-plugin)
* [`cli-practice plugins reset`](#cli-practice-plugins-reset)
* [`cli-practice plugins uninstall [PLUGIN]`](#cli-practice-plugins-uninstall-plugin)
* [`cli-practice plugins unlink [PLUGIN]`](#cli-practice-plugins-unlink-plugin)
* [`cli-practice plugins update`](#cli-practice-plugins-update)

## `cli-practice hello PERSON`

Say hello

```
USAGE
  $ cli-practice hello PERSON -f <value>

ARGUMENTS
  PERSON  Person to say hello to

FLAGS
  -f, --from=<value>  (required) Who is saying hello

DESCRIPTION
  Say hello

EXAMPLES
  $ cli-practice hello friend --from oclif
  hello friend from oclif! (./src/commands/hello/index.ts)
```

_See code: [src/commands/hello/index.ts](https://github.com/open-source/cli-practice/blob/v0.0.0/src/commands/hello/index.ts)_

## `cli-practice hello world`

Say hello world

```
USAGE
  $ cli-practice hello world

DESCRIPTION
  Say hello world

EXAMPLES
  $ cli-practice hello world
  hello world! (./src/commands/hello/world.ts)
```

_See code: [src/commands/hello/world.ts](https://github.com/open-source/cli-practice/blob/v0.0.0/src/commands/hello/world.ts)_

## `cli-practice help [COMMAND]`

Display help for cli-practice.

```
USAGE
  $ cli-practice help [COMMAND...] [-n]

ARGUMENTS
  COMMAND...  Command to show help for.

FLAGS
  -n, --nested-commands  Include all nested commands in the output.

DESCRIPTION
  Display help for cli-practice.
```

_See code: [@oclif/plugin-help](https://github.com/oclif/plugin-help/blob/v6.2.25/src/commands/help.ts)_

## `cli-practice plugins`

List installed plugins.

```
USAGE
  $ cli-practice plugins [--json] [--core]

FLAGS
  --core  Show core plugins.

GLOBAL FLAGS
  --json  Format output as json.

DESCRIPTION
  List installed plugins.

EXAMPLES
  $ cli-practice plugins
```

_See code: [@oclif/plugin-plugins](https://github.com/oclif/plugin-plugins/blob/v5.4.31/src/commands/plugins/index.ts)_

## `cli-practice plugins add PLUGIN`

Installs a plugin into cli-practice.

```
USAGE
  $ cli-practice plugins add PLUGIN... [--json] [-f] [-h] [-s | -v]

ARGUMENTS
  PLUGIN...  Plugin to install.

FLAGS
  -f, --force    Force npm to fetch remote resources even if a local copy exists on disk.
  -h, --help     Show CLI help.
  -s, --silent   Silences npm output.
  -v, --verbose  Show verbose npm output.

GLOBAL FLAGS
  --json  Format output as json.

DESCRIPTION
  Installs a plugin into cli-practice.

  Uses npm to install plugins.

  Installation of a user-installed plugin will override a core plugin.

  Use the CLI_PRACTICE_NPM_LOG_LEVEL environment variable to set the npm loglevel.
  Use the CLI_PRACTICE_NPM_REGISTRY environment variable to set the npm registry.

ALIASES
  $ cli-practice plugins add

EXAMPLES
  Install a plugin from npm registry.

    $ cli-practice plugins add myplugin

  Install a plugin from a github url.

    $ cli-practice plugins add https://github.com/someuser/someplugin

  Install a plugin from a github slug.

    $ cli-practice plugins add someuser/someplugin
```

## `cli-practice plugins:inspect PLUGIN...`

Displays installation properties of a plugin.

```
USAGE
  $ cli-practice plugins inspect PLUGIN...

ARGUMENTS
  PLUGIN...  [default: .] Plugin to inspect.

FLAGS
  -h, --help     Show CLI help.
  -v, --verbose

GLOBAL FLAGS
  --json  Format output as json.

DESCRIPTION
  Displays installation properties of a plugin.

EXAMPLES
  $ cli-practice plugins inspect myplugin
```

_See code: [@oclif/plugin-plugins](https://github.com/oclif/plugin-plugins/blob/v5.4.31/src/commands/plugins/inspect.ts)_

## `cli-practice plugins install PLUGIN`

Installs a plugin into cli-practice.

```
USAGE
  $ cli-practice plugins install PLUGIN... [--json] [-f] [-h] [-s | -v]

ARGUMENTS
  PLUGIN...  Plugin to install.

FLAGS
  -f, --force    Force npm to fetch remote resources even if a local copy exists on disk.
  -h, --help     Show CLI help.
  -s, --silent   Silences npm output.
  -v, --verbose  Show verbose npm output.

GLOBAL FLAGS
  --json  Format output as json.

DESCRIPTION
  Installs a plugin into cli-practice.

  Uses npm to install plugins.

  Installation of a user-installed plugin will override a core plugin.

  Use the CLI_PRACTICE_NPM_LOG_LEVEL environment variable to set the npm loglevel.
  Use the CLI_PRACTICE_NPM_REGISTRY environment variable to set the npm registry.

ALIASES
  $ cli-practice plugins add

EXAMPLES
  Install a plugin from npm registry.

    $ cli-practice plugins install myplugin

  Install a plugin from a github url.

    $ cli-practice plugins install https://github.com/someuser/someplugin

  Install a plugin from a github slug.

    $ cli-practice plugins install someuser/someplugin
```

_See code: [@oclif/plugin-plugins](https://github.com/oclif/plugin-plugins/blob/v5.4.31/src/commands/plugins/install.ts)_

## `cli-practice plugins link PATH`

Links a plugin into the CLI for development.

```
USAGE
  $ cli-practice plugins link PATH [-h] [--install] [-v]

ARGUMENTS
  PATH  [default: .] path to plugin

FLAGS
  -h, --help          Show CLI help.
  -v, --verbose
      --[no-]install  Install dependencies after linking the plugin.

DESCRIPTION
  Links a plugin into the CLI for development.

  Installation of a linked plugin will override a user-installed or core plugin.

  e.g. If you have a user-installed or core plugin that has a 'hello' command, installing a linked plugin with a 'hello'
  command will override the user-installed or core plugin implementation. This is useful for development work.


EXAMPLES
  $ cli-practice plugins link myplugin
```

_See code: [@oclif/plugin-plugins](https://github.com/oclif/plugin-plugins/blob/v5.4.31/src/commands/plugins/link.ts)_

## `cli-practice plugins remove [PLUGIN]`

Removes a plugin from the CLI.

```
USAGE
  $ cli-practice plugins remove [PLUGIN...] [-h] [-v]

ARGUMENTS
  PLUGIN...  plugin to uninstall

FLAGS
  -h, --help     Show CLI help.
  -v, --verbose

DESCRIPTION
  Removes a plugin from the CLI.

ALIASES
  $ cli-practice plugins unlink
  $ cli-practice plugins remove

EXAMPLES
  $ cli-practice plugins remove myplugin
```

## `cli-practice plugins reset`

Remove all user-installed and linked plugins.

```
USAGE
  $ cli-practice plugins reset [--hard] [--reinstall]

FLAGS
  --hard       Delete node_modules and package manager related files in addition to uninstalling plugins.
  --reinstall  Reinstall all plugins after uninstalling.
```

_See code: [@oclif/plugin-plugins](https://github.com/oclif/plugin-plugins/blob/v5.4.31/src/commands/plugins/reset.ts)_

## `cli-practice plugins uninstall [PLUGIN]`

Removes a plugin from the CLI.

```
USAGE
  $ cli-practice plugins uninstall [PLUGIN...] [-h] [-v]

ARGUMENTS
  PLUGIN...  plugin to uninstall

FLAGS
  -h, --help     Show CLI help.
  -v, --verbose

DESCRIPTION
  Removes a plugin from the CLI.

ALIASES
  $ cli-practice plugins unlink
  $ cli-practice plugins remove

EXAMPLES
  $ cli-practice plugins uninstall myplugin
```

_See code: [@oclif/plugin-plugins](https://github.com/oclif/plugin-plugins/blob/v5.4.31/src/commands/plugins/uninstall.ts)_

## `cli-practice plugins unlink [PLUGIN]`

Removes a plugin from the CLI.

```
USAGE
  $ cli-practice plugins unlink [PLUGIN...] [-h] [-v]

ARGUMENTS
  PLUGIN...  plugin to uninstall

FLAGS
  -h, --help     Show CLI help.
  -v, --verbose

DESCRIPTION
  Removes a plugin from the CLI.

ALIASES
  $ cli-practice plugins unlink
  $ cli-practice plugins remove

EXAMPLES
  $ cli-practice plugins unlink myplugin
```

## `cli-practice plugins update`

Update installed plugins.

```
USAGE
  $ cli-practice plugins update [-h] [-v]

FLAGS
  -h, --help     Show CLI help.
  -v, --verbose

DESCRIPTION
  Update installed plugins.
```

_See code: [@oclif/plugin-plugins](https://github.com/oclif/plugin-plugins/blob/v5.4.31/src/commands/plugins/update.ts)_
<!-- commandsstop -->
