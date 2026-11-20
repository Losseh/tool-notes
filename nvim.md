# nvim.md

## installation

```bash
sudo add-apt-repository ppa:neovim-ppa/unstable
sudo apt update
sudo apt install neovim
```

## tree-sitter

for syntax recognition

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

## pluginy do javy

```bash
nvim-java
spring-boot.nvim
nvim-dap
nui.nvim
blink.cmp
telescope.nvim
plenary.nvim
oil.nvim
which-key.nvim
```

## ~/.config/nvim/init.lua

```bash
vim.g.have_nerd_font = true
```
