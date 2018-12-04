---
title: Call My API from My Machine-to-Machine (M2M) App
description: Everything you need to know to call your API from your machine-to-machine (M2M) app.
ctaText: Go to Quickstart
ctaLink: /docs/quickstart/backend
template: microsite
topics:
  - authentication
  - oauth2
  - m2m
useCase:
  - call-api
---

Using Auth0 in your applications means that you will be "outsourcing" the authentication process to a centralized login page in the same way that Gmail, YouTube, and any other Google property redirects to [accounts.google.com](http://accounts.google.com) whenever a user signs in.

With machine-to-machine (M2M) apps, however, the system authenticates and authorizes the app rather than a user.

## How it works

When your app needs to fetch user data from your API:

1. Your M2M application authenticates with your Auth0 Authorization Server.
2. Auth0 responds with an Access Token.
3. The Access Token can be used to call your API and retrieve requested data.

For M2M applications, Auth0 uses the [M2M Flow](/flows/concepts/m2m-flow).

<img src="/media/articles/microsites/overview-flow-call-api-m2m-app.png" alt="Flow Overview for Machine-to-Machine Apps" width="100%">

## Implementation overview

::: steps
  1. <strong>Configure your API</strong><br/><br/>Once you have created your API, you will need to authorize your M2M application and configure any scopes that applications can request during authorization.

  2. <strong>Get an Access Token</strong><br/><br/>Your app requests an Access Token from your Auth0 Authorization Server using the [M2M Flow](/flows/concepts/m2m-flow).

  3. <strong>Call your API</strong><br/><br/>When your app calls your API, it includes the retrieved Access Token in the HTTP Authorization header.

:::


The easiest way to implement the M2M Flow is to [follow our Backend/API Quickstarts](/quickstart/backend).

Or, to use our API endpoints, you can follow our tutorial: [Call My API Using the M2M Flow](/flows/guides/m2m-flow/call-api-using-m2m-flow).

:::: further-reading

::: guides
  * [Auth0 Backend/API Quickstarts](/quickstart/backend)
  * [Call My API Using the M2M Flow](/flows/guides/m2m-flow/call-api-using-m2m-flow)
  * [Change scopes and add custom claims to tokens using hooks](/api-auth/tutorials/client-credentials/customize-with-hooks)
:::

::: references
  * [SDKs](/libraries)
  * [Auth0 Authentication API](/api/authentication)
  * [OAuth 2.0](/protocols/oauth2)
:::

::: concepts  
  * [Access Tokens](/tokens/access-token)
  * [Where to store tokens](/security/store-tokens)
:::

::::

::: whats-next
  * Auth0 offers many ways to personalize your user's login experience and customize tokens using [rules](/rules) and [hooks](/hooks).
  * If you are building your own API and you want to secure the endpoints using Auth0, see [Protect My API](/microsites/protect-api/protect-api).
  * Learn more about the ways Auth0 can help you [manage user profiles](/microsites/manage-users/manage-users-and-user-profiles) and [maintain custom user data]().
:::