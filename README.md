### Sys1 WritesUp challenges

> [link](https://www.root-me.org/)

### FTP Authentification (5p points)

- analyze `Chap1.pcap` file
- follow the FTP traffic on Wireshark

```sh
USER ---------
331 Enter password.
PASS ********
230 -------- logged on.
```

### TELNET - authentication (5 Points)

- analyze `Chap2.pcap` file
- follow the TELNET traffic on Wireshark

```sh
........... ..!.."..'.....#..%..%........... ..!..".."........P. ....".....b........b....	B.
........................"......'.....#..&..&..$..&..&..$.. .....#.....'........... .9600,9600....#.bam.zing.org:0.0....'..DISPLAY.bam.zing.org:0.0......xterm-color.............!.............."............
OpenBSD/i386 (oof) (ttyp1)

login: .."........"ffaakkee
.
Password:****

Last login: Thu Dec  2 21:32:59 on ttyp1 from bam.zing.org
Warning: no Kerberos tickets issued.
OpenBSD 2.6-beta (OOF) #4: Tue Oct 12 20:42:32 CDT 1999

Welcome to OpenBSD: The proactively secure Unix-like operating system.

Please use the sendbug(1) utility to report bugs in the system.
Before reporting a bug, please try to reproduce it with the latest
version of the code.  With bug reports, please try to ensure that
enough information to reproduce the problem is enclosed, and if a
known fix for it exists, include that as well.

```

### ETHERNET - frame (10 Points)

1 . Convert the hexadecimal code to ASCII. at [rapidtables](https://www.rapidtables.com/convert/number/hex-to-ascii.html)

```sh

00 05 73 a0 00 00 e0 69 95 d8 5a 13 86 dd 60 00
00 00 00 9b 06 40 26 07 53 00 00 60 2a bc 00 00
00 00 ba de c0 de 20 01 41 d0 00 02 42 33 00 00
00 00 00 00 00 04 96 74 00 50 bc ea 7d b8 00 c1
d7 03 80 18 00 e1 cf a0 00 00 01 01 08 0a 09 3e
69 b9 17 a1 7e d3 47 45 54 20 2f 20 48 54 54 50
2f 31 2e 31 0d 0a 41 75 74 68 6f 72 69 7a 61 74
69 6f 6e 3a 20 42 61 73 69 63 20 59 32 39 75 5a
6d 6b 36 5a 47 56 75 64 47 6c 68 62 41 3d 3d 0d
0a 55 73 65 72 2d 41 67 65 6e 74 3a 20 49 6e 73
61 6e 65 42 72 6f 77 73 65 72 0d 0a 48 6f 73 74
3a 20 77 77 77 2e 6d 79 69 70 76 36 2e 6f 72 67
0d 0a 41 63 63 65 70 74 3a 20 2a 2f 2a 0d 0a 0d
0a

```

2 . Take the code base 64

> *******************==

3 . Go to Base64 decoding [Base64decode](https://www.base64decode.org/)

> PASSWORD : *****:*****

### Twitter authentication (15 Points)

analyze `Chap3.pcap` file
1 . follow the HTTP traffic on Wireshark

```sh
GET /statuses/replies.xml HTTP/1.1
User-Agent: CFNetwork/330
Cookie: _twitter_sess=BAh7CDoJdXNlcjA6B2lkIiVmZGQ2ODc5MTMwMWFhOTFiMWExZDViZmQwMGEz%250AOWNkMyIKZmxhc2hJQzonQWN0aW9uQ29udHJvbGxlcjo6Rmxhc2g6OkZsYXNo%250ASGFzaHsABjoKQHVzZWR7AA%253D%253D--ea12e7bc090d05202cd7e3f972c2b4414a97f657
Accept: */*
Accept-Language: en-us
Accept-Encoding: gzip, deflate
Authorization: Basic dXNlcnRlc3Q6cGFzc3dvcmQ=
Connection: keep-alive
Host: twitter.com
```

2 . Take the code base 64

> --------------------------=

3 . Go to Base64 decoding [Base64decode](https://www.base64decode.org/)

> PASSWORD : ---------------:-----------------

### Bluetooth - Unknown file (15 Points)

- analyze `ch18.bin` file

- Open the file in Wireshark, then click on Wireless > Bluetooth Devices > double-click on the first line.

```sh
BD_ADR  0c:b3:19:b9:4f:c6

OUI     SamsungE

NOM     GT-S7390G
```

The answer is the SHA1 hash of the concatenation of the MAC address (in uppercase) and the phone name.
</br>
Example:
AB:CD:EF:12:34:56myPhone -> *********************************************

> 0C:C3:19:B9:4F:C6GT-S7390G

Encrypt the following code at [SHA1](https://md5decrypt.net/)

> PASSWORD : -------------------------------
