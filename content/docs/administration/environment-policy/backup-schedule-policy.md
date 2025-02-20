---
title: Backup Schedule Policy
feature_name: BACKUP_POLICY
---

<HintBlock type="info">

The backup enforcement is **NOT retroactive**, which means the updated policy **won't** automatically alter the existing database backup setting, it will only enforce the future setup. On the other hand, Bytebase will report the discrepancy if the current setting does not conform to the active policy , which gives user the control to switch the existing setting at the appropriate time.

</HintBlock>

`Owner` or `DBA` can configure the backup schedule policy for a particular environment from the "Environment" detail page:

![env-backup-configure](/content/docs/disaster-recovery/backup/env-backup-configure.webp)

## Detect missing backup

Once policy is enforced, Bytebase will detect and report the missing backup according to the policy.

![database-overview](/content/docs/database-overview.png)

## Lock backup schedule

Backup policy will also prevent user changing to a non-conforming backup schedule.

![database-backup](/content/docs/disaster-recovery/backup/database-backup.webp)
