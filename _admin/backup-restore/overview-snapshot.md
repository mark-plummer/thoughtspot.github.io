---
title: [Work with snapshots]
last_updated: 12/9/2020
toc: true
redirect_from:
- /7.0.0.mar.sw/admin/backup-restore/overview-snapshot.html
- /7.0.1.jun.sw/admin/backup-restore/overview-snapshot.html
summary: "A snapshot is a point-in-time image of your running cluster. You can use a snapshot to restore the cluster to a specific point in time. In this section, we describe how to work with the default snapshot configuration that is enabled on every cluster, and how to make manual snapshots."
sidebar: mydoc_sidebar
permalink: /:collection/:path.html
---
To work with snapshots, use the `tscli` command line interface.

{% include warning.html content="Backups rely on the snapshot system, so you must never disable the periodic snapshot system. If you disable periodic snapshots and enable periodic backups, the backups either fail or use an outdated snapshot." %}

{: id="manual-snapshot"}
## About manual snapshots

You must create a snapshot [through the Admin Console](#admin-portal-create) or [using tscli](#snapshot-tscli) before making any changes to your cluster's environment, loading a large amount of data, or changing the structure of a table. ThoughtSpot supports up to 20 manual snapshots. You must clear them to create new snapshots. You can delete a snapshot [from the Admin Console](#admin-portal-delete).

ThughtSpot generates a snapshot in approximately 20 seconds, depending on the size of the cluster. To restore from a snapshot, contact [ThoughtSpot Support]({{ site.baseurl }}/admin/misc/contact.html#).

{% include note.html content="During an upgrade, all snapshots from the previous version of ThoughtSpot become manual snapshots." %}

{% include content/admin-portal/snapshot-manage.md %}

{: id="snapshot-tscli"}
## Create a snapshot using tscli

To create a snapshot using `tscli`, follow these steps:

1. Log in to the Linux shell using SSH.

2. Create a snapshot with the command `tscli snapshot create`, specifying the following parameters:

    * `name`: Specify a name for the snapshot. Note that snapshot names must not exceed 44 characters.
    * `reason`: Specify a reason for creating the snapshot.
    * `ttl`: Specify the snapshot's time to live, in days. If you specify `ttl` as `4`, the system deletes the snapshot after four days.

    ```
    $ tscli snapshot create <name> <reason> <ttl>
    ```

3. Check that the snapshot was created successfully by checking the directory listing:

    ```
    $ tscli snapshot ls
    ```
    Your snapshot should appear in the list of snapshots that `tscli snapshot ls` generates.

{: id="snapshot-policy"}
## Configure periodic snapshots with snapshot policy

Each ThoughtSpot cluster automatically creates periodic snapshots, based on its default snapshot policy.
The default snapshot policy is enabled for every cluster. You can display the current policy for periodic snapshots.
You can also change this policy.

{: id="snapshot-policy-view"}
### View snapshot policy

To view your current periodic snapshot policy, follow these steps:

1. Log in to the Linux shell using SSH.

    ```
    $ ssh admin@<cluster-IP>
    ```

2. Enter `tscli snapshot-policy show <name>` command to view the policy.

In the following example, the policy starts at midnight on Sunday. It retains the snapshots from the previous three 4-hour intervals, and two snapshots from two of the previous 4-hour
intervals. Here, ThoughtSpot retains 7 periodic snapshots overall. For
detailed information about understanding the schedule, see [Understand
backup/snapshot schedules](how-to-create-a-schedule.html).  

```
$ tscli snapshot-policy show
schedule {
  period {
    number: 1
    unit: HOUR
  }
  retention_policy {
    bucket {
      time {
        number: 1
        unit: HOUR
      }
      capacity: 3
    }
    bucket {
      time {
        number: 4
        unit: HOUR
      }
      capacity: 4
    }
    bucket {
      time {
        number: 1
        unit: DAY
      }
      capacity: 4
    }
    bucket {
      time {
        number: 1
        unit: WEEK
      }
      capacity: 2
    }
  }
  offset_minutes_from_sunday_midnight: 0
}
enabled: true

```

{: id="snapshot-policy-update"}
### Update the snapshot policy

Do not change the default policy, unless it is recommended by [ThoughtSpot Support]({{ site.baseurl }}/admin/misc/contact.html#).

{% include note.html content="Your policy must hold no more than 20 snapshots at any time. Exceeding this number impacts cluster performance." %}

To update your current periodic snapshot policy, follow these steps:
1. Log in to the Linux shell using SSH.
    ```
    $ ssh admin@<cluster-IP>
    ```
2. Enter `tscli snapshot-policy update`.
    ```
    $ tscli snapshot-policy update
    ```
3. In the editor, make changes to the current policy, and save them.

You cannot delete the snapshot policy. However, you can either disable or enable it.

{: id="snapshot-policy-dispable"}
### Disable the snapshot policy

To disable your current periodic snapshot policy, follow these steps:

1. Log in to the Linux shell using SSH.
    ```
    $ ssh admin@<cluster-IP>
    ```
2. Enter `tscli snapshot-policy disable`.
    ```
    $ tscli snapshot-policy disable
    ```

{: id="snapshot-policy-enable"}
### Enable the snapshot policy

To enable a specific periodic snapshot policy, follow these steps:  

1. Log in to the Linux shell using SSH.
    ```
    $ ssh admin@<cluster-IP>
    ```
2. Enter `tscli snapshot-policy enable`.
    ```
    $ tscli snapshot-policy disable
    ```
