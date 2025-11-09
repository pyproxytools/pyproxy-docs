You can chain multiple proxies together to anonymize client requests. Proxy chaining works on both HTTP and HTTPS requests

!!! warning
    Please note: For HTTPS requests, proxies must perform SSL inspection.

## Proxy chaining example
Proxy 1 :
```bash
python3 pyproxy.py --proxy-enable --proxy-host 127.0.0.1 --proxy-port 8080 --port 8081 --flask-port 5001
```

Proxy 2 :
```bash
python3 pyproxy.py --port 8080
```

cURL :
```bash
curl --proxy 127.0.0.1:8081 https://examle.com -k
```
