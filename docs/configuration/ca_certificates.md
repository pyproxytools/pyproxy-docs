This configuration is required to use SSL inspection. The proxy generates SSL certificates for intercepted HTTPS requests. These certificates will be presented to clients. The proxy will sign these certificates with a certificate authority. Therefore, it needs a CA (the key and the certificate).

The CA key and certificate should be placed in `./certs/ca/key.pem` and in `./certs/ca/cert.pem`.

## Generate a self-signed CA
You can generate a self-signed CA with OpenSSL.
```bash 
mkdir -p certs/ca/
openssl req -x509 -newkey rsa:4096 -keyout certs/ca/key.pem -out certs/ca/cert.pem -days 365 -nodes
```