# CORTEX OS — Nitrokey SSH Setup Guide

Hardware-backed SSH authentication for your CORTEX dropbox.

## What You Need

A **Nitrokey 3** hardware security key. Order one here:

| Model | Connector | Link |
|-------|-----------|------|
| Nitrokey 3A Mini | USB-A | https://shop.nitrokey.com/shop/nk3am-nitrokey-3a-mini-116 |
| Nitrokey 3A | USB-A | https://shop.nitrokey.com/shop/nk3a-nitrokey-3a-147 |
| Nitrokey 3C | USB-C | https://shop.nitrokey.com/shop/nk3cn-nitrokey-3c-nfc-148 |
| Nitrokey 3C NFC | USB-C + NFC | https://shop.nitrokey.com/shop/nk3cn-nitrokey-3c-nfc-148 |

> Recommended: **Nitrokey 3C NFC** if your machine has USB-C, **Nitrokey 3A Mini** if USB-A. Both work identically for SSH.

## Why Hardware Keys

- Your private SSH key lives **on the device**, not on your laptop
- Even if your laptop is compromised, nobody can steal the key
- Every SSH connection requires the physical key plugged in + your PIN
- No passwords to remember or leak — just plug in and enter your PIN
- Works with any operating system (macOS, Windows, Linux)
- Open-source firmware, made in Germany

---

## macOS

### 1. Install tools

```bash
brew install gnupg pinentry-mac
```

### 2. Configure GPG for macOS

```bash
mkdir -p ~/.gnupg
cat > ~/.gnupg/gpg-agent.conf << 'EOF'
pinentry-program /opt/homebrew/bin/pinentry-mac
enable-ssh-support
default-cache-ttl 600
max-cache-ttl 7200
EOF
gpgconf --kill gpg-agent
```

### 3. Plug in Nitrokey and verify

```bash
gpg --card-status
```

You should see `Nitrokey Nitrokey 3` as the reader.

### 4. Change default PINs

**Default PINs (change immediately):**
- User PIN: `123456` (you type this for every SSH/sign operation)
- Admin PIN: `12345678` (for card management only)

```bash
gpg --card-edit
```

Then inside the prompt:

```
admin
passwd
```

- Pick `3` → Change Admin PIN (old: `12345678`, new: your choice, min 8 chars)
- Pick `1` → Change User PIN (old: `123456`, new: your choice, min 6 chars)
- Type `q` to exit passwd menu

### 5. Set your name

Still in `gpg --card-edit`:

```
name
```

- Surname: your last name
- Given name: your first name

### 6. Switch to Ed25519 keys

```
key-attr
```

It asks 3 times (Sign, Encrypt, Auth). Each time pick:
- `2` (ECC)
- `1` (Curve 25519)

Enter your admin PIN when asked.

### 7. Generate keys on the device

```
generate
```

- Off-card backup? → `n` (key stays hardware-only)
- Validity → `0` (never expires), confirm → `y`
- Name → your full name
- Email → your email
- Comment → press Enter (empty)
- Confirm → `O`

Then:

```
quit
```

### 8. Export your SSH public key

```bash
gpg --export-ssh-key YOUR_EMAIL > ~/.ssh/id_nitrokey.pub
cat ~/.ssh/id_nitrokey.pub
```

**Send this public key to Tarek.** He will add it to your CORTEX dropbox container.

### 9. Configure SSH to use Nitrokey

Add to your `~/.bashrc` or `~/.zshrc`:

```bash
export SSH_AUTH_SOCK=$(gpgconf --list-dirs agent-ssh-socket)
gpgconf --launch gpg-agent
```

Then reload:

```bash
source ~/.zshrc
```

### 10. Test SSH to your dropbox

```bash
ssh -p YOUR_PORT worker@VPS_IP
```

A macOS popup asks for your Nitrokey PIN. Enter it → you're in.

---

## Windows

### 1. Install tools

Download and install:
- [Gpg4win](https://gpg4win.org/) (includes GPG + Kleopatra)
- [PuTTY](https://putty.org/) or use Windows OpenSSH

### 2. Plug in Nitrokey and verify

Open a terminal (cmd or PowerShell):

```
gpg --card-status
```

### 3. Follow steps 4–8 above

Same commands work in Windows terminal.

### 4. Configure SSH

For Windows OpenSSH, add to your environment:

```
set SSH_AUTH_SOCK=\\.\pipe\gnupg-ssh
```

Or use Kleopatra (GUI) to manage the key.

---

## Linux

### 1. Install tools

```bash
# Debian/Ubuntu
sudo apt install gnupg2 scdaemon pcscd

# Start smartcard daemon
sudo systemctl enable pcscd
sudo systemctl start pcscd
```

### 2. Configure GPG

```bash
mkdir -p ~/.gnupg
cat > ~/.gnupg/gpg-agent.conf << 'EOF'
enable-ssh-support
default-cache-ttl 600
max-cache-ttl 7200
EOF
gpgconf --kill gpg-agent
```

### 3. Follow steps 3–8 from macOS section

Same GPG commands.

### 4. Configure SSH

Add to `~/.bashrc`:

```bash
export SSH_AUTH_SOCK=$(gpgconf --list-dirs agent-ssh-socket)
gpgconf --launch gpg-agent
```

---

## After Setup

Send your SSH public key (from step 8) to **cortex-labs.xyz@proton.me** or to Tarek directly via WhatsApp or Signal. He will add it to your CORTEX container. After that, SSH works with your Nitrokey — no password needed.

**How it works**: Private key never leaves the Nitrokey. Every SSH connection requires the physical device plugged in + your PIN. Even if your laptop is compromised, nobody can steal the key.

---

## Troubleshooting

| Problem | Fix |
|---------|-----|
| `No card` | Plug in Nitrokey, run `gpg --card-status` |
| `PIN blocked` | Use admin PIN to unblock: `gpg --card-edit` → `admin` → `passwd` → option `2` |
| `ssh: no identity` | Check `ssh-add -l` — should show the Nitrokey key. If empty: `export SSH_AUTH_SOCK=$(gpgconf --list-dirs agent-ssh-socket)` |
| `Permission denied` | Your public key hasn't been added to the container yet — email cortex-labs.xyz@proton.me |
| PIN popup doesn't appear | macOS: check `pinentry-mac` is installed. Linux: check `gpg-agent` is running |

---

## More About Nitrokey

- Website: https://www.nitrokey.com
- Shop: https://shop.nitrokey.com
- Documentation: https://docs.nitrokey.com/nitrokey3
- Firmware (open-source): https://github.com/Nitrokey/nitrokey-3-firmware
- Made in Berlin, Germany. Open-source hardware and firmware.
