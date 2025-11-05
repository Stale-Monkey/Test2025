Perfect 👌 here’s the **clean, official-style version** starting **from Git configuration onward**, formatted like **GitHub documentation**, short, sharp, and ready to use 👇

---

# ⚙️ Configure Git & GitHub (Official Setup)

## 1. Configure Git Identity

Set your username and email — this links your commits to your GitHub account.

```bash
git config --global user.name "Your Name"
git config --global user.email yourname@example.com
```

> 💡 If you’ve enabled *“Keep my email addresses private”* in GitHub, use your **GitHub-provided private email**:
>
> ```bash
> git config --global user.email 123456789+username@users.noreply.github.com
> ```

---

## 2. Set Default Branch & Pull Behavior

Change default branch name from `master` → `main`:

```bash
git config --global init.defaultBranch main
```

Set default pull behavior (recommended):

```bash
git config --global pull.rebase false
```

Verify settings:

```bash
git config --get user.name
git config --get user.email
```

---

## 3. Create an SSH Key (for GitHub Authentication)

### 3.1 Check for Existing Key

```bash
ls ~/.ssh/id_ed25519.pub
```

If you see “No such file or directory”, continue to create one.

### 3.2 Generate a New SSH Key

```bash
ssh-keygen -t ed25519
```

Press **Enter** to accept the default file location.
You can optionally add a passphrase for extra security.

### 3.3 Copy Your Public Key

```bash
cat ~/.ssh/id_ed25519.pub
```

Copy the full output — it starts with `ssh-ed25519` and ends with your username.

---

## 4. Add SSH Key to GitHub

1. Go to **GitHub → Settings → SSH and GPG Keys**
2. Click **New SSH Key**
3. Enter a title (e.g., `ubuntu-laptop` or `macbook`)
4. Paste your key
5. Click **Add SSH Key**

---

## 5. Test SSH Connection

Run:

```bash
ssh -T git@github.com
```

Expected output:

```
Hi username! You’ve successfully authenticated, but GitHub does not provide shell access.
```

> ✅ If you see this, your SSH key is correctly configured.

---

## ✅ Summary

You’ve successfully:

* Linked your local Git to GitHub identity
* Set default branch behavior
* Created and added an SSH key
* Verified secure authentication

Next step: initialize a repo and start committing 🚀

```bash
git init
```

---

Would you like me to make this into a **GitHub Docs-style PDF** (with syntax highlighting, logo, and section headers)?
