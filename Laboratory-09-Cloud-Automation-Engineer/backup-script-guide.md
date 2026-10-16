# Backup Script Guide

## Overview

This guide explains how a Bash script can automate the backup of client data and how Cron can schedule the script to run every day.

## Full Bash Backup Script

```bash
#!/bin/bash
# Automated Backup Script for CloudNova Technologies

SOURCE_DIR="app-data"
BACKUP_DIR="backups"
TIMESTAMP=$(date +"%Y%m%d_%H%M%S")

echo "Initiating automated backup..."

# Create the backup directory if it does not exist
mkdir -p "$BACKUP_DIR"

# Compress the source directory into a tarball (.tar.gz)
tar -czf "$BACKUP_DIR/backup_$TIMESTAMP.tar.gz" "$SOURCE_DIR"

echo "Backup completed successfully at $TIMESTAMP!"
```

## File Permissions

Command:

```bash
chmod +x backup.sh
```

The `chmod +x` command adds execute permission to the `backup.sh` file, allowing Linux to run the script directly as a program.

## Executing the Backup

Command:

```bash
./backup.sh
```

This command executes the backup script and creates a compressed archive of the `app-data` directory.

## Verifying the Backup

Command:

```bash
ls -l backups/
```

This command lists the contents of the backup directory to verify that a `.tar.gz` file was created.

## Cron Job Schedule

Cron expression:

```cron
0 2 * * * /root/backup.sh
```

| Field | Value | Meaning |
|---|---|---|
| Minute | 0 | At minute 0 |
| Hour | 2 | At 2:00 AM |
| Day of Month | * | Every day of the month |
| Month | * | Every month |
| Day of Week | * | Every day of the week |

This schedule runs the backup script every day at 2:00 AM according to the server's configured timezone.

## Important Note About Cron

The provided script uses relative paths, so the scheduled job must run from the correct working directory. If the data and script are located in `/root`, a more reliable cron command is:

```cron
0 2 * * * cd /root && /root/backup.sh
```

This ensures that the script accesses `/root/app-data` and stores its backups in `/root/backups`.
