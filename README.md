# do

Static datasets shared by FlockOS builds.

## app-bible/v1

`app-bible/v1/` is the shared Bible dataset used by `New_Covenant/app.bible` and exported Nation builds.

Default runtime base URL:

```text
https://raw.githubusercontent.com/edidasken/do/main/app-bible/v1/
```

The app can override this at runtime with `window.FLOCK_BIBLE_DATA_BASE_URL` before loading `app.bible/bible.js`.

Large ESV source exports from `jburson/bible-data` are stored as book-level JSON chunks instead of single aggregate files. Use the manifests under:

```text
app-bible/v1/original-languages/jburson-bible-data/esv/books/manifest.json
app-bible/v1/original-languages/jburson-bible-data/esv/footnotes/manifest.json
app-bible/v1/original-languages/jburson-bible-data/esv/interlinear/manifest.json
app-bible/v1/original-languages/jburson-bible-data/esv/static/manifest.json
```

Large non-runtime source archives are stored as `.parts/` folders with a `manifest.json` that includes the original SHA-256 and a `cat .../part-*` reassembly command.

`app-bible/v1/offline-assets.json` is priority ordered for offline warmup. Lower `priority` values download first:

- `10`: critical manifests and dataset indexes
- `20`: Scripture core data
- `30`: cross-reference indexes and buckets
- `40`: study tools
- `50`: original-language/alignment chunks
- `60`: commentary indexes
- `70`: commentary chapter chunks
- `90`: reconstructable source archive parts

## shared-data/v1

`shared-data/v1/` contains static reference datasets used across FlockOS apps.

Default runtime base URL:

```text
https://raw.githubusercontent.com/edidasken/do/main/shared-data/v1/
```

`shared-data/v1/genealogy/` stores the biblical genealogy corpus as a manifest plus alphabet chunks.
