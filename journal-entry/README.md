generate key pair

```shell script
keytool -genkeypair -alias ss_cert_sslserver -keyalg RSA -keysize 2048 -storetype PKCS12 -keystore journal-entry-ssl-key.p12 -validity 3650
```
extract cert from p12
```shell script
keytool -exportcert -keystore journal-entry-ssl-key.p12 -storetype PKCS12 -storepass India@123 -alias journal-entry-ssl-key -file journal-entry-ssl-key.crt
```
create a truststore from above
```shell script
keytool -import -file journal-entry-ssl-key.crt -alias firstCA -keystore myTrustStore
```
