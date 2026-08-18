# Volkswagen Chelmsford — quotation tool

Two pages, no server, no accounts, nothing sent anywhere.

| Page | What it does |
|---|---|
| `index.html` | **Quote.** Price, deposit, term, mileage and rate in, monthly payment out. PCP by default, Hire Purchase on a toggle. |
| `overtime.html` | **Over time.** The original worksheet — what a run of PCP deals costs across ten or twenty years, and whether the rate or the deposit is the thing worth negotiating. |

## Files

| File | What it is |
|---|---|
| `index.html` | The quote calculator. Self-contained. |
| `overtime.html` | The long-run worksheet. Self-contained. |
| `manifest.webmanifest` | Makes it install as an app rather than a bookmark |
| `apple-touch-icon.png` | The home-screen icon on iPhone |
| `icon-192.png`, `icon-512.png` | Icons for Android / Chrome |
| `favicon-32.png` | The little tab icon |

## How the figures are worked out

Payments are monthly in arrears, the first one a month after delivery. On a PCP
the term carries one payment fewer than its length — a 48-month agreement is 47
payments and then the optional final payment in month 48, which is how
Volkswagen Financial Services write it. The APR is converted to a monthly rate
and the optional final payment is discounted back over the full term.

The optional final payment is estimated from a residual curve that takes the
term, the annual mileage, whether the car is new or used, and whether it is
electric or not. Electric cars carry a much lower guaranteed future value —
around 28% of the price over four years against roughly 41% for petrol and
diesel. The curve is calibrated against published Volkswagen representative
examples and reproduces their monthly figures to within about 20p. It is still
an estimate: the real guaranteed future value is set by VWFS and can differ, so
type the real one in when you have it.

Not included: road fund licence, insurance, excess mileage, damage beyond fair
wear and tear, or any acceptance fee. Nothing here is a quotation.

## Putting it online

1. Go to **github.com/new**. Name the repo `pcp`. Public. Tick
   **Add a README file**. **Create repository**.
2. **Add file → Upload files**. Drag in every file from this folder.
   **Commit changes**.
3. **Settings → Pages**. Source *Deploy from a branch*, branch `main`,
   folder `/ (root)`. **Save**.
4. A minute later it's live at `https://YOURNAME.github.io/pcp/`

## Getting it on the home screen

Open the address **in Safari** on the iPhone. Share button → **Add to Home
Screen** → **Add**. It opens full-screen with no address bar.

## Changing it later

Open the repo, click the file, click the pencil, edit, commit. The live site
updates within a minute. If the phone still shows the old version, close the
app fully and reopen it.
