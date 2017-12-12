## What is SSLDocker?

SSLDocker is a tiny multiple host reverse proxy with automatic HTTPS for multiple apps.

## Quick Start

### 1. Make a Config file named `conf.json` with the following example:

```
{
  "Email": "yourmail@domain.com",
  "GzipOn": true,
  "Http2https": true,
  "MaxHeader": 10,
  "Certs": "certs",
  "ProxyItems": [
    {"Host": "app1.com", "Target": "http://localhost:8082"},
    {"Host": "app2.com", "Target": "http://localhost:8083"},
    {"Host": "app3.com", "Target": "http://domain.com"},
    {"Host": "app4.com", "Target": "https://ssldomain.com"}
  ]
}
```

### 2. Start SSLDocker by running the following in your terminal:

```
$ ./ssldocker -c=conf.json
```

### 3. Open your Browser

Type your site's address to see it in action. Live sites are redirected to HTTPS for you.

## What did SSLDocker do for you ?

See official website [https://ssldocker.com/](https://ssldocker.com/)
