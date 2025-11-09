You can configure the proxy using environment variables instead of command-line arguments. The environment variable names follow the pattern `PYPROXY_<CLI_ARGUMENT>`, where the argument is in uppercase and hyphens (`-`) are replaced by underscores (`_`).

Environment Variable | Description | Default Value | Slim version
-- | -- | -- | --
`PYPROXY_VERSION` | Show version information | `N/A` |  
`PYPROXY_DEBUG` | Enable debug logging | `False` |  
`PYPROXY_HOST` | IP address to listen on | `0.0.0.0` |  
`PYPROXY_PORT` | Port to listen on | `8080` |  
`PYPROXY_CONFIG_FILE` | Path to config.ini file | `./config.ini` |  
`PYPROXY_ACCESS_LOG` | Path to the access log file | `logs/access.log` |  
`PYPROXY_BLOCK_LOG` | Path to the block log file | `logs/block.log` |  
`PYPROXY_HTML_403` | Path to the custom 403 Forbidden HTML page | `assets/403.html` |  
`PYPROXY_FILTER_MODE` | Disable URL and domain filtering | `False` |  
`PYPROXY_NO_FILTER` | Filter list mode (local or http) | `local` |  
`PYPROXY_BLOCKED_SITES` | Path to the text file containing the list of sites to block | `config/blocked_sites.txt` |  
`PYPROXY_BLOCKED_URL` | Path to the text file containing the list of URLs to block | `config/blocked_url.txt` |  
`PYPROXY_SHORTCUTS` | Path to the text file containing the list of shortcuts | `config/shortcuts.txt` | **not included**
`PYPROXY_CUSTOM_HEADER` | Path to the json file containing the list of custom headers | `config/custom_header.json` | **not included**
`PYPROXY_AUTHORIZED_IPS` | Path to the txt file containing the list of authorized ips | `config/authorized_ips.txt` |
`PYPROXY_NO_LOGGING_ACCESS` | Disable access logging | `False` |  
`PYPROXY_NO_LOGGING_BLOCK` | Disable block logging | `False` |  
`PYPROXY_SSL_INSPECT` | Enable SSL inspection | `False` |  
`PYPROXY_INSPECT_CA_CERT` | Path to the CA certificate | `certs/ca/cert.pem` |  
`PYPROXY_INSPECT_CA_KEY` | Path to the CA key | `certs/ca/key.pem` |  
`PYPROXY_INSPECT_CERTS_FOLDER` | Path to the generated certificates folder | `certs/` |  
`PYPROXY_CANCEL_INSPECT` | Path to the text file containing the list of URLs without SSL inspection | `config/cancel_inspect.txt` |  
`PYPROXY_FLASK_PORT` | Port to listen on for the monitoring interface | `5000` | **not included**
`PYPROXY_FLASK_PASS` | Default password to Flask interface | `password` | **not included**
`PYPROXY_PROXY_ENABLE` | Enable proxy after PyProxy | `False` |
`PYPROXY_PROXY_HOST` | Proxy IP to use after PyProxy | `127.0.0.1` |
`PYPROXY_PROXY_PORT` | Proxy Port to use after PyProxy | `8081` |

## Example Usage with Docker Compose
To configure `pyproxy` with Docker Compose and set environment variables, you can add the following to your `docker-compose.yml` file:

```yaml
services:
  pyproxy:
    image: ghcr.io/6c656c65/pyproxy:latest
    environment:
      PYPROXY_HOST: 0.0.0.0
      PYPROXY_PORT: 8080
      PYPROXY_SSL_INSPECT: "True"
      PYPROXY_FLASK_PORT: 5000
      PYPROXY_DEBUG: "True"
```