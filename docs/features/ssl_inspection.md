By default, proxies don't decrypt passing HTTPS requests; they simply forward them. To enable SSL decryption, you must first give it a CA so it can generate certificates for each site.
Either you can import your own CA or you can generate it with [this documentation](../configuration/ca_certificates.md).

!!! warning
    Please note: It is not recommended to use a self-signed CA for production. Clients must trust the CA used.

## Change the file path
You can change the path to the CA's key and certificate files. Here's the associated documentation, depending on your configuration.
By default, the paths are `certs/ca/key.pem` and `certs/ca/cert.pem`

* [From an .ini file](../configuration/from_ini_file.md)
* [With command argument](../configuration/command_argument.md)
* [Environment variables](../configuration/env_var.md)