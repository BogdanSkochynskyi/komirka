---
title: Komirka — Privacy policy
---

# Komirka — Privacy policy

*Effective: 26 November 2026 · Applies to the Komirka Chrome extension, version 1.0.0 and later.*
*[Українською](privacy-uk.md)*

Komirka replaces Chrome's New Tab page with a shortcut grid and can archive your open tabs into
bookmarks on a schedule. It has **no servers, no accounts, no analytics and no ads**. The developer
never receives your shortcuts, tabs, bookmarks or browsing data.

## What stays in your browser

All of this is stored only by Chrome itself, on your device or in your own Chrome sync:

| What | Where | Why |
|---|---|---|
| Your shortcuts (address, title, position), grid size, background, archive retention and display settings | `chrome.storage.sync` — your Chrome profile; Chrome syncs it to your other devices if Chrome sync is on | To show the same New Tab on all your devices |
| The time Komirka first ran on your account | `chrome.storage.sync` | Early access: installs from before its end keep Pro 3 more months |
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

Only one kind of request, and only in these cases:

**Background photos — Wikimedia Commons** (`commons.wikimedia.org`, images from `upload.wikimedia.org` / `thumb.wikimedia.org`).
Only while a photo background is selected, or when you click a photo preview in the settings. The
request asks for a random featured picture of the chosen topic. It contains no personal data; it
carries the extension name, its version and the address of this site, as Wikimedia asks of all apps.
Wikimedia's privacy policy: <https://foundation.wikimedia.org/wiki/Policy:Privacy_policy>.

**Early access: no purchases, no licence checks.** Komirka is in early access: all features are included,
there is nothing to buy inside the extension, and it makes no licence checks and no requests to any payment
service. Before paid Pro launches, this policy will be updated to say which payment service is used and what
it receives; that version will be announced at least 2 weeks ahead.

Your Chrome sync data (shortcuts, settings, bookmarks) is handled by Google under
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
  "Review your synced data" (or delete your shortcuts in Komirka before removing it).

## Changes and contact

If this policy changes, the new version is published on this page with a new date.
Questions: open an issue at <https://github.com/BogdanSkochynskyi/komirka/issues>.
