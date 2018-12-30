Security requirements for OpenID Connect Core 1.0 incorporating errata set 1 (https://openid.net/specs/openid-connect-core-1_0.html)

The raw requirements do not capture ALL requirements, but aims to capture ALL security requirements.  The standard does not explicitly mention for most requirements whether or not they are security requirements, so I have used my judgement to determine this.

Security requirements have been captured for the following response_types:
* Authorization code flow (corresponding to the 'web application' confidential client type defined by OAuth2 (RFC6749) section 2.1)
  * code 
* Hybrid flow (corresponding to the 'user-agent-based application' public client type defined by OAuth2 (RFC6749) section 2.1)
  * code id_token
  * code token
  * code id_token token

The Implicit flow is not considered.