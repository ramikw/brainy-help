# Automatic Backups

Brainy automatically creates regular backups of your entire database to protect against data loss.

## How Backups Work

### Backup Location
- Backups are stored in the folder named after your username, inside your database directory
- By default, the database directory is your app settings directory

### Backup Naming
- Each backup is named by date and time (e.g., `2026_05_01_19_44_45.backup`)
- The date helps you identify when each backup was created
- Multiple backups accumulate over time

## Restoring from a Backup

If something goes wrong and you need to restore from a backup:

### Steps to Restore

1. **Close Brainy** — Exit the application completely

2. **Navigate to Database Directory** — Locate your backups
   - Go to where your database files are stored — by default, this is your app settings directory
   - Open the folder named after your username
   - Backup files are named by date and time (e.g., `2026_05_01_19_44_45.backup`)

3. **Select Your Backup** — Choose which backup to restore from
   - Pick the timestamp closest to when you last had good data

4. **Prepare for Restore**
   - Delete or rename the current `brainy.db` file (save it elsewhere as a safety measure)
   - Rename your chosen backup file to `brainy.db`

5. **Restart Brainy** — Open the application
   - It will load data from the restored backup

### Example
```
Original:  2026_05_01_19_44_45.backup
Restore:   brainy.db
```

## Best Practices

- ✅ Enable auto-sync to keep cloud copies of your data
- ✅ Periodically backup your database directory to external storage
- ✅ Note the timestamps of your most important backups
- ⚠️ Always keep the current `brainy.db` file as a safety measure before testing restores
