You can define a list of subnets that are allowed to use the proxy

!!! warning
    Please note: To reload the list of allowed IP addresses, you must restart the proxy

By default, the list of authorized subnets is defined in the file `config/authorized_ips.txt`.

Here is an example of a `txt` file :
```
0.0.0.0/0
127.0.0.1/8
10.0.0.1/32
```

## Change the file path
You can change the path to the files containing authorized IP addresses. Here is the associated documentation, depending on your configuration.

* [From an .ini file](../configuration/from_ini_file.md)
* [With command argument](../configuration/command_argument.md)
* [Environment variables](../configuration/env_var.md)

## Disable IP address filtering
The IP address filtering system is activated as soon as the file is present. Simply do not create the authorized IP file.
