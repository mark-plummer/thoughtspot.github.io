{: id="prerequisites"}
## Configuration prerequisites

Before you configure SAML, collect the following information:

| &#10063; | [ThoughtSpot service address](#ts-service-address) |
| &#10063; | [Service port](#ts-service-port) |
| &#10063; | [Unique service name](#ts-service-name) |
| &#10063; | [Skew time in seconds](#skew-time) |
| &#10063; | [Protocol](#protocol) |
| &#10063; | [IDP Metadata XML File](#metadata-xml-file) |
| &#10063; | [Automatically add SAML users to Thoughtspot](#auto-add) |
| &#10063; | [Also use ThoughtSpot internal authentication](#ts-auth) |

{: id="ts-service-address" }
### ThoughtSpot service address
A fully qualified and resolvable domain name for the ThoughtSpot service. For example, *thoughtspot.thoughtspot-customer.com*. If you do not have the DNS name, you can use the front-end IP address. However, using the DNS name instead of the IP address is a best practice.

{: id="ts-service-port" }
### Service port
Enter `443` in this box. This is the port of the server where your ThoughtSpot instance is running.

{: id="ts-service-name" }
### Unique service name
The unique key used by your Identity Provider to identify the client. For example, *urn:thoughtspot:callosum:saml*. You may know this as the *Entity ID*.

{: id="skew-time" }
### Skew time in seconds
The allowed skew time, after which the authentication response is rejected and sent back from the IDP. *86400* is a popular choice. The default is *3600*.

{: id="protocol"}
### Protocol
The connection protocol for ThoughtSpot. For example, `https`.

{: id="metadata-xml-file" }
### IdP Metadata XML File
The absolute path to your Identity Provider’s metadata file. This file is provided by your IDP. You need this file so that the configuration persists over upgrades. It is a best practice to set it up on persistent/HA storage (NAS volumes) or in the same absolute path on all nodes in the cluster. For example, *idp-meta.xml*. If your IDP needs an Assertion Consumer Service URL to create the metadata file, use `https://<hostname_or_IP>/callosum/v1/saml/SSO`.

{% include note.html content="If your IdP does not allow you to import the IdP metadata XML file, you must map values manually. For the ThoughtSpot system to pick up certain attributes, you must map them to specific fields. Map the username you would like to use to <code>NameId</code>, and map the email id of the user to <code>mail</code>." %}

{: id="auto-add" }
### Automatically add SAML users to Thoughtspot: (yes/no)
Choose whether or not to add SAML users to ThoughtSpot when they first authenticate. If you choose 'yes', then new users will be automatically created in ThoughtSpot upon first successful SSO login. If you choose 'no', then SAML users will not be added in ThoughtSpot upon first successful SSO login. Instead, you must [add users manually]({{ site.baseurl }}/admin/users-groups/add-user.html#add-user) or through [Active Directory]({{ site.baseurl }}/admin/setup/LDAP-config-AD.html).

{: id="ts-auth" }
### Also use ThoughtSpot internal authentication: (y/n)

If 'y', then ThoughtSpot local/internal users (including local administrative users) will still be authenticated outside the scope of SSO.
