# 👒 vegapull-records

Collection of datasets for One Piece TCG.

The data in this repository has been obtained using the [vegapull scraper CLI](https://githube.com/Coko7/vegapull).

## 🗃️ File structure

Datasets are categorized by language and consist of two main directories:
- `images`: broken into sub-directories per pack and includes all images
- `json`: contains JSON data for all cards
    - `packs.json`: contains the list of packs
    - `cards_{PACK-ID}.json`: contains the list of cards for pack `PACK-ID`

Example:
```
data/
├── english/
│   ├── images/
│   │   ├── 569001/
│   │   │   ├── ST01-001.png
│   │   │   ├── ...
│   │   │   └── ST01-017.png
│   │   ├── ...
│   │   └── 569901/
│   │       ├── EB01-006_p3.png
│   │       └── ...
│   └── json/
│       ├── cards_569001.json
│       ├── cards_569002.json
│       ├── ...
│       ├── cards_569901.json
│       └── packs.json
└── jp/
    ├── images/
    │   └── ...
    └── json/
        └── ...
```

## ⌛ How old is the data?

- 🇬🇧 English: April 27, 2025
- 🇯🇵 Japan: August 31, 2024

## ⚠️ Disclaimer

I had some trouble when fetching data for the japanese version:
- Wrong formatting/missing data for `colors` or `counter` values on some cards
- Duplicate cards with same data and art

These issues are with the original data itself and I did not find a clean/reliable way to handle them.
I tried to patch them by writing some custom code when fetching data for the `jp` version.
Fortunately, the `english` version does not seem to suffer from these problems.
So, keep this in mind when picking a dataset. I would recommend working with the `english` dataset.
