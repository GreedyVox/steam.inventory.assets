# YAARRGH! Battle Island! — Steam Inventory Assets

Official public image host for the Steam Inventory items used by **YAARRGH! Battle Island!**, developed by **GreedyVox**.

This repository exists so Steam can download and cache stable, publicly accessible inventory artwork. It is an asset-delivery repository, not an open-source or open-content collection.

> **Copyright notice:** All artwork and visual assets in this repository are proprietary. Viewing or downloading a file does not grant permission to reuse it. See the [Asset Licence](LICENSE.md).

## Published inventory assets

| Item | Steam ItemDef | Small icon | Large icon |
| --- | ---: | --- | --- |
| Doubloons | `1500` | [200 × 200 PNG](https://greedyvox.github.io/steam.inventory.assets/Doubloon.200x200.png) | [2048 × 2048 PNG](https://greedyvox.github.io/steam.inventory.assets/Doubloon.2048x2048.png) |

## Steamworks ItemDef fields

```json
"icon_url": "https://greedyvox.github.io/steam.inventory.assets/Doubloon.200x200.png",
"icon_url_large": "https://greedyvox.github.io/steam.inventory.assets/Doubloon.2048x2048.png"
```

Steam's servers must be able to open both URLs without authentication, cookies, or expiring tokens.

## Updating an asset

Steam downloads and caches inventory images. For a visible artwork revision:

1. Export a matched `200 × 200` PNG and `2048 × 2048` PNG.
2. Give both files a new versioned name, for example:

   ```text
   Doubloon.v2.200x200.png
   Doubloon.v2.2048x2048.png
   ```

3. Commit and publish the new files through GitHub Pages.
4. Open both public URLs in a private browser window and confirm that each URL returns the PNG directly.
5. Update `icon_url` and `icon_url_large` in the Steam Inventory ItemDef.
6. Keep every older file that is still referenced by a published ItemDef or cached Steam page.

Changing the filename is preferred to overwriting an existing image because it gives Steam a new URL to fetch.

## Repository rules

- Store only artwork owned by GreedyVox or used with written permission.
- Keep filenames and capitalisation stable after publication.
- Do not delete assets that are still referenced by Steamworks.
- Do not submit third-party artwork, trademarks, or copyrighted material without permission.
- Do not submit pull requests containing replacement artwork unless GreedyVox has authorised the contribution in writing.

## Licence

Copyright © 2026 GreedyVox. All rights reserved.

The images, artwork, and associated visual assets are provided under the repository's [proprietary asset licence](LICENSE.md). No open-source, Creative Commons, or public-domain licence applies unless a file is explicitly marked otherwise.

Steam and Steamworks are trademarks of Valve Corporation. This repository is not affiliated with or endorsed by Valve Corporation.
