# node-url

This module is a fork of [defunctzombie/node-url](https://github.com/defunctzombie/node-url), but built for ES3 support.

The upstream module itself is a [Browserify](http://browserify.org/) stand-in for the [node built-in `url`](https://nodejs.org/api/url.html).

## Installation

### Option A - for node + browser support

Install as a development dependency alongside browserify itself. And then configure Browserify to load `url-es3` in place of `url`.
This enables your code to use the node built-in `url` when running on node, but Browserify will substitute `url-es3` when running in the browser.

1. Install as dev dependency
``` shell
    npm install --save-dev url-es3
```
2. Configure browserify substitution in `package.json`
``` json
    browser: {
      "url": "url-es3"
    }
```
3. Require as `url`
``` javascript
    var url = require('url');
```

### Option B - for browser only (or intending to use url-es3 directly)

1. Install as production dependency
    ```` shell
    npm install --save url-es3
    ````
2. Require directly
    ```` javascript
    var url = require('url-es3');
    ````
## API

See [upstream module](https://github.com/defunctzombie/node-url) and [node builtin](https://nodejs.org/api/url.html).

