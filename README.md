# 👒 vegapull-records

Collection of datasets for One Piece TCG.

The data in this repository has been obtained using the [vegapull scraper CLI](https://github.com/Coko7/vegapull).

## 🗃️ File structure

Datasets are categorized by language and contain JSON data for all TCG cards:
- `packs.json`: contains the list of packs
- `cards_{PACK-ID}.json`: contains the list of cards for pack `PACK-ID`

Example:
```
data/
├── english/
│   ├── cards_569001.json
│   ├── cards_569002.json
│   ├── ...
│   ├── cards_569901.json
│   └── packs.json
└── japanese/
    └── cards.json
```

**NOTE:** The current data for the japanese version was fetched using an older version of the CLI where all of the data
was put in a single JSON file (`cards.json`).

## 🖼️ Where can I download images?

Storing images directly on GitHub is not the best approach.
Instead, these images are zipped into an archive and can be downloaded along with the latest release.

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
