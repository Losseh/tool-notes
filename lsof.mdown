# lsof

## list all processes that LISTEN on what ports

```bash
sudo lsof -i -P -n | grep LISTEN
```

## what process used specific port
```bash
sudo lsof -i :8080
```

