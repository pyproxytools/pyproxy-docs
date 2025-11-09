A shortcut system is available to allow users to access sites more quickly. For example, the query `http://gh/` can be translated to `https://github.com`.

By default, the list of shortcuts is defined in `config/shortcuts.txt`.
They must be in the key=value format, for example `gh=https://github.com`.

!!! warning
    This feature is not available in the `slim` version.

## Change the file path
You can change the path to the files containing the shortcuts. Here is the associated documentation, depending on your configuration.

* [From an .ini file](../configuration/from_ini_file.md)
* [With command argument](../configuration/command_argument.md)
* [Environment variables](../configuration/env_var.md)

## Disable shortcuts
The shortcut system is activated when the file is present. Simply do not create the shortcut file.
