# npmtest-bytebuffer

#### basic test coverage for  bytebuffer (v5.0.1)  [![npm package](https://img.shields.io/npm/v/npmtest-bytebuffer.svg?style=flat-square)](https://www.npmjs.org/package/npmtest-bytebuffer) [![travis-ci.org build-status](https://api.travis-ci.org/npmtest/node-npmtest-bytebuffer.svg)](https://travis-ci.org/npmtest/node-npmtest-bytebuffer)

#### The swiss army knife for binary data in JavaScript.

[![NPM](https://nodei.co/npm/bytebuffer.png?downloads=true&downloadRank=true&stars=true)](https://www.npmjs.com/package/bytebuffer)

| git-branch : | [alpha](https://github.com/npmtest/node-npmtest-bytebuffer/tree/alpha)|
|--:|:--|
| coverage : | [![istanbul-coverage](https://npmtest.github.io/node-npmtest-bytebuffer/build/coverage.badge.svg)](https://npmtest.github.io/node-npmtest-bytebuffer/build/coverage.html/index.html)|
| test-report : | [![test-report](https://npmtest.github.io/node-npmtest-bytebuffer/build/test-report.badge.svg)](https://npmtest.github.io/node-npmtest-bytebuffer/build/test-report.html)|
| build-artifacts : | [![build-artifacts](https://npmtest.github.io/node-npmtest-bytebuffer/glyphicons_144_folder_open.png)](https://github.com/npmtest/node-npmtest-bytebuffer/tree/gh-pages/build)|

- [https://npmtest.github.io/node-npmtest-bytebuffer/build/coverage.html/index.html](https://npmtest.github.io/node-npmtest-bytebuffer/build/coverage.html/index.html)

[![istanbul-coverage](https://npmtest.github.io/node-npmtest-bytebuffer/build/screenCapture.buildCi.browser.%252Ftmp%252Fbuild%252Fcoverage.lib.html.png)](https://npmtest.github.io/node-npmtest-bytebuffer/build/coverage.html/index.html)

- [https://npmtest.github.io/node-npmtest-bytebuffer/build/test-report.html](https://npmtest.github.io/node-npmtest-bytebuffer/build/test-report.html)

[![test-report](https://npmtest.github.io/node-npmtest-bytebuffer/build/screenCapture.buildCi.browser.%252Ftmp%252Fbuild%252Ftest-report.html.png)](https://npmtest.github.io/node-npmtest-bytebuffer/build/test-report.html)

- [https://npmdoc.github.io/node-npmdoc-bytebuffer/build/apidoc.html](https://npmdoc.github.io/node-npmdoc-bytebuffer/build/apidoc.html)

[![apidoc](https://npmdoc.github.io/node-npmdoc-bytebuffer/build/screenCapture.buildCi.browser.%252Ftmp%252Fbuild%252Fapidoc.html.png)](https://npmdoc.github.io/node-npmdoc-bytebuffer/build/apidoc.html)

![npmPackageListing](https://npmtest.github.io/node-npmtest-bytebuffer/build/screenCapture.npmPackageListing.svg)

![npmPackageDependencyTree](https://npmtest.github.io/node-npmtest-bytebuffer/build/screenCapture.npmPackageDependencyTree.svg)



# package.json

```json

{
    "name": "bytebuffer",
    "version": "5.0.1",
    "author": "Daniel Wirtz <dcode@dcode.io>",
    "description": "The swiss army knife for binary data in JavaScript.",
    "main": "dist/bytebuffer-node.js",
    "browser": "dist/bytebuffer.js",
    "repository": {
        "type": "git",
        "url": "https://github.com/dcodeIO/bytebuffer.js.git"
    },
    "bugs": {
        "url": "https://github.com/dcodeIO/bytebuffer.js/issues"
    },
    "keywords": [
        "net",
        "array",
        "buffer",
        "arraybuffer",
        "typed array",
        "bytebuffer",
        "json",
        "websocket",
        "webrtc"
    ],
    "dependencies": {
        "long": "~3"
    },
    "devDependencies": {
        "closurecompiler": "~1",
        "lxiv": "~0.2",
        "metascript": "~0",
        "pretty-hrtime": "^1.0.0",
        "testjs": "~1",
        "utfx": "^1.0.1"
    },
    "license": "Apache-2.0",
    "engines": {
        "node": ">=0.8"
    },
    "scripts": {
        "prepublish": "npm test",
        "test": "node node_modules/testjs/bin/testjs tests/suite.js",
        "make": "npm run-script build && npm run-script compile && npm run-script compress && npm test",
        "build": "node scripts/build.js",
        "compile": "npm run-script compile-default && npm run-script compile-dataview",
        "compile-default": "ccjs dist/bytebuffer.js --create_source_map=dist/bytebuffer.min.map --externs=externs/minimal-env.js --externs=node_modules/long/externs/long.js > dist/bytebuffer.min.js",
        "compile-dataview": "ccjs dist/bytebuffer-dataview.js --create_source_map=dist/bytebuffer-dataview.min.map --externs=externs/minimal-env.js --externs=node_modules/long/externs/long.js > dist/bytebuffer-dataview.min.js",
        "compress": "gzip -c -9 dist/bytebuffer.min.js > dist/bytebuffer.min.js.gz && gzip -c -9 dist/bytebuffer-dataview.min.js > dist/bytebuffer-dataview.min.js.gz"
    }
}
```



# misc
- this document was created with [utility2](https://github.com/kaizhu256/node-utility2)
