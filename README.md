# Bishop Fox

Bishop Fox is an offensive security firm delivering penetration testing, red teaming, application and cloud
security assessment, and continuous threat exposure management. Its managed **Cosmos** platform keeps a
living inventory of an organization's external attack surface — domains, subdomains, DNS records, network
ranges, IP addresses, open ports, and IP/hostname services — pairing continuous automated discovery with
human operator validation so customers receive triaged, exploitable findings instead of scanner noise.

- Website: https://bishopfox.com/
- Cosmos platform: https://bishopfox.com/services/cosmos
- Cosmos portal: https://cosmos.bishopfox.com/
- GitHub: https://github.com/BishopFox
- Open source tools: https://bishopfox.com/tools
- Vulnerability disclosure policy: https://bishopfox.com/vulnerability-disclosure-policy

## API surface

| | |
|---|---|
| API | Bishop Fox Cosmos API (v5) |
| Base URL | `https://api.cosmos.bishopfox.com/` |
| Auth | OAuth 2.0 client credentials → Bearer JWT (`https://bishopfox.auth0.com/oauth/token`, audience `cosmos_public`) |
| Reference docs | Portal-gated (inside `cosmos.bishopfox.com`) |
| OpenAPI | **Not published** — see `well-known/bishop-fox-well-known.yml` for the full probe table |
| Previous version | v1, retired 2025-12-05 |

The API is live and reachable: `/v5/*` resources return `401 {"message":"Unauthorized"}` to anonymous
callers. No OpenAPI, AsyncAPI, GraphQL, MCP server, or A2A agent card is published anywhere on
`bishopfox.com`, `api.cosmos.bishopfox.com`, or `cosmos.bishopfox.com`.

## Artifacts

| Dir | File | Method |
|---|---|---|
| `llms/` | `bishop-fox-llms.txt` | searched (verbatim from `bishopfox.com/llms.txt`) |
| `well-known/` | `bishop-fox-security.txt`, `bishop-fox-openid-configuration.json`, `bishop-fox-oauth-authorization-server.json`, `bishop-fox-well-known.yml` | searched |
| `authentication/` | `bishop-fox-authentication.yml` | searched |
| `scopes/` | `bishop-fox-scopes.yml` | searched |
| `conventions/` | `bishop-fox-conventions.yml` | searched |
| `errors/` | `bishop-fox-problem-types.yml` | probed (live 401/404 envelopes) |
| `lifecycle/` | `bishop-fox-lifecycle.yml` | searched |
| `conformance/` | `bishop-fox-conformance.yml` | derived |
| `data-model/` | `bishop-fox-data-model.yml` | searched |
| `packages/` | `bishop-fox-packages.yml` | searched |
| `security/` | `bishop-fox-domain-security.yml`, `bishop-fox-vulnerability-disclosure.yml` | probed / searched |
