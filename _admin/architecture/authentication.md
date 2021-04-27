---
title: [Authentication]
last_updated: 4/22/2020
summary: "ThoughtSpot provides LDAP/AD, SAML, and ThoughtSpot login to authenticate users."
sidebar: mydoc_sidebar
permalink: /:collection/:path.html
---
ThoughtSpot provides three ways to authenticate users: LDAP/AD, SAML, and
ThoughtSpot login. If possible, ThoughtSpot recommends that you use LDAP/AD or
SAML.

Use the following table to help you choose an authentication option.

<table>
  <tr>
    <th><a href="{{ site.baseurl }}/admin/setup/configure-SAML-with-tscli.html">SAML</a></th>
    <th><a href="{{ site.baseurl }}/admin/setup/about-LDAP.html">LDAP/AD</a></th>
    <th><a href="{{ site.baseurl }}/admin/users-groups/add-user.html">ThoughtSpot</a></th>
  </tr>
  <tr>
    <td>
    <ul>
    <li>Use SAML for single sign-on authentication.</li>
    <li>Can redirect from ThoughtSpot to SAML logins.</li>
    <li>Recommended for portal integration.</li>
    <li>Option to sync users and groups if stored in LDAP/AD.</li>
    </ul>
    </td>
    <td>
    <ul>
    <li>Configuration.</li>
    <li>Users authenticate against LDAP or AD.</li>
    <li>Option to sync users and groups with ThoughtSpot to manage group membership.</li>
    </ul>
    </td>
    <td>
    <ul>
    <li>User created and managed in ThoughtSpot.</li>
    <li><a href="{{ site.baseurl }}/admin/users-groups/add-user.html#password">Password strength control</a></li>
    <li>No other enterprise password control (expiration, failed logins, etc.).</li>
    <li>Only recommended when SAML and LDAP are not options.</li>
    </ul>
    </td>
  </tr>
</table>

All users and groups must be known to ThoughtSpot. If you are using LDAP/AD or
SAML and don’t create users in ThoughtSpot, a user is created when the user
first logs in. However, this user is assigned to the `All` group and can only
see content available for all users.

Groups are the primary way that security is managed. Groups are not
automatically created. You can create [groups]({{ site.baseurl }}/admin/users-groups/add-group.html) and [users]({{ site.baseurl }}/admin/users-groups/add-user.html) manually, or you must
automate the assignment from a source system. ThoughtSpot has an assignment
script that works with most LDAP / AD stores. It also has public APIs that you
can use to sync users and groups between source systems and your ThoughtSpot
appliance.
