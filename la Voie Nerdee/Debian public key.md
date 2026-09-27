[[Debian]] uses different public keys to sign the Debian images:

## 🔑 The one you'll probably need

![[key-DA87E80D6294BE9B.txt]]
```
Key fingerprint = DF9B 9C49 EAA9 2984 3258  9D76 DA87 E80D 6294 BE9B
pub   rsa4096/DA87E80D6294BE9B 2011-01-05 [SC]
uid   Debian CD signing key debian-cd@lists.debian.org
```

## 🔐 The testing one
![[key-42468F4009EA8AC3.txt]]
```
Key fingerprint = F41D 3034 2F35 4669 5F65  C669 4246 8F40 09EA 8AC3
pub   rsa4096/42468F4009EA8AC3 2014-04-15 [SC]
uid   Debian Testing CDs Automatic Signing Key debian-cd@lists.debian.org
```

## 🗝️ The ancient one

![[key-988021A964E6EA7D.txt]]
```
Key fingerprint = 1046 0DAD 7616 5AD8 1FBC  0CE9 9880 21A9 64E6 EA7D
pub   rsa4096/988021A964E6EA7D 2009-10-03
uid   Debian CD signing key debian-cd@lists.debian.org
```

[SC] stands for *Sign and Certify* - keys that have this remark are used for signing modern Debian images





[^1]: Sources:
		https://www.debian.org/CD/verify
