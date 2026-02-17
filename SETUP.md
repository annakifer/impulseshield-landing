# Landing Page Setup

## 1. Formspree (Email Capture)

Formspree's free tier gives you 50 submissions/month — plenty for validation.

### Steps:

1. Go to [formspree.io](https://formspree.io) and sign up with `impulseshield@gmail.com`
2. Click **"New Form"**
3. Name it "ImpulseShield Beta Signups"
4. Copy the **form endpoint** — it looks like: `https://formspree.io/f/xAbCdEfG`
5. Open `index.html` and find this line:
   ```html
   <form action="https://formspree.io/f/YOUR_FORM_ID" method="POST">
   ```
6. Replace `YOUR_FORM_ID` with your actual form ID (e.g. `xAbCdEfG`)
7. Save the file

### Test it:
- Open `index.html` in your browser
- Submit a test email
- Check your Formspree dashboard — the submission should appear there
- You'll also get an email notification at `impulseshield@gmail.com`

---

## 2. Netlify Deployment

Netlify's free tier includes unlimited static sites and custom domains.

### Option A: Deploy via GitHub (Recommended)

1. Push this repo to GitHub (if not already)
2. Go to [app.netlify.com](https://app.netlify.com) and sign up/log in with GitHub
3. Click **"Add new site" > "Import an existing project"**
4. Select the `impulseshield-landing` repo
5. Leave the **publish directory** blank (files are at the repo root)
6. Click **"Deploy site"**
7. Your site will be live at a random Netlify URL (e.g. `random-name.netlify.app`)
8. Optionally click **"Domain settings"** to set a custom subdomain like `impulseshield.netlify.app`

Every time you push to `main`, Netlify will auto-redeploy.

### Option B: Manual Deploy (Drag & Drop)

1. Go to [app.netlify.com](https://app.netlify.com)
2. Drag the `impulseshield-landing` folder onto the deploy area
3. Site is live immediately

---

## 3. Preview Locally

To preview the page before deploying, just open the HTML file in your browser:

```bash
open index.html
```

---

## 4. Custom Domain (Optional, Later)

If validation goes well and you want a real domain:

1. Buy a domain (Namecheap, Google Domains, etc.)
2. In Netlify, go to **Domain settings > Add custom domain**
3. Follow the DNS instructions Netlify provides
