# 👒 op-tcg-data

Collection of datasets for One Piece TCG.

## Where is the scraper?

For practical reasons, scraper code is kept in a separate repository: https://github.com/Coko7/op-tcg-scraper

## 🃏 Datasets

Supported datasets:
- [English version](https://en.onepiece-cardgame.com)
- ⚠️ [Japanese version](https://www.onepiece-cardgame.com)

Each dataset includes its own `cards.json` as well as images for all card arts.
Japanese version has more data (more cards and images) than English version.

## ⚠️ Disclaimer

I had some trouble when fetching data for the japanese version (`jp`):
- Wrong formatting/missing data for `colors` or `counter` values on some cards
- Duplicate cards with same data and art

These issues are with the original data itself and I did not find a clean/reliable way to handle them.
I tried to patch them by writing some custom code when fetching data for the `jp` version.
Fortunately, the `en` version does not seem to suffer from these problems.
So, keep this in mind when picking a dataset. I would recommend working with the `en` dataset.

## 🗃️ File structure

```
data/
├── en/
│   ├── images/
│   │   ├── EB01-001.png
│   │   ├── EB01-001_p1.png
│   │   ├── ...
│   │   ├── ST14-016.png
│   │   └── ST14-017.png
│   └── cards.json
└── jp/
    ├── images/
    │   ├── EB01-001.png
    │   ├── EB01-001_p1.png
    │   ├── ...
    │   ├── ST20-004.png
    │   └── ST20-005.png
    └── cards.json
```
