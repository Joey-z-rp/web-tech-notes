### Cookie
- can set expiration time for each cookie
- size limit: 4KB
- data sent back to the server for every Http request
- typically used to remember stateful information for the stateless HTTP protocol
- use `HttpOnly` to prevent XSS
- `Domain` specifies allowed hosts to receive the cookie(If unspecified, it defaults to the host of the current document location, excluding subdomains. If Domain is specified, then subdomains are always included.)
- `Pat`h indicates a URL path that must exist in the requested URL in order to send the Cookie header(subdirectories included)
- `SameSite` cookies let servers require that a cookie shouldn't be sent with cross-site (where Site is defined by the registrable domain) requests, which provides some protection against cross-site request forgery attacks (CSRF)

### Session Storage
- maintains a separate storage area for **each given origin** that's available for the **duration of the page session** (as long as the browser is open, including page reloads and restores)
- keys and values are always strings
- size limit: generally 5MB-10MB
- stored in hard-drive until explicitly deleted
- data not sent back to the server for every Http request
- data only available on the same origin

### Local Storage
- same as session storage but persists even when the browser is closed and reopened


---
Reference:
[Web Storage API](https://developer.mozilla.org/en-US/docs/Web/API/Web_Storage_API)
[HTTP cookies](https://developer.mozilla.org/en-US/docs/Web/HTTP/Cookies)