# 🌀 Git Repository Synchronizer

A simple **Bash script** to keep two Git repositories in sync — ideal for mirroring git history between hosts like **GitHub ↔ GitLab**, or any two remote repositories that share the same project.

This tool pulls the latest changes from one repo and pushes them to the other — perfect for backups, migration workflows, or multi-platform mirroring.

---

## Features

- 🔄 **Bidirectional syncing**: Pull from one repo and push to the other  
- 📦 **Zero dependencies**: Written in portable Bash  
- 🌍 **Host-agnostic**: Works with GitHub, GitLab, Bitbucket, or any Git remote  
- ✔️ **Easy setup**: Just configure your repository URLs and run  
- 📜 **MIT-licensed**

---

## 💡 How It Works

The script:

1. Clones each repository locally (if not already present)
2. Fetches the latest commits from both repositories
3. Fast-forwards one repository into the other
4. Pushes the synchronized history back to both remotes

This ensures both repositories stay up-to-date with each other.

---

## 🛠️ Setup

1. **Edit the script**

   Open `synchronize_two_git_repo.sh` and set your repositories:

   ```bash
   REPO_A="git@github.com:you/repo-a.git"
   REPO_B="git@gitlab.com:you/repo-b.git"
   ```
Make the script executable

```sh
chmod +x synchronize_two_git_repo.sh
```
Run the script
```sh
./synchronize_two_git_repo.sh
```
### Typical Use Cases
Mirror GitHub ↔ GitLab repositories

Maintain off-site backups of your code

Synchronize distributed mirrors

Automate syncing with cron or CI pipelines

### 📦 Requirements
Git installed and available in PATH

SSH or HTTPS access to both repositories

A system capable of running Bash scripts

### ⚠️ Important Notes
Both repositories must share a common history

Concurrent development on both repos may cause conflicts

For advanced workflows, manual conflict resolution may be required

#### 🧹 License
MIT License — free to use, modify, and distribute.
