# BSCG Business Owner Tax Strategy Fact Finder

Client-facing interactive click-through based on the BSCG Business Owner Tax Strategy Fact Finder PDF.

## Live site (standalone — not Retirement Everest)

https://jonray757-hue.github.io/bscg-fact-finder/

## Client link with advisor pre-filled

```
https://jonray757-hue.github.io/bscg-fact-finder/?advisor=Johnny%20Harris&email=johnny@retirementfoundationforamerica.com
```

### Fondako leads (tagged in Strategy GHL via Make)

```
https://jonray757-hue.github.io/bscg-fact-finder/?source=fondako&advisor=Johnny%20Harris&email=johnny@retirementfoundationforamerica.com
```

Or: `?brand=fondako` / `?fondako=1`

Other sources (examples):
```
?source=website
?source=organic
?utm_source=google
```

Submit posts to Make.com (`hook.us2.make.com/...`):
- **All contacts** land in the **Strategy** GHL sub-account (not BSCG)
- **Fondako** vs website / organic / etc. = **tags only** (`is_fondako`, `source_tag`, `tags[]`)
- Fact-finder notes are in the payload as `notes` for the contact

## Deploy

Repo: `jonray757-hue/bscg-fact-finder` only. Do not nest under `retirement-everest`.

```bash
cd /Users/ramseykoaharris/Work/projects/bscg-fact-finder
./tools/push-to-github.sh
```

Enable Pages: Repo → Settings → Pages → **GitHub Actions**.

## Local preview

Open `index.html` in a browser, or:

```bash
cd /Users/ramseykoaharris/Work/projects/bscg-fact-finder
python3 -m http.server 8080
```

Then visit http://localhost:8080

## Deploy

Pushes to `main` auto-deploy via GitHub Actions (`.github/workflows/deploy-pages.yml`).

```bash
./tools/push-to-github.sh
```