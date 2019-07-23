# Nano brain snack: 3rd-party cookies

## Why am I reading this?
You're probably glad you're not the dev who had to implement the new GDPR features. BUT: don't you feel like a lost bagel when reading headlines about privacy issues and the new Firefox release? 
Read this if you need a nano-basis to understand 3rd-party cookies - the #1  public enemy of online privacy lovers (although my mom always clicks "Accept all cookies").
 
## Cookies 101

### Def  
As [MDN](hhttps://developer.mozilla.org/en-US/docs/Web/HTTP/Cookies) puts it:
"An HTTP cookie [...] is a small piece of data that a server sends to the user's web browser. 
**The browser may store it and send it back with the next request to the same server.**" 
Terminology: HTTP cookie = web cookie = browser cookie, as opposed to other types of cookies that we don't care about for this article.

### But why?
Cookies are used on the web since 1994, first to "check whether visitors to the Netscape website had already visited the site."
"Cookies are typically used to tell if two requests came from the same browser — to keep a user logged in or remember their display preferences. It remembers stateful information for the stateless HTTP protocol."

### What's it like inside?
A cookie is simply a key-value pair.
Example: (img)
It also has metadata attached to it:
- an expiry date

### How are cookies set/get?
Set: 2 ways:
- server-side: see https://developer.mozilla.org/en-US/docs/Web/HTTP/Cookies#Creating_cookies
- client-side: see document.cookie = "username=John Doe";
Get: 2 ways:
- server-side: see https://developer.mozilla.org/en-US/docs/Web/HTTP/Cookies#Creating_cookies
- client-side: see document.cookie = "username=John Doe";

Basically a HTTP request is made, with Set-Cookie header.

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

#### Cookies and security concerns

- whether it's HTTP or HTTPS

#### Existential crisis
Cookie use is not encouraged anymore. 
Alternatives to cookies.

* Cookies vs redux
* Cookies vs localStorage
* Cookies vs other Alternatives---> see wikipedia
