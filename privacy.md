# Privacy

## UI packages

peazip: https://peazip.github.io/

## terminal

archive directory with encryption + file names encryption
```bash
7z a -t7z -mhe=on -p docs_archive.7z docs_archive_dir
````

unpack
```bash
7z x docs_archive.7z
```

test integrity
```bash
7z t docs_archive.7z
```

list files
```bash
7z l docs_archive.7z
```
