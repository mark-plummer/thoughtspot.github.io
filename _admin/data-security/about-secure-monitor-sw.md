---
title: [About third-party security and monitoring software]
summary: "You can install third-party software for security, governance, and monitoring of ThoughtSpot."
sidebar: mydoc_sidebar
permalink: /:collection/:path.html
---
In addition to the ThoughtSpot monitoring and security features, some companies require specific additional third-party software to comply with their internal IT policies. This allows them to support all of their systems with a common set of security and management tools.

For example, you may wish to accomplish some security and monitoring tasks with your own third-party software. These tasks include things like pushing alerts, events, forensics, audit trails, insights, etc. from ThoughtSpot to your own local monitoring systems.

## Supported third-party software

ThoughtSpot supports installation of the following third-party software on the ThoughtSpot instance:

<dl>
<dlentry><dt>Qualys</dt>
  <dd>Qualys is a widely used technical vulnerabilities and security compliance scanning tool. For more information about Qualys, see the <a href="http://www.qualys.com/documentation/">Qualys documentation</a>.</dd></dlentry>

<dlentry><dt>SNMP (Simple Network Management Protocol)</dt>
  <dd>SNMP is an industry standard protocol used for monitoring network traffic and alert events.</dd></dlentry>

<dlentry><dt>Splunk</dt>
  <dd>You can install Splunk rsyslog and use it to forward ThoughtSpot logs to Splunk. For more information about Splunk, see the <a href="http://docs.splunk.com/">Splunk documentation</a>.</dd></dlentry></dl>

{% include warning.html content="ThoughtSpot does not support, certify or maintain any third-party software other than the Qualys agent, the SNMP agent for Linux, the Splunk agent, or AWS SSM. Use of non-certified software is very likely to result in loss of functionality for your ThoughtSpot cluster, or otherwise impact the ThoughtSpot application. Use of McAfee or any other virus scanner to scan directories, memory (RAM), filesystems or disks will result in severe loss of performance and/or functionality." %}

### Install third-party software

For details on how to install third-party software, see: [Installing third-party security and monitoring software]({{ site.baseurl}}/admin/data-security/install-secure-monitor-sw.html#)   

## What is not supported

When installing and configuring third-party software on a ThoughtSpot cluster, follow the following guidelines to avoid interfering with cluster operations:

- Avoid making any direct changes to any files outside of the /home directory.
- Do not remove existing SSH keys or authorized keys from /home/admin/.ssh
- Excessive resource usage, e.g. CPU, disk, memory, processes, etc.
- Killing any system or ThoughtSpot services, or causing node reboots.

Do not change any system wide configuration which may affect ThoughtSpot, such as:
- Network, e.g. IP addresses, DNS resolution
- Storage, e.g. removing existing mount points, removing drives
- Security, e.g. selinux

## Qualys

Qualys is supported for scanning of ThoughtSpot clusters for security vulnerabilities.

## SNMP Traps

ThoughtSpot has a built-in alerting service that can also be used to send SNMP traps. Many third-party monitoring systems share the common standard of using SNMP traps, and you can take advantage of those capabilities with ThoughtSpot.

ThoughtSpot supports SNMP for read only. So for example, you can read the IP address of the cluster, but not change it using SNMP.

See the [Alert code reference]({{ site.baseurl}}/reference/alerts-reference.html#) for details.

## Splunk rsyslog

ThoughtSpot monitoring and alerting logs are written to standard locations in the file system. This allows you to use rsyslog to collect them and send them to Splunk.

Here are some links to help you learn where various logs are written in ThoughtSpot:

- [Monitoring logs]({{ site.baseurl}}/admin/system-monitor/introduction.html#)
- [Audit logs]({{ site.baseurl}}/admin/data-security/audit-logs.html#)
- [Alert code reference]({{ site.baseurl}}/reference/alerts-reference.html#)
