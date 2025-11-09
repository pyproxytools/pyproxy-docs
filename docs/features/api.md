# API

The Monitoring API allows you to retrieve proxy server status, configuration, and manage filtering rules (blocked sites and URLs).

All routes are secured using HTTP Basic Authentication.

!!! note
    Here is a [python SDK](https://github.com/pyproxytools/pyproxy-sdk-py) to interact with the API.

---

## Endpoints

### `GET /`

Returns the main monitoring HTML dashboard.

---

### `GET /api/status`

Returns real-time monitoring information about the running proxy server.

**Response example:**
```json
{
  "pid": 12345,
  "threads": 10,
  "connections": 5,
  ...
}
```

---

### `GET /api/settings`

Returns the current proxy server configuration.

**Response example:**

```json
{
  "host": "127.0.0.1",
  "port": 8080,
  "debug": false,
  "html_403": true,
  "logger_config": { ... },
  "filter_config": { ... },
  "ssl_config": { ... },
  "flask_port": 5000
}
```

---

### `GET /api/filtering`

Returns current blocked domains and URLs.

**Response example:**

```json
{
  "blocked_sites": ["example.com", "malware.com"],
  "blocked_url": ["http://badurl.com/path"]
}
```

---

### `POST /api/filtering`

Add a domain or URL to the block list.

**Request body:**

```json
{
  "type": "domain" | "url",
  "value": "value_to_block"
}
```

**Responses:**

* `201`: Successfully added.
* `400`: Invalid input.
* `409`: Already blocked.

---

### `DELETE /api/filtering`

Remove a domain or URL from the block list.

**Request body:**

```json
{
  "type": "domain" | "url",
  "value": "value_to_unblock"
}
```

**Responses:**

* `200`: Successfully removed.
* `400`: Invalid input.
* `404`: Value not found.
* `500`: Server error.

---

## Authentication

All endpoints require HTTP Basic Authentication.

Provide your credentials in the `Authorization` header:

```http
Authorization: Basic <base64(username:password)>
```
