## Obejtivo
The password for the next level can be retrieved by submitting the password of the current level to **port 30001 on localhost** using SSL encryption.

**Helpful note: Getting “HEARTBEATING” and “Read R BLOCK”? Use -ign_eof and read the “CONNECTED COMMANDS” section in the manpage. Next to ‘R’ and ‘Q’, the ‘B’ command also works in this version of that command…**
## Datos de acceso
**bandit.labs.overthewire.org**
**bandit15**
jN2kgmIXJ6fShzhT2avhotn4Zcka6tnt
## Solución 
```
bandit15@bandit:~$ openssl s_client -connect localhost:30001
CONNECTED(00000003)
Can't use SSL_get_servername
depth=0 CN = localhost
verify error:num=18:self-signed certificate
verify return:1
depth=0 CN = localhost
verify error:num=10:certificate has expired
notAfter=Feb 24 22:59:04 2023 GMT
verify return:1
depth=0 CN = localhost
notAfter=Feb 24 22:59:04 2023 GMT
verify return:1
---
Certificate chain
 0 s:CN = localhost
   i:CN = localhost
   a:PKEY: rsaEncryption, 2048 (bit); sigalg: RSA-SHA1
   v:NotBefore: Feb 24 22:58:04 2023 GMT; NotAfter: Feb 24 22:59:04 2023 GMT
---
Server certificate
-----BEGIN CERTIFICATE-----
MIIDCzCCAfOgAwIBAgIEdtHsNjANBgkqhkiG9w0BAQUFADAUMRIwEAYDVQQDDAls
b2NhbGhvc3QwHhcNMjMwMjI0MjI1ODA0WhcNMjMwMjI0MjI1OTA0WjAUMRIwEAYD
VQQDDAlsb2NhbGhvc3QwggEiMA0GCSqGSIb3DQEBAQUAA4IBDwAwggEKAoIBAQCx
mrCINhzIGCIeMR5GsleGkWUZWNcLl1D3FFa0OwDgYG0lj4VP3fC2jf7SJ8DbMdGT
jqyOhsM+LZhKWPJ+NH60lzWTeYq6/pe2OMFhZ6bbd84coT7Fo7Evjk4bye2+qYsH
J6MR7Gk+bhL9U4KpCVOpZwHitiC4ZbX+s7n8PHQsfMeQfhSS7J+Xa0vTw3KQoVCg
3BhKTD9bt3gXVfGNaIvECku2sCECDkFyCR5+AqswPHCT7QK8Q3sb9gbA0/zhWbXb
h4RVpbwm+NqmDivMxPVSH+J6NzgmBpLTpeFsN05rlN9CdzRP9l+tLCJnf1irtKMI
0KkVzlGMg/vwLKYA0G5pAgMBAAGjZTBjMBQGA1UdEQQNMAuCCWxvY2FsaG9zdDBL
BglghkgBhvhCAQ0EPhY8QXV0b21hdGljYWxseSBnZW5lcmF0ZWQgYnkgTmNhdC4g
U2VlIGh0dHBzOi8vbm1hcC5vcmcvbmNhdC8uMA0GCSqGSIb3DQEBBQUAA4IBAQBx
vsPCAfYKiOZH0RDDB18SoiFpjkw3A9lSM14tvFlYsEdx31DvJNwc6QT/E8uOV2sB
Kl4wGwJQPJ7VT93CClFN3je9drqlNryCm+P4VO1Fhay8JIb6PyW0z4WCIlJqCRKT
68SPozIEfx/lwquR+MPyopny7tIlA1IZN4aF5yA+Gi570zC7UtdRBVyfGrdANeS8
5pmwA2NzxauCh3QJc2jWYVk4qmmTsLJBgElaFN1QrZHk60rxaUjS4rFnsSYZ/d4n
kmj3TPpRidAxlDM5qnXqD7fcBNy3s7XXk40ygWS/GsJJx38sHr0yFmMV7l0QKVBC
rsP6Hy0UaGAkUNBjj/Fi
-----END CERTIFICATE-----
subject=CN = localhost
issuer=CN = localhost
---
No client certificate CA names sent
Peer signing digest: SHA256
Peer signature type: RSA-PSS
Server Temp Key: X25519, 253 bits
---
SSL handshake has read 1339 bytes and written 373 bytes
Verification error: certificate has expired
---
New, TLSv1.3, Cipher is TLS_AES_256_GCM_SHA384
Server public key is 2048 bit
Secure Renegotiation IS NOT supported
Compression: NONE
Expansion: NONE
No ALPN negotiated
Early data was not sent
Verify return code: 10 (certificate has expired)
---
---
Post-Handshake New Session Ticket arrived:
SSL-Session:
    Protocol  : TLSv1.3
    Cipher    : TLS_AES_256_GCM_SHA384
    Session-ID: 41797C89700647D6458B0DEFCD49F7E7321B1BF510F5C4328B7D17A5D2B6683E
    Session-ID-ctx:
    Resumption PSK: D24EA7567077A38C3551AAAC75E3033028601A5A28B714B2EA39FA21CE6DE37235D3142E95CCF9DB318D15EDADAE0CB6
    PSK identity: None
    PSK identity hint: None
    SRP username: None
    TLS session ticket lifetime hint: 7200 (seconds)
    TLS session ticket:
    0000 - cb 00 ae d3 fc cf 12 aa-e1 f0 d3 ef 6c 0e a6 aa   ............l...
    0010 - 8e 32 8d 53 22 fe 9c 4b-83 4e 25 0e 1f a9 fc 8e   .2.S"..K.N%.....
    0020 - b5 6c 56 68 af 6e cf 1c-f5 32 1f 23 d3 da 61 10   .lVh.n...2.#..a.
    0030 - 1d 0e 4f 17 53 44 b2 e1-c2 61 2d eb a4 be 49 d1   ..O.SD...a-...I.
    0040 - a6 3b bf 7c 81 b3 dd 0c-61 b7 82 46 c7 4f 3a 2d   .;.|....a..F.O:-
    0050 - 8d 00 9e de d5 80 b8 12-58 35 e4 02 b4 18 cb 32   ........X5.....2
    0060 - 6a 11 50 fe 84 fc fc c1-99 d2 bd 61 97 28 f6 3b   j.P........a.(.;
    0070 - fc 3e 05 99 63 e2 f0 10-e8 9e 23 25 20 be 29 3f   .>..c.....#% .)?
    0080 - 4c 7e 6a 40 a9 be a4 7d-a2 10 08 af 25 e7 b5 f9   L~j@...}....%...
    0090 - f0 6b 65 1b 2c 1d 31 9b-1a 25 44 79 7d 91 9a 63   .ke.,.1..%Dy}..c
    00a0 - 7f d8 18 34 73 d9 f0 03-1f 5b 22 25 95 90 06 1e   ...4s....["%....
    00b0 - 7e 12 75 de e2 7f 05 75-ce da 75 a4 3a 0e ff 9b   ~.u....u..u.:...
    00c0 - 1b 5f 58 4e 15 d5 88 c3-d4 d0 1a 45 04 28 b8 c7   ._XN.......E.(..

    Start Time: 1677457822
    Timeout   : 7200 (sec)
    Verify return code: 10 (certificate has expired)
    Extended master secret: no
    Max Early Data: 0
---
read R BLOCK
---
Post-Handshake New Session Ticket arrived:
SSL-Session:
    Protocol  : TLSv1.3
    Cipher    : TLS_AES_256_GCM_SHA384
    Session-ID: B39E0BB21A10A02B1A9FB19D4F6812773FAEDF5164E432F3F308806C56539655
    Session-ID-ctx:
    Resumption PSK: 84221B9D31DF3E0331930367C6E66A9AB18CD3223576AD1B040D33B391D020F1AC1835AB5A45EE7DB5F39A53C35FBDE3
    PSK identity: None
    PSK identity hint: None
    SRP username: None
    TLS session ticket lifetime hint: 7200 (seconds)
    TLS session ticket:
    0000 - cb 00 ae d3 fc cf 12 aa-e1 f0 d3 ef 6c 0e a6 aa   ............l...
    0010 - f1 51 26 a7 e9 9a a9 e5-2d 0c 8d a3 53 81 9c a3   .Q&.....-...S...
    0020 - 9c d3 d7 97 bd f9 4b 62-8a 5d d8 aa d1 4a 2f 8b   ......Kb.]...J/.
    0030 - 11 53 77 dc d5 30 13 f1-dc 9d a9 f0 39 38 3c c1   .Sw..0......98<.
    0040 - 87 47 86 b7 ff d8 53 6f-80 ad 92 13 33 79 60 79   .G....So....3y`y
    0050 - 9f 4c 65 8a 3a 05 d3 07-b5 39 0f c0 c0 23 5b ab   .Le.:....9...#[.
    0060 - 74 99 de 99 64 68 dd 73-e0 35 f1 5a 78 c3 a3 66   t...dh.s.5.Zx..f
    0070 - 5d f4 64 84 7f 3f 7b 5e-f4 73 f1 80 29 64 b6 d3   ].d..?{^.s..)d..
    0080 - 0c fc ad 79 8b 42 7a f8-44 34 fd 18 a1 df 41 54   ...y.Bz.D4....AT
    0090 - b9 29 4d 91 0a 2d a1 82-c6 e2 b1 50 00 a3 f2 b4   .)M..-.....P....
    00a0 - d9 ad 73 de ba ff 42 6e-d8 59 d6 d1 c9 76 e1 c8   ..s...Bn.Y...v..
    00b0 - 22 cc 99 0e 98 41 68 40-e6 6f 99 b9 2d f5 a8 91   "....Ah@.o..-...
    00c0 - 3d f3 07 3d e5 10 d3 0b-34 86 ff ac 25 3a 7d 9e   =..=....4...%:}.

    Start Time: 1677457822
    Timeout   : 7200 (sec)
    Verify return code: 10 (certificate has expired)
    Extended master secret: no
    Max Early Data: 0
---
read R BLOCK
jN2kgmIXJ6fShzhT2avhotn4Zcka6tnt
Correct!
JQttfApK4SeyHwDlI9SXGR50qclOAil1

closed
bandit15@bandit:~$
```
## Notas adicionales 

## Referencia 