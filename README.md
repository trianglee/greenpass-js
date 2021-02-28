# Overview

Self-contained HTML to verify Green Pass QR code signature, using
the Israel Ministry of Health RSA public key.

No data is sent anywhere, signature verification is done entirely off-line 
in the browser.  
**In any case, don't put sensitive data into this page without reading the code first!**

# Origins

Based on the details and verification code provided by Ministry of Health in
https://github.com/MohGovIL/Ramzor, and on the reverse-engeering work done by 
Yuval Adam in https://github.com/yuvadm/greenpass.

# Public Key

Hard-coded Ministry of Health public key is from
https://github.com/yuvadm/greenpass/blob/main/certs/RamzorQRPubKey.pem.

It can be extracted from the official DER certificate in
https://github.com/MohGovIL/Ramzor/blob/main/Verification/RamzorQRPubKey.der, using -

```
openssl x509 -pubkey -in RamzorQRPubKey.der -inform der -outform pem -noout
```
