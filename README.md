# CCF mockup — client preview on Vercel

A self-contained static preview of the CCF landing page. `index.html` already includes the image and scripts, so there's no build step.

`vercel.json` sends `noindex` headers so search engines won't index the mockup. Remove them when the real site launches.

## Deploy (about 5 minutes)

1. **Create a GitHub repo**
   - On github.com, go to New repository. Name it something like `ccf-mockup` and make it Private.
   - Use "uploading an existing file" and drag in `index.html`, `vercel.json` and this README. Commit.
2. **Import the repo into Vercel**
   - Go to vercel.com, then Add New → Project → Import your GitHub repo.
   - Framework Preset: **Other**. Leave Build Command and Output Directory empty. Root Directory: `./`.
   - Click **Deploy**.
3. **Share the link**
   - Vercel gives you a URL like `ccf-mockup.vercel.app`.
   - Optional: rename it under Project → Settings → Domains (e.g. `ccf-preview.vercel.app`).
   - Optional: password-protect it under Settings → Deployment Protection. Password protection requires a paid plan. Vercel Authentication is free but requires the viewer to have a Vercel account.

## Updating

Replace `index.html` in the repo and commit. Vercel redeploys automatically.

## Notes for the client walkthrough

- The contact form uses a placeholder Web3Forms key. Submitting shows the success state, but **no email is sent** in the mockup.
- The striped boxes are image placeholders with art direction notes.
- The CAPTCHA box is a placeholder for Turnstile/hCaptcha.
- Fonts render with system fallbacks (Helvetica/Arial) until the self-hosted fonts are added in the production build.
