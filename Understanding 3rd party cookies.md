# NanoTechsSnack: 3rd-party cookies in 5 minutes
// Unbaking third-party cookies
// Tech snack: 3rd-party cookies

## Why am I reading this?
You're probably glad you're not the dev who had to implement the new GDPR feature.
 
## Cookies 101

### Def 
"An HTTP cookie (web cookie, browser cookie) is a small piece of data that a server sends to the user's web browser. 
**The browser may store it and send it back with the next request to the same server. **
Typically, it's used to tell if two requests came from the same browser — keeping a user logged-in, for example. It remembers stateful information for the stateless HTTP protocol."

### Origins 
Cookies are used on the web since 1994.  
"The first use of cookies [...] was checking whether visitors to the Netscape website had already visited the site."

### Cookie dough - What are cookies made of?  
A cookie is simply a key-value pair.
Example:

### How are cookies set/get?
Set: 2 ways:
- server-side: see https://developer.mozilla.org/en-US/docs/Web/HTTP/Cookies#Creating_cookies
- client-side: see document.cookie = "username=John Doe";
Get: 2 ways:
- server-side: see https://developer.mozilla.org/en-US/docs/Web/HTTP/Cookies#Creating_cookies
- client-side: see document.cookie = "username=John Doe";

basically a HTTP request is made, with Set-Cookie header.

Note: 
If your cookie is set server-side, it will be readable by client code. 
(because you won't be able to use the HttpOnly flag)
So you're exposing your users to session hijacking: 
https://developer.mozilla.org/en-US/docs/Web/HTTP/Cookies#Session_hijacking_and_XSS or https://en.wikipedia.org/wiki/Session_hijacking


### Zoom on cookie flavours


o | first-party | third-party
---------|----------|---------
 session | good: bad:  | xx
 persistent | B2 | C2

So, which one is evil?
Technically, all cookies are similar.

The evil twin: 3rd party cookies and associated problems


Alread back then, some privacy issues were raised.
"Cookies were discussed in two U.S. Federal Trade Commission hearings in 1996 and 1997"
Sources:
https://en.wikipedia.org/wiki/HTTP_cookie#Alternatives_to_cookies 
http://www.historyofinformation.com/detail.php?id=2102


### How trackers work (or don't)


#### Trackers cryptonite
* DNT messages
* Set DNT in your browser
* Use a browser that does DNT by default
* Use browser extensions such as [Privacy Badger](https://addons.mozilla.org/en-US/firefox/addon/privacy-badger17/)
* Delete your cookies regularly

### Side notes 

#### Existential crisis
Cookie use is not encouraged anymore. 
Alternatives to cookies.

* Cookies vs redux
* Cookies vs localStorage
* Cookies vs other Alternatives---> see wikipedia

https://medium.com/mediafem-blog/how-will-googles-move-to-restrict-third-party-cookies-affect-publishers-b7c7d91ac1ef



## Sources
- https://en.wikipedia.org/wiki/HTTP_cookie#Alternatives_to_cookies
- https://privacy.net/stop-cookies-tracking/
- https://piwik.- pro/blog/first-party-vs-third-party-cookies-why-first-party-is-the-way-to-go/
- https://www.opentracker.net/article/third-party-cookies-vs-first-party-cookies
- https://web.dev/samesite-cookies-explained
- https://www.grahamcluley.com/whats-difference-first-third-party-cookies/
- https://medium.com/datadriveninvestor/cookies-vs-local-storage-2f3732c7d977
- https://jwt.io/
- https://www.whatismybrowser.com/detect/are-third-party-cookies-enabled
- https://www.eff.org/issues/do-not-track
- https://www.digitaltrends.com/computing/history-of-cookies-and-effect-on-privacy/
- https://www.worldprivacyforum.- org/2011/03/resource-page-behavioral-advertising-and-privacy/
- https://donttrack.us/
- https://chrome.google.- com/webstore/detail/duckduckgo-privacy-essent/bkdgflcldnnnapblkhphbgpggdiikppg
- https://blog.mozilla.org/firefox/cross-site-tracking-lets-unpack-that/
- https://blog.mozilla.- org/blog/2018/10/23/latest-firefox-rolls-out-enhanced-tracking-protection/
- https://blog.mozilla.- org/futurereleases/2018/08/30/changing-our-approach-to-anti-tracking/
- https://blog.mozilla.- org/futurereleases/2018/10/23/the-path-to-enhanced-tracking-protection/ 
- https://www.wired.com/story/privacy-browsers-duckduckgo-ghostery-brave/
- 
https://medium.com/datadriveninvestor/cookies-vs-local-storage-2f3732c7d977
https://www.digitaltrends.com/computing/history-of-cookies-and-effect-on-privacy/

https://stackoverflow.com/questions/40848816/why-not-use-cookies-instead-of-redux

====== 
QUESTIONS:
- cookie set on user device vs sent to server, and how/when are they "set"/"sent"... ? See https://developers.google.com/web/tools/chrome-devtools/network/reference#filter-by-property
- why is the cookie list in the URL bar and in devTools not the same length?
- what's the point of a third-party session cookie? see http://www.fonerepair.com/information/cookies_policy.html
- link between http request and cookie? +++ read https://developer.mozilla.org/en-US/docs/Web/HTTP/Cookies
- Resource type: XHR vs script??? --> see https://developer.mozilla.org/en-US/docs/Mozilla/Add-ons/WebExtensions/API/webRequest/ResourceType
- Types of cookies: +++ see https://developers.google.com/web/tools/chrome-devtools/storage/cookies

https://developer.mozilla.org/en-US/docs/Web/HTTP/Cookies

src https://stackoverflow.com/questions/13851946/header-origin-vs-host

What do the values mean? 
How to retrieve cookies? What if they're the same name?
Is there a way to know where the cookie come from?
