# api documentation for  [natural-brain (v0.2.3)](https://github.com/mysamai/natural-brain)  [![npm package](https://img.shields.io/npm/v/npmdoc-natural-brain.svg?style=flat-square)](https://www.npmjs.org/package/npmdoc-natural-brain) [![travis-ci.org build-status](https://api.travis-ci.org/npmdoc/node-npmdoc-natural-brain.svg)](https://travis-ci.org/npmdoc/node-npmdoc-natural-brain)
#### A BrainJS neural network natural language classifier

[![NPM](https://nodei.co/npm/natural-brain.png?downloads=true)](https://www.npmjs.com/package/natural-brain)

[![apidoc](https://npmdoc.github.io/node-npmdoc-natural-brain/build/screenCapture.buildNpmdoc.browser._2Fhome_2Ftravis_2Fbuild_2Fnpmdoc_2Fnode-npmdoc-natural-brain_2Ftmp_2Fbuild_2Fapidoc.html.png)](https://npmdoc.github.io/node-npmdoc-natural-brain/build/apidoc.html)

![npmPackageListing](https://npmdoc.github.io/node-npmdoc-natural-brain/build/screenCapture.npmPackageListing.svg)

![npmPackageDependencyTree](https://npmdoc.github.io/node-npmdoc-natural-brain/build/screenCapture.npmPackageDependencyTree.svg)



# package.json

```json

{
    "author": {
        "name": "David Luecke",
        "email": "daff@neyeon.com",
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
            "name": "daffl",
            "email": "daff@neyeon.de"
        }
    ],
    "name": "natural-brain",
    "optionalDependencies": {},
    "readme": "ERROR: No README data found!",
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



# <a name="apidoc.tableOfContents"></a>[table of contents](#apidoc.tableOfContents)

#### [module natural-brain](#apidoc.module.natural-brain)
1.  [function <span class="apidocSignatureSpan">natural-brain.</span>disableStopWords ()](#apidoc.element.natural-brain.disableStopWords)
1.  [function <span class="apidocSignatureSpan">natural-brain.</span>enableStopWords ()](#apidoc.element.natural-brain.enableStopWords)
1.  [function <span class="apidocSignatureSpan">natural-brain.</span>load (filename, stemmer, callback)](#apidoc.element.natural-brain.load)
1.  [function <span class="apidocSignatureSpan">natural-brain.</span>restore (data, stemmer)](#apidoc.element.natural-brain.restore)
1.  object <span class="apidocSignatureSpan">natural-brain.</span>stopwords



# <a name="apidoc.module.natural-brain"></a>[module natural-brain](#apidoc.module.natural-brain)

#### <a name="apidoc.element.natural-brain.disableStopWords"></a>[function <span class="apidocSignatureSpan">natural-brain.</span>disableStopWords ()](#apidoc.element.natural-brain.disableStopWords)
- description and source-code
```javascript
disableStopWords = function () {
  _stopwords2.default.words.splice(0, _stopwords2.default.words.length);
  return stopwordsBackup;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.natural-brain.enableStopWords"></a>[function <span class="apidocSignatureSpan">natural-brain.</span>enableStopWords ()](#apidoc.element.natural-brain.enableStopWords)
- description and source-code
```javascript
enableStopWords = function () {
  if (!_stopwords2.default.length) {
    _stopwords2.default.words.push.apply(_stopwords2.default.words, stopwordsBackup);
  }
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.natural-brain.load"></a>[function <span class="apidocSignatureSpan">natural-brain.</span>load (filename, stemmer, callback)](#apidoc.element.natural-brain.load)
- description and source-code
```javascript
load = function (filename, stemmer, callback) {
  _classifier2.default.load(filename, function (err, classifier) {
    if (err) {
      callback(err);
    }
    callback(err, BrainJSClassifier.restore(classifier, stemmer));
  });
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.natural-brain.restore"></a>[function <span class="apidocSignatureSpan">natural-brain.</span>restore (data, stemmer)](#apidoc.element.natural-brain.restore)
- description and source-code
```javascript
restore = function (data, stemmer) {
  var result = new BrainJSClassifier({}, stemmer);

  result.classifier.brain.fromJSON(data.classifier.brain);
  result.docs = data.docs;
  result.features = data.features;

  return result;
}
```
- example usage
```shell
n/a
```



# misc
- this document was created with [utility2](https://github.com/kaizhu256/node-utility2)
