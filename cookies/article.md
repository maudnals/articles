# Third-party cookies 101

## Why am I reading this? 

You're probably glad you're not the dev who took on the GDPR tickets. I know it because I was that dev, and I wasn't glad.   
But: do you feel like a lost bagel when reading headlines about privacy issues? 
A star of today's privacy concerns are third-party cookies (well not a concern for my mom who frantically clicks "Accept all") - so that's a start.  
Read along if you're both lazy and vaguely excited about exploring how third-party cookies work.

##  But first, cookies [skip]

### Def  
An HTTP cookie is a "small piece of data that a server sends to the user's web browser [...] the browser may store it and send it back with the next request to the same server." 
Source: [MDN](https://developer.mozilla.org/en-US/docs/Web/HTTP/Cookies)

Terminology hint: HTTP cookie = web cookie = browser cookie, as opposed to other types of cookies that we won't care about in this article because why would we.

### Why 

Cookies are super useful to browser users, to:
- keep them logged in
- not need to give their preference again

OK, the goal for the browser "to send it back with the next request to the same server" is to store stateful information from the stateless HTTP protocol. 

Cookies are used on the web since 1994 Netscape.
to "check whether visitors to the Netscape website had already visited the site." 
"Cookies are typically used to tell if two requests came from the same browser — to keep a user logged in or remember their display preferences."

### What's inside
A cookie is a key-value pair.  
Example:  
(img)

It also has metadata attached to it, such as an expiry date.

### How are cookies set/get


Request Cookie = Cookie the client sends along with the request.
Response Cookies = HTTP header name Set-Cookie (so this contains the "Request Cookie" value for all future requests).


Set: 2 ways:
- server-side: see https://developer.mozilla.org/en-US/docs/Web/HTTP/Cookies#Creating_cookies
// Basically a HTTP request is made, with Set-Cookie header.
- client-side: `document.cookie = "username=John Doe"`;
Get: 2 ways:
- server-side: see https://developer.mozilla.org/en-US/docs/Web/HTTP/Cookies#Creating_cookies
- client-side: `document.cookie`;

## Cookie types 

o | first-party | third-party
---------|----------|---------
 session | good: bad:  | xx
 persistent | B2 | C2


NB: it's a bit counter intuitive that session have expiry data and not others 

## Third-party magic

So, which one is evil?
Technically, all cookies are similar.

3rd-party cookies and associated concerns

Alread back then, some privacy issues were raised.
"Cookies were discussed in two U.S. Federal Trade Commission hearings in 1996 and 1997"
Sources:
https://en.wikipedia.org/wiki/HTTP_cookie#Alternatives_to_cookies 
http://www.historyofinformation.com/detail.php?id=2102


Evil, really?
Not that first party cookies too, can track your behaviour - only, not across other websites.
The law says it must be disclosed.


### How trackers work (or don't)

#### Trackers cryptonite
* DNT messages
* Set DNT in your browser
* Use a browser that does DNT by default
* Use browser extensions such as [Privacy Badger](https://addons.mozilla.org/en-US/firefox/addon/privacy-badger17/)
* Delete your cookies regularly

### Asides

#### Cookies and security concerns

- HTTP vs HTTPS
- session hijacking
- 


Note: 
If your cookie is set server-side, it will be readable by client code. 
(because you won't be able to use the HttpOnly flag)
So you're exposing your users to session hijacking: 
https://developer.mozilla.org/en-US/docs/Web/HTTP/Cookies#Session_hijacking_and_XSS or https://en.wikipedia.org/wiki/Session_hijacking


#### New flavours!
sameSite

#### Existential crisis
Cookie use is not encouraged anymore. 
Alternatives to cookies.

* Cookies vs redux
* Cookies vs localStorage
* Cookies vs other Alternatives---> see wikipedia


## Other members of the tracking mafia 
- fingerprinting (= next article)
