# 📦 From Docker

## Latest version
For a containerized deployment to the latest stable version using Docker, execute the following commands:

```bash
docker pull ghcr.io/pyproxytools/pyproxy:latest
docker run -d ghcr.io/pyproxytools/pyproxy:latest
```

## Other version
To get a version other than the latest one :

```bash
docker pull ghcr.io/pyproxytools/pyproxy:1.2.0
docker run -d ghcr.io/pyproxytools/pyproxy:1.2.0
```

## After
After fetching the sources, you can configure the proxy

* [From an .ini file](../configuration/from_ini_file.md)
* [With command argument](../configuration/command_argument.md)
* [Environment variables](../configuration/env_var.md)
* [CA certificates](../configuration/ca_certificates.md)

# 📦 Installation with Docker Compose

If you prefer to use **Docker Compose** for easier management of multi-container setups, you can define the `pyproxy` service in a `docker-compose.yml` file. This will allow you to manage and configure the containerized proxy application easily.

An example `docker-compose.yml` to configure the latest version of `pyproxy` is available at the root of the project

Note: Environment variables should be formatted as `PYPROXY_<CLI_ARGUMENT>` where the CLI argument is in uppercase and hyphens (`-`) are replaced by underscores (`_`).

With this `docker-compose.yml` file, you can start the containerized `pyproxy` service by running:

```bash
docker-compose up -d
```
