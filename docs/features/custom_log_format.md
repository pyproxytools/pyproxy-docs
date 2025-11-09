You can customize the output format of the console log and the access and block files by configuring the `console_format`, `access_log_format`, or `block_log_format` option in the `[Logging]` section of your `.ini` configuration file.

## Log format configuration example
### Key-value
`config.ini`:
```ini
[Logging]
console_format = date=%(asctime)s level=%(levelname)s file=%(filename)s function=%(funcName)s message=%(message)s
access_log_format = date=%(asctime)s ip_src=%(ip_src)s url=%(url)s method=%(method)s domain=%(domain)s port=%(port)s protocol=%(protocol)s bytes_sent=%(bytes_sent)s bytes_received=%(bytes_received)s tls_version=%(tls_version)s
block_log_format = date=%(asctime)s ip_src=%(ip_src)s url=%(url)s method=%(method)s domain=%(domain)s port=%(port)s protocol=%(protocol)s
datefmt = %Y-%m-%d %H:%M:%S
```

This configuration will output logs with timestamps, log levels, and messages, colored according to the log level.
### JSON
`config.ini`:
```ini
[Logging]
console_format = {"date": "%(asctime)s", "level": "%(levelname)s", "file": "%(filename)s", "function": "%(funcName)s", "message":"%(message)s"}
access_log_format = {"date": "%(asctime)s", "ip_src": "%(ip_src)s", "url": "%(url)s", "method": "%(method)s", "domain": "%(domain)s", "port": "%(port)s", "protocol": "%(protocol)s", "bytes_sent": "%(bytes_sent)s", "bytes_received": "%(bytes_received)s", "tls_version": "%(tls_version)s"}
block_log_format = {"date": "%(asctime)s", "ip_src": "%(ip_src)s", "url": "%(url)s", "method": "%(method)s", "domain": "%(domain)s", "port": "%(port)s", "protocol": "%(protocol)s"}
datefmt = %Y-%m-%dT%H:%M:%S
```

## List of variables
The console_format option controls how log messages appear in the console. Colors will be applied automatically even if you don’t include color codes explicitly. You can include fields provided by the `logging` library such as `%(asctime)s`, `%(levelname)s` and `%(message)s`. [Here is the list](https://docs.python.org/3/library/logging.html#logrecord-attributes) of possible variables to use

Other variables are possible to use for `access_log_format` and `block_log_format`:

| Scope | Name |
|----------|-------|
| `block` and `access` | `ip_src` |
| `block` and `access` | `url` |
| `block` and `access` | `method` |
| `block` and `access` | `domain` |
| `block` and `access` | `port` |
| `block` and `access` | `protocol` |
| `access` | `bytes_sent` |
| `access` | `bytes_received` |
| `access` | `tls_version` |
