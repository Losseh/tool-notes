# updates

```bash
# update apt, snap, cargo packages
echo "-- updating apt packages"
sudo apt update
sudo apt upgrade
echo "-- updating snap packages"
sudo snap refresh
echo "-- updating cargo packages"
cargo install-update -a
```

## cargo

```bash
# install cargo updater and its deps
sudo apt update
sudo apt install pkg-config libssl-dev build-essential
cargo install cargo-update
```

```bash
# Update all installed packages
cargo install-update -a

# Check which packages have updates
cargo install-update -l

# Update a specific package
cargo install-update package_name
```

## snap

```bash
sudo snap refresh
```
