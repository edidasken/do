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

## shared-data/v1

`shared-data/v1/` contains static reference datasets used across FlockOS apps.

Default runtime base URL:

```text
https://raw.githubusercontent.com/edidasken/do/main/shared-data/v1/
```

`shared-data/v1/genealogy/` stores the biblical genealogy corpus as a manifest plus alphabet chunks.
