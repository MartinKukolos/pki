# pki

```

$cert = New-Object System.Security.Cryptography.X509Certificates.X509Certificate2("./cert_export_cert2-idenity-root.crt")
$ctl = New-Object System.Security.Cryptography.X509Certificates.X509Certificate2Collection
$ctl.Add($cert)
$sstBytes = $ctl.Export([System.Security.Cryptography.X509Certificates.X509ContentType]::SerializedStore)
[System.IO.File]::WriteAllBytes("./identity-root.sst", $sstBytes)
```