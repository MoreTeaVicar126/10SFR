# 10SFR Games

A small GitHub Pages site for form 10SFR.

Live address: https://moreteavicar126.github.io/10SFR/

```
index.html          Landing page: links to the games, QR code, install steps
sheet.html          Printable A4 sheet (open it, then press "Print this sheet")
qr/                 QR code images (index, biscuits, dice, stockman)
biscuits/           Brody's Biscuits   (index.html, manifest.json, sw.js, icons/)
dice/               Dice Games         (same layout)
stockman/           Max the Stockman   (same layout)
```

Each game is its own installable app (PWA): it has a `manifest.json`, a service
worker `sw.js` that saves it for offline play, and icons.

## Putting it on GitHub

1. Sign in to GitHub as **MoreTeaVicar126**.
2. Create a new **public** repository called **10SFR** (capital letters, exactly as written).
3. Choose **Add file, Upload files** and drag in everything inside this folder
   (including the `biscuits`, `dice`, `stockman` and `qr` folders), then **Commit changes**.
4. Go to **Settings, Pages**. Under **Build and deployment**, choose
   **Deploy from a branch**, branch **main**, folder **/ (root)**, then **Save**.
5. After a minute or two the site appears at the address above.
6. On your own phone, open the address, tap each game and check it installs.

## Changing a game later

Replace that game's `index.html`, but keep the block of lines that starts
`<link rel="manifest"` just before `</head>`. Then open that game's `sw.js` and
change `const VERSION = 'v1';` to `'v2'` so phones fetch the new copy.

## If you use a different repository name

The QR codes point at `https://moreteavicar126.github.io/10SFR/`. If the repository
is called something else, the QR codes must be regenerated with the new address.
