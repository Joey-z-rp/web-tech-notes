## URLs

### Absolute URLs VS Relative URLs
In the examples below I assume the website is running from the following location on the server `/var/www/mywebsite`.

#### `http://yourdomain.com/images/example.png`
This absolute url resolves to `/var/www/website/images/example.png`. This type of URL is something you would **always** want to avoid for requesting resources from your own website. However it can be used for requesting a resource from an external domain over a certain protocol e.g https (`https://externalsite.com/path/to/image.png`).


#### `//yourdomain.com/images/example.png`
This URL is relative based on the current scheme used and should **almost always** be used when including external resources (images, javascripts etc). It uses the current scheme of the page it is on.
E.g you are on the page `http://yourdomain.com` and on that page there is an image tag `<img src="//yourdomain.com/images/example.png">`, the URL of the image would resolve in `http://yourdomain.com/images/example.png`.
This prevent loading resources over https when it is not needed and automatically makes sure the resource is requested over https when it is needed.

#### `/images/example.png`
For local resources this is the **prefered** way of referencing them. This is a relative URL based on the document root (`/var/www/mywebsite`) of your website. This means when you have `<img src="/images/example.png">` it will always resolve to `/var/www/mywebsite/images/example.png`.

#### `images/example.png` or `./images/example.png`
This URL is relative to the current path. What this means is that it will resolve to different paths depending on where you are in the site.
For example when you are on the page `http://yourdomain.com` and you use `<img src="images/example.png">` it would resolve on the server to `/var/www/mywebsite/images/example.png` as expected, however when your are on the page `http://yourdomain.com/some/path` and you use the exact same image tag it suddenly will resolve to `/var/www/mywebsite/some/path/images/example.png`.

#### `../images/example.png`
This URL is a relative going up one level from current path.

### Query String
- key value pairs
- after `?`
- multiple query parameters are separated by the ampersand `&`
- the order of the queries doesn't matter
- example: `http://example.com/path/to/page?name=ferret&color=purple`

### Hashtag
- typically used to identify a portion of that document
- introduced by a hash mark `#`
- after query string
- does not refresh the page (no request being sent)
- targets `id` or `name`(deprecated)
- example: `http://www.example.org/foo.html#bar`

### Encoding/Decoding
- URLs can only be sent over the Internet using the ASCII character-set
- to convert URLs to/from a valid ASCII format
- replaces unsafe ASCII characters with a `%` followed by two hexadecimal digits
- replaces a space with a plus (+) sign or with %20
- uses `encodeURIComponent()` and `decodeURIComponent()`
- example: `?x=test` will be encoded to `%3Fx%3Dtest`

---
Reference:
[Absolute vs relative URLs](https://stackoverflow.com/questions/2005079/absolute-vs-relative-urls)
[Query string](https://en.wikipedia.org/wiki/Query_string)
[Fragment identifier](https://en.wikipedia.org/wiki/Fragment_identifier)
[HTML URL Encoding Reference](https://www.w3schools.com/tags/ref_urlencode.asp)