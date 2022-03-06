# Security on Mozilla

## Security check websites:
Overall links:
https://www.privacytools.io/#browser

JS:
https://z0ccc.github.io/LocateJS/

Track checker:
https://coveryourtracks.eff.org/

## Settings on Mozilla
- Default Search Engine => DuckDuckGo
- "Do Not Track" => Always
- Network Settings:
  - Use proxy settings => true
  - Proxy DNS when using SOCKS v5
  - Enable DNS over HTTPS => ?
    - Read before enabling! https://blog.powerdns.com/2019/09/25/centralised-doh-is-bad-for-privacy-in-2019-and-beyond/
- Cookies and Site Data:
  - Delete cookies and site data when Firefox is closed => true
- Permissions:
  - Block pop-up windows => true
  - Warn you when websites try to install add-ons => true
- Firefox Data Collection and Use:
  - Allow personalized => false
- Enable HTTPS-Only Mode in all windows

## Plugins for Mozilla
### Remember, the more plugins you have, the more chance that one of them may betray your security & privacy.
- Canvasblocker by kkapsner – Protects against canvas fingerprinting methods (source on GitHub) <br>
https://addons.mozilla.org/en-US/android/addon/canvasblocker/ <br>
https://github.com/kkapsner/CanvasBlocker

- Trace by AbsoluteDouble – Protects against various fingerprinting methods (source on GitHub) <br>
https://addons.mozilla.org/en-US/firefox/addon/absolutedouble-trace/ <br>
https://github.com/jake-cryptic/AbsoluteDoubleTrace/

- Chameleon by sereneblue – Allows you to spoof user agent values (source on GitHub) <br>
https://addons.mozilla.org/en-US/firefox/addon/chameleon-ext/ <br>
https://github.com/sereneblue/chameleon

- uBlock Origin - An efficient wide-spectrum content blocker. Easy on CPU and memory. <br>
https://addons.mozilla.org/en-US/firefox/addon/ublock-origin/

- NoScript - script-blocker that allows you to identify/block scripts running on websites. <br>
https://addons.mozilla.org/en-US/firefox/addon/noscript/

- HTTPS Everywhere:
(It is in the Mozilla already. Could be enabled by: Settings > Privacy & Security > Scroll to Bottom > Enable HTTPS-Only Mode) <br>
https://www.eff.org/deeplinks/2021/09/https-actually-everywhere

- Decentraleyes <br>
https://addons.mozilla.org/en-US/firefox/addon/decentraleyes/ <br>
https://git.synz.io/Synzvato/decentraleyes

- ClearURLs <br>
https://addons.mozilla.org/en-US/firefox/addon/clearurls/ <br>
https://gitlab.com/KevinRoebert/ClearUrls/-/blob/master/README.md

- xBrowserSync <br>
https://addons.mozilla.org/en-GB/firefox/addon/xbs/

- Cookie AutoDelete <br>
https://addons.mozilla.org/en-US/firefox/addon/cookie-autodelete/ <br>
https://github.com/Cookie-AutoDelete/Cookie-AutoDelete/issues

- Privacy Badger <br>
https://addons.mozilla.org/en-US/firefox/addon/privacy-badger17/ <br>
https://github.com/EFForg/privacybadger

- DuckDuckGo Privacy Essentials <br>
https://addons.mozilla.org/en-US/firefox/addon/duckduckgo-for-firefox/ <br>
https://github.com/duckduckgo/duckduckgo-privacy-extension

- User-Agent Switcher and Manager <br>
https://addons.mozilla.org/en-US/firefox/addon/user-agent-string-switcher/ <br>
https://github.com/ray-lothian/UserAgent-Switcher/

### The next plugins were not properly tested and I have no trust to them. However, they look interesting to me.
- AudioContext Fingerprint Defender <br>
https://addons.mozilla.org/en-US/firefox/addon/audioctx-fingerprint-defender/

- Canvas Fingerprint Defender <br>
https://addons.mozilla.org/en-US/firefox/addon/canvas-fingerprint-defender/

- WebGL Fingerprint Defender <br>
https://addons.mozilla.org/en-US/firefox/addon/webgl-fingerprint-defender/

- Font Fingerprint Defender <br>
https://addons.mozilla.org/en-US/firefox/addon/font-fingerprint-defender/


## Things to change in about:config
~~~
Basic fingerprint protection: 
privacy.resistFingerprinting => true

WebGL disable:
webgl.disabled => true

WebRTC disable: 
media.peerconnection.enabled => false

Geolocation tracking disable:
geo.enabled => false

Isolate cookies to the first party domain:
privacy.firstparty.isolate => true

Block cryptominers:
privacy.trackingprotection.cryptomining.enabled => true

Tracking protection:
privacy.trackingprotection.enabled => true (may be redundant if you are using uBlock Origin 3rd party filters)

Block microphone and camera status of your device:
media.navigator.enabled => false

Disable "prefetching" DNS requests:
network.dns.disablePrefetch => true

Disable "prefetching" DNS requests by Firefox:
network.prefetch-next => false

Disable websites getting clipboard event notifications:
dom.event.clipboardevents.enabled => false
~~~

## user.js Firefox hardening
Consider to check out user.js hardening: <br>
https://github.com/arkenfox/user.js

## Useful Links
* Browser fingerprinting: https://restoreprivacy.com/browser-fingerprinting/
* Firefox Privacy: https://restoreprivacy.com/firefox-privacy/
* WebRTC Leaks: https://restoreprivacy.com/webrtc-leaks/
* DNS Prefetching: https://www.usenix.org/legacy/events/leet10/tech/full_papers/Krishnan.pdf
* DoH good or bad: https://blog.powerdns.com/2019/09/25/centralised-doh-is-bad-for-privacy-in-2019-and-beyond/
* Identifying User Agent: https://www.eff.org/deeplinks/2010/01/tracking-by-user-agent
* Additional info about fingerprint: https://medium.com/@useradd_deploy/whats-my-fingerprint-b8df1d8e3293