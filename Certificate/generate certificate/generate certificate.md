

# how to generate certificate
----------------------------
```bash

openssl genrsa -des3 -out server.key
openssl rsa -in server.key -out private.key
openssl req -x509 -nodes -days 365 -newkey rsa:2048 -keyout private.key -out public.crt
```
