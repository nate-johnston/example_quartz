---
title: "Ungoogled Extensions"
source: "https://www.ungoogledextensions.com/"
author:
  - "[[Luke Gosnell]]"
published:
created: 2026-03-01
description:
tags:
  - "clippings"
---
![](https://www.ungoogledextensions.com/projectImages/Chromium_logo.png)

1. Visit the to search for an extension.
2. Copy the URL of the extension to download.
3. Paste the URL.
4. Select your Chromium version. [(auto-detect)](https://www.ungoogledextensions.com/#)

#### How to Install

1. Open [chrome://extensions](https://www.ungoogledextensions.com/). Enable developer mode (top right of screen) and refresh.
2. Drag-and-drop the CRX from a file browser into the page of the extensions tab.
  

#### Troubleshooting

- If your browser does not allow you to download, click the copy button instead and paste the URL in a different browser
- Alternatively, go to [chrome://flags](https://www.ungoogledextensions.com/) and set "Handling of extension MIME type requests" to "Download as regular file"
- Copy + paste chrome:// links in a new tab if your Chromium install does not allow opening links to local resources.
  

#### Notes

- This is a quick and easy solution to downloading extensions for Chromium-based browsers, HOWEVER:  
	For a more intuitive solution with built-in semi-auto-updating, see [github.com/NeverDecaf/chromium-web-store](https://github.com/NeverDecaf/chromium-web-store).
- Instructions for downloading extensions manually can be found [here](https://ungoogled-software.github.io/ungoogled-chromium-wiki/faq#can-i-install-extensions-or-themes-from-the-chrome-webstore).
- Find your version here: [chrome://settings/help](https://www.ungoogledextensions.com/help)
- Take back the web from soulless megacorporations with other privacy-respecting web browsers, such as [Pale Moon](https://www.palemoon.org/).
- While you're at it, go fully off the grid with [Beaker](https://beakerbrowser.com/) or [Tor](https://www.torproject.org/).
- This project is [OPEN SOURCE](https://github.com/lukegosnellranken/UngoogledExtensions)!
  

#### Adblock for YouTube

- In recent times, Google has made it increasingly tricky to get around their anti-adblock measures.
- I've found [this extension](https://adskipper.me/) to be the most reliable, as it skips ads near-immediately as opposed to outright blocking them.
- Adblock on YouTube is broken as of Chromium v133+. Luckily, the fix is simple. Go to [chrome://flags](https://www.ungoogledextensions.com/) and enable "Disable WebGL." Voilà!
  

#### Suggested Extensions (click title to select)

- General
- [(view)](https://chromewebstore.google.com/detail/ublock-origin/cjpalhdlnbpafiamejdnhcphjbkeiagm)
	- [(view)](https://chromewebstore.google.com/detail/custom-new-tab/lfjnnkckddkopjfgmbcpdiolnmfobflj)
	- [(view)](https://chromewebstore.google.com/detail/tab-group/gjgjkhbmehogehkdnoooeihkipifimme)
	- [(view)](https://chromewebstore.google.com/detail/decentraleyes/ldpochfccmkkmhdbclfhpagapcfdljkj)
	- [(view)](https://chromewebstore.google.com/detail/fakespot-fake-amazon-revi/nakplnnackehceedgkgkokbgbmfghain)
	- [(view)](https://chromewebstore.google.com/detail/gofullpage-full-page-scre/fdpohaocaechififmbbbbbknoalclacl)
	- [(view)](https://chromewebstore.google.com/detail/the-camelizer/ghnomdcacenbmilgjigehppbamfndblo)
	- [(view)](https://chromewebstore.google.com/detail/volume-master/jghecgabfgfdldnmbfkhmffcabddioke)
	- [(view)](https://chromewebstore.google.com/detail/google-single-sheet-expor/magflfolbnbmmafkacalffmggnbnjaib)
- Webdev
- [(view)](https://chromewebstore.google.com/detail/react-developer-tools/fmkadmapgofadopljbjfkapdkoienihi)
	- [(view)](https://chromewebstore.google.com/detail/width-and-height-display/hhcddohiohbojnfdmfpbbhiaompeiemo)
	- [(view)](https://chromewebstore.google.com/detail/window-resizer/kkelicaakdanhinjdeammmilcgefonfh)
- YouTube
- [(view)](https://chromewebstore.google.com/detail/ad-skipper/dinhbmppbaekibhlomcimjbhdhacoael)
	- [(view)](https://chromewebstore.google.com/detail/sponsorblock-for-youtube/mnjggcdmjocbbbhaepdhchncahnbgone)
	- [(view)](https://chromewebstore.google.com/detail/return-youtube-dislike/gebbhagfogifgggkldgodflihgfeippi)
	- [(view)](https://chromewebstore.google.com/detail/youtube-redux/mdgdgieddpndgjlmeblhjgljejejkikf)
  

#### "Why can't I just use the official webstore?"

- The Chrome Web Store installs extensions only through Google‑controlled Chrome APIs.
- “Add to Chrome” sends signed, authenticated requests with install tokens and metadata.
- Ungoogled Chromium lacks these tokens and headers, so the Web Store will not serve.crx files.
- The Web Store never exposes direct.crx links because downloads rely on Google’s install API.
- Ungoogledextensions.com bypasses the Web Store and queries Google’s public update service.
- The update service accepts anonymous requests with a valid extension ID and version.
- The site’s JavaScript builds update URLs and downloads.crx files without authentication.
  

#### Feedback

- For general feedback, troubleshooting, and to suggest extensions to add to the list above, post to the [repo discussion page](https://github.com/lukegosnellranken/UngoogledExtensions/discussions/9).
- To report a bug, please add an issue to the [repo issues page](https://github.com/lukegosnellranken/UngoogledExtensions/issues).