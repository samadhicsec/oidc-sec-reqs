Security requirements for RFC 6749 The OAuth 2.0 Authorization Framework (https://tools.ietf.org/html/rfc6749)

The raw requirements do not capture ALL requirements, but aim to capture ALL security requirements.  The standard does not explicitly mention for most requirements whether or not they are security requirements, so I have used my judgement to determine this.

Security requirements have been captured for the following grant types:
* Authorization Code grant 
  * response_type=code 
* Client Credentials grant 
  * response_type=client_credentials

The Implicit and Resource Owner Password Credentials grants are not considered.

The files are as follows:

| File | Description | Requirements Count |
| ---- | ----| ---- |
| rfc6749-sec-reqs-raw.json    | Security requirements extracted directly from RFC 6749.  Categorised by section, role, flow, priority and step. | 99 |
| rfc6749-general-reqs.json | De-duplicated general (not flow specific) security requirements grouped by protocol stage, category, priority and response_type | 4 |
| rfc6749-client-reqs.json | De-duplicated Client security requirements grouped by protocol stage, category, priority and response_type | 34 |
| rfc6749-authz-server-reqs.json | De-duplicated Authorization Server security requirements grouped by protocol stage, category, priority and response_type | 67 |

The contents of the files (excluding rfc6749-sec-reqs-raw.json) are a JSON array of the following object:

| Key | Value Description |
| ---- | ----|
| id  | An internal ID, do not use |
| protocol_stage | One of: all, client-registration-request, client-registration-response, authn-request, consent, redirect, token-request, token-response |
| category | Arbitrary description of the part of the protocol_stage the requirement applies to |
| priority | One of: Must, Should, Could |
| requirement | Description of requirement relative the protocol_stage and category |
| response_type | The values of the response_type parameter sent in the authn-request that this requirement applies to.  One of: code, client_credentials |
| reference | The sections in the standard this requirement is derived from |