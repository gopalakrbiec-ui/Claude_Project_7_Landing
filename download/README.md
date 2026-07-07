# App download folder

Place the installable Android app here so the website's **Download APK**
button and the install guide (`install.html`) work.

## Required file

| File | What it must be |
|---|---|
| `savi-nenapu.apk` | A **signed universal APK** — the installable app |

**Do NOT put an `.aab` here.** An Android App Bundle (`.aab`) is only for
uploading to Google Play; phones cannot install it. Users need a `.apk`.

## How to produce the universal APK from your `.aab`

Option A — Android Studio (simplest):
1. Build → Build Bundle(s) / APK(s) → **Build APK(s)**
2. Use the signed release APK it produces.

Option B — bundletool (from an existing `.aab`):
```
bundletool build-apks --bundle=app.aab --output=app.apks \
  --mode=universal \
  --ks=your-keystore.jks --ks-key-alias=YOUR_ALIAS
unzip app.apks -d out
# out/universal.apk is the installable file
```

Rename the result to `savi-nenapu.apk` and commit it into this folder.

## Notes
- Keep it under ~100 MB (GitHub's per-file limit). If the APK is larger,
  host it as a GitHub Release asset instead and point the button there.
- Update the APK here whenever you ship a new beta build; the download
  URL stays the same.
