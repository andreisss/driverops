# driverops

## Create a certificate ##

```makecert -r -pe -ss PrivateCertStore -n "CN=MyDriver Test Certificate" MyDriverTestCert.cer```

## sign the driver ##

```signtool sign /v /s PrivateCertStore /n "MyDriver Test Certificate" /t http://timestamp.digicert.com /fd SHA256 C:\Users\andrea\Source\repos\MyDriver1\x64\Release\MyDriver1.sys```

## create a service ##

```sc create MyDriver1 type= kernel binPath= "C:\Users\andrea\Source\repos\MyDriver1\x64\Release\MyDriver1.sys"```

## start and query a service ##

```
sc start MyDriver1
sc query MyDriver1
```
