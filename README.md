# WPAD_PAC

In the end what worked for me was [using Chrome to navigate to][2]:

> chrome://net-internals/#proxy

which gave me the `.pac` file (= proxy auto-config file) which I could then download and read to determine the proxy that was being selected.

***=== Addenda ===***

This [no longer works as of Chrome 71][3].

So what I did was:

 1. Find the previous version of Chrome, which gives [70.0.3538][4].
 2. [Look this up][5] on https://omahaproxy.appspot.com, which gives version 587811.
 3. Find that version of **Chromium** on the [snapshots page][6].  The version seemed to be present on the [Windows 64 bit version page][7], which leads me to the [587811 version page][8] with the file [`chrome-win32.zip`][9].
 4. Download, unzip, run `chrome.exe` and you can again use the address `chrome://net-internals/#proxy` to find the PAC script!

**So to summarize the steps required:**

 1. Download Chromium version 70.0.3538 = build 587811 [here][9] (Windows, otherwise see above steps).
 2. Unzip and run `chrome.exe`
 3. Navigate to `chrome://net-internals/#proxy`

  [1]: https://superuser.com/questions/346372/how-do-i-know-what-proxy-server-im-using
  [2]: https://superuser.com/questions/346372/how-do-i-know-what-proxy-server-im-using#1163035
  [3]: https://stackoverflow.com/questions/22368515/how-to-see-the-proxy-settings-on-windows#30751938
  [4]: https://en.wikipedia.org/wiki/Google_Chrome_version_history
  [5]: https://superuser.com/questions/936432/how-do-i-install-a-previous-version-of-chrome#987935
  [6]: https://commondatastorage.googleapis.com/chromium-browser-snapshots/index.html
  [7]: https://commondatastorage.googleapis.com/chromium-browser-snapshots/index.html?prefix=Win_x64/
  [8]: https://commondatastorage.googleapis.com/chromium-browser-snapshots/index.html?prefix=Win_x64/587811/
  [9]: https://www.googleapis.com/download/storage/v1/b/chromium-browser-snapshots/o/Win_x64%2F587811%2Fchrome-win32.zip?generation=1535669834391189&alt=media
