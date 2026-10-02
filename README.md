# tadhkiruk.app — public website

Plain static HTML/CSS. No build step, no dependencies, independent of the Flutter app.

- Arabic (default, RTL) at the root; English under `/en/`.
- Pages: home, privacy, terms, support, delete-data.
- Contact address used everywhere: `support@tadhkiruk.app`.

## Deploy (Cloudflare Pages, free)

1. Register `tadhkiruk.app` at Cloudflare Registrar (sold at cost).
2. Cloudflare dashboard → Workers & Pages → Create → Pages → Upload assets,
   drag in this `website/` folder (or connect the git repo and set the build
   output directory to `website`, with no build command).
3. Pages project → Custom domains → add `tadhkiruk.app`.
4. Email → Email Routing → create `support@tadhkiruk.app` forwarding to your
   real inbox, and confirm the verification email.

## URLs to give the stores

- Privacy policy: https://tadhkiruk.app/privacy.html
- Account/data deletion: https://tadhkiruk.app/delete-data.html
- Support: https://tadhkiruk.app/support.html

When the policy text changes, update `privacy.html`, `en/privacy.html`, and
`lib/features/settings/presentation/screens/privacy_policy_screen.dart`
together, plus the "last updated" date in each.
