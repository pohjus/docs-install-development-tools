# Setting Up Git with GitHub in WSL2 (Using SSH)

## Step 1: Install Git in WSL2

First, make sure Git is installed inside WSL2.

```bash
sudo apt update && sudo apt install git -y
```

Verify the installation:

```bash
git --version
```

---

## Step 2: Configure Git

Set up your Git username and email (must match your GitHub account):

```bash
git config --global user.name "Your Name"
git config --global user.email "your-email@example.com"
```

Confirm the configuration:

```bash
git config --list
```

---

## Step 3: Generate an SSH Key

Generate a new SSH key pair for authentication with GitHub.

```bash
ssh-keygen -t ed25519 -C "your-email@example.com"
```

- If you see `ssh-keygen: command not found`, install it:

  ```bash
  sudo apt install openssh-client -y
  ```

- When prompted for a file location, **press Enter** to accept the default (`~/.ssh/id_ed25519`).
- When prompted for a passphrase, either enter a secure passphrase (recommended) or leave it empty.

---

## Step 4: Start the SSH Agent

Start the SSH agent and add your new key:

```bash
eval "$(ssh-agent -s)"
ssh-add ~/.ssh/id_ed25519
```

---

## Step 5: Add Your SSH Key to GitHub

1. Copy the SSH public key to your clipboard:

   ```bash
   cat ~/.ssh/id_ed25519.pub
   ```

2. Open [GitHub SSH Key Settings](https://github.com/settings/keys).
3. Click **"New SSH key"**.
4. **Title**: Add a descriptive name (e.g., "WSL2 Machine").
5. **Key type**: Select `Authentication Key`.
6. **Key**: Paste the copied key.
7. Click **"Add SSH key"**.

---

## Step 6: Verify the Connection to GitHub

Test if SSH authentication works:

```bash
ssh -T git@github.com
```

You should see:

```
Hi your-username! You've successfully authenticated, but GitHub does not provide shell access.
```

If you see `Permission denied (publickey)`, ensure:

- The key was added to the SSH agent (`ssh-add -l` should list it).
- The key is correctly added to GitHub.

---

## Step 7: Add GitHub to Known Hosts (Optional but Recommended)

Check GitHub’s SSH fingerprints:

```bash
ssh-keyscan -t ed25519 github.com | tee -a ~/.ssh/known_hosts
```

Confirm the fingerprint matches one of these:

- **SHA256**: `SHA256:p2QAMXNIC1TJYWeIOttrVc98/R1BUFWu3/LiyKgUfQM`
- **MD5**: `MD5:3b:47:01:6c:1c:90:0e:9c:d8:75:32:54:42:8b:d5:2f`

---

## Step 8: Clone a Repository via SSH

Now you can clone repositories using SSH:

```bash
git clone git@github.com:your-username/your-repo.git
```

If cloning succeeds without asking for a password, SSH authentication is working.
