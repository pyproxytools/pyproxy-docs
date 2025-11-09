By default, the proxy provides a Flask web interface on port `5000/http` to monitor it. This interface allows you to view processes, their status, configuration, and active connections.

All of these routes require basic authentication. The default credentials are `admin:password`

!!! note
    Here is the [API documentation](../features/api.md).

    Here is a [python SDK](https://github.com/pyproxytools/pyproxy-sdk-py) to interact with the API.

!!! warning
    This feature is not available in the `slim` version.

## Change the monitoring configuration
You can modify the monitoring system, for example, the port or access password. Here is the associated documentation, depending on your configuration.

* [From an .ini file](../configuration/from_ini_file.md)
* [With command argument](../configuration/command_argument.md)
* [Environment variables](../configuration/env_var.md)