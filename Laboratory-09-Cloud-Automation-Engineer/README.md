# Laboratory 09 - Cloud Automation Engineer

## Mission Overview

This laboratory introduces cloud automation using Bash scripting and Cron scheduling in Linux. The activity focuses on creating an automated backup script, managing file permissions, compressing important client data, and scheduling backups to run automatically.

## Objectives

- Understand Bash scripting, variables, and Cron jobs.
- Create a sample folder containing client data.
- Write a Bash script to automate file backups.
- Understand and modify Linux file permissions.
- Execute and verify an automated backup script.
- Create a scheduled task using Cron.
- Document the backup process and automation commands.

## Commands Executed

```bash
mkdir app-data
echo "This is critical client data." > app-data/data.txt
nano backup.sh
./backup.sh
chmod +x backup.sh
./backup.sh
ls -l backups/
crontab -l
env EDITOR=nano crontab -e
crontab -l
```

## Skills Learned

- Understanding Linux Bash scripts
- Using variables in automation
- Creating and editing scripts with nano
- Managing file permissions using chmod
- Automating backups using tar
- Working with compressed backup files
- Scheduling recurring tasks using Cron
- Verifying automated processes
- Documenting cloud automation workflows
