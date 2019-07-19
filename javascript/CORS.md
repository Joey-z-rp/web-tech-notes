### CORS
Cross-Origin Resource Sharing is a mechanism that uses additional HTTP headers to tell a browser to let a web application running at one origin (domain) have permission to access selected resources from a server at a different origin.

#### What requests use CORS?
- `XMLHttpRequest` or `Fetch`
- Web Fonts (for cross-domain font usage in `@font-face` within CSS)
- WebGL textures
- Images/video frames drawn to a canvas using `CanvasRenderingContext2D.drawImage()`, `drawImage()`.

#### Preflighted Requests
- **simple requests** don't trigger a preflight
- Other requests will trigger a preflight request by `OPTIONS` HTTP method

#### The HTTP response headers
- `Access-Control-Allow-Origin`
- `Access-Control-Expose-Headers`
- `Access-Control-Max-Age`
- `Access-Control-Allow-Credentials`
- `Access-Control-Allow-Methods`
- `Access-Control-Allow-Headers`

---
Reference:
[Cross-Origin Resource Sharing (CORS)](https://developer.mozilla.org/en-US/docs/Web/HTTP/CORS)