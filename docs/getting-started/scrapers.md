---
title: Add scrapers
icon: material/magnify
---

# Step 5 — Add scrapers

Scrapers are how cli_debrid finds torrents for your content. You need at least one scraper configured before cli_debrid can add anything to your debrid account.

---

## Recommended for beginners

**Start with Zilean and Torrentio.** Both are free, require no self-hosting, and cover the vast majority of content.

| Scraper | Type | Requires | Best for |
|---|---|---|---|
| [Zilean](../scrapers/zilean.md) | Debrid cache index | Nothing | Speed — checks what's already cached in debrid |
| [Torrentio](../scrapers/torrentio.md) | Torrent indexer | Nothing | Wide coverage, easy setup |
| [MediaFusion](../scrapers/mediafusion.md) | Torrent indexer | Nothing (public) or self-hosted | High-quality results |
| [Jackett](../scrapers/jackett.md) | Torrent proxy | Self-hosted | Access to private trackers |
| [Prowlarr](../scrapers/prowlarr.md) | Torrent proxy | Self-hosted | Modern replacement for Jackett |
| [Nyaa](../scrapers/nyaa.md) | Torrent indexer | Nothing | Anime |

---

## Adding a scraper

1. Go to **Settings → Scraping**
2. Click **Add Scraper**
3. Select the scraper type and fill in the URL
4. Save

### Zilean (recommended first scraper)

Zilean indexes what's already cached in your debrid account. Hits are instant — no waiting for debrid to download.

Full guide: [:octicons-arrow-right-24: Zilean setup](../scrapers/zilean.md){ .md-button }

Default URL (public instance):
```
https://zileanfortheweebs.midnightignite.me
```

### Torrentio

Torrentio is a Stremio addon that also works as a scraper API. No account needed.

Full guide: [:octicons-arrow-right-24: Torrentio setup](../scrapers/torrentio.md){ .md-button }

Default URL:
```
https://torrentio.strem.fun
```

### MediaFusion

MediaFusion is a more advanced scraper with better filtering. Can be used with the public instance or self-hosted.

Full guide: [:octicons-arrow-right-24: MediaFusion setup](../scrapers/mediafusion.md){ .md-button }

---

## Scraper priority

Scrapers are checked in order. Put your fastest/most reliable scraper first:

1. Zilean (fastest — cache hits only)
2. Torrentio or MediaFusion (broader search)
3. Jackett/Prowlarr (private trackers, slowest)

Adjust order under **Settings → Scraping → Scraper Priority**.

---

## Testing a scraper

After adding a scraper, use **Settings → Debug → Test Scraper** to search for a known title and confirm results come back.

---

For full documentation on all supported scrapers and advanced configuration, see the [:octicons-arrow-right-24: Scrapers reference](../scrapers/index.md#available-scrapers).

---

## Next step

[:octicons-arrow-right-24: Step 6 — Add content sources](content-sources.md){ .md-button .md-button--primary }
