# browsers-lang-stats

Languages distributions in Firefox and Chromium? You can see the chart [here][gh-pages].

Repository contains scripts collecting the language statistics for
[mozilla-firefox/firefox] and [chromium/chromium] repositories. Gathered data then assembled into a pie charts 
`browsers-lang-stats.mustache`.

Page is updated weekly with a Travis Cron job. See the `date` meta tag for
the exact build time.

# Build stat

Build json document with the language details for Chromium and FireFox:
```
dev/build-data ./firefox > build/data.json
dev/build-data ./chromium >> build/data.json
```

# Build pie charts

Expand mustache template:

```
mustache data.json browsers-lang-stats.mustache > browsers-lang-stats.html
```

[mozilla-firefox/firefox]: https://github.com/mozilla-firefox/firefox
[chromium/chromium]: https://github.com/chromium/chromium
[gh-pages]: https://optiklab.github.io/browsers-lang-stats.html
