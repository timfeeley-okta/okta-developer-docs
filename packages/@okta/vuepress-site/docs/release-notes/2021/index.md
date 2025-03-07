---
title: Okta API Products Release Notes 2021
---
## August

### Monthly Release 2021.08.0

| Change                                                                   | Expected in Preview Orgs |
|--------------------------------------------------------------------------|--------------------------|
| [Okta Sign-In Widget, version 5.9.1](#okta-sign-in-widget-version-5-9-1) | August 4, 2021 |
| [Brands API is Self-Service EA](#brands-api-is-self-service-ea)              | August 4, 2021 |
| [Risk Providers and Risk Events APIs are EA](#risk-providers-and-risk-events-apis-are-ea) | August 4, 2021 |
| [SAML parameter SessionNotOnOrAfter is GA in Preview](#saml-parameter-sessionnotonorafter-is-ga-in-preview)| August 4, 2021 |
| [Support for Push Status using the Apps API is GA in Production](#support-for-push-status-using-the-apps-api-is-ga-in-production)| August 4, 2021 |
| [The Device Authorization grant type is Self-Service EA](#the-device-authorization-grant-type-is-self-service-ea) | August 4, 2021 |
| [Token-based SSO between native apps is Self-Service EA](#token-based-sso-between-native-apps-is-self-service-ea) | August 4, 2021 |

#### Okta Sign-In Widget, version 5.9.1

For details about this release, see the Okta [Sign-In Widget Release Notes](https://github.com/okta/okta-signin-widget/releases/tag/okta-signin-widget-5.9.1). For more information about the Widget, see the Okta [Sign-In Widget Guide](/code/javascript/okta_sign-in_widget/). <!--OKTA-416419-->

#### Brands API is Self-Service EA

The Okta [Brands API](/docs/reference/api/brands/) allows customization of the look and feel of pages and templates. It allows you to upload your own brand assets (colors, background image, logo, and favicon) to replace Okta's default brand assets. You can then publish these assets directly to the Okta-hosted Sign-In Page, error pages, email templates, and the Okta End-User Dashboard. See [Customize your Okta experience with the Brands API](/docs/guides/customize-themes/). <!-- 414350-->

#### Risk Providers and Risk Events APIs are EA

The Okta [Risk Providers API](/docs/reference/api/risk-providers/) enables security teams to integrate IP-based risk signals to analyze and orchestrate risk-based access using the authentication layer. Practitioners can step up, reduce friction, or block the user based on risk signals across the customer's security stack. Apart from improving security efficacy, this feature also enhances the user experience by reducing friction for good users based on positive user signals. The Okta [Risk Events API](/docs/reference/api/risk-events/) provides the ability for third-party Risk Providers to send Risk Events to Okta. See [Third-party risk provider integration](/docs/guides/third-party-risk-integration/overview/). <!-- OKTA-415574 -->

#### SAML parameter SessionNotOnOrAfter is GA in Preview

The SAML parameter `SessionNotOnOrAfter` for SAML assertions is available for use with Okta's [SAML Inline Hooks](/docs/reference/saml-hook/). This optional parameter specifies the session lifetime, in seconds, and is included in the SAML assertion. The `SessionNotOnOrAfter` parameter allows the Identity Provider to control the session of the Service Provider. Most SAML applications manage their own sessions. However, some SAML applications require this parameter from the Identity Provider for session management. <!--OKTA-406633-->

#### Support for Push Status using the Apps API is GA in Production

Developers can use the `pushStatus` [parameter](/docs/reference/api/apps/#username-template-object) to handle a username update to an app integration. Previously, this option wasn't available through the Apps API, which caused inconsistent behavior between app integrations configured using the Okta Admin Console and those configured through the API. <!--OKTA-413817-->

#### The Device Authorization grant type is Self-Service EA

Advancements in internet technology have seen an explosion of smart devices and the Internet of Things. Consumers need to sign in to applications that run on these devices, but the devices either lack support for a web browser or have limited ability for input, such as smart TVs, car consoles, and thermostats. As a result, users resort to insecure authentication solutions that are error-prone and time-consuming.

The [Device Authorization grant](/docs/reference/api/oidc/#device-authorize) feature is an OAuth 2.0 grant type that allows users to sign in to input-constrained devices and also to devices that lack web browsers. This feature enables users to use a secondary device, such as a laptop or mobile phone, to complete sign-in to applications that run on such devices. See [Configure Device Authorization](/docs/guides/device-authorization-grant/main/). <!-- OKTA-411412 -->

#### Token-based SSO between native apps is Self-Service EA

Single-Sign On (SSO) between browser-based web applications is achieved by leveraging shared cookies. Unlike web applications, native applications can't use web cookies. With Native SSO, Okta offers a token-based approach to [achieve SSO between native applications](/docs/reference/api/oidc/#scopes).

Native SSO allows you to protect native OpenID Connect applications, such as desktop apps and mobile apps, and achieve SSO and Single Logout (SLO) between these applications. See [Configure SSO for native apps](/docs/guides/configure-native-sso/main/). <!-- OKTA-411335 -->

## July

### Weekly Release 2021.07.2

| Change                                                                         | Expected in Preview Orgs |
|--------------------------------------------------------------------------------|--------------------------|
| [Bug fixed in 2021.07.2](#bug-fixed-in-2021-07-2)                            | July 28, 2021            |

#### Bug fixed in 2021.07.2

Authentication responses didn't include the Provider ID (`IdP.id`) or Provider Type (`IdP.type`) properties for some Okta-sourced users. (OKTA-410677)

### Weekly Release 2021.07.1

| Change                                                                         | Expected in Preview Orgs |
|--------------------------------------------------------------------------------|--------------------------|
| [Bug fixed in 2021.07.1](#bug-fixed-in-2021-07-1)                            | July 14, 2021            |

#### Bug fixed in 2021.07.1

When factor sequencing was enabled for passwordless authentication flows, requests to the `/authn` endpoint returned personal user information prior to primary authentication. (OKTA-407199)

### Monthly Release 2021.07.0

| Change                                                                   | Expected in Preview Orgs |
|--------------------------------------------------------------------------|--------------------------|
| [Support for Push Status using the Apps API is GA in Preview](#support-for-push-status-using-the-apps-api-is-ga-in-preview) | July 8, 2021 |
| [Provisioning for Org2Org app integrations is GA in Production](#provisioning-for-org2org-app-integrations-is-ga-in-production) | July 8, 2021 |
| [New Domains API response properties available](#new-domains-api-response-properties-available) | July 8, 2021 |
| [Rate limit events for user and session user activity](#rate-limit-events-for-user-and-session-user-activity) | July 8, 2021 |
| [Schemas API feature unique attributes is now GA in Preview](#schemas-api-feature-unique-attributes-is-now-ga-in-preview) | July 8, 2021 |
| [The SAML 2.0 Assertion grant flow is now GA in Preview](#the-saml-2-0-assertion-grant-flow-is-now-ga-in-preview) | July 8, 2021 |
| [Event Hook preview tab is now GA in Preview](#event-hook-preview-tab-is-now-ga-in-preview) | July 8, 2021 |
| [Bugs fixed in 2021.07.0](#bugs-fixed-in-2021-07-0) | July 8, 2021 |

#### Support for Push Status using the Apps API is GA in Preview

Developers can use the `pushStatus` parameter to handle a username update to an app integration. Previously, this option wasn't available through the [Apps API](/docs/reference/api/apps), which caused inconsistent behavior between app integrations configured using the Okta Admin Console and those configured through the API.
<!--OKTA-405533-->

#### Provisioning for Org2Org app integrations is GA in Production

Previously, Okta admins could only configure provisioning for the Org2Org app integration using the Admin Console. With the introduction of Multi-Org functions within the [Apps API](/docs/reference/api/apps), you can write code scripts or use SDKs to automate Okta hub and spoke scenarios.

Additionally, you can set or update the Logo or Notes fields for any of your Okta app integrations using the API. <!--OKTA-405943-->

#### New Domains API response properties available

The [Domains API](/docs/reference/api/domains) includes the new response object properties of `certificateSourceType` and `expiration`. The `certificateSourceType` is a required property that indicates whether the Certificate is provided by the user. The accepted value is `Manual`. The `expiration` property on the DNSRecord object is an optional property that defines the TXT record expiration. <!--OKTA-403600-->

#### Rate limit events for user and session user activity

Previously, rate limit violation events for user and session user were logged as org-wide system events (`system.org.rate_limit.violation`). These rate limit violation events are now logged more specifically as [operation events](/docs/reference/rl-system-log-events/#operation-rate-limits) (`system.operation.rate_limit.violation`). <!--OKTA-394607-->

#### Schemas API feature unique attributes is now GA in Preview

The Schemas API now includes [unique attributes](/docs/reference/api/schemas/#uniqueattributes) for custom properties in the Okta User Profile and the Okta Group Profile. You can declare a maximum of five unique properties for each user type and five unique properties in the Okta Group Profile. This feature helps prevent the duplication of data and ensures data integrity. <!--OKTA-400824-->

#### The SAML 2.0 Assertion grant flow is now GA in Preview

You can use the SAML 2.0 Assertion flow to request an access token when you want to use an existing trust relationship without a direct user approval step at the authorization server. The flow enables a client app to reuse an authorization by supplying a valid, signed SAML assertion to the authorization server in exchange for an access token. This flow is often used in migration scenarios from legacy Identity Providers that don't support OAuth. See [Implement the SAML 2.0 Assertion flow](/docs/guides/implement-saml2/overview/). <!--OKTA-406626-->

#### Event Hook preview tab is now GA in Preview

Event Hooks that you configure in the Admin Console or by [Event Hooks Management API](https://developer.okta.com/docs/reference/api/event-hooks/) can now preview the JSON body of the Event Hook in the Admin Console, as well as delivering the preview request to your external service without manually triggering an actual event. See [Event Hook Preview](https://help.okta.com/oie/en-us/Content/Topics/automation-hooks/event-hooks-preview.htm).

#### Bugs fixed in 2021.07.0

- The IdP claim wasn't available in the `id_token` or included with the Token Inline Hook request. (OKTA-407459)

- When the Users lifecycle API `users/{{userId}}/lifecycle/reset_factors` was called to reset user factors, a status 403 error was received, even with a valid bearer token and scope (`okta.users.manage`). (OKTA-404613)

- When an OIDC client app was created, the [Apps API](/docs/reference/api/apps) call couldn't modify the `visibility.hide` property. (OKTA-399408)

## June

### Weekly Release 2021.06.4

| Change                                                                         | Expected in Preview Orgs |
|--------------------------------------------------------------------------------|--------------------------|
| [Bugs fixed in 2021.06.4](#bugs-fixed-in-2021-06-4)                              | June 30, 2021            |

#### Bugs fixed in 2021.06.4

* The group app assignment process failed to assign users to an app when a database exception occurred. (OKTA-378076)

* To follow cryptographic standards, the default client secret length has been increased for public applications. (OKTA-303734)

### Weekly Release 2021.06.3

| Change                                                                         | Expected in Preview Orgs |
|--------------------------------------------------------------------------------|--------------------------|
| [Bugs fixed in 2021.06.3](#bugs-fixed-in-2021-06-3)                              | June 23, 2021             |

#### Bugs fixed in 2021.06.3

* When some app types were created using the Apps API, duplicate [app labels](/docs/guides/customize-tokens-returned-from-okta/-/create-app-profile-attribute/) were not allowed. (OKTA-403289)

* If an app’s sign-in policy required an MFA prompt every time and the [`prompt=login` parameter](/docs/guides/shared-sso-android-ios/-/optional-settings/#always-prompt-for-sign-in-regardless-of-session) was present in the `/authorize` request, the MFA prompt didn’t appear for federated users. (OKTA-394991)

### Weekly Release 2021.06.2

| Change                                                                         | Expected in Preview Orgs |
|--------------------------------------------------------------------------------|--------------------------|
| [Bug fixed in 2021.06.2](#bug-fixed-in-2021-06-2)                              | June 16, 2021             |

#### Bug fixed in 2021.06.2

When the [Features endpoint of the Apps API](/docs/reference/api/apps/#update-feature-for-application) was called to enable or disable user deactivation (`lifecycleDeactivate` property), the call didn't toggle the `REACTIVATE_USERS` app feature. (OKTA-399233)

### Weekly Release 2021.06.1

| Change                                                                         | Expected in Preview Orgs |
|--------------------------------------------------------------------------------|--------------------------|
| [Bugs fixed in 2021.06.1](#bugs-fixed-in-2021-06-1)                            | June 9, 2021             |

#### Bugs fixed in 2021.06.1

* User credential updates failed and returned an error message if the [User Type](/docs/reference/api/user-types/) was set to a non-email username. (OKTA-334754)

* When an `/authorize` request with an [IdP parameter](/docs/reference/api/idps/#add-identity-provider) that referenced a SAML Identity Provider (IdP) was sent, an internal server error was returned because it was assumed that all IdPs are social IdPs. (OKTA-385800)

* Service clients were unable to update [SAML apps](/docs/reference/api/apps/#update-application) due to a user context check that failed to pass. (OKTA-395492)

### Monthly Release 2021.06.0

| Change                                                                                              | Expected in Preview Orgs |
|-----------------------------------------------------------------------------------------------------|--------------------------|
| [Okta Sign-In Widget, version 5.7.0](#okta-sign-in-widget-version-5-7-0) | June 3, 2021 |
| [Domains API is GA in Production](#domains-api-is-ga-in-production) | June 3, 2021 |
| [Flexible Consent is GA in Preview](#flexible-consent-is-ga-in-preview) | June 3, 2021 |
| [Provisioning for Org2Org app integrations can be configured using the API](#provisioning-for-org2org-app-integrations-can-be-configured-using-the-api)| June 3, 2021 |
| [Refresh Token Rotation is GA in Production](#refresh-token-rotation-is-ga-in-production) | June 3, 2021 |
| [Retrieving applications by catalog name is now available](#retrieving-applications-by-catalog-name-is-now-available) | June 3, 2021 |
| [The application.lifecycle.create event is now generated for OIDC Apps](#the-application-lifecycle-create-event-is-now-generated-for-oidc-apps) | June 3, 2021 |
| [The Subscriptions API is GA in Preview](#the-subscriptions-api-is-ga-in-preview) | June 3, 2021 |

#### Okta Sign-In Widget, version 5.7.0

For details about this release, see the Okta [Sign-In Widget Release Notes](https://github.com/okta/okta-signin-widget/releases/tag/okta-signin-widget-5.7.0). For more information about the Widget, see the Okta [Sign-In Widget Guide](/code/javascript/okta_sign-in_widget/). <!--OKTA-391046-->

#### Domains API is GA in Production

The [Domains API](/docs/reference/api/domains/) is now Generally Available in Production. This API allows you to customize your Okta org domain name for a seamless branded experience so that your users can see the same base URL for your application. <!--OKTA-395907-->

#### Flexible Consent is GA in Preview

Flexible Consent is now Generally Available in Preview. Customers are unable to request consent-enabled scopes when using the [Client Credential grant flow](/docs/guides/implement-client-creds/overview/). Since the Client Credential grant flow doesn't involve an end user, consent shouldn't be required for these flows. The authorization server should understand that this flow doesn't involve a user, ignore the consent for these scopes, and include the scope in the response. However, the authorization server returns an error. This causes customers to design separate scopes when using the Client Credentials grant flow.

The new Flexible Consent setting allows customers to use a single set of scopes in both 3-legged and 2-legged OAuth flows. When a scope is requested during a Client Credentials grant flow and `CONSENT` is set to `FLEXIBLE`, the scope is granted in the access token with no consent prompt. This allows customers to use the same scopes for both user and service-based OAuth flows. <!--OKTA-392294-->

#### Provisioning for Org2Org app integrations can be configured using the API

Previously, Okta admins could only configure provisioning for the Org2Org app integration using the Admin Console. With the introduction of Multi-Org functions within the [Apps API](/docs/reference/api/apps/#application-provisioning-connection-operations), you can write code scripts or use SDKs to automate Okta hub and spoke scenarios.

Additionally, you can set or update the **Logo** or **Notes** fields for any of your Okta app integrations using the API. <!--OKTA-397181-->

#### Refresh Token Rotation is GA in Production

[Refresh Token Rotation](/docs/guides/refresh-tokens/refresh-token-rotation/) is now Generally Available in Production. Refresh Token Rotation helps a public client to securely rotate refresh tokens after each use. A new refresh token is returned each time the client makes a request to exchange a refresh token for a new access token. <!--OKTA-399846-->

#### Retrieving applications by catalog name is now available

You can now look up apps by their catalog name using the [Apps API](/docs/reference/api/apps/). Use a `name` expression (for example: `name eq ":name"`) with the `filter` parameter to search for apps by catalog name on the `/apps` endpoint. <!--OKTA-391038-->

#### The application.lifecycle.create event is now generated for OIDC Apps

When OpenID Connect (OIDC) apps are created using the App Integration Wizard or the Apps API, the `application.lifecycle.create` event is now generated. Additionally, app context is now included with the event. <!--OKTA-389740-->

#### The Subscriptions API is GA in Preview

The [Subscriptions API](/docs/reference/api/admin-notifications/) is now Generally Available in Preview. The Subscriptions API provides operations to manage email subscription settings for Okta administrator notifications.

* Super Admins can manage the default admin notifications that each admin receives based on their role.
* Individual admins can update their own notification preferences by subscribing or unsubscribing.
<!--OKTA-395158-->

## May

### Weekly Release 2021.05.3

| Change                                                                         | Expected in Preview Orgs |
|--------------------------------------------------------------------------------|--------------------------|
| [Okta Sign-In Widget, version 5.6.4](#okta-sign-in-widget-version-5-6-4)       | May 26, 2021             |
| [Bugs fixed in 2021.05.3](#bugs-fixed-in-2021-05-3)                            | May 26, 2021             |

#### Okta Sign-In Widget, version 5.6.4

For details about this release, see the Okta [Sign-In Widget Release Notes](https://github.com/okta/okta-signin-widget/releases/tag/okta-signin-widget-5.6.4). For more information about the Widget, see the Okta [Sign-In Widget Guide](/code/javascript/okta_sign-in_widget/). <!--OKTA-397857-->

#### Bugs fixed in 2021.05.3

* Array indexing [expressions](/docs/reference/okta-expression-language/#constants-and-operators) (for example: `myArray[0]`) were blocked at validation even when the array and the index were valid. (OKTA-395810)

* SAML requests and responses weren't logged in the [System Log](/docs/reference/api/system-log/) as distinct event fields and lacked detail about the SAML assertion. (OKTA-378981)

### Weekly Release 2021.05.2

| Change                                                                                              | Expected in Preview Orgs |
|-----------------------------------------------------------------------------------------------------|--------------------------|
| [Bugs fixed in 2021.05.2](#bugs-fixed-in-2021-05-2)         | May 19, 2021           |

#### Bugs fixed in 2021.05.2

* When a user was enrolled with SMS or Call factors and an additional or retry [API call](/docs/reference/api/factors) was made within 30 seconds of enrollment, the response included multiple rate limit headers. (OKTA-379654)

* When [OIDC apps](/docs/reference/api/oauth-clients/#register-new-client) were created concurrently, some apps were created in a deactivated state. (OKTA-384407)

* The [Client Credentials Flow](/docs/guides/implement-client-creds/overview/) could not implement a custom claim named `scope`. (OKTA-389874)

### Weekly Release 2021.05.1

| Change                                                                                              | Expected in Preview Orgs |
|-----------------------------------------------------------------------------------------------------|--------------------------|
| [Okta Sign-In Widget, version 5.6.1](#okta-sign-in-widget-version-5-6-1) | May 12, 2021 |
| [Bugs fixed in 2021.05.1](#bugs-fixed-in-2021-05-1)         | May 12, 2021           |

#### Okta Sign-In Widget, version 5.6.1

For details about this release, see the Okta [Sign-In Widget Release Notes](https://github.com/okta/okta-signin-widget/releases/tag/okta-signin-widget-5.6.1). For more information about the Widget, see the Okta [Sign-In Widget Guide](/code/javascript/okta_sign-in_widget/). <!--OKTA-393866-->

#### Bugs fixed in 2021.05.1

* Duplicate parameter names were passed in requests to the following [OAuth endpoints](/docs/reference/api/oidc/#possible-errors), and no error message was sent. (OKTA-132318)

  * `/token`
  * `/authorize`
  * `/revoke`
  * `/introspect`

* When an OpenID Connect [application was created](/docs/reference/api/apps/#add-application) using a deactivated application's name, a "Duplicate Client Name" error appeared. (OKTA-215049)

* When using the [Factor lifecycle operations endpoints](/docs/reference/api/factors/#factor-lifecycle-operations) to enroll a phone number, users who entered an incorrect phone format received the wrong Factor Service error messages. (OKTA-385106)

### Monthly Release 2021.05.0

| Change                                                                                              | Expected in Preview Orgs |
|-----------------------------------------------------------------------------------------------------|--------------------------|
| [Access-Control-Expose-Headers now available in CORS response](#access-control-expose-headers-now-available-in-cors-response) | May 5, 2021 |
| [Administrator Roles API third-party admin status update](#administrator-roles-api-third-party-admin-status-update) | May 5, 2021 |
| [Custom Group Profile Properties is Self-Service EA in Preview](#custom-group-profile-properties-is-self-service-ea-in-preview) | May 5, 2021 |
| [Domains API is GA in Preview](#domains-api-is-ga-in-preview) | May 5, 2021 |
| [Domains API supports OAuth 2.0](#domains-api-supports-oauth-2-0) | May 5, 2021 |
| [Okta Sign-In Widget, version 5.6.0](#okta-sign-in-widget-version-5-6-0) | May 5, 2021 |
| [Refresh Token Rotation is GA in Preview](#refresh-token-rotation-is-ga-in-preview) | May 5, 2021 |
| [SAML parameter SessionNotOnOrAfter is GA in Preview](#saml-parameter-sessionnotonorafter-is-ga-in-preview) | May 5, 2021 |
| [System Log API SCIM filter expression update](#system-log-api-scim-filter-expression-update) | May 5, 2021 |
| [Bug fixed in 2021.05.0](#bug-fixed-in-2021-05-0)         | May 5, 2021 |

#### Access-Control-Expose-Headers now available in CORS response

The `Access-Control-Expose-Headers` header is now included in the response to an Okta CORS endpoint call. This header can be accessed by the cross-origin user agent and includes the following possible header names:

* `Date`
* `Link`
* `X-Okta-Edge-Log`
* `X-Okta-Request-Id`
* `X-Rate-Limit-Limit`
* `X-Rate-Limit-Remaining`
* `X-Rate-Limit-Reset`
<!--OKTA-357710-->

#### Administrator Roles API third-party admin status update

The [Administrator Roles API](/docs/reference/api/roles/) has been updated to support third-party admin status for a user or a group without requiring a role assignment. See [Role assignment operations](/docs/reference/api/roles/#role-assignment-operations). <!--OKTA-381780-->

#### Custom Group Profile Properties is Self-Service EA in Preview

[Custom Group Profile properties](/docs/reference/api/groups/#custom-profile-properties) has been released in Preview as Self-Service Early Access. The [Groups API](/docs/reference/api/groups/) can now manage [custom Group Profile properties](/docs/reference/api/groups/#custom-profile-properties) after these properties are added to the Group Profile schema. The [Schemas API](/docs/reference/api/schemas) includes a new [Groups Schema object](/docs/reference/api/schemas/#group-schema-object) and [operations](/docs/reference/api/schemas/#group-schema-operations) that support custom Group properties. You can use the Schemas API or the Profile Editor in the Admin Console to manage schema extensions. Custom Group Profile properties provide flexibility to manage the default profile for Okta groups in the Okta Admin Console Profile Editor or through the Schemas API. This new functionality simplifies group management and lets you quickly add, edit, or remove custom profile attributes to groups. <!--OKTA-389897-->

#### Domains API is GA in Preview

The [Domains API](/docs/reference/api/domains/) is now Generally Available in Preview. This API allows you to customize your Okta org domain name for a seamless branded experience so that your users can see the same base URL for your application. <!--OKTA-386752-->

#### Domains API supports OAuth 2.0

The [Domains API](/docs/reference/api/domains/) has been updated to support OAuth 2.0. You can grant access to the Domains API using the `okta.domains.manage` and the `okta.domains.read` scopes instead of using SSWS tokens. See [Scopes and supported endpoints](/docs/guides/implement-oauth-for-okta/scopes/). <!--OKTA-381286-->

#### Okta Sign-In Widget, version 5.6.0

For details about this release, see the Okta [Sign-In Widget Release Notes](https://github.com/okta/okta-signin-widget/releases/tag/okta-signin-widget-5.6.0). For more information about the Widget, see the Okta [Sign-In Widget Guide](/code/javascript/okta_sign-in_widget/). <!--OKTA-391046-->

#### Refresh Token Rotation is GA in Preview

[Refresh Token Rotation](/docs/guides/refresh-tokens/refresh-token-rotation/) is now Generally Available in Preview. Refresh Token Rotation helps a public client to securely rotate refresh tokens after each use. When refresh token rotation behavior is enabled in Okta, a new refresh token is returned each time the client makes a request to exchange a refresh token for a new access token.
<!--OKTA-390933-->

#### SAML parameter SessionNotOnOrAfter is GA in Preview

The SAML parameter `SessionNotOnOrAfter` is now Generally Available in Preview for SAML assertions and is available for use with Okta’s [SAML Inline Hooks](/docs/reference/saml-hook/). This optional parameter specifies the session lifetime, in seconds, and is included in the SAML assertion. The `SessionNotOnOrAfter` parameter allows the Identity Provider to control the session of the Service Provider. Most SAML applications manage their own sessions. However, some SAML applications require this parameter from the Identity Provider for session management. <!--OKTA-390950-->

#### System Log API SCIM filter expression update

The [System Log API](/docs/reference/api/system-log/) has been updated to return an HTTP 400 response code when a request is made with a SCIM filter expression using the `co` (contains) operator with the `debugContext.debugData.url` or `debugContext.debugData.requestUri` field values. Use an alternative filter expression field such as `actor.id` or `target.id` to filter events in the System Log API. <!--OKTA-388434-->

#### Bug fixed in 2021.05.0

* When a [Dynamic Client Registration API](/docs/reference/api/oauth-clients/) call was created without a JSON Web Key Set (JWKS) configured, the error message returned was misleading, stating an invalid JWKS. (OKTA-383344)

## April

### Weekly Release 2021.04.2

| Change                                                                                              | Expected in Preview Orgs |
|-----------------------------------------------------------------------------------------------------|--------------------------|
| [Okta Sign-In Widget, version 5.5.4](#okta-sign-in-widget-version-5-5-4) | April 28, 2021 |
| [Bugs fixed in 2021.04.2](#bugs-fixed-in-2021-04-2)         | April 28, 2021           |

#### Okta Sign-In Widget, version 5.5.4

For details about this release, see the Okta [Sign-In Widget Release Notes](https://github.com/okta/okta-signin-widget/releases/tag/okta-signin-widget-5.5.4). For more information about the Widget, see the Okta [Sign-In Widget Guide](/code/javascript/okta_sign-in_widget/). <!--OKTA-387717,OKTA-389358-->

#### Bugs fixed in 2021.04.2

* System performance was degraded when the [List Users](/docs/reference/api/users/#list-users) or [Get User](/docs/reference/api/users/#get-user) API was used to fetch credentials with complex delegated authentication. You can avoid this performance issue by omitting the credential fetching operation. See omit credential response options in [List Users - Content-Type header fields](/docs/reference/api/users/#content-type-header-fields-2) or [Get User - Content-Type header fields](/docs/reference/api/users/#content-type-header-fields). (OKTA-371358)

* When the [Users API](/docs/reference/api/users) was used to create a user with an address containing a 4-byte UTF-8 encoded character, an incorrect 500 system error was returned. (OKTA-382882)

### Weekly Release 2021.04.1

| Change                                                                                              | Expected in Preview Orgs |
|-----------------------------------------------------------------------------------------------------|--------------------------|
| [Okta Sign-In Widget, version 5.5.2](#okta-sign-in-widget-version-5-5-2) | April 14, 2021 |
| [Increased authorization code lifetime](#increased-authorization-code-lifetime) | April 14, 2021 |
| [Bugs fixed in 2021.04.1](#bugs-fixed-in-2021-04-1)         | April 14, 2021           |

#### Okta Sign-In Widget, version 5.5.2

For details about this release, see the Okta [Sign-In Widget Release Notes](https://github.com/okta/okta-signin-widget/releases/tag/okta-signin-widget-5.5.2). For more information about the Widget, see the Okta [Sign-In Widget Guide](/code/javascript/okta_sign-in_widget/). <!--OKTA-385739-->

#### Increased authorization code lifetime

The OAuth 2.0 authorization code lifetime has increased from one minute to five minutes. <!--OKTA-379556-->

#### Bugs fixed in 2021.04.1

* A sign-in hint wasn’t passed to a SAML identity provider in an Org2Org configuration if the request contained a `login_hint` and an `idp` parameter. (OKTA-379879)

* When a call was made to the [User API](/docs/reference/api/users/) without permission to update a user profile’s property that was marked as [sensitive](https://help.okta.com/en/prod/Content/Topics/users-groups-profiles/usgp-hide-sensitive-attributes.htm), two error messages were returned. One of the error messages contained information about the sensitive property. (OKTA-380344)

### Monthly Release 2021.04.0

| Change                                                                                              | Expected in Preview Orgs |
|-----------------------------------------------------------------------------------------------------|--------------------------|
| [Okta Sign-In Widget, version 5.5.0](#okta-sign-in-widget-version-5-5-0) | April 1, 2021 |
| [Domains API now in EA in Preview](#domains-api-is-now-in-ea-in-preview) | April 1, 2021 |
| [Groups API extended search now GA in Production](#groups-api-extended-search-is-now-ga-in-production) | April 1, 2021 |
| [Bug fixed in 2021.04.0](#bug-fixed-in-2021-04-0)         | April 1, 2021           |

#### Okta Sign-In Widget, version 5.5.0

For details about this release, see the Okta [Sign-In Widget Release Notes](https://github.com/okta/okta-signin-widget/releases/tag/okta-signin-widget-5.5.0). For more information about the Widget, see the Okta [Sign-In Widget Guide](/code/javascript/okta_sign-in_widget/).

#### Domains API is now in EA in Preview

The [Domains API](/docs/reference/api/domains/) is now in Early Access in Preview.

#### Groups API extended search is now GA in Production

The Groups API support for [extended search](/docs/reference/api/groups/#list-groups-with-search) is now Generally Available (GA) in Production.

#### Bug fixed in 2021.04.0

* Sometimes the public OAuth metadata API responses did not include a `Vary: Origin` header, resulting in some browsers incorrectly caching the response across Origins. (OKTA-373689)

## March

### Weekly Release 2021.03.3

| Change                                                    | Expected in Preview Orgs |
| --------------------------------------------------------- | ------------------------ |
| [Bug fixed in 2021.03.3](#bug-fixed-in-2021-03-3)         | March 25, 2021           |

#### Bug fixed in 2021.03.3

When an OAuth2 request was made with an access token instead of a required ID token, the error message didn't clarify that the request was made with the wrong token.

### Weekly Release 2021.03.2

| Change                                                    | Expected in Preview Orgs |
| --------------------------------------------------------- | ------------------------ |
| [Bugs fixed in 2021.03.2](#bugs-fixed-in-2021-03-2)       | March 17, 2021           |

#### Bugs fixed in 2021.03.2

* After updating a Group `name` using the [Groups API](/docs/reference/api/groups/#update-group), the change wasn't reflected in the target application with [**Group Push**](https://help.okta.com/en/prod/okta_help_CSH.htm#ext_Directory_Using_Group_Push) enabled. (OKTA-375190)

* When creating a User with a recovery question using an OAuth access token rather than an API token, an invalid session error was returned. (OKTA-361888)

### Weekly Release 2021.03.1

| Change                                                    | Expected in Preview Orgs |
| --------------------------------------------------------- | ------------------------ |
| [Bugs fixed in 2021.03.1](#bugs-fixed-in-2021-03-1)       | March 10, 2021           |

#### Bugs fixed in 2021.03.1

* When `AppUser` was updated after enabling `APPLICATION_ENTITLEMENT_POLICY`, some [user attributes](/docs/guides/build-provisioning-integration/-/attribute-mapping/), such as the Manager attribute, were prevented from being updated in an application. (OKTA-329758)

* When using the [`/api/v1/users` endpoint](/docs/reference/api/users/) to generate the sign-in request for an Identity engine user through a mapping, if you created the same user by sending in more than one request at the same time, an incorrect 500 error message (internal server error) was sometimes returned instead of a 400 error message. (OKTA-318474)

### Monthly Release 2021.03.0

| Change                                                                                              | Expected in Preview Orgs |
|-----------------------------------------------------------------------------------------------------|--------------------------|
| [The SAML 2.0 Assertion grant flow is now Self-Service Early Access (EA)](#the-saml-2-0-assertion-grant-flow-is-now-self-service-early-access-ea) | March 3, 2021 |
| [The Okta Org API is now GA](#the-okta-org-api-is-now-ga) | March 3, 2021         |
| [The /login/token/redirect endpoint now has a dedicated rate limit](#the-login-token-redirect-endpoint-now-has-a-dedicated-rate-limit) | March 3, 2021          |
| [The new LDAP Interface authentication type is now GA](#the-new-ldap-interface-authentication-type-is-now-ga) | March 3, 2021          |
| [Bugs fixed in 2021.03.0](#bugs-fixed-in-2021-03-0) | March 3, 2021         |

#### The SAML 2.0 Assertion grant flow is now Self-Service Early Access (EA)

The SAML 2.0 Assertion grant flow is now Self-Service EA. You can use the SAML 2.0 Assertion flow to request an access token when you want to use an existing trust relationship without a direct user approval step at the authorization server. The flow enables a client app to reuse an authorization by supplying a valid, signed SAML assertion to the authorization server in exchange for an access token. This flow is often used in migration scenarios from legacy Identity Providers that don't support OAuth. See [Implement the SAML 2.0 Assertion flow](/docs/guides/implement-saml2/overview/).<!--OKTA-373421-->

#### The Okta Org API is now GA

The Okta [Org API](/docs/reference/api/org/) is now GA. This API allows you to manage your org account settings, contact information, logo, Okta support settings, Okta communication settings, and preferences. <!--OKTA-369570-->

#### The /login/token/redirect endpoint now has a dedicated rate limit

The `/login/token/redirect` endpoint now has its own dedicated [rate limit](/docs/reference/rl-global-enduser/). Previously this endpoint shared a rate limit with other traffic that didn't have dedicated rate limits for each endpoint. <!--OKTA-363694-->

#### The new LDAP Interface authentication type is now GA

The new LDAP Interface `authType` is now GA. When you create a [Sign On Policy](/docs/reference/api/policy/#authcontext-condition-object), you can now create rules that apply only to LDAP Interface user authentications. With this change, you can apply a Sign On Policy to LDAP Interface authentications and exclude other authentication methods.

#### Bugs fixed in 2021.03.0

* When a POST request was made using an OAuth access token (with the `okta.users.manage` scope) to the `/{userId}/factors/{factorId}/verify` endpoint, an "Invalid Session" error was returned. (OKTA-364443)

* After a new password was set, the password changed notification was sent in error to new users that were created with no credentials through the API. (OKTA-362241)

## February

### Monthly Release 2021.02.0

| Change                                                                                              | Expected in Preview Orgs |
|-----------------------------------------------------------------------------------------------------|--------------------------|
| [Okta Org API now available in Self-Service Early Access (EA)](#okta-org-api-now-available-in-self-service-early-access-ea) | February 3, 2021         |
| [Automatically mark a flow hook as "VERIFIED"](#automatically-mark-a-flow-hook-as-verified) | February 3, 2021         |
| [Event Hook preview tab now in Early Access (EA)](#event-hook-preview-tab-now-in-early-access-ea)      | February 3, 2021          |
| [Wildcards for OAuth redirect subdomains](#wildcards-for-oauth-redirect-subdomains) | February 3, 2021         |
| [Charset parameter no longer added in content-type header](#charset-parameter-no-longer-added-in-content-type-header) | February 3, 2021         |
| [Bug fixed in 2021.02.0](#bug-fixed-in-2021-02-0) | February 3, 2021         |

#### Okta Org API now available in Self-Service Early Access (EA)

The Okta Org API is now available in Self-Service EA. This API allows you to manage your org account settings, contact information, logo, Okta support settings, Okta communication settings, and preferences. See [Org API](/docs/reference/api/org/).<!--OKTA-325713-->

#### Automatically mark a flow hook as "VERIFIED"

When a request is made to `/api/v1/eventHooks/{eventHookId}/lifecycle/verify` for an [Event Hook](/docs/reference/api/event-hooks/) that has an Okta Workflows endpoint configured, the Event Hook is automatically marked as "VERIFIED". The verification step isn't required.<!--OKTA-364393-->

#### Event Hook preview tab now in Early Access (EA)

Event Hooks configured in the Admin Console or by [Event Hooks Management API](https://developer.okta.com/docs/reference/api/event-hooks/) can now preview the JSON body of the Event Hook in the Admin Console, as well as delivering the preview request to your external service without manually triggering an actual event.

Previewing the JSON body of the Event Hook assists developers or administrators create or troubleshoot the request syntax. The JSON body can also be edited for different request scenarios.

See [Event Hook Preview](https://help.okta.com/en/prod/Content/Topics/automation-hooks/event-hooks-preview.htm).<!--OKTA-364119-->

#### Wildcards for OAuth redirect subdomains

Developers can now use the [Apps API](/docs/reference/api/apps/#settings-10) to set multiple redirect URI subdomains with a single parameter using the asterisk (*) wildcard. This feature provides convenience and flexibility in cases where subdomains vary by only a few characters. For example: `https://subdomain*.example.com/oidc/redirect` may be used to represent subdomain1, subdomain2, and subdomain3.

>**Note:** Potential risks of using this feature include scenarios whereby attackers could illegitimately gain access to authorization codes by crafting the requested `redirect_uri` so that the code is returned to a subdomain that they control. See the [Authorization Code Redirection URI Manipulation](https://tools.ietf.org/html/rfc6749#section-10.6) section and the [Open Redirectors](https://tools.ietf.org/html/rfc6749#section-10.15) section of The OAuth 2.0 Authorization Framework.<!--OKTA-364361-->

#### Charset parameter no longer added in content-type header
To be compliant with the [RFC for JSON data interchange format](https://tools.ietf.org/html/rfc8259#section-11)
, the charset parameter from application/json is no longer added in the Content-Type header of responses from Okta's API endpoints.<!--OKTA-365536-->

#### Bug fixed in 2021.02.0

When performing a GET on the [`/oauth2/v1/clients` endpoint](/docs/reference/api/oauth-clients/#list-client-applications) on an org that has a deactivated OIN client, a "404 resource not found" error occurred. (OKTA-365031)

## January

### Weekly Release 2021.01.1

| Change                                                    | Expected in Preview Orgs |
| --------------------------------------------------------- | ------------------------ |
| [Bugs fixed in 2021.01.1](#bugs-fixed-in-2021-01-1)       | January 13, 2021           |

#### Bugs fixed in 2021.01.1

* Active Directory (AD) bulk imports and RealTimeSync (RTS) failed when the Microsoft AD user profile contained `tokenGroups`, `tokenGroupsGlobalAndUniversal`, or `tokenGroupsNoGCAcceptable` attributes. (OKTA-354900)

* In the SmartSheet provisioning profile, admins were unable to change the **Group Priority** setting to **Combine values across groups** for the `smartsheet.userPermissions` variable. The error message "Not allowed to modify property userPermissions from the base schema" was returned. (OKTA-325187)


### Monthly Release 2021.01.0

| Change                                                                                              | Expected in Preview Orgs |
|-----------------------------------------------------------------------------------------------------|--------------------------|
| [Group object source property is now GA in Production](#group-object-source-property-is-now-ga-in-production) | January 7, 2021         |
| [New Apps API endpoints in Early Access (EA)](#new-apps-api-endpoints-in-early-access-ea) | January 7, 2021         |
| [Developers can now use SWA for testing SCIM app integrations](#developers-can-now-use-swa-for-testing-scim-app-integrations)      | January 7, 2021          |
| [The Subscriptions API is now available in Self-Service Early Access (EA)](#the-subscriptions-api-is-now-available-in-self-service-early-access-ea) | January 7, 2021          |
| [New phone rate limits](#new-phone-rate-limits) | January 7, 2021          |
| [WebAuthn feature validation updates with Trusted Origins API](#webauthn-feature-validation-updates-with-trusted-origins-api) | January 7, 2021         |
| [Bug fixed in 2021.01.0](#bug-fixed-in-2021-01-0) | January 7, 2021         |

#### Group object source property is now GA in Production

For [Groups API](/docs/reference/api/groups/) requests that return a Group or a list of Groups, the Group object type APP_GROUP includes a `source` property that provides the ID of the source application for the returned Group. This property is now GA in Production. See [Group attributes](/docs/reference/api/groups/#group-attributes).<!--OKTA-326611-->

#### New Apps API endpoints in Early Access (EA)

The [Apps API](/docs/reference/api/apps/) now includes additional Early Access endpoints and objects for provisioning connections and features:

- [Application Logo operations](/docs/reference/api/apps/#application-logo-operations) (`/apps/${applicationId}/logo`)
- [Application Provisioning Connection operations](/docs/reference/api/apps/#application-provisioning-connection-operations) (`/apps/${applicationId}/connections`)
- [Application Features operations](/docs/reference/api/apps/#application-feature-operations) (`/apps/${applicationId}/features`)
- [Provisioning Connection object](/docs/reference/api/apps/#provisioning-connection-object)
- [Provisioning Connection Profile object](/docs/reference/api/apps/#provisioning-connection-profile-object)
- [Application Feature object](/docs/reference/api/apps/#application-feature-object)

These updates improve the ability of administrators to configure application logos and provisioning details, previously available only through the Admin Console.

>**Note:** Currently, only the Okta Org2Org application supports Application Provisioning Connection and Application Features operations. <!--OKTA-335123-->

#### Developers can now use SWA for testing SCIM app integrations

ISVs and developers who want to create and submit a SCIM-only app integration to the OIN can now use SWA as the sign-in method for SCIM app testing.<!--OKTA-352742-->

#### The Subscriptions API is now available in Self-Service Early Access (EA)

The [Subscriptions API](/docs/reference/api/admin-notifications/) is now available in Self-Service EA. The Subscriptions API provides operations to manage email subscription settings for Okta administrator notifications.<!--OKTA-325794-->

#### New phone rate limits

Users who attempt Voice and SMS enrollment can now be rate limited. Voice and SMS enrollment rate-limit events are now logged in the System Log.

See [System Log events for rate limits](/docs/reference/rl-system-log-events).<!--OKTA-355134-->

#### WebAuthn feature validation updates with Trusted Origins API

The WebAuthn feature now supports trusted cross-origin and cross-Relying Party Identifier (RP ID) validation when using the [Trusted Origins API](/docs/reference/api/trusted-origins/). Trusted Origins are configured in the Okta Trusted Origins framework either through the Admin Console or using the API. These Trusted Origins, configured with the CORS scope, now support orgs using WebAuthn for sign-in pages hosted at Trusted Origins distinct from the org's Okta URL (that is, different from the org's Okta or custom domain URL).
<!--OKTA-352629-->

#### Bug fixed in 2021.01.0

Non-CORS requests to the OAuth 2.0 `/introspect` and `/revoke` endpoints failed when the Okta session cookie was present. (OKTA-356288)
