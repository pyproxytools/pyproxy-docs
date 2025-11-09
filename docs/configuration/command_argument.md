You can launch the proxy directly and configure it with the following arguments:

| Argument | Short | Description | Default Value | Slim version |
|----------|-------|-------------|---------------|---------------|
| `--version` | `-v` | Show version information | N/A | |
| `--debug` | | Enable debug logging | `False` | |
| `--host` | `-H` | IP address to listen on | `0.0.0.0` | |
| `--port` | `-P` | Port to listen on | `8080` | |
| `--config-file` | `-f` | Path to `config.ini` file | `./config.ini` | |
| `--access-log` | | Path to the access log file | `logs/access.log` | |
| `--block-log` | | Path to the block log file | `logs/block.log` | |
| `--html-403` | | Path to the custom 403 Forbidden HTML page | `assets/403.html` | |
| `--filter-mode` | | Disable URL and domain filtering | `False` | |
| `--no-filter` | | Filter list mode (local or http) | `local` | |
| `--blocked-sites` | | Path to the text file containing the list of sites to block | `config/blocked_sites.txt` | |
| `--blocked-url` | | Path to the text file containing the list of URLs to block | `config/blocked_url.txt` | |
| `--shortcuts` | | Path to the text file containing the list of shortcuts | `config/shortcuts.txt` | **not included** |
| `--custom-header` | | Path to the json file containing the list of custom headers | `config/custom_header.json` | **not included** |
| `--authorized-ips` | | Path to the txt file containing the list of authorized ips | `config/authorized_ips.txt` | |
| `--no-logging-access` | | Disable access logging | `False` | |
| `--no-logging-block` | | Disable block logging | `False` | |
| `--ssl-inspect` | | Enable SSL inspection | `False` | |
| `--inspect-ca-cert` | | Path to the CA certificate | `certs/ca/cert.pem` | |
| `--inspect-ca-key` | | Path to the CA key | `certs/ca/key.pem` | |
| `--inspect-certs-folder` | | Path to the generated certificates folder | `certs/` | |
| `--cancel-inspect` | | Path to the text file containing the list of URLs without ssl inspection | `config/cancel_inspect.txt` | |
| `--flask-port` | | Port to listen on for monitoring interface | `5000` | **not included** |
| `--flask-pass` | | Default password to Flask interface | `password` | **not included** |
| `--proxy-enable` | | Enable proxy after PyProxy | `False` | |
| `--proxy-host` | | Proxy IP to use after PyProxy | `127.0.0.1` | |
| `--proxy-port` | | Proxy Port to use after PyProxy | `8081` | |

## Example
### With source
Example of a launch with SSL inspection for HTTPS requests
```bash
python3 pyproxy.py --ssl-inspect
```

!!! warning
    Please note: for SSL inspection, you must configure a certificate authority to generate SSL certificates.
    Here is the documentation on [SSL Inspection](../features/ssl_inspection.md)

### With Docker image
Example of a launch with SSL inspection for HTTPS requests
```bash
docker run -d ghcr.io/6c656c65/pyproxy:latest --ssl-inspect
```
!!! warning
    Please note: for SSL inspection, you must configure a certificate authority to generate SSL certificates.
    Here is the documentation on [SSL Inspection](../features/ssl_inspection.md)

## With configuration file
You can configure the proxy using a [From an .ini file](../configuration/from_ini_file.md) instead of arguments.