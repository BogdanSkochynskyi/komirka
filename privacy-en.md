---
title: Komirka — Privacy policy
---

# Komirka — Privacy policy

*Effective: 25 November 2026 · Applies to the Komirka Chrome extension, version 1.0.0 and later.*
*[Українською](privacy-uk.md)*

Komirka replaces Chrome's New Tab page with a shortcut grid and can archive your open tabs into
bookmarks on a schedule. It has **no servers, no accounts, no analytics and no ads**. The developer
never receives your shortcuts, tabs, bookmarks or browsing data.

## What stays in your browser

All of this is stored only by Chrome itself, on your device or in your own Chrome sync:

| What | Where | Why |
|---|---|---|
| Your shortcuts (address, title, position), grid size, background, archive retention and display settings | `chrome.storage.sync` — your Chrome profile; Chrome syncs it to your other devices if Chrome sync is on | To show the same New Tab on all your devices |
| Your Pro licence key and the result of its last check | `chrome.storage.sync` | So Pro works on all your devices without entering the key again |
| Archive settings of this device (on/off, schedule, device name), the archive folder id, scheduler state, photo rotation state | `chrome.storage.local` — this device only | To run the archive and the background on this device |
| Up to 3 background photos | IndexedDB of the extension — this device only | So the New Tab never shows a blank background |
| Archived tabs (page title and address) | Your Chrome bookmarks, in the archive folder the extension creates | This is the tab archive; you can see and delete these bookmarks in Chrome at any time |

**Tab archive.** Only when you turn the archive on, Komirka asks for permission to read your open tabs
(address, title, tab group, last-used time) and to manage bookmarks. It uses them only to save tabs
into its own bookmark folder and close them. It never reads page contents and never touches bookmarks
outside its own folder. Turning the archive off gives these permissions back.

**Toolbar button.** When you click the Komirka button, it reads the address and title of the current tab
only, so you can add it to your New Tab.

**Site icons** come from Chrome's own local icon cache; no request is made for them.

## What leaves your browser

Only two kinds of requests, and only in these cases:

1. **Background photos — Wikimedia Commons** (`commons.wikimedia.org`, images from `upload.wikimedia.org` / `thumb.wikimedia.org`).
   Only while a photo background is selected, or when you click a photo preview in the settings. The
   request asks for a random featured picture of the chosen topic. It contains no personal data; it
   carries the extension name, its version and the address of this site, as Wikimedia asks of all apps.
   Wikimedia's privacy policy: <https://foundation.wikimedia.org/wiki/Policy:Privacy_policy>.
2. **Pro licence check — Polar** (`api.polar.sh`). Only if you entered a Pro licence key: when you enter
   it, and then about every 6 hours. The request contains only the key and Komirka's seller id at Polar.
   Polar answers whether the key is valid. Polar's privacy policy: <https://polar.sh/legal/privacy>.

Buying Pro happens on Polar's checkout page, not inside the extension. Polar is the merchant of record:
your e-mail address and payment details are given to Polar (and its payment processor), not to the
extension. The developer sees your purchase in Polar's dashboard as any seller would.

Your Chrome sync data (shortcuts, settings, the licence key, bookmarks) is handled by Google under
Google's privacy policy; Komirka does not run its own sync.

## What Komirka does not do

- No analytics, tracking, advertising or telemetry.
- No selling or sharing of data with anyone; data is not used for credit decisions.
- No reading of page contents.
- No remote code: everything the extension runs is inside the package you install.

## Deleting your data

- Delete a shortcut or the archive bookmarks from the New Tab page or from Chrome's bookmarks.
- Removing the extension deletes what it stored on that device (`chrome.storage` and IndexedDB). The
  archive bookmarks stay in your bookmarks until you delete them, so nothing you archived is lost.
- Synced data can be erased in your Google account: Chrome → Settings → You and Google → Sync →
  "Review your synced data" (or delete your shortcuts and the key in Komirka before removing it).
- To stop licence checks, remove the key in Settings → Pro.

## Changes and contact

If this policy changes, the new version is published on this page with a new date.
Questions: open an issue at <https://github.com/BogdanSkochynskyi/komirka/issues>.
