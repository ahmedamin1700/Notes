---
id: 1733477276-vault-backup
aliases:
  - Vault Backup
tags:
  - workplace
---

# Vault Backup

to automate the process of committing the changes in the notes and pushing the repo.

```bash
#!/bin/bash

# Navigate to the repository directory
cd /path/to/your/repo || exit

# Generate the timestamp
timestamp=$(date '+%Y-%m-%d %H:%M:%S')

# Stage all changes
git add .

# Commit with a timestamped message
git commit -m "vault backup: $timestamp"

# Push changes to the remote repository
git push
```

finally add the below lines
open the cron editor:

```
crontab -e
```
```
0 * * * * /path/to/vault_backup.sh >> /path/to/vault_backup.log 2>&1
```
