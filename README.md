# rugbyhubby.com
# rugbyhubby.com

Personal landing page for [rugbyhubby.com](https://rugbyhubby.com) — a home for my writing, photography, and the tools I build along the way.

## What this is

A single-page static site built with plain HTML and CSS, hosted on GitHub Pages and served via Cloudflare.

## Stack

| Layer | Service |
|---|---|
| Domain registrar | Hostinger |
| DNS & security | Cloudflare (free) |
| Hosting | GitHub Pages (free) |
| SSL | Cloudflare (automatic) |
| Email routing | Cloudflare Email Routing (free) |

## Email

Inbound email to `bill@rugbyhubby.com` and `contact@rugbyhubby.com` is forwarded via Cloudflare Email Routing to a personal inbox. No mail server required.

## DNS setup

| Type | Name | Purpose |
|---|---|---|
| A | @ | GitHub Pages (×4 IPs) |
| CNAME | www | GitHub Pages |
| MX | @ | Cloudflare Email Routing |
| TXT | @ | SPF record (email security) |
| TXT | _dmarc | DMARC record (anti-spoofing) |

## Structure

```
/
└── index.html       # Single-page landing site
└── README.md        # This file
```

## Updating the site

To make changes, edit `index.html` directly in this repo (or clone locally) and commit to `main`. GitHub Pages deploys automatically within a minute or two.

### Annual donation link update

In `index.html`, find the donate button near the bottom and update the `href`:

```html
<!-- UPDATE THIS LINK EACH YEAR WITH THE CURRENT DONATION URL -->
<a class="donate-btn" href="YOUR_DONATION_LINK_HERE" target="_blank" rel="noopener">Donate →</a>
```

## Future plans

- [ ] Add tools section — `rugbyhubby.com/wellness`
- [ ] Add tools section — `rugbyhubby.com/guitar`
- [ ] Add Multiple Myeloma awareness/donation detail page
