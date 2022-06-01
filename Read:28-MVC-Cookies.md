# Read: 28 - MVC / Cookies
- HTTP cookie is a small piece of data that a server sends to a user's web browser.
- The browser may store the cookie and send it back to the same server with later requests.
- Typically, an HTTP cookie is used to tell if two requests come from the same browser—keeping a user logged in, for example.
-  It remembers stateful information for the stateless HTTP protocol.

## Creating cookies
```
Set-Cookie: <cookie-name>=<cookie-value>
```

This instructs the server sending headers to tell the client to store a pair of cookies:=>

HTTP/2.0 200 OK
Content-Type: text/html
Set-Cookie: yummy_cookie=choco
Set-Cookie: tasty_cookie=strawberry

## Define the lifetime of a cookie
For example:
Set-Cookie: id=a3fWa; Expires=Thu, 31 Oct 2021 07:28:00 GMT;
  
## Restrict access to cookies
Here's an example:

Set-Cookie: id=a3fWa; Expires=Thu, 21 Oct 2021 07:28:00 GMT; Secure; HttpOnly

## Define where cookies are sent
For example, if you set Domain=mozilla.org, cookies are available on subdomains like developer.mozilla.org.

## Cookie prefixes

__Host- => it's accepted in a Set-Cookie header only if it's also marked with the Secure attribute, was sent from a secure origin, does not include a Domain attribute, and has the Path attribute set to /.

__Secure-
it's accepted in a Set-Cookie header only if it's marked with the Secure attribute and was sent from a secure origin. This is weaker than the __Host- prefix.
