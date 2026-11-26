# yazi

## installation

```bash
curl -fsSL https://yazi-rs.github.io/builds/yazi-keyring.gpg | sudo tee /usr/share/keyrings/yazi-keyring.gpg >/dev/null
echo 'deb [signed-by=/usr/share/keyrings/yazi-keyring.gpg] https://yazi-rs.github.io/builds/ stable main' | sudo tee /etc/apt/sources.list.d/yazi.list >/dev/null
sudo apt update && sudo apt install yazi
```

## flavors

### gruvbox dark

```bash
git clone git@github.com:bennyyip/gruvbox-dark.yazi.git ~/.config/yazi/flavors/gruvbox-dark.yazi
git clone https://github.com/dracula/yazi.git ~/.config/yazi/flavors/dracula.yazi
```
