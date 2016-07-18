# Client Portal Assets

This repository holds a variety of assets which are used across the Client Portal ecosystem. The intent is that if they need to be changed, there is a single point where they are kept, and can be rolled out to apps by upgrading their dependency on this package.

# Usage

In order to include this into your application, add the following to your `dependencies` in your app's `package.json`:

    "client_portal-assets": "reevoo/client_portal-assets"

We highly recommend using [npm-shrinkwrap](https://docs.npmjs.com/cli/shrinkwrap) to ensure your dependencies are up to date.

# Development

## Font generation tools:

We are using [Font Custom](https://github.com/FontCustom/fontcustom) to generate a font family with svg icons, so we can customise their colour.		

```bash
# On Mac
brew install fontforge --with-python		
brew install eot-utils		

# On Linux
sudo apt-get install fontforge
wget http://people.mozilla.com/~jkew/woff/woff-code-latest.zip
unzip woff-code-latest.zip -d sfnt2woff && cd sfnt2woff && make && sudo mv sfnt2woff /usr/local/bin/
```

## Releasing a new version of client_portal-assets

Ensure the `package.json` is correct and then tag the new version with a semantic version number, prefixed with a "v", so version 1.2.1 (for example) would have tag "v1.2.1" on it.

# License

Given the fact that this contains Reevoo logos and trademarks, it has been licensed under [Apache 2.0](http://www.apache.org/licenses/LICENSE-2.0), see `LICENSE` for more details.
