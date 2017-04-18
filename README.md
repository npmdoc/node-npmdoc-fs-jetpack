# npmdoc-fs-jetpack

#### api documentation for  [fs-jetpack (v0.13.3)](https://github.com/szwacz/fs-jetpack)  [![npm package](https://img.shields.io/npm/v/npmdoc-fs-jetpack.svg?style=flat-square)](https://www.npmjs.org/package/npmdoc-fs-jetpack) [![travis-ci.org build-status](https://api.travis-ci.org/npmdoc/node-npmdoc-fs-jetpack.svg)](https://travis-ci.org/npmdoc/node-npmdoc-fs-jetpack)

#### Better file system API

[![NPM](https://nodei.co/npm/fs-jetpack.png?downloads=true&downloadRank=true&stars=true)](https://www.npmjs.com/package/fs-jetpack)

- [https://npmdoc.github.io/node-npmdoc-fs-jetpack/build/apidoc.html](https://npmdoc.github.io/node-npmdoc-fs-jetpack/build/apidoc.html)

[![apidoc](https://npmdoc.github.io/node-npmdoc-fs-jetpack/build/screenCapture.buildCi.browser.%252Ftmp%252Fbuild%252Fapidoc.html.png)](https://npmdoc.github.io/node-npmdoc-fs-jetpack/build/apidoc.html)

![npmPackageListing](https://npmdoc.github.io/node-npmdoc-fs-jetpack/build/screenCapture.npmPackageListing.svg)

![npmPackageDependencyTree](https://npmdoc.github.io/node-npmdoc-fs-jetpack/build/screenCapture.npmPackageDependencyTree.svg)



# package.json

```json

{
    "author": {
        "name": "Jakub Szwacz"
    },
    "bugs": {
        "url": "https://github.com/szwacz/fs-jetpack/issues"
    },
    "dependencies": {
        "minimatch": "^3.0.2"
    },
    "description": "Better file system API",
    "devDependencies": {
        "chai": "^3.5.0",
        "codecov": "^1.0.1",
        "eslint": "^2.13.1",
        "eslint-config-airbnb-base": "^3.0.1",
        "eslint-plugin-import": "^1.9.2",
        "fs-extra": "^0.16.3",
        "istanbul": "^0.4.5",
        "lint-staged": "^3.4.0",
        "mocha": "^3.1.2",
        "pre-commit": "^1.1.2",
        "release-assist": "^1.0.1"
    },
    "directories": {},
    "dist": {
        "shasum": "9e6c47118f0bb3d880cc88f9f8a7d25863f4fb15",
        "tarball": "https://registry.npmjs.org/fs-jetpack/-/fs-jetpack-0.13.3.tgz"
    },
    "engines": {
        "node": ">=4"
    },
    "gitHead": "f863ebf73bf8bfa50a6d27ecee75d651336bf2e4",
    "homepage": "https://github.com/szwacz/fs-jetpack",
    "keywords": [
        "fs",
        "file system"
    ],
    "license": "MIT",
    "lint-staged": {
        "*.js": "eslint"
    },
    "main": "main.js",
    "maintainers": [
        {
            "name": "szwacz"
        }
    ],
    "name": "fs-jetpack",
    "optionalDependencies": {},
    "pre-commit": [
        "lint-staged",
        "test"
    ],
    "repository": {
        "type": "git",
        "url": "git+https://github.com/szwacz/fs-jetpack.git"
    },
    "scripts": {
        "lint": "eslint .",
        "lint-staged": "lint-staged",
        "release-finish": "release-assist --finish",
        "release-start": "release-assist --start",
        "test": "mocha \"spec/**/*.spec.js\"",
        "test-with-coverage": "istanbul cover node_modules/.bin/_mocha -- 'spec/**/*.spec.js'"
    },
    "version": "0.13.3"
}
```



# misc
- this document was created with [utility2](https://github.com/kaizhu256/node-utility2)
