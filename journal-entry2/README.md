generate key pair

```shell script
keytool -genkeypair -alias ss_cert_sslserver -keyalg RSA -keysize 2048 -storetype PKCS12 -keystore journal-entry-ssl-key.p12 -validity 3650
```

