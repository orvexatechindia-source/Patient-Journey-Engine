# Enquira Engine: early-access demo

A working, clickable demo of **Enquira Engine** (₹14,999 per location a month, excluding GST), for clinics already on LeadSquared, Zoho, HubSpot, Practo or any other CRM. It runs entirely in the browser with a made-up clinic, Kovai Hair Clinic in RS Puram, Coimbatore. There is no server, no login and no real patient data, and it resets every time the page reloads.

## Try it on your computer

Open `site/index.html` in Chrome, Edge, Safari or Firefox. Press **Start the tour** in the panel at the bottom right and click **Next step** eight times:

Tamil WhatsApp enquiry → AI reply in seconds with consent → missed call answered by the AI receptionist in Tamil → red flag to a named counsellor → booking synced to LeadSquared → emergency alarm (press Accept and join) → visit sent back to Meta and Google Ads → the owner’s morning briefing.

## Push it to GitHub (one command)

You need Git and the [GitHub CLI](https://cli.github.com), signed in once with `gh auth login`.

| Computer | Private repository | Public repository with a free GitHub Pages site |
|---|---|---|
| Mac or Linux | `./push.sh` | `./push.sh enquira-engine-demo public` |
| Windows | `.\push.ps1` | `.\push.ps1 -Visibility public` |

With **public**, the included workflow publishes the demo to `https://<your-username>.github.io/enquira-engine-demo/` on every push, usually within a minute. GitHub Pages for **private** repositories needs a paid GitHub plan, so for a private repository host it with Vercel or Netlify instead.

## Host it on your temp domain

| Host | Steps |
|---|---|
| GitHub Pages | Push as **public**, then add your domain under Settings › Pages › Custom domain |
| Vercel | Import the repository; `vercel.json` already serves the `site` folder. Add your domain under Settings › Domains |
| Netlify | Import the repository; `netlify.toml` already publishes `site`. Add your domain under Domain management |

Search engines are told not to list the demo (`noindex` and `robots.txt`). Serve it over HTTPS.

## Link the two demos

To show a link to the other demo in the top ribbon, paste its address into this line near the top of `site/index.html`:

```html
<meta name="enquira-other-demo" content="">
```

## Before you share it

- Everything AI, calls, payments and integrations is simulated. The demo shows how the product works, not a live connection.
- The emergency alarm and test alarm play a beep.
- Prices are early-access prices and may change.
- Retention keeps public reviews and offers switched off with "Needs legal review", and the demo never shows testimonials or before-and-after images for promotion, in line with the NMC guidelines.
