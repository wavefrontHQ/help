### Using SAML SSO
By default, user accounts authenticate to Tanzu Observability with passwords.

From this page, as a user with the **SAML IdP Admin** permission, you can integrate your service instance with your SAML SSO provider, so that all users authenticate to Tanzu Observability through your identity provider.

To integrate your SAML SSO provider:
1. Obtain your identity provider metadata.

    For ADFS, Google SSO, Okta, OneLogin, PingOne, WorkspaceOne, and Azure AD identity providers, Tanzu Observability includes integrations with setup instructions. To navigate to the corresponding integration, from the **Identity Provider** drop-down menu, select your provider, and click the **Setup Instructions** link.
2. Copy your identity provider metadata and paste it in the **Configure Connection** text box.
3. Click **Test** and wait for a successful validation of the integration.
4. Click **Save**.

To update your SAML SSO integration, for example, if you must replace the certificate:
1. Delete the existing configuration by clicking the **Click Here** link.
2.Integrate your SAML SSO provider again.

**Read More**<br/>
[Single-Tenant Authentication and Self-Service SAML SSO](https://docs.wavefront.com/auth_self_service_sso.html)
