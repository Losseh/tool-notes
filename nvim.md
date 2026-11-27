# nvim.md

## shortcuts

### space - search

- '/' - fuzzy search
- s - files

### z - folding

- `za` - toggles the fold under the cursor
- `zM` - closes all folds
- `zR` - opens all folds

### commands

general structure: `range` `command`

#### full buffer - `%`

`:%!cmd`, e.g.:

- `:%!jq .` - pretty prints the json file
- `:%!js -c .` - minifies a json file
- `:%!jq '.items[0]'` replaces the buffer with one part of the file.

#### specific ranges

- `:10,20!sort` - sort lines from 10 to 20 (both included)
- `:10,20!sort | uniq` - sort lines and remove duplicates from 10 to 20 (both included)

#### visual selection range

- `:'<,'>!cmd` -  filters only the selected lines.

### buffers navifagation - ctrl + w

- w - next buffer
- s - split window
- v - vsplit window

### macros

1. q - start recording
2. macro name, e.g. 1
3. do steps
4. q - stop recording

### font resizing

`set guifont=Source Code Pro,DejaVu Sans Mono,Courier New,monospace:h10`

## installation

```bash
sudo add-apt-repository ppa:neovim-ppa/unstable
sudo apt update
sudo apt install neovim
```

## tree-sitter

for syntax recognition

### tree-sitter installation

#### with cargo

```bash
cargo install tree-sitter-cli
```

#### from zip

```bash
curl -L https://github.com/tree-sitter/tree-sitter/releases/download/v0.27.2/tree-sitter-cli-linux-x64.zip \
  -o /tmp/tree-sitter.zip
unzip -o /tmp/tree-sitter.zip -d ~/.local/bin
chmod +x ~/.local/bin/tree-sitter
```

## markdown lint

```bash
npm i -g markdownlint-cli
```

## kickstart

```bash
git clone https://github.com/nvim-lua/kickstart.nvim.git "${XDG_CONFIG_HOME:-$HOME/.config}"/nvim
```
