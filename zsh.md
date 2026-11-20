# zsh

## installation

```bash
sudo apt install zsh
```

## oh-my-zsh

https://github.com/ohmyzsh/ohmyzsh

```bash
sh -c "$(curl -fsSL https://raw.githubusercontent.com/ohmyzsh/ohmyzsh/master/tools/install.sh)"
```

## customization

```bash
sudo apt install \
  zsh-autosuggestions \
  zsh-syntax-highlighting \
  zsh-completions
```

```bash
~/.zshrc:
# Autocompletion
autoload -Uz compinit
compinit
```

```bash
# Autosuggestions
source /usr/share/zsh-autosuggestions/zsh-autosuggestions.zsh

# Syntax highlighting
source /usr/share/zsh-syntax-highlighting/zsh-syntax-highlighting.zsh
```
