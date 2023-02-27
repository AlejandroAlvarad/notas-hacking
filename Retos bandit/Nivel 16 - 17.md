## Obejtivo
The credentials for the next level can be retrieved by submitting the password of the current level to **a port on localhost in the range 31000 to 32000**. First find out which of these ports have a server listening on them. Then find out which of those speak SSL and which don’t. There is only 1 server that will give the next credentials, the others will simply send back to you whatever you send to it.
## Datos de acceso
**bandit.labs.overthewire.org**
**bandit16**
JQttfApK4SeyHwDlI9SXGR50qclOAil1
## Solución 
```
bandit16@bandit:~$ nmap  localhost
Starting Nmap 7.80 ( https://nmap.org ) at 2023-02-23 14:19 UTC
Nmap scan report for localhost (127.0.0.1)
Host is up (0.00015s latency).
Not shown: 994 closed ports
PORT      STATE SERVICE
22/tcp    open  ssh
1111/tcp  open  lmsocialserver
1840/tcp  open  netopia-vo2
4321/tcp  open  rwhois
8000/tcp  open  http-alt
30000/tcp open  ndmps

Nmap done: 1 IP address (1 host up) scanned in 0.08 seconds
bandit16@bandit:~$ nmap -p 31000-32000 localhost
Starting Nmap 7.80 ( https://nmap.org ) at 2023-02-23 14:20 UTC
Nmap scan report for localhost (127.0.0.1)
Host is up (0.000096s latency).
Not shown: 996 closed ports
PORT      STATE SERVICE
31046/tcp open  unknown
31518/tcp open  unknown
31691/tcp open  unknown
31790/tcp open  unknown
31960/tcp open  unknown

Nmap done: 1 IP address (1 host up) scanned in 0.06 seconds
bandit16@bandit:~$ openssl s_client - connec
s_client: Unknown option: -
s_client: Use -help for summary.
bandit16@bandit:~$
bandit16@bandit:~$
bandit16@bandit:~$
bandit16@bandit:~$
bandit16@bandit:~$
bandit16@bandit:~$ openssl s_client - connect localhost:31691
s_client: Unknown option: -
s_client: Use -help for summary.
bandit16@bandit:~$ openssl s_client -connect localhost:31790
CONNECTED(00000003)
Can't use SSL_get_servername
depth=0 CN = localhost
verify error:num=18:self-signed certificate
verify return:1
depth=0 CN = localhost
verify error:num=10:certificate has expired
notAfter=Feb 21 22:03:58 2023 GMT
verify return:1
depth=0 CN = localhost
notAfter=Feb 21 22:03:58 2023 GMT
verify return:1
---
Certificate chain
 0 s:CN = localhost
   i:CN = localhost
   a:PKEY: rsaEncryption, 2048 (bit); sigalg: RSA-SHA1
   v:NotBefore: Feb 21 22:02:58 2023 GMT; NotAfter: Feb 21 22:03:58 2023 GMT
---
Server certificate
-----BEGIN CERTIFICATE-----
MIIDCzCCAfOgAwIBAgIELZxFNDANBgkqhkiG9w0BAQUFADAUMRIwEAYDVQQDDAls
b2NhbGhvc3QwHhcNMjMwMjIxMjIwMjU4WhcNMjMwMjIxMjIwMzU4WjAUMRIwEAYD
VQQDDAlsb2NhbGhvc3QwggEiMA0GCSqGSIb3DQEBAQUAA4IBDwAwggEKAoIBAQC8
C8jJ2//6TxiFBwjuC7+xUcu293V+n8pLxHfVnpZG9fvlOBG3nA3hm2/iNYybZNla
R58hZmfPWEKcuX7GZGvNUOAa6wOg2WYrMo1+6NCcynmCdJEabv2kemvOtBQFeV43
EUW+BW/+6903QuSHsjDewSoljGtmRGjg0oXUgyOlzGDQR/EfX7N8KGubYzZcHf+i
uZ35xMF5HQWi7Zf2ObapcbIfyjw2JWQLVqa8eDbZ4R4HKXYBLeJ4rZoYbPO1JUuX
IY6g+zV0yrgeX3EE36S4fYG/c5eixWRsA+KMYdJjtd2JTvEyyU9kSRQBNIJQOlmH
956MMGFmMqXn+kus9wgbAgMBAAGjZTBjMBQGA1UdEQQNMAuCCWxvY2FsaG9zdDBL
BglghkgBhvhCAQ0EPhY8QXV0b21hdGljYWxseSBnZW5lcmF0ZWQgYnkgTmNhdC4g
U2VlIGh0dHBzOi8vbm1hcC5vcmcvbmNhdC8uMA0GCSqGSIb3DQEBBQUAA4IBAQCQ
ZF30iIq43MI9neBsmpAg3W5GsZzzV/JVOPDK1BG1ynEF5hqd6SFuRRSNXXy1AN3O
jL5m5B8sIh53vzfDBhv5XgSeKDm8KPqNn9CF5yP+neVglcJh3frf6DX4yE4yntHZ
SyxWErfMX/s5P1W4NdNoph6zNWBN5EjPls9mYo4gfkUnS72FDLfyGmPan8WKUP00
hhK6TdtbcetA/9HODOD2QL82tugZvCK9qPnNHG9TkcgaJ8LW9AY/ZCwnIYsODUQi
gYSDr2Ya4GuSAp2Vn4KkaJ1+NGmE+AxUMJ0rNsKUg6JelZ6vZ4TcFNbOSqaiCOtj
5xezGlZxL+dTerQ6hBwn
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
    Session-ID: 43054ADC10BF22BD3691DB9A9485ECA09CB8B61D1912E2B6B6093D1C5493DF51
    Session-ID-ctx:
    Resumption PSK: 39C34448AC99DCBB4E34A764EDAB876ECBC24D85924810D74EA0A5D59BBA4BADE09C6693AB6D58C2C3B1CBE8C68B42EC
    PSK identity: None
    PSK identity hint: None
    SRP username: None
    TLS session ticket lifetime hint: 7200 (seconds)
    TLS session ticket:
    0000 - c6 5e 1a 4b fa 61 a1 cf-47 91 bc ee 77 38 8c 18   .^.K.a..G...w8..
    0010 - 5c cd 6c b1 4f 71 91 77-b8 8c 08 4e da 5b c9 1a   \.l.Oq.w...N.[..
    0020 - 97 8e c8 c1 83 1a 0a ff-a1 33 d7 fb 87 57 a0 58   .........3...W.X
    0030 - 73 7c 70 45 db d3 5d ca-bb e6 4e ab 8c 92 e5 cb   s|pE..]...N.....
    0040 - b9 87 2e 0e fb e7 a4 f7-f1 c4 a8 e4 a9 38 c2 25   .............8.%
    0050 - d9 e4 10 10 4c 68 da 09-fa 46 99 06 14 dd b4 24   ....Lh...F.....$
    0060 - 52 54 39 51 05 df 63 32-d4 55 f9 42 6c a6 f2 23   RT9Q..c2.U.Bl..#
    0070 - 8a e8 39 e3 54 83 71 b3-be 94 92 1f f3 c7 cd 03   ..9.T.q.........
    0080 - ac 50 10 12 9d f3 b0 08-c5 f8 15 70 73 d0 34 48   .P.........ps.4H
    0090 - 54 45 a7 7a d1 ad 24 1a-cb d5 78 17 c8 8b cb 91   TE.z..$...x.....
    00a0 - b9 4c bd 42 79 6d 53 a6-77 22 a8 a7 62 29 d1 bd   .L.BymS.w"..b)..
    00b0 - 72 22 69 40 a7 8a 32 25-a4 84 ac 1e e2 6e 6f 73   r"i@..2%.....nos
    00c0 - ac 4a 94 0a 1e e6 79 e7-2d 69 64 f1 00 f7 88 b6   .J....y.-id.....

    Start Time: 1677162250
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
    Session-ID: 2F5A0CDC1BF4361808DA2F343AFC5C8574313FAA87F213C8AD486D2EBB372C93
    Session-ID-ctx:
    Resumption PSK: 27251A0B9877DB57FA9DB15D5A615EEBEF748B225CD32D792A1A2571859DAA51A3F40C0CD4E08A616CE0FEEAA61E7515
    PSK identity: None
    PSK identity hint: None
    SRP username: None
    TLS session ticket lifetime hint: 7200 (seconds)
    TLS session ticket:
    0000 - c6 5e 1a 4b fa 61 a1 cf-47 91 bc ee 77 38 8c 18   .^.K.a..G...w8..
    0010 - 35 39 88 fa 49 1a 2d be-70 ef 64 66 e0 be 81 70   59..I.-.p.df...p
    0020 - 7a 3d e3 01 0d cc d1 0a-76 f8 1a 92 a4 8d 10 f4   z=......v.......
    0030 - 6f 62 66 fe 6c 0f ef 44-6a 17 57 6a f3 0d 62 89   obf.l..Dj.Wj..b.
    0040 - 77 94 66 96 cf dd 41 ce-98 a0 1d 69 de ba 21 31   w.f...A....i..!1
    0050 - 69 ea d3 69 2d 35 11 d9-e6 88 4a f5 a5 05 f1 cf   i..i-5....J.....
    0060 - 6e 36 20 a6 86 5b ce dc-12 65 6a 27 49 0d 18 b7   n6 ..[...ej'I...
    0070 - ee db fe 58 5b ee 57 56-9d 4a 4e 0e 9f 6b 98 7f   ...X[.WV.JN..k..
    0080 - 62 51 28 ef 27 f5 45 32-a6 50 7e 30 23 38 3e 0b   bQ(.'.E2.P~0#8>.
    0090 - 69 b4 78 3d 67 b2 c9 dd-70 73 22 73 e0 15 eb 9a   i.x=g...ps"s....
    00a0 - bd e4 54 61 1a fa 37 9c-75 50 e6 d5 ea 6d 7f 0a   ..Ta..7.uP...m..
    00b0 - f6 1e e4 66 78 34 e3 c7-15 8a 6c 59 47 a8 31 7a   ...fx4....lYG.1z
    00c0 - 08 ab 21 a8 5d 36 5c b9-d0 b2 42 cb 8e 8d c1 b8   ..!.]6\...B.....

    Start Time: 1677162250
    Timeout   : 7200 (sec)
    Verify return code: 10 (certificate has expired)
    Extended master secret: no
    Max Early Data: 0
---
read R BLOCK
JQttfApK4SeyHwDlI9SXGR50qclOAil1
Correct!
-----BEGIN RSA PRIVATE KEY-----
MIIEogIBAAKCAQEAvmOkuifmMg6HL2YPIOjon6iWfbp7c3jx34YkYWqUH57SUdyJ
imZzeyGC0gtZPGujUSxiJSWI/oTqexh+cAMTSMlOJf7+BrJObArnxd9Y7YT2bRPQ
Ja6Lzb558YW3FZl87ORiO+rW4LCDCNd2lUvLE/GL2GWyuKN0K5iCd5TbtJzEkQTu
DSt2mcNn4rhAL+JFr56o4T6z8WWAW18BR6yGrMq7Q/kALHYW3OekePQAzL0VUYbW
JGTi65CxbCnzc/w4+mqQyvmzpWtMAzJTzAzQxNbkR2MBGySxDLrjg0LWN6sK7wNX
x0YVztz/zbIkPjfkU1jHS+9EbVNj+D1XFOJuaQIDAQABAoIBABagpxpM1aoLWfvD
KHcj10nqcoBc4oE11aFYQwik7xfW+24pRNuDE6SFthOar69jp5RlLwD1NhPx3iBl
J9nOM8OJ0VToum43UOS8YxF8WwhXriYGnc1sskbwpXOUDc9uX4+UESzH22P29ovd
d8WErY0gPxun8pbJLmxkAtWNhpMvfe0050vk9TL5wqbu9AlbssgTcCXkMQnPw9nC
YNN6DDP2lbcBrvgT9YCNL6C+ZKufD52yOQ9qOkwFTEQpjtF4uNtJom+asvlpmS8A
vLY9r60wYSvmZhNqBUrj7lyCtXMIu1kkd4w7F77k+DjHoAXyxcUp1DGL51sOmama
+TOWWgECgYEA8JtPxP0GRJ+IQkX262jM3dEIkza8ky5moIwUqYdsx0NxHgRRhORT
8c8hAuRBb2G82so8vUHk/fur85OEfc9TncnCY2crpoqsghifKLxrLgtT+qDpfZnx
SatLdt8GfQ85yA7hnWWJ2MxF3NaeSDm75Lsm+tBbAiyc9P2jGRNtMSkCgYEAypHd
HCctNi/FwjulhttFx/rHYKhLidZDFYeiE/v45bN4yFm8x7R/b0iE7KaszX+Exdvt
SghaTdcG0Knyw1bpJVyusavPzpaJMjdJ6tcFhVAbAjm7enCIvGCSx+X3l5SiWg0A
R57hJglezIiVjv3aGwHwvlZvtszK6zV6oXFAu0ECgYAbjo46T4hyP5tJi93V5HDi
Ttiek7xRVxUl+iU7rWkGAXFpMLFteQEsRr7PJ/lemmEY5eTDAFMLy9FL2m9oQWCg
R8VdwSk8r9FGLS+9aKcV5PI/WEKlwgXinB3OhYimtiG2Cg5JCqIZFHxD6MjEGOiu
L8ktHMPvodBwNsSBULpG0QKBgBAplTfC1HOnWiMGOU3KPwYWt0O6CdTkmJOmL8Ni
blh9elyZ9FsGxsgtRBXRsqXuz7wtsQAgLHxbdLq/ZJQ7YfzOKU4ZxEnabvXnvWkU
YOdjHdSOoKvDQNWu6ucyLRAWFuISeXw9a/9p7ftpxm0TSgyvmfLF2MIAEwyzRqaM
77pBAoGAMmjmIJdjp+Ez8duyn3ieo36yrttF5NSsJLAbxFpdlc1gvtGCWW+9Cq0b
dxviW8+TFVEBl1O4f7HVm6EpTscdDxU+bCXWkfjuRb7Dy9GOtt9JPsX8MBTakzh3
vBgsyi/sN3RqRBcGU40fOoZyfAMT8s1m/uYv52O6IgeuZ/ujbjY=
-----END RSA PRIVATE KEY-----

closed
```
## Notas adicionales 

## Referencia 