# show last 50 logs from docker container

```bash
docker logs haproxy-dw --tail 50
```

# generate random chain of characters

```bash
tr -dc 'a-zA-Z0-9' < /dev/urandom | head -c {numberOfCharacters}
```

# konfigruacja programów w linuxie

```bash
/usr/share/applications/*.desktop
~/.share/local/applications/*.desktop
```

# czytanie logów tail

```bash
tail -f [File] -s [seconds to refresh]
```
