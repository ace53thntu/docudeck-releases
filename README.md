# DocuDeck releases

Download DocuDeck, a native macOS client for MongoDB and Amazon DocumentDB.

**[Download the latest version for Mac (Apple Silicon)](https://github.com/ace53thntu/docudeck-releases/releases/latest/download/DocuDeck-darwin-arm64.dmg)**

That link always points to the newest release. Older versions and release notes are on the
[Releases page](https://github.com/ace53thntu/docudeck-releases/releases).

## What DocuDeck does

- Connects to MongoDB and Amazon DocumentDB 4.0, 5.0 and 8.0. You choose the server version, and
  DocuDeck uses the matching driver and rules, so older DocumentDB clusters work too.
- Browse databases and collections, query documents, run aggregations, and view schema, indexes and
  explain plans.
- Import and export JSON or CSV. Export and import saved connections, with passwords encrypted if
  you choose to include them.
- New connections are read-only by default. Passwords are kept in the macOS keychain.
- Optional: lets Claude Code on your Mac read the connections you choose, read-only.

## Requirements

- macOS 11 (Big Sur) or later
- A Mac with Apple Silicon (M1 or later)

## Install

1. Download `DocuDeck-darwin-arm64.dmg` from the link above.
2. Open it and drag **DocuDeck** into **Applications**.
3. Open DocuDeck from Applications. The first time, macOS may say it can't check the app:
   - right-click DocuDeck and choose **Open**, then **Open** again; or
   - go to **System Settings → Privacy & Security** and click **Open Anyway**.

Run DocuDeck from Applications, not from inside the disk image, so it can update itself.

## Updates

DocuDeck 1.2.0 and later update themselves:

- DocuDeck checks for a new version 30 seconds after it opens, then every 4 hours. You can also
  check at any time with **ⓘ → Check now**.
- When a new version is found, a bar appears. Click **Update now**, then **Restart now**. If you
  click **Later**, the update installs when you quit DocuDeck.
- Nothing installs until you click. Every update is signed, and DocuDeck refuses any file that
  isn't signed with its key, or that is older than the version you have.
- To turn automatic checks off, untick **ⓘ → Check for updates automatically**.

If you have a version older than 1.2.0, download and install the latest version once by hand.
Updates after that are automatic.

## Files in each release

| File | What it is |
|---|---|
| `DocuDeck-darwin-arm64.dmg` | The installer (the same file under a name that never changes) |
| `DocuDeck-<version>-darwin-arm64.dmg` | The installer for that version |
| `DocuDeck-<version>-darwin-arm64.zip` | Used by the built-in updater |
| `docudeck-update.json` | Used by the built-in updater (version, checksum, signature) |

Most people only need the `.dmg`.

## For IT administrators

A root-owned file `/etc/docudeck.conf` (JSON) can fix settings for every user of a Mac, for example:
```JSON
{ "autoUpdates": false, "exportPasswords": false, "mcpEnabled": false }
```

## Notes

DocuDeck is an independent tool. It is not affiliated with, sponsored or endorsed by MongoDB, Inc.
or Amazon Web Services. MongoDB is a trademark of MongoDB, Inc.; Amazon DocumentDB and AWS are
trademarks of Amazon.com, Inc. or its affiliates. Open-source licenses are listed in the app under
**ⓘ → Open-source licenses**.
