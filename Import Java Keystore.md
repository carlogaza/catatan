# Importing SSL / Certificate File into Java Key Store

1. Download SSL / Certificate of Website using Chrome or Firefox. <br>`Klik SSL Button` > `View Certificate` > `Download Certificate`.
2. If certificate in `.PEM` format, convert it into `.DER` format using `openssl`!
```
openssl x509 -outform der -in certificate.pem -out certificate.der
```
3. Import your certificate into your java keystore! <br> Default keystore password: `changeit`
```
keytool -import -alias your-alias -keystore your-keystore.jks -file certificate.der
```
4. Done!

---
### List all of certificate in Keystore
```
keytool -list -keystore your-keystore.jks
```

---
### Delete certificate in Keystore
```
keytool -delete -alias your-alias -keystore your-keystore.jks
```
