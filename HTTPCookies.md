# HTTP Cookies

An HTTP cookie (web cookie, browser cookie) is a small piece of data that a server sends to a user's web browser. The browser may 
store the cookie and send it back to the same server with later requests. Typically, an HTTP cookie is used to tell if two 
requests come from the same browser—keeping a user logged in, for example. It remembers stateful information for the stateless 
HTTP protocol.

*Cookies are mainly used for three purposes:*

*Session management*
Logins, shopping carts, game scores, or anything else the server should remember

*Personalization*
User preferences, themes, and other settings

*Tracking*
Recording and analyzing user behavior

Cookies were once used for general client-side storage. While this made sense when they were the only way to store data on the 
client, modern storage APIs are now recommended. Cookies are sent with every request, so they can worsen performance (especially 
for mobile data connections). Modern APIs for client storage are the Web Storage API (localStorage and sessionStorage) and 
IndexedDB.

### Creating cookies
After receiving an HTTP request, a server can send one or more Set-Cookie headers with the response. The browser usually stores 
the cookie and sends it with requests made to the same server inside a Cookie HTTP header. You can specify an expiration date or 
time period after which the cookie shouldn't be sent. You can also set additional restrictions to a specific domain and path to 
limit where the cookie is sent.

### The Set-Cookie and Cookie headers
The Set-Cookie HTTP response header sends cookies from the server to the user agent. A simple cookie is set like this:

<!-- Set-Cookie: <cookie-name>=<cookie-value> -->

### This instructs the server sending headers to tell the client to store a pair of cookies:

<!-- HTTP/2.0 200 OK
Content-Type: text/html
Set-Cookie: yummy_cookie=choco
Set-Cookie: tasty_cookie=strawberry -->

### Define the lifetime of a cookie

The lifetime of a cookie can be defined in two ways:

1.Session cookies are deleted when the current session ends. The browser defines when the "current session" ends, and some 
browsers 
use session restoring when restarting. This can cause session cookies to last indefinitely.

2.Permanent cookies are deleted at a date specified by the Expires attribute, or after a period of time specified by the Max-Age 
attribute.

### Restrict access to cookies
You can ensure that cookies are sent securely and aren't accessed by unintended parties or scripts in one of two ways:
1. with the 
2. Secure attribute and the HttpOnly attribute.

### Define where cookies are sent

The Domain and Path attributes define the scope of a cookie: what URLs the cookies should be sent to.

### Domain attribute
The Domain attribute specifies which hosts can receive a cookie. If unspecified, the attribute defaults to the same host that set 
the cookie, excluding subdomains. If Domain is specified, then subdomains are always included. Therefore, specifying Domain is 
less restrictive than omitting it. However, it can be helpful when subdomains need to share information about a user.

### SameSite attribute
The SameSite attribute lets servers specify whether/when cookies are sent with cross-site requests (where Site is defined by the 
registrable domain and the scheme: http or https). This provides some protection against cross-site request forgery attacks (CSRF)
It takes three possible values: Strict, Lax, and None.

### Cookie prefixes
Because of the design of the cookie mechanism, a server can't confirm that a cookie was set from a secure origin or even tell 
where a cookie was originally set.

A vulnerable application on a subdomain can set a cookie with the Domain attribute, which gives access to that cookie on all 
other subdomains. This mechanism can be abused in a session fixation attack. See session fixation for primary mitigation methods.

## Security

1.Use the HttpOnly attribute to prevent access to cookie values via JavaScript.

2.Cookies that are used for sensitive information (such as indicating authentication) should have a short lifetime, with the 
SameSite attribute set to Strict or Lax. (See SameSite attribute, above.) In browsers that support SameSite, this ensures that 
the authentication cookie isn't sent with cross-site requests. This would make the request effectively unauthenticated to the 
application server.

### Cookie-related regulations
Legislation or regulations that cover the use of cookies include:

1. The General Data Privacy Regulation (GDPR) in the European Union
2. The ePrivacy Directive in the EU
3. The California Consumer Privacy Act

### These regulations include requirements such as:

1. Notifying users that your site uses cookies.
2. Allowing users to opt out of receiving some or all cookies.
3. Allowing users to use the bulk of your service without receiving cookies.











