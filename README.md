# hashcompare
hashcompare helps you compare a file with a given checksum. It works with MD5 (by default), SHA-1, SHA-256 and SHA-512.

## Usage
```
hashcompare FILE HASH [OPTIONS]

Options:
-5, --md5           MD5 (default)
-1, --sha1          SHA1
-256, --sha256      SHA256
-512, --sha512      SHA512
--help              Displays help message
```

## Examples

```
ali@zion:~$ hashcompare /usr/bin/hashcompare 8eb8c7875adfa943c9a900d1da16f3a3
True. Checksums matched.
ali@zion:~$ hashcompare /usr/bin/hashcompare 8eb8c7875adfa943c9a900d1da16f3a3 --md5
True. Checksums matched.
ali@zion:~$ hashcompare /usr/bin/hashcompare 8eb8c7875adfa12345a900d1da16f3a3 --md5
False. Checksums did not match.
```