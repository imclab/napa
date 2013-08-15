# napa
A helper for installing repos without a `package.json` with npm.

## usage

Install with `npm install napa` then setup your local `package.json` scripts as such:

```json
{
  "scripts": {
    "install": "node_modules/.bin/napa username/repo"
  }
}
```

Now when you run `npm install` it will `git clone git://github.com/username/repo node_modules/repo`.

### Want to name the package something else?

```json
{
  "scripts": {
    "install": "node_modules/.bin/napa username/repo:adifferentname"
  }
}
```

Now it will install to `node_modules/adifferentname`.

### Want to install a package not on github?

```json
{
  "scripts": {
    "install": "node_modules/.bin/napa git://example.com/user/repo:privatepackage"
  }
}
```

### Multiple packages?

```json
{
  "scripts": {
    "install": "node_modules/.bin/napa user/repo1:dude user/repo2:rad user/repo3:cool"
  }
}
```

### Install globally
If you don't like typing `node_modules/.bin` you can install this module globally with `npm install napa -g` then shorten to:

```json
{
  "scripts": {
    "install": "napa user/repo"
  }
}
```

## Release History
* 0.1.0 - initial release

## License
Copyright (c) 2013 Kyle Robinson Young  
Licensed under the MIT license.
