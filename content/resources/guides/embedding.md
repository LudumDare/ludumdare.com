+++
title = "Embedding Guide"
weight = 100

[taxonomies]
Categories = ["Account"]
+++
Since Ludum Dare 51, we now support uploading and embedding to game pages.

Uploading to Ludum Dare is not required, but some features (embedding) are only supported if you upload.


## Downloads
We support many common file formats. If you're not sure what to use, we recommend `zip`. Files are uploaded from your game page. Simply edit them (click the pencil icon the bottom corner), scrolling to the "Downloads" section, and click the **upload** button.


### Details
* Supported file extension(s):
  * Archives: `zip`, `tar.gz`, `tar.bz2`, `7z`
  * Windows: `msi`, `exe`
  * Apple: `dmg`
  * Linux: `flatpak`, `snap`, `deb`, `rpm`
* Max file size: 256 MB

**IMPORTANT**: Embedded games have different restrictions. See below for details.

GitHub discussion on additional formats: <https://github.com/JammerCore/JammerCore/discussions/2171>

## Embedding
You can embed web games directly on a game pages. We support HTML5 games 

To upload, you must prepare a `zip` file with all of your files, and an `index.html` file in the root (top-level folder). Your `zip` file can be uploaded via the **upload** button in the **Embedding** section.

**IMPORTANT**: Web games run in a strict sandbox! See the **JavaScript Restrictions** section below.

### Details
* Supported file extension(s):
  * Archives: `zip`
* Max file size: 256 MB

### File structure 
* `index.html` in the root directory of the ZIP file
  * (TODO: Allow users to change this)

### Layout Restrictions
* 948x533 pixel resolution (16:9)
  * (TODO: Allow users to change this)

### JavaScript Restrictions
* no external requests (`fetch`, `XMLHttpRequest`)
* no storage or cookies (`localStorage`, `sessionStorage`, `indexDB`)

### Supported JavaScript features
Our embeds are a standard `<iframe>`. You should be able to use any feature supported by modern browsers (other than those mentioned above). Features that require non-standard configurations or permissions are listed below.

* `requestFullScreen()`
* Performance features, via [cross-origin isolation](https://web.dev/cross-origin-isolation-guide/) (`SharedArrayBuffer`, high resolution timers)
* WebAssembly `wasm` files (`Content-Type: application/wasm`)

GitHub discussion on additional browser features: https://github.com/JammerCore/JammerCore/discussions/2172

### Mobile
We've been focused on the desktop experience, and though it should still work, the mobile web-game experience might be sub-par.

GitHub issue: <https://github.com/JammerCore/JammerCore/issues/2169>

### Persistent storage
At the time of this writing, embedded games don't support persistent storage. We are exploring some options, but to keep things secure we will not be enabling access to a traditional storage method.

GitHub issue: <https://github.com/JammerCore/JammerCore/issues/2170>

### Accessing external data
For privacy and security reasons, we will not be allowing access to external websites or data. If your game requires external data, we recommend hosting it yourself and linking it.

### Embedding embedded Ludum Dare games on other websites
At the time of this writing this is unsupported. If there's enough interest, we may add this.

GitHub discussion: <https://github.com/JammerCore/JammerCore/discussions/2172>
