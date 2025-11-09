A header customization system is available.
By default, the list of custom headers is defined in the `config/custom_header.json` file.

Here is an example of a `json` file :
```json
{
    "https://example.com": {
      "X-Custom-Header": "HeaderValue",
      "X-Another-Header": "AnotherValue"
    },
    "https://example2.com": {
      "X-Different-Header": "DifferentValue"
    }
  }
```

!!! warning
    This feature is not available in the `slim` version.

## Change the file path
You can change the path to the files containing custom headers. Here is the associated documentation, depending on your configuration.

* [From an .ini file](../configuration/from_ini_file.md)
* [With command argument](../configuration/command_argument.md)
* [Environment variables](../configuration/env_var.md)

## Disable header customization
The header customization system is activated when the file is present. Simply do not create the header customization file.