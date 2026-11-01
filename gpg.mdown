# GPG

## encrypt

```bash
gpg -r recipient@gmail.com -e file_to_encrypt.txt
gpg --recipient recipient@gmail.com --encrypt file_to_encrypt.txt
```

## decrypt

```bash
gpg -d file_to_decrypt.txt.gpg
gpg --decrypt file_to_decrypt.txt.gpg
```

## list keys

```bash
gpg --list-keys
```
