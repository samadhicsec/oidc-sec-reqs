Security requirements for OpenID Connect Core 1.0 incorporating errata set 1 (https://openid.net/specs/openid-connect-core-1_0.html)

The raw requirements do not capture ALL requirements, but aims to capture ALL security requirements.  The standard does not explicitly mention for most requirements whether or not they are security requirements, so I have used my judgement to determine this.

Security requirements have been captured for the following response_types:
* Authorization code flow (categorized by: all tokens returned from Token Endpoint; Tokens NOT revealed to User Agent; Client can be authenticated; Refresh Token possible)
  * code 
* Hybrid flow (categorized by: NOT all tokens returned from Token Endpoint; Tokens revealed to User Agent; Client can be authenticated; Refresh Token possible)
  * code id_token
  * code token
  * code id_token token

The Implicit flow is not considered.

The contents of the files are as follows:

| File | Description | Requirements Count |
| ---- | ----| ---- |
| oidc-core-sec-reqs-raw.json    | Security requirements extracted directly from the OIDC standard.  Categorised by section, role, flow, priority and step. | 167 |
| oidc-core-client-reqs.json | De-duplicated Client security requirements grouped by protocol stage, category, priority and response_type | 26 |
| oidc-core-token-validation.json | De-duplicated ID token validation security requirements grouped by protocol stage, category, priority and response_type | 24 |
| oidc-core-authz-server-reqs.json | De-duplicated Authorization Server (a.k.a OpenID Provider (OP), Relying Party) security requirements grouped by protocol stage, category, priority and response_type | 80 |