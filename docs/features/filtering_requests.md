By default, all requests passing through the proxy can be filtered based on block lists. The block lists are located in `config/blocked_sites.txt` and `config/blocked_url.txt`. Block lists can be local on the proxy or remote via HTTP

!!! warning
    Please note: URL filtering in https is only possible if SSL inspection is enabled.

## Change the file path
You can change the path to the files containing the block lists. Here is the associated documentation, depending on your configuration.

* [From an .ini file](../configuration/from_ini_file.md)
* [With command argument](../configuration/command_argument.md)
* [Environment variables](../configuration/env_var.md)

## Disable filtering
You can also disable query filtering. Here is the associated documentation, depending on your configuration.

* [From an .ini file](../configuration/from_ini_file.md)
* [With command argument](../configuration/command_argument.md)
* [Environment variables](../configuration/env_var.md)
