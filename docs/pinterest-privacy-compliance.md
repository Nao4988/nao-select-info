# Pinterest privacy and developer-compliance review

Reviewed: 2026-09-17

This note records a conservative review of Nao Select against current official Pinterest sources. It is not legal advice and does not reinterpret an unclear permission as approval.

## Official sources

- [Pinterest Developer Guidelines](https://policy.pinterest.com/en/developer-guidelines)
- [Pinterest Developer and API Terms](https://developers.pinterest.com/terms/)
- [Pinterest API access tiers](https://developers.pinterest.com/docs/key-concepts/access-tiers/)
- [Connect an app](https://developers.pinterest.com/docs/getting-started/connect-app/)
- [Authentication and authorization](https://developers.pinterest.com/docs/getting-started/set-up-authentication-and-authorization/)

## Confirmed requirements

The official guidance requires an accurate privacy policy linked during API-access application. Pinterest's Trial guidance states that the policy URL must load completely, be publicly accessible, and be hosted on a domain clearly associated with the app.

Pinterest account access must use authorization such as an access token. An app must not solicit Pinterest passwords, session cookies, or other login credentials. API credentials must remain private. Nao Select therefore keeps app secrets and tokens out of this repository, databases, logs, and URLs.

Pinterest API information must not be sold or shared with a third party, including another advertising service. Account information must not be combined with other services except where required for the service provided to the account holder. Pinterest Materials must not be used to train or improve AI or machine-learning models without Pinterest's express permission. Nao Select therefore does not send Pinterest API data to an external AI service or to Rakuten.

Pinterest also requires the end user to knowingly choose each publishing action. Nao Select's intended design uses per-item review and an explicit Safety Gate rather than background or unreviewed bulk publishing.

## Data-persistence finding

The Developer Guidelines state that, except for campaign analytics for the developer's own account or an account whose holder expressly granted access, information accessed through Pinterest Materials including the API may not be stored; the API should be called when the information is needed.

Accordingly, synthetic schemas and mock identifiers may be used for local tests, but they do not establish permission to persist identifiers or other values returned by the real Pinterest API. Until each real response field and permitted retention basis is documented, Nao Select must block any path that would persist real Pinterest API response data.

Compliance state:

`BLOCKED_PINTEREST_API_DATA_PERSISTENCE_TERMS_REVIEW`

This state must remain open before any live Sandbox operation that could persist Board IDs, Pin IDs, response metadata, or other Pinterest API-derived values. Campaign analytics, if later enabled, must be limited to an authorized account, a defined purpose, and the minimum necessary retention period.

## Current public-policy alignment

- The tool is described as personal, local, and under development.
- Dry-run is the current default; live Pinterest API use is not claimed.
- Password and session-cookie collection is explicitly excluded.
- Credentials remain local and are not published.
- Pinterest API data is not sent to external AI services, sold, or shared.
- Real Pinterest API data is not described as permanently stored.
- Pinterest publishing requires deliberate user review and Safety Gates.
- The tool is not directed to children under 13.

## Items requiring confirmation before live use

- Field-by-field classification of every Pinterest API response value.
- Whether any operational identifier needed for write reconciliation may be retained, and under what documented Pinterest permission.
- Deletion or non-persistence behavior for real Board, Pin, and operation-response identifiers.
- Any future Analytics retention period and account-authorization evidence.
- Re-review of the then-current Developer Guidelines and Developer and API Terms immediately before live Sandbox use.
