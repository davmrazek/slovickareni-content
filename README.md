# slovickareni-content

Daily puzzle content for the **Slovíčkaření** app, served as static files over
raw.githubusercontent.com. The app fetches only *today's* file, caches it, and falls
back to the copy bundled in the build whenever this host is unreachable — so nothing
here is load-bearing for an offline player.

```
crossword/YYYY-MM-DD.json     mini crossword   (EXPO_PUBLIC_PUZZLES_URL)
connections/YYYY-MM-DD.json   Souvislosti      (EXPO_PUBLIC_CONNECTIONS_URL)
privacy.html                  privacy policy   (GitHub Pages)
```

Files are generated and validated in the app repo; publish with
`node app/scripts/publish-content.mjs <this repo> --days 365` there, then commit here.
Never hand-edit a puzzle file — edit the source and republish, or the app's bundled
copy and this one disagree.
