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