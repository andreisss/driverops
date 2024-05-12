# driverops

## Create a certificate ##

```makecert -r -pe -ss PrivateCertStore -n "CN=MyDriver Test Certificate" MyDriverTestCert.cer```

## sign the driver ##

```signtool sign /v /s PrivateCertStore /n "MyDriver Test Certificate" /t http://timestamp.digicert.com /fd SHA256 C:\Users\andrea\Source\repos\MyDriver1\x64\Release\MyDriver1.sys```
