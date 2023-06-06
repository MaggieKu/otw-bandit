bandit14@bandit:~$ nc localhost 30000 < /etc/bandit_pass/bandit14
Correct!
jN2kgmIXJ6fShzhT2avhotn4Zcka6tnt

bandit15@bandit:~$ openssl s_client -connect localhost:30001 -ign_eof < /etc/bandit_pass/bandit15
CONNECTED(00000003)
Can't use SSL_get_servername
depth=0 CN = localhost
verify error:num=18:self-signed certificate
verify return:1
depth=0 CN = localhost
verify error:num=10:certificate has expired
notAfter=May  7 21:33:41 2023 GMT
verify return:1
depth=0 CN = localhost
notAfter=May  7 21:33:41 2023 GMT
verify return:1
---
Certificate chain
 0 s:CN = localhost
   i:CN = localhost
   a:PKEY: rsaEncryption, 2048 (bit); sigalg: RSA-SHA1
   v:NotBefore: May  7 21:32:41 2023 GMT; NotAfter: May  7 21:33:41 2023 GMT
---
Server certificate
-----BEGIN CERTIFICATE-----
MIIDCzCCAfOgAwIBAgIEU+dQVDANBgkqhkiG9w0BAQUFADAUMRIwEAYDVQQDDAls
b2NhbGhvc3QwHhcNMjMwNTA3MjEzMjQxWhcNMjMwNTA3MjEzMzQxWjAUMRIwEAYD
VQQDDAlsb2NhbGhvc3QwggEiMA0GCSqGSIb3DQEBAQUAA4IBDwAwggEKAoIBAQC0
6XnyVIeZLtoIK47uogunWQZQxDUdZOAepC7td55A65+Mx7r21N2R3LHj/EQRoy1E
Te4gZN+ct3KhI61uLotGlfr+Orv/71Vaw+7qAo6tTkcqBYxQYb7lyPNDErS88O6n
R8ojh+KeG3PPEpm6CtJMSqnAdhpzrU7sjNb/rmTYKHlKmlJYHeFsug/SkKcAuwDQ
z20NatimfMhVqgzOwqt3FLqfFbOh7IAHIlUzJtynp9rIT1EFjxus1ueFqylaR4Jt
BXz9emIFcdLRoUAvrdh8cJrvDuO/Edzv8S5H4tG0++bT6McMaIW+N6iEFK8S4iJE
KtDCzXbiNxyp/rnUbUV7AgMBAAGjZTBjMBQGA1UdEQQNMAuCCWxvY2FsaG9zdDBL
BglghkgBhvhCAQ0EPhY8QXV0b21hdGljYWxseSBnZW5lcmF0ZWQgYnkgTmNhdC4g
U2VlIGh0dHBzOi8vbm1hcC5vcmcvbmNhdC8uMA0GCSqGSIb3DQEBBQUAA4IBAQAj
ntVKYDgsPILFC1lCFT5yY7P4ECkYyk36V+mmTkqQYoAsVe+wGTkx4lkNotO9H7/U
jC5DI+0YHwLVyumHQm61t6ALR5YhtjCpjjlCNDrbbzKdAB/xTb6twuquHjL9IMRj
55+GINqiXrHXrQhBQeFXNj2NTyTHQqf98S87kKC5RYpbGdYY92Z1r/Bx7VhA2BFU
1qfeBJAaU326/pcv2gZJ7zSroSJBHqqHkTu7oSG6G/Pe3Yb18Assnml6Fjb5Ew0F
VPB+lnI1CQHGRehp6IV1+IjwCDIJ+VlTenAjdU0RYqA2WxttChLNIX4DQEpscZa4
ZWCLVY8HeVW2pSgM6B+u
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
    Session-ID: 6629D5FFE22ECE19E92A05E88F77F63C2A422DC38ED96618433C0FB5EEB58DD1
    Session-ID-ctx:
    Resumption PSK: 04667BDFA66877EC65A505A9A25E295C2E284E43E62C1AAB70C7AB847674CB740B3457331993802CA19529BBA7912CD2
    PSK identity: None
    PSK identity hint: None
    SRP username: None
    TLS session ticket lifetime hint: 7200 (seconds)
    TLS session ticket:
    0000 - 54 69 c4 6e f3 66 e0 75-7a 50 7e a0 cf ab a2 bf   Ti.n.f.uzP~.....
    0010 - e8 0f 64 d1 a5 ef a1 b1-a2 92 6b 6a fc 27 be 4b   ..d.......kj.'.K
    0020 - df e1 ba 85 2f d9 a7 54-b8 b6 f5 5c ce 37 e8 14   ..../..T...\.7..
    0030 - 0d bf 75 68 d5 e3 00 a5-0a 0e f2 ff 62 b7 61 71   ..uh........b.aq
    0040 - 6b 11 86 86 da 7d 12 cb-3b fc ab 09 d9 90 f8 de   k....}..;.......
    0050 - 4a da 2a a4 15 78 f9 2c-a4 bc c7 8a 8b be f3 83   J.*..x.,........
    0060 - 61 c8 91 a4 77 aa 4b 5c-0c 0f 18 68 e6 d6 52 c9   a...w.K\...h..R.
    0070 - fa d3 bc 70 71 92 ac ec-09 40 96 69 0d 1d ab 3d   ...pq....@.i...=
    0080 - ab e9 79 0a a7 02 cb ea-49 55 32 bc 98 2c ee e2   ..y.....IU2..,..
    0090 - 4f b5 64 36 ab ee 85 c8-0f 0a 99 19 fd 7a 3a 18   O.d6.........z:.
    00a0 - ed c1 e5 57 c6 cd e3 f9-5b 38 9f b5 8f ff 07 78   ...W....[8.....x
    00b0 - dd 94 d7 6b d1 50 23 bd-72 0c 38 59 a2 7a ef aa   ...k.P#.r.8Y.z..
    00c0 - 88 3a 9d 82 17 5a b1 ae-64 38 e8 46 df 1d 90 5f   .:...Z..d8.F..._

    Start Time: 1683571873
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
    Session-ID: B9B0335021304414D7C025A4C46614AD7A181BD126E74864EE74CAD934DF81A1
    Session-ID-ctx:
    Resumption PSK: DB00585C44BE895BB3A30F14FBED205A6CB7C982E8FBFD30941AD4C8FBA5F27B61D846702CDD86B9189EA01A0001EE55
    PSK identity: None
    PSK identity hint: None
    SRP username: None
    TLS session ticket lifetime hint: 7200 (seconds)
    TLS session ticket:
    0000 - 54 69 c4 6e f3 66 e0 75-7a 50 7e a0 cf ab a2 bf   Ti.n.f.uzP~.....
    0010 - 8d 49 f0 8e 62 45 00 80-7b bc a3 bb 4e a2 95 10   .I..bE..{...N...
    0020 - 00 62 a6 04 f7 f0 5d ff-e4 79 2e 51 d2 42 5d ce   .b....]..y.Q.B].
    0030 - b0 f7 07 f4 2c 62 95 06-db a5 61 40 77 60 ab e2   ....,b....a@w`..
    0040 - 90 54 33 c9 74 d5 c8 d3-58 47 01 33 de d7 b8 15   .T3.t...XG.3....
    0050 - b3 48 78 7a cd 12 5b e5-08 b7 3a d1 f0 29 e2 48   .Hxz..[...:..).H
    0060 - 5b 19 cb f9 2e 89 c0 49-7f 1c fe ac f4 16 8d ce   [......I........
    0070 - 7c ed e5 f3 31 86 53 88-3a c8 76 72 b3 ca c0 d4   |...1.S.:.vr....
    0080 - 9a cd 73 30 0d 88 22 6d-21 6c e7 9d 4c 93 d6 13   ..s0.."m!l..L...
    0090 - 26 81 b4 92 38 45 4f 5b-48 ee 7c 3c fd d3 bd 38   &...8EO[H.|<...8
    00a0 - 37 f0 20 84 ad 51 50 25-af fc 60 27 a8 7c 6b f0   7. ..QP%..`'.|k.
    00b0 - e6 e8 28 1e b3 7c aa a4-9b 87 df 2d f4 b9 00 50   ..(..|.....-...P
    00c0 - 3c 56 d8 e7 5c bd 53 bc-26 da 20 38 7f 4a b2 e5   <V..\.S.&. 8.J..

    Start Time: 1683571873
    Timeout   : 7200 (sec)
    Verify return code: 10 (certificate has expired)
    Extended master secret: no
    Max Early Data: 0
---
read R BLOCK
Correct!
JQttfApK4SeyHwDlI9SXGR50qclOAil1

closed