# do

Static datasets shared by FlockOS builds.

## app-bible/v1

`app-bible/v1/` is the shared Bible dataset used by `New_Covenant/app.bible` and exported Nation builds.

Default runtime base URL:

```text
https://raw.githubusercontent.com/edidasken/do/main/app-bible/v1/
```

The app can override this at runtime with `window.FLOCK_BIBLE_DATA_BASE_URL` before loading `app.bible/bible.js`.
