---
title: [Configure SAML]
summary: "You can configure Security Assertion Markup Language (SAML) using ThoughtSpot's command line interface, tscli."
last_updated: 11/18/2019
sidebar: mydoc_sidebar
permalink: /:collection/:path.html
---
ThoughtSpot can use Security Assertion Markup Language (SAML) to authenticate
users. You can set up SAML through the shell on the ThoughtSpot instance [using a
`tscli` based configurator](#tscli), or [through the Admin Console](#admin-portal).

Before configuring SAML, you need this information:

-   Domain name for ThoughtSpot service (E.g. - `thoughtspot.ts-customer.com`).
-   Port of the server where your ThoughtSpot instance is running (E.g. - `443`).
-   Protocol, or the authentication mechanism for ThoughtSpot (E.g. - `http` or `https`)
-   Unique service name that is used as the unique key by IDP to identify the client (E.g. - `urn:thoughtspot:callosum:saml`). You may know this as the *Entity ID*.
-   Allowed skew time, which is the time after authentication response is rejected and sent back from the IDP. `86400` is a popular choice.
-   The absolute path to identity provider's metadata file. Typically called `idp-meta.xml` or similar. This is needed so that the configuration persists over upgrades. Best to set it up on persistent/HA storage (NAS volumes) else in the same absolute path on all nodes in the cluster. If your IDP needs an Assertion Consumer Service URL to create the metadata file, use `<https://<hostname_or_IP>/callosum/v1/saml/SSO`.
- ThoughtSpot's metadata file, `spring_saml_metadata.xml`. To download this file, navigate to `https://<hostname-or-IP>/callosum/v1/saml/metadata`. The file automatically downloads.
-   This configurator also checks with the user if internal authentication needs to be set or not. This internal authentication mechanism is used to authenticate `tsadmin` and other ThoughtSpot local users. Set it to true by default to let local system/admin users in via the frontend.

{: id="tscli"}
## Configure SAML using tscli

Use this procedure to set up SAML on ThoughtSpot for user authentication. Note that this configuration persists across software updates, so you do not have to reapply it if you update to a newer release of ThoughtSpot.

1. Log in to the Linux shell using SSH.
2. Execute the command to launch the interactive SAML configuration:

    ```
    tscli saml configure
    ```

3. Complete the configurator prompts with the information and files you gathered above.
4. When the configuration is complete, open a Web browser and go to the ThoughtSpot login page.
   It should now show the Single Sign On option.

{: id="admin-portal"}
## Configure SAML using the Admin Console

{% include content/admin-portal/authentication-saml.md %}
