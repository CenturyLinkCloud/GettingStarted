{{{
  "title": "Server Snapshot",
  "date": "03-18-2015",
  "author": "",
  "attachments": [],
  "related_products": [],
  "related_questions": [],
  "preview" : "",
  "contentIsHTML": false
}}}

Snapshots allow a server to be quickly reverted back to a set point in time. This can be very useful if you want to perform a short term test or configuration changes. However, due to the way that snapshots operate, a snapshot is not a backup of a machine and there is a 10 day max life of a snapshot.

1. Once you've navigated to the server you'd like to snapshot, select **snapshot** from the **actions** drop down in the power bar.

  ![The Snapshot button in the Control Portal](../images/servers-snapshot-1.png)

2. A dialog will appear where you'll need to select the number of days you wish to retain the snapshot. If a snapshot already exists, it will be replaced by the new snapshot &mdash; a server can only have a single snapshot at a time.

  ![The Snapshot button in the Control Portal](../images/servers-snapshot-2.png)

3. Select the **create snapshot** button in the dialog window, and the snapshot will be queued.

4. Once the snapshot has been taken, it will appear in the **Server Info** column on the right side of the server status page. The name of the snapshot reflects the date and time the snapshot was taken.

  ![An existing server snapshot in the Control Portal](../images/servers-snapshot-3.png)

5. To restore the snapshot, select the snapshot name. A **Restore From Snapshot** dialog window. Clicking the Restore from Snapshot will redirect you to the Restore Snapshot Queue page where the snapshot will be applied. Once the restore process is complete, your server will be available it will appear in the group that you originally selected it be placed.

  ![Restore a snapshot in the Control Portal](../images/servers-snapshot-4.png)

6. Congratulations, you've just taken and restored a server snapshot!
