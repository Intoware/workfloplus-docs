---
layout: default
title: OAuth2
parent: Authentication
permalink: /authentication/oauth2

nav_order: 10
---

## OAuth2

{{site.product_name}} uses OAuth2 exclusively<sup>*1</sup> for authentication across all of its APIs.

More details as to the approaches and advantages that make OAuth2 a very good option for authentication can be found online, the primary source being the [IETFs own memo](https://datatracker.ietf.org/doc/html/rfc6749).

A developer or systems integrator working on an integration to {{site.product_name}} will need to follow a 2 stage process in order to access {{site.product_name}} APIs

1. Request or load a token
2. Make a request to an API using that token

### 1. Accessing a token

Tokens can be requested from the Identity Server; in order to gain a token you must provide valid credentials. Once signed in to {{site.product_name}} you can request a token from the [developer tools page]({{ site.accounts_dev_tools_url }}), however, manually requesting a token is not a useful approach for enabling an integration - you will want your integration to be able to request tokens from an API as they are needed.

The good news is that that API exists, however, for security reasons you cannot practicably access that API using your user credentials. Instead the recommended approach is to create a _machine to machine (M2M) client_, these clients are very similar to a user, they are enabled with one or more permissions that define what they are and aren't allowed to do, however, whilst a user in {{site.product_name}} represents a person, an M2M client represents a tool/product/integration that is permitted to interface with {{site.product_name}}.


### 2. Make an API Request

Once you have either generated a new token or loaded an existing token you'll need to include it in your request within a header of the form
```json
{
    "Authorization": "Bearer {token}"
}
```

#### Footnotes
<sub>*1 with the exception of the Query API, more information can be found in the Query API section</sub>
