# oidc-sec-reqs

This repo gives the technical security requirements for implementing an OIDC Client leveraging the OIDC authorization code flow.

The requirements (for the most part) originate from the following standards (and each requirement references the corresponding standard calling for that requirement): 
* OIDC-TV - OIDC Core 1.0, 3.1.3.7 ID Token Validation 
* OIDC-Sec - OIDC Core 1.0, 16 Security Considerations 
* OIDC-Comp - OpenID Connect Relying Party Certification, Authorization Code flow 
* OAuth2-Sec - Security Considerations from OAuth 2.0, RFC6749 
* OAuth2-TM - OAuth2.0 Threat Model Considerations, RFC6819 
* OAuth2-BSP - OAuth 2.0 Security Best Current Practice, Draft 05

To understand the requirements the following terminology is used:

* OP - Is the OpenID Provider, this is the same as the Identity Provider (IdP) and for OIDC in the context of OAuth is the same as the Authorisation Server (AS).
* Client - a.k.a the Relying Part (RP), is the application that requires the user's ID Token to identify the user, and the access token/refresh token to query the Token and UserInfo Endpoints.

OIDC comes in different variations and options, and OAuth2 is a framework, so the following assumptions or restrictions are in place for these requirements:
* Only using Authorisation Code flow
* Not supporting encrypted requests (Authorisation, Token, UserInfo)
* Not supporting signed requests (Authorisation, Token, UserInfo)
* Not supporting encrypted ID Tokens
* The 'none' signing algorithm is not supported
* Not supporting webfinger for discovery
* Not supporting dynamic registration by Client
* Not supporting Request Object By Reference
* Not supporting Distributed Claims
* Not supporting Aggregated Claims