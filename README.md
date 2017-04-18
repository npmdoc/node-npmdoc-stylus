# npmdoc-stylus

#### api documentation for  [stylus (v0.54.5)](https://github.com/stylus/stylus)  [![npm package](https://img.shields.io/npm/v/npmdoc-stylus.svg?style=flat-square)](https://www.npmjs.org/package/npmdoc-stylus) [![travis-ci.org build-status](https://api.travis-ci.org/npmdoc/node-npmdoc-stylus.svg)](https://travis-ci.org/npmdoc/node-npmdoc-stylus)

#### Robust, expressive, and feature-rich CSS superset

[![NPM](https://nodei.co/npm/stylus.png?downloads=true&downloadRank=true&stars=true)](https://www.npmjs.com/package/stylus)

- [https://npmdoc.github.io/node-npmdoc-stylus/build/apidoc.html](https://npmdoc.github.io/node-npmdoc-stylus/build/apidoc.html)

[![apidoc](https://npmdoc.github.io/node-npmdoc-stylus/build/screenCapture.buildCi.browser.%252Ftmp%252Fbuild%252Fapidoc.html.png)](https://npmdoc.github.io/node-npmdoc-stylus/build/apidoc.html)

![npmPackageListing](https://npmdoc.github.io/node-npmdoc-stylus/build/screenCapture.npmPackageListing.svg)

![npmPackageDependencyTree](https://npmdoc.github.io/node-npmdoc-stylus/build/screenCapture.npmPackageDependencyTree.svg)



# package.json

```json

{
    "author": {
        "name": "TJ Holowaychuk"
    },
    "bin": {
        "stylus": "./bin/stylus"
    },
    "browserify": "./lib/browserify.js",
    "bugs": {
        "url": "https://github.com/stylus/stylus/issues"
    },
    "dependencies": {
        "css-parse": "1.7.x",
        "debug": "*",
        "glob": "7.0.x",
        "mkdirp": "0.5.x",
        "sax": "0.5.x",
        "source-map": "0.1.x"
    },
    "description": "Robust, expressive, and feature-rich CSS superset",
    "devDependencies": {
        "jscoverage": "0.3.8",
        "mocha": "*",
        "should": "8.x"
    },
    "directories": {
        "doc": "docs",
        "example": "examples",
        "test": "test"
    },
    "dist": {
        "shasum": "42b9560931ca7090ce8515a798ba9e6aa3d6dc79",
        "tarball": "https://registry.npmjs.org/stylus/-/stylus-0.54.5.tgz"
    },
    "engines": {
        "node": "*"
    },
    "gitHead": "5aff5ed0e3f482ed48f30110e24fccad7f5559ab",
    "homepage": "https://github.com/stylus/stylus",
    "keywords": [
        "css",
        "parser",
        "style",
        "stylesheets",
        "jade",
        "language"
    ],
    "license": "MIT",
    "main": "./index.js",
    "maintainers": [
        {
            "name": "kizu"
        },
        {
            "name": "panya"
        },
        {
            "name": "tjholowaychuk"
        }
    ],
    "name": "stylus",
    "optionalDependencies": {},
    "repository": {
        "type": "git",
        "url": "git://github.com/stylus/stylus.git"
    },
    "scripts": {
        "prepublish": "npm prune",
        "test": "mocha test/ test/middleware/ --require should --bail --check-leaks --reporter dot",
        "test-cov": "mocha test/ test/middleware/ --require should --bail --reporter html-cov > coverage.html"
    },
    "version": "0.54.5"
}
```



# misc
- this document was created with [utility2](https://github.com/kaizhu256/node-utility2)
