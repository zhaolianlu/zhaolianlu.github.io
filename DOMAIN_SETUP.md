# Custom Domain Setup

The site should first remain available and verified at `https://zhaolianlu.github.io/`. Do not activate the custom domain until DNS ownership and routing have been confirmed.

## DNS record

Create this record with the DNS provider for `zhaolianlulab.org`:

| Type | Host | Target |
|---|---|---|
| CNAME | `www` | `zhaolianlu.github.io` |

Do not include `https://` or a path in the target.

## GitHub Pages configuration

After DNS propagation:

1. Open the authorized repository's **Settings > Pages**.
2. Enter `www.zhaolianlulab.org` as the custom domain.
3. Wait for GitHub's DNS check to succeed.
4. Enable **Enforce HTTPS** after the certificate is issued.
5. Verify both the custom domain and `https://zhaolianlu.github.io/` behavior.

## Hugo base URL

The additive configuration currently uses `https://zhaolianlu.github.io/` so the initial deployment works without DNS. Changing the production base URL to `https://www.zhaolianlulab.org/` requires editing the newly created `config/_default/zz_lab.yaml` after the custom domain is active.

