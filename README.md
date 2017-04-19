# npmdoc-natural-brain

#### api documentation for  [natural-brain (v0.2.3)](https://github.com/mysamai/natural-brain)  [![npm package](https://img.shields.io/npm/v/npmdoc-natural-brain.svg?style=flat-square)](https://www.npmjs.org/package/npmdoc-natural-brain) [![travis-ci.org build-status](https://api.travis-ci.org/npmdoc/node-npmdoc-natural-brain.svg)](https://travis-ci.org/npmdoc/node-npmdoc-natural-brain)

#### A BrainJS neural network natural language classifier

[![NPM](https://nodei.co/npm/natural-brain.png?downloads=true&downloadRank=true&stars=true)](https://www.npmjs.com/package/natural-brain)

- [https://npmdoc.github.io/node-npmdoc-natural-brain/build/apidoc.html](https://npmdoc.github.io/node-npmdoc-natural-brain/build/apidoc.html)

[![apidoc](https://npmdoc.github.io/node-npmdoc-natural-brain/build/screenCapture.buildCi.browser.%252Ftmp%252Fbuild%252Fapidoc.html.png)](https://npmdoc.github.io/node-npmdoc-natural-brain/build/apidoc.html)

![npmPackageListing](https://npmdoc.github.io/node-npmdoc-natural-brain/build/screenCapture.npmPackageListing.svg)

![npmPackageDependencyTree](https://npmdoc.github.io/node-npmdoc-natural-brain/build/screenCapture.npmPackageDependencyTree.svg)



# package.json

```json

{
    "author": {
        "name": "David Luecke",
        "url": "https://feathersjs.com"
    },
    "bugs": {
        "url": "https://github.com/mysamai/natural-brain/issues"
    },
    "contributors": [],
    "dependencies": {
        "brain.js": "^0.7.0",
        "debug": "^2.2.0",
        "natural": "^0.4.0"
    },
    "description": "A BrainJS neural network natural language classifier",
    "devDependencies": {
        "babel-cli": "^6.10.1",
        "babel-core": "^6.10.4",
        "babel-plugin-add-module-exports": "^0.2.1",
        "babel-preset-es2015": "^6.9.0",
        "chai": "^3.5.0",
        "expect.js": "^0.3.1",
        "jshint": "^2.9.2",
        "mocha": "^2.5.3",
        "rimraf": "^2.5.3"
    },
    "directories": {
        "lib": "lib"
    },
    "dist": {
        "shasum": "b4650fc2efcb49047cbffffe3de89c9f16b4fd06",
        "tarball": "https://registry.npmjs.org/natural-brain/-/natural-brain-0.2.3.tgz"
    },
    "engines": {
        "node": ">= 0.12.0"
    },
    "gitHead": "f487bcc1862b056b6ea2373c5e470f09231cede3",
    "homepage": "https://github.com/mysamai/natural-brain",
    "keywords": [],
    "license": "MIT",
    "main": "lib/",
    "maintainers": [
        {
            "name": "daffl"
        }
    ],
    "name": "natural-brain",
    "optionalDependencies": {},
    "repository": {
        "type": "git",
        "url": "git://github.com/mysamai/natural-brain.git"
    },
    "scripts": {
        "changelog": "github_changelog_generator && git add CHANGELOG.md && git commit -am \"Updating changelog\"",
        "compile": "rimraf lib/ && babel -d lib/ src/",
        "jshint": "jshint src/. test/. --config",
        "mocha": "mocha --recursive test/ --compilers js:babel-core/register",
        "prepublish": "npm run compile",
        "publish": "git push origin --tags && npm run changelog && git push origin",
        "release:major": "npm version major && npm publish",
        "release:minor": "npm version minor && npm publish",
        "release:patch": "npm version patch && npm publish",
        "start": "npm run compile && node example/app",
        "test": "npm run compile && npm run jshint && npm run mocha",
        "watch": "babel --watch -d lib/ src/"
    },
    "version": "0.2.3"
}
```



# misc
- this document was created with [utility2](https://github.com/kaizhu256/node-utility2)
