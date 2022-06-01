# Read: 28 - MVC / Cookies

a cookie is a small text file that is stored by a browser on the user’s machine. Cookies are plain text; they contain no executable code. A web page or server instructs a browser to store this information and then send it back with each subsequent request based on a set of rules.

- HTTP cookie is a small piece of data that a server sends to a user's web browser.
- The browser may store the cookie and send it back to the same server with later requests.
- Typically, an HTTP cookie is used to tell if two requests come from the same browser—keeping a user logged in, for example.
-  It remembers stateful information for the stateless HTTP protocol.

## Creating cookies
```
Set-Cookie: <cookie-name>=<cookie-value>
```

This instructs the server sending headers to tell the client to store a pair of cookies:=>

```
HTTP/2.0 200 OK
Content-Type: text/html
Set-Cookie: yummy_cookie=choco
Set-Cookie: tasty_cookie=strawberry
```

## The expires option
Each of the options after the cookie value are separated by a semicolon and space and each specifies rules about when the cookie should be sent back to the server. The first option is expires, which indicates when the cookie should no longer be sent to the server and therefore may be deleted by the browser. The value for this option is a date in the format Wdy, DD-Mon-YYYY HH:MM:SS GMT such as:

Set-Cookie: name=Nicholas; expires=Sat, 02 May 2009 23:38:25 GMT

## The domain option
The next option is domain, which indicates the domain(s) for which the cookie should be sent. By default, domain is set to the host name of the page setting the cookie, so the cookie value is sent whenever a request is made to the same host name.Â  For example, the default domain for a cookie set on this site would be www.nczonline.net. The domain option is used to widen the number of domains for which the cookie value will be sent. Sample:

Set-Cookie: name=Nicholas; domain=nczonline.net

## The path option
Another way to control when the Cookie header will be sent is to specify the path option. Similar to the domain option, path indicates a URL path that must exist in the requested resource before sending the Cookie header. This comparison is done by comparing the option value character-by-character against the start of the request URL. If the characters match, then the Cookie header is sent. Sample:

Set-Cookie: name=Nicholas; path=/blog



## Define the lifetime of a cookie
For example:

```
Set-Cookie: id=a3fWa; Expires=Thu, 31 Oct 2021 07:28:00 GMT;
```

## Restrict access to cookies
Here's an example:

```
Set-Cookie: id=a3fWa; Expires=Thu, 21 Oct 2021 07:28:00 GMT; Secure; HttpOnly
```

## Define where cookies are sent

```
For example, if you set Domain=mozilla.org, cookies are available on subdomains like developer.mozilla.org.
```
## The secure option
The last option is secure. Unlike the other options, this is just a flag and has no additional value specified. A secure cookie will only be sent to the server when a request is made using SSL and the HTTPS protocol. The idea that the contents of the cookie are of high value and could be potentially damaging to transmit as clear text. Sample:

Set-Cookie: name=Nicholas; secure
## Using expiration dates
When a cookie is created with an expiration date, that expiration date relates to the cookie identified by name-domain-path-secure. In order to change the expiration date of a cookie, you must specify the exact same tuple. When changing a cookie’s value, you need not set the expiration date each time because it’s not part of the identifying information. Example:

Set-Cookie: name=Mike; expires=Sat, 03 May 2025 17:44:22 GMT

## Cookie prefixes

__Host- => it's accepted in a Set-Cookie header only if it's also marked with the Secure attribute, was sent from a secure origin, does not include a Domain attribute, and has the Path attribute set to /.

__Secure- => it's accepted in a Set-Cookie header only if it's marked with the Secure attribute and was sent from a secure origin. This is weaker than the __Host- prefix.


