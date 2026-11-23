# astronlabs57.github.io

Astron Labs website – app portfolio, privacy policies and legal notice.
Served via GitHub Pages at **https://astronlabs.dev** (see `CNAME`). Plain static HTML, no build step.

## Structure

| Path | Purpose |
|---|---|
| `index.html` | Landing page / app portfolio (inline CSS) |
| `privacy.html` | Privacy overview: links to all app policies + website privacy policy |
| `privacy/<app>.html` | Per-app privacy policy (`yummykids`, `airfryerbuddy`, `workouttimer`, `chargelocator`, `russianradio`) |
| `impressum.html` | Legal notice (Impressum, § 5 DDG) |
| `assets/legal.css` | Shared styles for legal pages |
| `app-ads.txt` | AdMob authorized sellers – must stay at the domain root |

## Privacy policy URLs (Play Console)

- YummyKids: https://astronlabs.dev/privacy/yummykids.html
- Airfryer Buddy: https://astronlabs.dev/privacy/airfryerbuddy.html
- Workout Timer: https://astronlabs.dev/privacy/workouttimer.html
- Charge Locator: https://astronlabs.dev/privacy/chargelocator.html
- RussianRadio: https://astronlabs.dev/privacy/russianradio.html (app not yet on the landing page – add it to `index.html` once live)

Never rename or delete these files – Google Play rejects/suspends apps whose policy URL breaks.

## Maintaining policies

Policies describe what each app actually does (permissions, SDKs, network hosts, local storage, backup rules).
When an app adds a permission, SDK, network endpoint or changes backup rules, update its policy **and** the
Play Console Data safety form, then bump "Last updated".

## Local preview

Pages use root-absolute paths (`/assets/legal.css`), so open them via a local server, not `file://`:

```sh
python -m http.server 8000   # then open http://localhost:8000
```
