# Cocoon

A personal workstation setup for Umbrel baked with cloud-init

## Usage

1. Launch an OrbStack machine (or any Debian-based VM)
2. Point it at `setup.yml` as cloud-init userdata
3. Wait for first boot to finish

## After first boot

```bash
# Authenticate with GitHub
gh auth login

# Upload keys to GitHub
gh ssh-key add /root/.ssh/id_ed25519.pub
gh gpg-key add <(gpg --armor --export jonathanirhodia@gmail.com)
```

## Updating Umbrel

```bash
/usr/local/bin/update-os
```

This pulls the latest Umbrel and dockur patches, rebuilds, and restarts the daemon.
