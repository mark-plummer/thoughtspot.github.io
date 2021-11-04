---
title: [Collect security logs]
summary: "Collect security audit logs to monitor user activity in ThoughtSpot and increase your system security."
last_updated: 10/11/2021
sidebar: mydoc_sidebar
permalink: /:collection/:path.html
---

ThoughtSpot Cloud provides security audit events related to account activities and user actions within ThoughtSpot. These events can help your SOC team detect potential security threats or compromised user accounts in your organization. These human-readable and comprehensive events can be shipped to your SIEM application in near real-time. Security events remain within the system for 30 days. To integrate with your SIEM or view these logs, [contact ThoughtSpot Support]({{ site.baseurl }}/admin/misc/contact.html).

ThoughtSpot security events include the following information:

- An event ID
- A unique description of the event (e.g. “A user account was created”)
- Timestamp (in UTC) yyyy/mm/dd:hh:mm:ss
- User ID of the person initiating the event
- IP of the user
- Fields specific to the event (e.g. name of the new account)

{: id="security-events"}
### Security events

The possible events are:

- [account-logout](#logout-successful)
- [answer-creation](#create-answer)
- [answer-deletion](#delete-answers)
- [answer-update](#update-answers)
- [create-rls-rule](#create-rls-rule)
- [delete-rls-rules](#delete-rls-rules)
- [failed-login](#login-failed)
- [failed-logout](#logout-failed)
- [group-creation](#user-groups-created)
- [group-deletion](#user-groups-deleted)
- [group-modification](#user-group-modified)
- [group-principals-update](#principals-in-group-update)
- [locked-account](#account-locked)
- [object-sharing](#share-objects)
- [password-change](#update-password)
- [pinboard-creation](#create-pinboard)
- [pinboard-deletion](#delete-pinboards)
- [pinboard-update](#update-pinboards)
- [privilege-change](#privilege-changes)
- [profile-change](#users-modified)
- [successful-login](#login-successful)
- [table-creation](#create-tables)
- [update-rls-rule](#update-rls-rule)
- [user-account-creation](#users-created)
- [user-account-deletion](#users-deleted)
<!-- - [user-group-change](#user-group-change)-->
- [user-invitation](#user-invited)

### Event descriptions

ThoughtSpot defines these events as follows:

<dl>
<dlentry id="logout-successful">
 <dt>Account logout</dt>
 <dd>A user logs out from ThoughtSpot.</dd>
</dlentry>
<dlentry id="create-answer">
 <dt>Answer creation</dt>
 <dd>A user attempts to create a new answer.</dd>
</dlentry>
<dlentry id="delete-answers">
 <dt>Answer deletion</dt>
 <dd>A user attempts to delete an answer.</dd>
</dlentry>
<dlentry id="update-answers">
 <dt>Answer update</dt>
 <dd>A user attempts to modify an existing answer.</dd>
</dlentry>
<dlentry id="create-rls-rule">
 <dt>Row-level security (RLS) rule creation</dt>
 <dd>A user creates an RLS rule on a table.</dd>
</dlentry>
<dlentry id="delete-rls-rules">
 <dt>RLS rule deletion</dt>
 <dd>A user deletes an RLS rule on a table.</dd>
</dlentry>
<dlentry id="login-failed">
 <dt>Failed login</dt>
 <dd>A user fails to log in due to an incorrect password, or IdP/ADP deny the authentication request.</dd>
</dlentry>
<dlentry id="logout-failed">
 <dt>Failed logout</dt>
 <dd>User logout failed.</dd>
</dlentry>
<dlentry id="user-groups-created">
 <dt>Group creation</dt>
 <dd>A user creates a new group, either manually through the Admin Portal, or through the internal API.</dd>
</dlentry>
<dlentry id="user-groups-deleted">
 <dt>Group deletion</dt>
 <dd>A user deletes a group, either manually through the Admin Portal, or through the internal API.</dd>
</dlentry>
<dlentry id="group-modification">
 <dt>Group modification</dt>
 <dd>A user modifies the properties of a group, either in Admin Portal or over internal API. (Properties include group name, display name, and sharing visibility.)</dd>
</dlentry>
<dlentry id="principals-in-group-update">
 <dt>Group principals update</dt>
 <dd>A user successfully or unsuccessfully attempts to add or remove users or groups from a group.</dd>
</dlentry>
<dlentry id="account-locked">
 <dt>Locked account</dt>
 <dd>A local user fails to authenticate _x_ times in a row, locking the account. Administrators can configure the number of authentication attempts before lockout within ThoughtSpot.</dd>
</dlentry>
<!--
<dlentry id="object-creation">
 <dt>Object creation</dt>
 <dd>A user creates a new object (pinboard, worksheet, answer, etc.) in ThoughtSpot.</dd>
</dlentry>
<dlentry id="object-deletion">
 <dt>Object deletion</dt>
 <dd>A user successfully or unsuccessfully attempts to delete an object (pinboard, worksheet, answer).</dd>
</dlentry>
<dlentry id="object-modification">
 <dt>Object modification</dt>
 <dd>A user successfully or unsuccessfully attempts to change the properties of an object.</dd>
</dlentry>
-->
<dlentry id="share-objects">
 <dt>Object sharing</dt>
 <dd>A user successfully or unsuccessfully attempts to share an object (Pinboard, Worksheet, Answer) with another user or group.</dd>
</dlentry>
<dlentry id="update-password">
 <dt>Password change</dt>
 <dd>A user successfully or unsuccessfully attempts to change their password.</dd>
</dlentry>
<dlentry id="create-pinboard">
 <dt>Pinboard creation</dt>
 <dd>A user attempts to create a new Pinboard.</dd>
</dlentry>
<dlentry id="delete-pinboards">
 <dt>Pinboard deletion</dt>
 <dd>A user attempts to delete a Pinboard.</dd>
</dlentry>
<dlentry id="update-pinboards">
 <dt>Pinboard update</dt>
 <dd>A user attempts to modify an existing Pinboard.</dd>
</dlentry>
<dlentry id="privilege-changes">
 <dt>Privilege change</dt>
 <dd>A user adds or removes one or several privileges from a group.</dd>
</dlentry>
<dlentry id="users-modified">
 <dt>Profile change</dt>
 <dd>A user profile changes, either manually in the Admin Portal or over SAML sync.</dd>
</dlentry>
<dlentry id="update-rls-rule">
<dt>RLS rule update</dt>
<dd>A user modifies an RLS rule on a table.</dd>
</dlentry>
<dlentry id="login-successful">
  <dt>Successful login</dt>
  <dd>A local, IdP or AD user logs in to ThoughtSpot.</dd>
 </dlentry>
 <dlentry id="create-tables">
  <dt>Table creation</dt>
  <dd>A user attempts to create a new table.</dd>
 </dlentry>
 <dlentry id="users-created">
  <dt>User account creation</dt>
  <dd>A new user creates an account, either manually in the Admin Portal or through the internal API.</dd>
 </dlentry>
 <dlentry id="users-deleted">
  <dt>User account deletion</dt>
  <dd>A user account is deleted, either manually in the Admin Portal or through the internal API.</dd>
 </dlentry>
<!--
 <dlentry id="user-group-change">
  <dt>User group change</dt>
  <dd>A successful or unsuccessful attempt to change the user list to a group by adding or removing members.</dd>
 </dlentry>
 -->
 <dlentry id="user-invited">
  <dt>User invitation</dt>
  <dd>A user is invited to ThoughtSpot for a free trial.</dd>
 </dlentry>
</dl>


<!--
ThoughtSpot includes a number of management tools, monitoring applications, and automated processes to support system security. System security includes managing access and privileges, audit logs, security policies, and Linux OS installed package updates.

## Audit logs

There are several ways you can view audit log information in ThoughtSpot. You can see recent events in the Control Center or view more detailed audit logs using tscli. Administrators can view audit logs of configuration changes users have made to ThoughtSpot in these ways:

- Monitor events from the [Control Center]({{ site.baseurl }}/admin/system-monitor/monitor-pinboards.html#).
- Generate audit log reports through the `tscli` command.


You can access an audit log of cluster events through tscli. You can also access information on cluster updates, configurations, data loading and metadata events.

Use the `tscli event list` command to return an audit list of events from the cluster. The syntax is:

```
tscli event list
   [--include <all|config|notification>]
   [--since <hours,minutes,days>
   | --from <yyyymmdd-HH:MM>
   --to <yyyymmdd-HH:MM>]
   [--detail]
   [--summary_contains
   <'string1'| 'string2' ...>]
   [--detail_contains
   <'string1'| 'string2' ...>]
   [--attributes
   <key1='value1'|
   key2='value2' ...>]
```

Optional parameters are:

| Parameter | Description |
|---------------|---------------------|
| `--include` | Specifies the type of events to include, and can be `all`, `config`, or `notification`. |
| `--detail` | Returns the events in a detail format rather than a tabular summary, which is the default. |
| `--summary_contains <'string1' | 'string2' ...>` | Specifies a string to check for in the event summary. Enclose strings in single quotes, and separate multiple strings with &pipe;. Events that match all specified strings will be returned. |
| `--detail_contains <'string1'| 'string2' ...>` | Specifies a string to check for in the detail. Enclose strings in single quotes, and separate multiple strings with `|` (pipe symbol). Events that match all specified strings will be returned.|
| `--attributes <key1='value1' &pipe; key2='value2' ...>` | Specifies attributes to match as key=value pairs. Separate multiple attributes with `|` (pipe symbol). Events that match all specified key/value pairs will be returned. Put single quotes around the value(s). |

And a time window made up of either:

- `--since <hours,minutes,days>` is a time in the past for where the event audit begins, ending at the present time. Specify a human readable duration string, e.g. 4h (4 hours), 30m (30 minutes), 1d (1 day).

Or both:

- `--from <yyyymmdd-HH:MM>` is a timestamp for where to begin the event audit. It must be of the form: yyyymmdd-HH:MM.
- `--to <yyyymmdd-HH:MM>` is a timestamp for where to end the event audit. It must be of the form: yyyymmdd-HH:MM.

To get audit logs:

1. Log in to the Linux shell using SSH.
2. Issue the `tscli event list` command, with the desired parameters, for example:

    ```
    $ tscli event list
       --include config
       --since 24 hours
    ```


## Security policies

Security policies are the principles and processes ThoughtSpot uses in development to ensure a product that conforms to security standards. Security policies ensure a secure product with each release. When a release is in development, each build is tested using Qualys Network Security and Vulnerability Management Suite. Issues and vulnerabilities are fixed proactively, based on the results.

The ThoughtSpot Engineering and ThoughtSpot Support teams are notified of Common Vulnerabilities and Exposures (CVEs), so they can patch OS packages proactively as well. You can view installed packages along with their version numbers at any time, in order to see if you require an update to ThoughtSpot.

Whenever a CVE is identified, and an OS package needs to be updated, the next patch release will include the patch or update. You can view installed Linux packages at any time, along with the version numbers of the installed packages.

## Third-party security software for security, governance, and monitoring of ThoughtSpot

You can install supported [third-party security and monitoring software]({{ site.baseurl}}/admin/data-security/about-secure-monitor-sw.html#) on a ThoughtSpot cluster.
-->
