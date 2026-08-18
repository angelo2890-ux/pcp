# PCP over the long run

A single-page worksheet that compares PCP deposits and interest rates across a
whole run of cars, not just one deal.

## What's in here

| File | What it is |
|---|---|
| `index.html` | The entire app, React and charts included. The only file that matters. |
| `manifest.webmanifest` | Makes it install as an app rather than a bookmark |
| `apple-touch-icon.png` | The home-screen icon on iPhone |
| `icon-192.png`, `icon-512.png` | Icons for Android / Chrome |
| `favicon-32.png` | The little tab icon |

## Putting it online (all in a browser, no software to install)

1. Go to **github.com/new**. Name the repo `pcp` — anything is fine.
   Set it to **Public**. Tick **Add a README file**. Click **Create repository**.
2. On the repo page click **Add file → Upload files**. Drag in every file from
   this folder. Scroll down, click **Commit changes**.
3. Click **Settings** (top of the repo) → **Pages** in the left sidebar.
4. Under *Build and deployment*, set **Source** to *Deploy from a branch*,
   **Branch** to `main` and the folder to `/ (root)`. Click **Save**.
5. Wait 1–2 minutes, then refresh that Settings → Pages screen. It'll show
   your address: `https://YOURNAME.github.io/pcp/`

## Getting it on the home screen

Open that address **in Safari** on the iPhone (not Chrome — only Safari can add
to the home screen properly on iOS).

Share button (the square with the arrow) → **Add to Home Screen** → **Add**.

It'll sit there with the red PCP stamp icon and open full-screen with no
address bar, like a real app.

## Changing it later

Go to the repo, click `index.html`, click the pencil icon, edit, commit.
The live site updates within a minute or so. If the phone shows the old
version, close the app fully (swipe up) and reopen it.

## Notes

- `index.html` is completely self-contained. React and the charting library are
  built into it, so there is no CDN to go missing and it works with no signal
  once Safari has it cached.
- Nothing is stored and nothing is sent anywhere. It's all worked out on the phone.
- The only thing loaded from outside is the two Google fonts. Without a
  connection it falls back to the system fonts and still works fine.
