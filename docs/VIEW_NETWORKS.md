# Viewing the interactive networks

Interactive network outputs live in `networks/` as `*.html` files.

## Recommended: download and open locally

1) Download the desired `*.html` file (and/or the whole `networks/` folder).
2) Open the file in a desktop browser (Chrome/Firefox/Safari).

### Download from GitHub (no coding)

1) Click **Code → Download ZIP**
2) Unzip the download
3) Open `networks/index.html` in a browser

### Download from Colab

If you generated or edited files in Colab, you can zip and download the folder:

```bash
!zip -r networks.zip networks
```

```python
from google.colab import files
files.download("networks.zip")
```

## Internet connection note

Some of the HTML outputs reference external CDN assets (e.g., `cdnjs` / `jsdelivr`), so viewing may require an internet connection.

## How to verify “works offline”

### No coding (recommended)

1) Disconnect from the internet (turn off Wi‑Fi).
2) Open `networks/index.html`, then open one of the network pages.

If the page is blank or unstyled, that page likely needs internet access to load its CDN assets.

Note: if you opened the page once while online, your browser may have cached the assets and it may still appear to work offline. To avoid a “cached” result, use a private/incognito window or a fresh browser profile.

### Optional: list which files reference CDNs

From the repo root:

```bash
rg -n "https?://" networks/*.html
```
