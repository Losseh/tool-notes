# zellij

## rust

```bash
curl --proto '=https' --tlsv1.2 -sSf https://sh.rustup.rs | sh
```

update

```bash
rustup update stable
rustup default stable
rustc --version
```

## installation

```bash
# this also updates zellij
cargo install --locked zellij
zellij --version
# in case of compilation errors
rustup update
cargo install --locked zellij
# install without compilation 
cargo install cargo-binstall
cargo binstall zellij
```

## desktop entry

```bash
zellij setup --install-desktop-entry
```
