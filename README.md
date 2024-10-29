control
=================

An organization tool


[![oclif](https://img.shields.io/badge/cli-oclif-brightgreen.svg)](https://oclif.io)
[![Version](https://img.shields.io/npm/v/control.svg)](https://npmjs.org/package/control)
[![Downloads/week](https://img.shields.io/npm/dw/control.svg)](https://npmjs.org/package/control)


<!-- toc -->
* [Usage](#usage)
* [Commands](#commands)
<!-- tocstop -->
# Usage
<!-- usage -->
```sh-session
$ npm install -g control
$ control COMMAND
running command...
$ control (--version)
control/0.0.0 linux-x64 node-v22.9.0
$ control --help [COMMAND]
USAGE
  $ control COMMAND
...
```
<!-- usagestop -->
# Commands
<!-- commands -->
* [`control hello PERSON`](#control-hello-person)
* [`control hello world`](#control-hello-world)
* [`control help [COMMAND]`](#control-help-command)
* [`control plugins`](#control-plugins)
* [`control plugins add PLUGIN`](#control-plugins-add-plugin)
* [`control plugins:inspect PLUGIN...`](#control-pluginsinspect-plugin)
* [`control plugins install PLUGIN`](#control-plugins-install-plugin)
* [`control plugins link PATH`](#control-plugins-link-path)
* [`control plugins remove [PLUGIN]`](#control-plugins-remove-plugin)
* [`control plugins reset`](#control-plugins-reset)
* [`control plugins uninstall [PLUGIN]`](#control-plugins-uninstall-plugin)
* [`control plugins unlink [PLUGIN]`](#control-plugins-unlink-plugin)
* [`control plugins update`](#control-plugins-update)

## `control hello PERSON`

Say hello

```
USAGE
  $ control hello PERSON -f <value>

ARGUMENTS
  PERSON  Person to say hello to

FLAGS
  -f, --from=<value>  (required) Who is saying hello

DESCRIPTION
  Say hello

EXAMPLES
  $ control hello friend --from oclif
  hello friend from oclif! (./src/commands/hello/index.ts)
```

_See code: [src/commands/hello/index.ts](https://github.com/ericbaukhages/control/blob/v0.0.0/src/commands/hello/index.ts)_

## `control hello world`

Say hello world

```
USAGE
  $ control hello world

DESCRIPTION
  Say hello world

EXAMPLES
  $ control hello world
  hello world! (./src/commands/hello/world.ts)
```

_See code: [src/commands/hello/world.ts](https://github.com/ericbaukhages/control/blob/v0.0.0/src/commands/hello/world.ts)_

## `control help [COMMAND]`

Display help for control.

```
USAGE
  $ control help [COMMAND...] [-n]

ARGUMENTS
  COMMAND...  Command to show help for.

FLAGS
  -n, --nested-commands  Include all nested commands in the output.

DESCRIPTION
  Display help for control.
```

_See code: [@oclif/plugin-help](https://github.com/oclif/plugin-help/blob/v6.2.16/src/commands/help.ts)_

## `control plugins`

List installed plugins.

```
USAGE
  $ control plugins [--json] [--core]

FLAGS
  --core  Show core plugins.

GLOBAL FLAGS
  --json  Format output as json.

DESCRIPTION
  List installed plugins.

EXAMPLES
  $ control plugins
```

_See code: [@oclif/plugin-plugins](https://github.com/oclif/plugin-plugins/blob/v5.4.15/src/commands/plugins/index.ts)_

## `control plugins add PLUGIN`

Installs a plugin into control.

```
USAGE
  $ control plugins add PLUGIN... [--json] [-f] [-h] [-s | -v]

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
  Installs a plugin into control.

  Uses npm to install plugins.

  Installation of a user-installed plugin will override a core plugin.

  Use the CONTROL_NPM_LOG_LEVEL environment variable to set the npm loglevel.
  Use the CONTROL_NPM_REGISTRY environment variable to set the npm registry.

ALIASES
  $ control plugins add

EXAMPLES
  Install a plugin from npm registry.

    $ control plugins add myplugin

  Install a plugin from a github url.

    $ control plugins add https://github.com/someuser/someplugin

  Install a plugin from a github slug.

    $ control plugins add someuser/someplugin
```

## `control plugins:inspect PLUGIN...`

Displays installation properties of a plugin.

```
USAGE
  $ control plugins inspect PLUGIN...

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
  $ control plugins inspect myplugin
```

_See code: [@oclif/plugin-plugins](https://github.com/oclif/plugin-plugins/blob/v5.4.15/src/commands/plugins/inspect.ts)_

## `control plugins install PLUGIN`

Installs a plugin into control.

```
USAGE
  $ control plugins install PLUGIN... [--json] [-f] [-h] [-s | -v]

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
  Installs a plugin into control.

  Uses npm to install plugins.

  Installation of a user-installed plugin will override a core plugin.

  Use the CONTROL_NPM_LOG_LEVEL environment variable to set the npm loglevel.
  Use the CONTROL_NPM_REGISTRY environment variable to set the npm registry.

ALIASES
  $ control plugins add

EXAMPLES
  Install a plugin from npm registry.

    $ control plugins install myplugin

  Install a plugin from a github url.

    $ control plugins install https://github.com/someuser/someplugin

  Install a plugin from a github slug.

    $ control plugins install someuser/someplugin
```

_See code: [@oclif/plugin-plugins](https://github.com/oclif/plugin-plugins/blob/v5.4.15/src/commands/plugins/install.ts)_

## `control plugins link PATH`

Links a plugin into the CLI for development.

```
USAGE
  $ control plugins link PATH [-h] [--install] [-v]

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
  $ control plugins link myplugin
```

_See code: [@oclif/plugin-plugins](https://github.com/oclif/plugin-plugins/blob/v5.4.15/src/commands/plugins/link.ts)_

## `control plugins remove [PLUGIN]`

Removes a plugin from the CLI.

```
USAGE
  $ control plugins remove [PLUGIN...] [-h] [-v]

ARGUMENTS
  PLUGIN...  plugin to uninstall

FLAGS
  -h, --help     Show CLI help.
  -v, --verbose

DESCRIPTION
  Removes a plugin from the CLI.

ALIASES
  $ control plugins unlink
  $ control plugins remove

EXAMPLES
  $ control plugins remove myplugin
```

## `control plugins reset`

Remove all user-installed and linked plugins.

```
USAGE
  $ control plugins reset [--hard] [--reinstall]

FLAGS
  --hard       Delete node_modules and package manager related files in addition to uninstalling plugins.
  --reinstall  Reinstall all plugins after uninstalling.
```

_See code: [@oclif/plugin-plugins](https://github.com/oclif/plugin-plugins/blob/v5.4.15/src/commands/plugins/reset.ts)_

## `control plugins uninstall [PLUGIN]`

Removes a plugin from the CLI.

```
USAGE
  $ control plugins uninstall [PLUGIN...] [-h] [-v]

ARGUMENTS
  PLUGIN...  plugin to uninstall

FLAGS
  -h, --help     Show CLI help.
  -v, --verbose

DESCRIPTION
  Removes a plugin from the CLI.

ALIASES
  $ control plugins unlink
  $ control plugins remove

EXAMPLES
  $ control plugins uninstall myplugin
```

_See code: [@oclif/plugin-plugins](https://github.com/oclif/plugin-plugins/blob/v5.4.15/src/commands/plugins/uninstall.ts)_

## `control plugins unlink [PLUGIN]`

Removes a plugin from the CLI.

```
USAGE
  $ control plugins unlink [PLUGIN...] [-h] [-v]

ARGUMENTS
  PLUGIN...  plugin to uninstall

FLAGS
  -h, --help     Show CLI help.
  -v, --verbose

DESCRIPTION
  Removes a plugin from the CLI.

ALIASES
  $ control plugins unlink
  $ control plugins remove

EXAMPLES
  $ control plugins unlink myplugin
```

## `control plugins update`

Update installed plugins.

```
USAGE
  $ control plugins update [-h] [-v]

FLAGS
  -h, --help     Show CLI help.
  -v, --verbose

DESCRIPTION
  Update installed plugins.
```

_See code: [@oclif/plugin-plugins](https://github.com/oclif/plugin-plugins/blob/v5.4.15/src/commands/plugins/update.ts)_
<!-- commandsstop -->
