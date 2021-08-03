---
title: [Configure SAML SSO authentication]
last_updated: 04/3/2021
summary: "You can configure SAML authentication for embedded ThoughtSpot instance to authenticate federated users."
sidebar: mydoc_sidebar
permalink: /:collection/:path.html
---

ThoughtSpot supports the Single Sign-On (SSO) authentication method with the Security Assertion Markup Language (SAML) authentication and authorization framework. With SAML SSO, users can authenticate to the SAML identity provider to access the ThoughtSpot application or the embedded ThoughtSpot content in an external web application. It also allows them to navigate seamlessly between different applications with their existing credentials.

## About SAML authentication

SAML is an XML standard that allows secure exchange of user authentication and authorization data between trusted partners. It enables the following entities to exchange identity, authentication, and authorization information:

### SAML entities

The SAML SSO authentication involves several entities.

-   **Identity Provider (IdP)**                                       
    The Identity Management system that maintains the user identity information. The IdP acts as a SAML authority and authenticates SSO users. ThoughtSpot supports the SAML authentication framework with popular Identity Providers such as Okta, Azure Active Directory, PingFederate, Microsoft Active Directory Federation Services (ADFS), and Onelogin.

-   **Service Provider (SP)**                                   
    The provider of a business function or application service; for example, ThoughtSpot. The SP relies on the IdP to authenticate users before allowing access to its services.

-   **Federated user**                                             
    A user whose identity information is managed by the IdP. The federated users have SSO credentials and authenticate to the IdP to access various application services.

### SAML assertion and attributes

Both SP-initiated and IdP-initiated authentication workflows rely on assertions that are exchanged between the SAML endpoints through a web browser.

Some of the most commonly used elements are:

-   **SAML assertion**                                           
    The user authentication and authorization information issued by the IdP. SAML assertions contain all the information necessary for a service provider to confirm if the user identity is valid.

-   **Metadata**                                                   
    Data in the XML format to establish interoperability between the IdP and SP. It contains the URLs of the endpoints, entity ID, and so on.

-   **Assertion Services Consumer (ACS) URL**                               
    The endpoint URL to which the user’s browser sends the SAML response received from the IdP after authenticating a user.

-   **Entity ID**                                                      
    A unique service name to identify the client application from which the SSO login request originates.

-   **SAML attributes**                                                     
    The attributes associated with the user; for example, username and email address.

### SSO workflows

Most SAML deployments support the following authentication workflows:

-   SP-initiated SSO                                                  
    In the SP-initiated SSO authentication flow, the SSO request originates from the client application. For example, when a user tries to access the ThoughtSpot standalone application or the ThoughtSpot content embedded in an external application, a federation authentication request is created and sent to the IdP server.

-   IdP-initiated SSO                                                    
    In the IdP-initiated SSO authentication flow, the user authenticates to the IdP first. The browser then redirects the login request to the host application and allows the user to access the requested content.

## SAML authentication workflow for a ThoughtSpot embedded instance

With SAML SSO authentication, your host applications can allow federated users to access the embedded ThoughtSpot content without the need for a separate ThoughtSpot login.

A typical SP-initiated SSO authentication workflow consists of the following steps:

1.  A federated user tries to access a ThoughtSpot page, pinboard, or visualization in the host application.
2.  The host application sends the authentication request to ThoughtSpot.
3.  If the SAML SSO authentication method is configured for the ThoughtSpot embedded instance, the browser sends the SAML request to the IdP.                  
    -   If the user has already authenticated to the IdP, the login request is redirected to the host application.
    -   If the user is not authenticated, the browser displays a login page to allow the user to authenticate to the IdP and then redirects.                             
4.  The requested ThoughtSpot page or resource is displayed.

## Configuration steps

To configure SAML SSO authentication on the ThoughtSpot embedded instance, complete the following steps:

-   Enable SAML authentication on ThoughtSpot
-   Configure the IdP server for SAML authentication
-   Enable SSO authentication in Visual Embed SDK
-   Add SAML redirect domain to the allowed list in ThoughtSpot

Before you begin, make sure you have the admin user privileges to configure SAML support on ThoughtSpot.


## Enable SAML authentication

You need admin privileges to enable SAML SSO authentication.

1. Configure the ThoughtSpot application instance on your IDP server.  
2. Log in to your ThoughtSpot application instance.
3. [Configure the SAML attributes]({{ site.baseurl }}/admin/ts-cloud/authentication-integration.html).

## Configure the IdP server for SAML authentication
ThoughtSpot supports SAML authentication with several identity and access management providers, such as Okta, OneLogin, PingFederate, Microsoft ADFS, Microsoft Azure Active Directory, and so on.
If you want to use one of these providers as your IdP, make sure you follow the SAML configuration steps described in the Identity provider’s documentation.

To determine if ThoughtSpot supports your preferred IdP, [contact ThoughtSpot Support]({{ site.baseurl }}/admin/misc/contact.html).

{% include note.html content="When configuring SAML 2.0, make sure you map the SAML user attributes to appropriate fields. For example, you must map the SAML user’s username to the <code>NameId</code> attribute in OneLogin. Similarly, in Okta, you must map the username to <code>userPrincipalName</code>. You must also map the email address of the user to the mail attribute, and the display name you would like to use to the correct display name attribute. If your IdP does not allow you to import the IdP metadata XML file, you must map these values manually." %}

### Enable SSO authentication in the Visual Embed SDK
If you want to use SSO authentication for embedded ThoughtSpot content, make sure you set the `AuthType` parameter to `SSO` in the SDK when calling the `init` function from your application.

For more information, see the embedding instructions for [full ThoughtSpot application]({{ site.baseurl }}/admin/ts-cloud/full-app-embed.html), [search]({{ site.baseurl }}/admin/ts-cloud/embed-search.html) , [pinboard]({{ site.baseurl }}/admin/ts-cloud/embed-pinboard-sdk.html), or [visualization]({{ site.baseurl }}/admin/ts-cloud/embed-a-visualization.html).

## Allow SAML Redirect Domains

If you have to redirect SAML users to a login URL to a host server in a different domain, make sure you add the SAML redirect domains to the list of allowed domains in ThoughtSpot.

To whitelist a SAML redirect domain, follow these steps:

1. Log in to your ThoughtSpot application instance.
2. Click the **Develop** tab.
3. Under **Customizations**, click **Settings**.
4. In SAML redirect domains, add the domains to the whitelist.

   You can add multiple domains as comma-separated values.    
5. Click **Save changes**.
