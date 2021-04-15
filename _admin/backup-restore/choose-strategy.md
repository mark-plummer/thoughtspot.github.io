---
title: [Understand the backup strategies]
last_updated: 10/14/2019
summary: "Consider the strategies for backing up your ThoughtSpot cluster."
sidebar: mydoc_sidebar
permalink: /:collection/:path.html
---
{: id="snapshots"}
## Snapshots

A snapshot is a point-in-time image of your running cluster. Snapshots are both taken on and restored to a cluster while it is running. Each cluster has a periodic snapshot configuration enabled by default. This configuration instructs the system to periodically take snapshots. Creation of a snapshot takes about 20 seconds. After creation, a snapshot persists on disk in the cluster's HDFS.

You can also create a snapshot manually. You should create a snapshot before making any changes to the environment, loading a large amount of new data, or changing the structure of a table. A snapshot may only be restored to the same cluster on which it was taken. The cluster software release version must match the snapshot release version.

If you need to move data between clusters or restore to a cluster that was updated to a new release, contact ThoughtSpot Support.

{: id="backups"}
## Backups

A backup is a procedure that stores a snapshot outside of a ThoughtSpot cluster. Backups are stored in a directory on a local or network file system. You can store all of the data associated with a snapshot or a portion of that data or only metadata. There is no default configuration enabled for backing up a cluster. You can configure on yourself or you can take backups manually. Backing up periodically protects your company from losing data and/or user work.

You can use a backup to restore a cluster to a prior state, a differently configured appliance, or move the backup from an appliance to a virtual cluster or vice versa.

{: id="offline-backups"}
## Offline backup cluster

The most robust strategy for backup and recovery requires having a backup cluster offline that is kept in sync with the production cluster. Then, if the production cluster fails, the backup cluster can be drafted to take its place with minimal loss of work and disruption to operations.

Details on this architecture, and instructions on setting it up, are available in the [ThoughtSpot Disaster Recovery Guide]({{ site.baseurl }}/disaster-recovery/about-disaster-recovery.html).

{: id="choose-strategy"}
## Choosing a strategy

Depending on your situation and your goals, you can choose to use either a snapshot or a backup. This table should help you decide:

<table>
<colgroup>
<col width="16%" />
<col width="42%" />
<col width="42%" />
</colgroup>
                <tr>
                    <td/>
                    <td><strong>Snapshot</strong></td>
                    <td><strong>Backup</strong></td>
                </tr>
                <tr id="purpose">
                    <td><strong>Purpose</strong></td>
                    <td>Restore to a cluster to particular point in time.</td>
                    <td>
                        <ul>
                            <li>Restore a cluster to a prior state.</li>
                            <li>Move a cluster to a different appliance.</li>
                            <li>Move a cluster to VM appliance.</li>
                            <li>Removing a node.</li>
                            <li>Restoring to a cluster that runs a different release from the one where the backup was taken.</li>
                        </ul>
                    </td>
                </tr>
                <tr id="storage">
                    <td><strong>Storage</strong></td>
                    <td>In the cluster's HDFS</td>
                    <td>Outside the cluster on either local or NAS disk.</td>
                </tr>
                <tr id="advantages">
                    <td><strong>Advantages</strong></td>
                    <td>
                        <ul>
                            <li>Can be taken on, or restored to, a running cluster</li>
                            <li>Fastest create and restore</li>
                        </ul>
                    </td>
                    <td>
                        <ul>
                            <li>Very stable.</li>
                            <li>Can be used to recover from data loss or corruption, even if the cluster is destroyed.</li>
                            <li>Can be typed as <em>full</em>, <em>lightweight</em>, or <em>dataless</em>.</li>
                        </ul>
                    </td>
                </tr>
                <tr id="limitations">
                    <td><strong>Limitations</strong></td>
                    <td>
                        <ul>
                            <li>Include all data, state, and metadata created between
                                snapshot create and restore.</li>
                            <li>Lost if the HDFS name node fails, if you lose multiple disks, or if the entire cluster is destroyed</li>
                            <li>Can be restored only to the cluster were they are taken</li>
                        </ul>
                    </td>
                    <td>
                        <ul>
                            <li>Require deleting the existing cluster first.</li>
                            <li>You are responsible for validating your backup configuration as
                                viable for restoring a cluster.</li>
                            <li>Best practice recommends you to maintain multiple backups.</li>
                            <li>Typically, very large in memory size.</li>
                        </ul>
                    </td>
                </tr>
            </table>


You should never restore from a snapshot or backup yourself. Contact ThoughtSpot Support for help.

## Additional resources
As you develop your expertise in snapshots and backups, we recommend the following ThoughtSpot U course:
* [Snapshots and Backups](https://training.thoughtspot.com/3-snapshots-backups/461810){:target="_blank"}

See other training resources at <br/>
<a href="https://training.thoughtspot.com/" target="_blank"><img src="{{ "/images/ts-u.png" | prepend: site.baseurl  }}" alt="ThoughtSpot U"></a>
