# mrerp.in

The public website for MisterERP: `index.html`, `privacy.html`, `404.html`, one `style.css`, the
favicons (made from the app logo `Mister/Mister.svg`) and `CNAME`. Plain HTML: no scripts, cookies,
analytics or build step.

The MisterERP application itself is a separate repo, checked out at `C:\MisterERP`.

## Privacy policy

`privacy.html` is the page Google's OAuth consent screen links to. It covers only what MisterERP
does with Google data (Gmail send, Drive backup); other features (AI invoice import, WhatsApp,
licensing) get a section when they ship. Keep it matching the scopes MisterERP actually requests,
and change the date at the top whenever the policy changes.

## Hosting

GitHub Pages, deployed from `main`, root folder. Every push is live a minute or two later.
`mrerp.in` is registered at GoDaddy and its DNS stays there:

| Type  | Name | Value |
|-------|------|-------|
| A     | @    | 185.199.108.153, 185.199.109.153, 185.199.110.153, 185.199.111.153 |
| AAAA  | @    | 2606:50c0:8000::153, 2606:50c0:8001::153, 2606:50c0:8002::153, 2606:50c0:8003::153 |
| CNAME | www  | mehrotratechlabs.github.io |
| TXT   | _github-pages-challenge-mehrotratechlabs | GitHub domain verification |

HTTPS is enforced. Changing the custom domain in the Pages settings makes GitHub commit to
`CNAME`, so `git pull` before the next push.
