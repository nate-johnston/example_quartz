
# Commands

Here is how to check the dates of a website's SSL certificate:

```
% echo | openssl s_client -servername dranesvilleumc.org -connect dranesvilleumc.org:443 2>/dev/null | openssl x509 -noout -dates
notBefore=Dec 26 16:06:28 2025 GMT
notAfter=Mar 26 16:06:27 2026 GMT
```
