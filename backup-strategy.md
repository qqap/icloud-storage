# Backup Strategy

## The Problem

- iCloud plan: 5GB free (was 100% full)
- Photos: **0 bytes local** — all photos exist only in iCloud
- WhatsApp backup: ~924MB eating iCloud quota
- iPhone backup: ~1.5GB in iCloud

If iCloud plan lapses, photos could be permanently deleted. Apple publishes no fixed deletion deadline.

## Why iCloud is Risky as a Solo Backup

- Month-to-month only — no annual prepay option
- Payment fails → drops to 5GB free tier immediately
- Data over 5GB stops syncing
- Apple deletes over-quota data within ~30 days (not guaranteed — no published timeline)
- **No fixed deadline = data loss on Apple's schedule, not yours**

## iPhone Backup Options

| Option | Cost | Risk | Notes |
|--------|------|------|-------|
| iCloud only | $1/mo (50GB) | High if payment lapses | Current setup |
| Local Mac (Finder) | Free | Low | Manual, cable required |
| Local Mac + iCloud | $1/mo | Very low | Best of both |

## Recommended: Local Mac Backup

Plug iPhone into Mac → open Finder → select iPhone → **Back Up Now**.

- Includes everything: WhatsApp, photos, apps, settings
- Stored on Mac, not Apple's servers
- Free, no subscription dependency
- Do monthly

Once local backup is set up, the WhatsApp iCloud backup can be deleted to free ~924MB:
> iPhone → Settings → [your name] → iCloud → Manage Storage → WhatsApp → Delete Data

## WhatsApp on iPhone

**Note:** WhatsApp on iPhone only backs up to iCloud. Google Drive backup is Android-only.
Local Mac backup (via Finder) covers WhatsApp as part of the full iPhone backup.

## Photos

All photos are cloud-only (0 bytes local). Before reducing iCloud plan:
1. Do a full local Mac backup via Finder (includes photos)
2. Or download photos manually via Image Capture app
