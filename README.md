# npmtest-satellizer

#### basic test coverage for  [satellizer (v0.15.5)](https://github.com/sahat/satellizer)  [![npm package](https://img.shields.io/npm/v/npmtest-satellizer.svg?style=flat-square)](https://www.npmjs.org/package/npmtest-satellizer) [![travis-ci.org build-status](https://api.travis-ci.org/npmtest/node-npmtest-satellizer.svg)](https://travis-ci.org/npmtest/node-npmtest-satellizer)

#### Token-based AngularJS Authentication

[![NPM](https://nodei.co/npm/satellizer.png?downloads=true&downloadRank=true&stars=true)](https://www.npmjs.com/package/satellizer)

| git-branch : | [alpha](https://github.com/npmtest/node-npmtest-satellizer/tree/alpha)|
|--:|:--|
| coverage : | [![istanbul-coverage](https://npmtest.github.io/node-npmtest-satellizer/build/coverage.badge.svg)](https://npmtest.github.io/node-npmtest-satellizer/build/coverage.html/index.html)|
| test-report : | [![test-report](https://npmtest.github.io/node-npmtest-satellizer/build/test-report.badge.svg)](https://npmtest.github.io/node-npmtest-satellizer/build/test-report.html)|
| test-server-github : | [![github.com test-server](https://npmtest.github.io/node-npmtest-satellizer/GitHub-Mark-32px.png)](https://npmtest.github.io/node-npmtest-satellizer/build/app/index.html) | | build-artifacts : | [![build-artifacts](https://npmtest.github.io/node-npmtest-satellizer/glyphicons_144_folder_open.png)](https://github.com/npmtest/node-npmtest-satellizer/tree/gh-pages/build)|

- [https://npmtest.github.io/node-npmtest-satellizer/build/coverage.html/index.html](https://npmtest.github.io/node-npmtest-satellizer/build/coverage.html/index.html)

[![istanbul-coverage](https://npmtest.github.io/node-npmtest-satellizer/build/screenCapture.buildCi.browser.%252Ftmp%252Fbuild%252Fcoverage.lib.html.png)](https://npmtest.github.io/node-npmtest-satellizer/build/coverage.html/index.html)

- [https://npmtest.github.io/node-npmtest-satellizer/build/test-report.html](https://npmtest.github.io/node-npmtest-satellizer/build/test-report.html)

[![test-report](https://npmtest.github.io/node-npmtest-satellizer/build/screenCapture.buildCi.browser.%252Ftmp%252Fbuild%252Ftest-report.html.png)](https://npmtest.github.io/node-npmtest-satellizer/build/test-report.html)

- [https://npmdoc.github.io/node-npmdoc-satellizer/build/apidoc.html](https://npmdoc.github.io/node-npmdoc-satellizer/build/apidoc.html)

[![apidoc](https://npmdoc.github.io/node-npmdoc-satellizer/build/screenCapture.buildCi.browser.%252Ftmp%252Fbuild%252Fapidoc.html.png)](https://npmdoc.github.io/node-npmdoc-satellizer/build/apidoc.html)

![npmPackageListing](https://npmtest.github.io/node-npmtest-satellizer/build/screenCapture.npmPackageListing.svg)

![npmPackageDependencyTree](https://npmtest.github.io/node-npmtest-satellizer/build/screenCapture.npmPackageDependencyTree.svg)



# package.json

```json

{
    "author": {
        "name": "Sahat Yalkabov",
        "url": "http://sahatyalkabov.com"
    },
    "bugs": {
        "url": "https://github.com/sahat/satellizer/issues"
    },
    "dependencies": {},
    "description": "Token-based AngularJS Authentication",
    "devDependencies": {
        "angular-mocks": "^1.5.8",
        "babel-core": "^6.14.0",
        "babel-eslint": "^6.1.2",
        "babel-loader": "^6.2.5",
        "babel-polyfill": "^6.13.0",
        "babel-preset-es2015": "^6.14.0",
        "babel-preset-es2015-rollup": "^1.2.0",
        "jasmine-core": "^2.4.1",
        "karma": "^1.2.0",
        "karma-coverage": "^1.1.1",
        "karma-jasmine": "^1.0.2",
        "karma-phantomjs-launcher": "^1.0.1",
        "karma-source-map-support": "^1.1.0",
        "karma-sourcemap-loader": "^0.3.7",
        "karma-typescript-preprocessor": "^0.2.1",
        "karma-webpack": "^1.8.0",
        "npm-run-all": "^3.0.0",
        "phantomjs-prebuilt": "^2.1.12",
        "publish-please": "^2.2.0",
        "rollup": "^0.34.10",
        "rollup-plugin-babel": "^2.6.1",
        "rollup-plugin-node-resolve": "^2.0.0",
        "rollup-plugin-typescript": "^0.8.1",
        "rollup-plugin-uglify": "^1.0.1",
        "supervisor": "^0.11.0",
        "ts-loader": "^0.8.2",
        "ts-node": "^1.3.0",
        "tslint": "~3.15.1",
        "tslint-loader": "^2.1.5",
        "typescript": "^1.8.10",
        "uglify-js": "^2.7.3",
        "webpack": "^1.13.2"
    },
    "directories": {},
    "dist": {
        "shasum": "43c93d2d361c4b6b6cf9d06d23b8881302b557a4",
        "tarball": "https://registry.npmjs.org/satellizer/-/satellizer-0.15.5.tgz"
    },
    "gitHead": "d9a1737a78dee17bcc4e358fa598587d119caad0",
    "homepage": "https://github.com/sahat/satellizer",
    "license": "MIT",
    "main": "dist/satellizer.js",
    "maintainers": [
        {
            "name": "sahat"
        }
    ],
    "name": "satellizer",
    "optionalDependencies": {},
    "repository": {
        "type": "git",
        "url": "git+https://github.com/sahat/satellizer.git"
    },
    "scripts": {
        "build": "npm run clean && tsc && rollup -c && uglifyjs dist/satellizer.js -o dist/satellizer.min.js && npm run copy",
        "bump": "npm version patch",
        "clean": "rimraf build dist",
        "copy": "npm-run-all copy:*",
        "copy:angular": "cp dist/satellizer.js examples/client/vendor",
        "copy:ionic": "cp -R dist examples/ionic/www/lib/satellizer",
        "copy:php": "cp -R examples/client/ examples/server/php/public/",
        "postversion": "npm test && npm run build && git add -A dist && git commit -m 'Release'",
        "publish-please": "publish-please",
        "start": "supervisor ./examples/server/node/server.js",
        "test": "karma start"
    },
    "tags": [
        "authentication",
        "login",
        "token",
        "jwt",
        "angularjs",
        "angular",
        "auth",
        "facebook",
        "google",
        "linkedin",
        "twitter",
        "foursquare",
        "github",
        "yahoo",
        "oauth",
        "oauth 1.0",
        "oauth 2.0",
        "oauth2",
        "oauth1",
        "sign-in",
        "social",
        "twitch"
    ],
    "version": "0.15.5",
    "bin": {}
}
```



# misc
- this document was created with [utility2](https://github.com/kaizhu256/node-utility2)
