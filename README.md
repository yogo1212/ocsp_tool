Manage OCSP data for a certificate.

Example usage:
Keep an ocsp.der for cert.pem up to date in a loop (using sleep!).
chain.pem is used as the issuer certificate for the request and to verify the
OCSP repsonse. Files created by certbot will do (Let's Encrypt).
printf is called whenever there's an udpate.

```
./ocsp_tool sustain cert.pem chain.pem ocsp.der \
	printf 'file "%s" was updated, valid until %s (UNIX timestamp)\n'
```
