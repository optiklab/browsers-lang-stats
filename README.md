# browsers-lang-stats

Languages distributions in Firefox and Chromium? You can see the chart [here][gh-pages].

Repository contains scripts collecting the language statistics for
[mozilla/gecko-dev] and [chromium/chromium] repositories. Gathered data then assembled into a pie charts 
`index.mustache`.

Page is updated weekly with a Travis Cron job. See the `date` meta tag for
the exact build time.

# Build stat

Build json document with the language details for Chromium and FireFox:
```
dev/build-data ./gecko-dev > build/data.json
dev/build-data ./chromium >> build/data.json
```

# Build pie charts

Expand mustache template:

```
mustache data.json index.mustache > index.html
```

[mozilla/gecko-dev]: https://github.com/mozilla/gecko-dev
[chromium/chromium]: https://github.com/chromium/chromium
[gh-pages]: https://4e6.github.io/firefox-lang-stats/
