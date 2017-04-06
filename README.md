# api documentation for  [fs-jetpack (v0.13.3)](https://github.com/szwacz/fs-jetpack)  [![npm package](https://img.shields.io/npm/v/npmdoc-fs-jetpack.svg?style=flat-square)](https://www.npmjs.org/package/npmdoc-fs-jetpack) [![travis-ci.org build-status](https://api.travis-ci.org/npmdoc/node-npmdoc-fs-jetpack.svg)](https://travis-ci.org/npmdoc/node-npmdoc-fs-jetpack)
#### Better file system API

[![NPM](https://nodei.co/npm/fs-jetpack.png?downloads=true)](https://www.npmjs.com/package/fs-jetpack)

[![apidoc](https://npmdoc.github.io/node-npmdoc-fs-jetpack/build/screenCapture.buildNpmdoc.browser._2Fhome_2Ftravis_2Fbuild_2Fnpmdoc_2Fnode-npmdoc-fs-jetpack_2Ftmp_2Fbuild_2Fapidoc.html.png)](https://npmdoc.github.io/node-npmdoc-fs-jetpack/build/apidoc.html)

![npmPackageListing](https://npmdoc.github.io/node-npmdoc-fs-jetpack/build/screenCapture.npmPackageListing.svg)

![npmPackageDependencyTree](https://npmdoc.github.io/node-npmdoc-fs-jetpack/build/screenCapture.npmPackageDependencyTree.svg)



# package.json

```json

{
    "author": {
        "name": "Jakub Szwacz",
        "email": "jakub@szwacz.com"
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
            "name": "szwacz",
            "email": "jakub@szwacz.com"
        }
    ],
    "name": "fs-jetpack",
    "optionalDependencies": {},
    "pre-commit": [
        "lint-staged",
        "test"
    ],
    "readme": "ERROR: No README data found!",
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



# <a name="apidoc.tableOfContents"></a>[table of contents](#apidoc.tableOfContents)

#### [module fs-jetpack](#apidoc.module.fs-jetpack)
1.  [function <span class="apidocSignatureSpan">fs-jetpack.</span>append (path, data, options)](#apidoc.element.fs-jetpack.append)
1.  [function <span class="apidocSignatureSpan">fs-jetpack.</span>appendAsync (path, data, options)](#apidoc.element.fs-jetpack.appendAsync)
1.  [function <span class="apidocSignatureSpan">fs-jetpack.</span>copy (from, to, options)](#apidoc.element.fs-jetpack.copy)
1.  [function <span class="apidocSignatureSpan">fs-jetpack.</span>copyAsync (from, to, options)](#apidoc.element.fs-jetpack.copyAsync)
1.  [function <span class="apidocSignatureSpan">fs-jetpack.</span>createReadStream (path, options)](#apidoc.element.fs-jetpack.createReadStream)
1.  [function <span class="apidocSignatureSpan">fs-jetpack.</span>createWriteStream (path, options)](#apidoc.element.fs-jetpack.createWriteStream)
1.  [function <span class="apidocSignatureSpan">fs-jetpack.</span>cwd ()](#apidoc.element.fs-jetpack.cwd)
1.  [function <span class="apidocSignatureSpan">fs-jetpack.</span>dir (path, criteria)](#apidoc.element.fs-jetpack.dir)
1.  [function <span class="apidocSignatureSpan">fs-jetpack.</span>dirAsync (path, criteria)](#apidoc.element.fs-jetpack.dirAsync)
1.  [function <span class="apidocSignatureSpan">fs-jetpack.</span>exists (path)](#apidoc.element.fs-jetpack.exists)
1.  [function <span class="apidocSignatureSpan">fs-jetpack.</span>existsAsync (path)](#apidoc.element.fs-jetpack.existsAsync)
1.  [function <span class="apidocSignatureSpan">fs-jetpack.</span>file (path, criteria)](#apidoc.element.fs-jetpack.file)
1.  [function <span class="apidocSignatureSpan">fs-jetpack.</span>fileAsync (path, criteria)](#apidoc.element.fs-jetpack.fileAsync)
1.  [function <span class="apidocSignatureSpan">fs-jetpack.</span>find (startPath, options)](#apidoc.element.fs-jetpack.find)
1.  [function <span class="apidocSignatureSpan">fs-jetpack.</span>findAsync (startPath, options)](#apidoc.element.fs-jetpack.findAsync)
1.  [function <span class="apidocSignatureSpan">fs-jetpack.</span>inspect (path, fieldsToInclude)](#apidoc.element.fs-jetpack.inspect)
1.  [function <span class="apidocSignatureSpan">fs-jetpack.</span>inspectAsync (path, fieldsToInclude)](#apidoc.element.fs-jetpack.inspectAsync)
1.  [function <span class="apidocSignatureSpan">fs-jetpack.</span>inspectTree (path, options)](#apidoc.element.fs-jetpack.inspectTree)
1.  [function <span class="apidocSignatureSpan">fs-jetpack.</span>inspectTreeAsync (path, options)](#apidoc.element.fs-jetpack.inspectTreeAsync)
1.  [function <span class="apidocSignatureSpan">fs-jetpack.</span>list (path)](#apidoc.element.fs-jetpack.list)
1.  [function <span class="apidocSignatureSpan">fs-jetpack.</span>listAsync (path)](#apidoc.element.fs-jetpack.listAsync)
1.  [function <span class="apidocSignatureSpan">fs-jetpack.</span>move (from, to)](#apidoc.element.fs-jetpack.move)
1.  [function <span class="apidocSignatureSpan">fs-jetpack.</span>moveAsync (from, to)](#apidoc.element.fs-jetpack.moveAsync)
1.  [function <span class="apidocSignatureSpan">fs-jetpack.</span>path ()](#apidoc.element.fs-jetpack.path)
1.  [function <span class="apidocSignatureSpan">fs-jetpack.</span>read (path, returnAs)](#apidoc.element.fs-jetpack.read)
1.  [function <span class="apidocSignatureSpan">fs-jetpack.</span>readAsync (path, returnAs)](#apidoc.element.fs-jetpack.readAsync)
1.  [function <span class="apidocSignatureSpan">fs-jetpack.</span>remove (path)](#apidoc.element.fs-jetpack.remove)
1.  [function <span class="apidocSignatureSpan">fs-jetpack.</span>removeAsync (path)](#apidoc.element.fs-jetpack.removeAsync)
1.  [function <span class="apidocSignatureSpan">fs-jetpack.</span>rename (path, newName)](#apidoc.element.fs-jetpack.rename)
1.  [function <span class="apidocSignatureSpan">fs-jetpack.</span>renameAsync (path, newName)](#apidoc.element.fs-jetpack.renameAsync)
1.  [function <span class="apidocSignatureSpan">fs-jetpack.</span>symlink (symlinkValue, path)](#apidoc.element.fs-jetpack.symlink)
1.  [function <span class="apidocSignatureSpan">fs-jetpack.</span>symlinkAsync (symlinkValue, path)](#apidoc.element.fs-jetpack.symlinkAsync)
1.  [function <span class="apidocSignatureSpan">fs-jetpack.</span>write (path, data, options)](#apidoc.element.fs-jetpack.write)
1.  [function <span class="apidocSignatureSpan">fs-jetpack.</span>writeAsync (path, data, options)](#apidoc.element.fs-jetpack.writeAsync)
1.  object <span class="apidocSignatureSpan">fs-jetpack.</span>inspect_tree
1.  object <span class="apidocSignatureSpan">fs-jetpack.</span>streams
1.  object <span class="apidocSignatureSpan">fs-jetpack.</span>utils

#### [module fs-jetpack.append](#apidoc.module.fs-jetpack.append)
1.  [function <span class="apidocSignatureSpan">fs-jetpack.append.</span>async (path, data, options)](#apidoc.element.fs-jetpack.append.async)
1.  [function <span class="apidocSignatureSpan">fs-jetpack.append.</span>sync (path, data, options)](#apidoc.element.fs-jetpack.append.sync)
1.  [function <span class="apidocSignatureSpan">fs-jetpack.append.</span>validateInput (methodName, path, data, options)](#apidoc.element.fs-jetpack.append.validateInput)

#### [module fs-jetpack.dir](#apidoc.module.fs-jetpack.dir)
1.  [function <span class="apidocSignatureSpan">fs-jetpack.dir.</span>async (path, passedCriteria)](#apidoc.element.fs-jetpack.dir.async)
1.  [function <span class="apidocSignatureSpan">fs-jetpack.dir.</span>createAsync (path, opts)](#apidoc.element.fs-jetpack.dir.createAsync)
1.  [function <span class="apidocSignatureSpan">fs-jetpack.dir.</span>createSync (path, opts)](#apidoc.element.fs-jetpack.dir.createSync)
1.  [function <span class="apidocSignatureSpan">fs-jetpack.dir.</span>sync (path, passedCriteria)](#apidoc.element.fs-jetpack.dir.sync)
1.  [function <span class="apidocSignatureSpan">fs-jetpack.dir.</span>validateInput (methodName, path, criteria)](#apidoc.element.fs-jetpack.dir.validateInput)

#### [module fs-jetpack.exists](#apidoc.module.fs-jetpack.exists)
1.  [function <span class="apidocSignatureSpan">fs-jetpack.exists.</span>async (path)](#apidoc.element.fs-jetpack.exists.async)
1.  [function <span class="apidocSignatureSpan">fs-jetpack.exists.</span>sync (path)](#apidoc.element.fs-jetpack.exists.sync)
1.  [function <span class="apidocSignatureSpan">fs-jetpack.exists.</span>validateInput (methodName, path)](#apidoc.element.fs-jetpack.exists.validateInput)

#### [module fs-jetpack.file](#apidoc.module.fs-jetpack.file)
1.  [function <span class="apidocSignatureSpan">fs-jetpack.file.</span>async (path, passedCriteria)](#apidoc.element.fs-jetpack.file.async)
1.  [function <span class="apidocSignatureSpan">fs-jetpack.file.</span>sync (path, passedCriteria)](#apidoc.element.fs-jetpack.file.sync)
1.  [function <span class="apidocSignatureSpan">fs-jetpack.file.</span>validateInput (methodName, path, criteria)](#apidoc.element.fs-jetpack.file.validateInput)

#### [module fs-jetpack.find](#apidoc.module.fs-jetpack.find)
1.  [function <span class="apidocSignatureSpan">fs-jetpack.find.</span>async (path, options)](#apidoc.element.fs-jetpack.find.async)
1.  [function <span class="apidocSignatureSpan">fs-jetpack.find.</span>sync (path, options)](#apidoc.element.fs-jetpack.find.sync)
1.  [function <span class="apidocSignatureSpan">fs-jetpack.find.</span>validateInput (methodName, path, options)](#apidoc.element.fs-jetpack.find.validateInput)

#### [module fs-jetpack.inspect](#apidoc.module.fs-jetpack.inspect)
1.  [function <span class="apidocSignatureSpan">fs-jetpack.inspect.</span>async (path, options)](#apidoc.element.fs-jetpack.inspect.async)
1.  [function <span class="apidocSignatureSpan">fs-jetpack.inspect.</span>sync (path, options)](#apidoc.element.fs-jetpack.inspect.sync)
1.  [function <span class="apidocSignatureSpan">fs-jetpack.inspect.</span>validateInput (methodName, path, options)](#apidoc.element.fs-jetpack.inspect.validateInput)
1.  object <span class="apidocSignatureSpan">fs-jetpack.inspect.</span>supportedChecksumAlgorithms
1.  object <span class="apidocSignatureSpan">fs-jetpack.inspect.</span>symlinkOptions

#### [module fs-jetpack.inspect_tree](#apidoc.module.fs-jetpack.inspect_tree)
1.  [function <span class="apidocSignatureSpan">fs-jetpack.inspect_tree.</span>async (path, options)](#apidoc.element.fs-jetpack.inspect_tree.async)
1.  [function <span class="apidocSignatureSpan">fs-jetpack.inspect_tree.</span>sync (path, options)](#apidoc.element.fs-jetpack.inspect_tree.sync)
1.  [function <span class="apidocSignatureSpan">fs-jetpack.inspect_tree.</span>validateInput (methodName, path, options)](#apidoc.element.fs-jetpack.inspect_tree.validateInput)

#### [module fs-jetpack.list](#apidoc.module.fs-jetpack.list)
1.  [function <span class="apidocSignatureSpan">fs-jetpack.list.</span>async (path)](#apidoc.element.fs-jetpack.list.async)
1.  [function <span class="apidocSignatureSpan">fs-jetpack.list.</span>sync (path)](#apidoc.element.fs-jetpack.list.sync)
1.  [function <span class="apidocSignatureSpan">fs-jetpack.list.</span>validateInput (methodName, path)](#apidoc.element.fs-jetpack.list.validateInput)

#### [module fs-jetpack.move](#apidoc.module.fs-jetpack.move)
1.  [function <span class="apidocSignatureSpan">fs-jetpack.move.</span>async (from, to)](#apidoc.element.fs-jetpack.move.async)
1.  [function <span class="apidocSignatureSpan">fs-jetpack.move.</span>sync (from, to)](#apidoc.element.fs-jetpack.move.sync)
1.  [function <span class="apidocSignatureSpan">fs-jetpack.move.</span>validateInput (methodName, from, to)](#apidoc.element.fs-jetpack.move.validateInput)

#### [module fs-jetpack.read](#apidoc.module.fs-jetpack.read)
1.  [function <span class="apidocSignatureSpan">fs-jetpack.read.</span>async (path, returnAs)](#apidoc.element.fs-jetpack.read.async)
1.  [function <span class="apidocSignatureSpan">fs-jetpack.read.</span>sync (path, returnAs)](#apidoc.element.fs-jetpack.read.sync)
1.  [function <span class="apidocSignatureSpan">fs-jetpack.read.</span>validateInput (methodName, path, returnAs)](#apidoc.element.fs-jetpack.read.validateInput)

#### [module fs-jetpack.rename](#apidoc.module.fs-jetpack.rename)
1.  [function <span class="apidocSignatureSpan">fs-jetpack.rename.</span>async (path, newName)](#apidoc.element.fs-jetpack.rename.async)
1.  [function <span class="apidocSignatureSpan">fs-jetpack.rename.</span>sync (path, newName)](#apidoc.element.fs-jetpack.rename.sync)
1.  [function <span class="apidocSignatureSpan">fs-jetpack.rename.</span>validateInput (methodName, path, newName)](#apidoc.element.fs-jetpack.rename.validateInput)

#### [module fs-jetpack.streams](#apidoc.module.fs-jetpack.streams)
1.  [function <span class="apidocSignatureSpan">fs-jetpack.streams.</span>createReadStream (path, options)](#apidoc.element.fs-jetpack.streams.createReadStream)
1.  [function <span class="apidocSignatureSpan">fs-jetpack.streams.</span>createWriteStream (path, options)](#apidoc.element.fs-jetpack.streams.createWriteStream)

#### [module fs-jetpack.symlink](#apidoc.module.fs-jetpack.symlink)
1.  [function <span class="apidocSignatureSpan">fs-jetpack.symlink.</span>async (symlinkValue, path)](#apidoc.element.fs-jetpack.symlink.async)
1.  [function <span class="apidocSignatureSpan">fs-jetpack.symlink.</span>sync (symlinkValue, path)](#apidoc.element.fs-jetpack.symlink.sync)
1.  [function <span class="apidocSignatureSpan">fs-jetpack.symlink.</span>validateInput (methodName, symlinkValue, path)](#apidoc.element.fs-jetpack.symlink.validateInput)

#### [module fs-jetpack.utils](#apidoc.module.fs-jetpack.utils)
1.  [function <span class="apidocSignatureSpan">fs-jetpack.utils.</span>cleanAfterTest ()](#apidoc.element.fs-jetpack.utils.cleanAfterTest)
1.  [function <span class="apidocSignatureSpan">fs-jetpack.utils.</span>exec ()](#apidoc.element.fs-jetpack.utils.exec)
1.  [function <span class="apidocSignatureSpan">fs-jetpack.utils.</span>prepareFiles (jetpackDir, creationConfig)](#apidoc.element.fs-jetpack.utils.prepareFiles)
1.  [function <span class="apidocSignatureSpan">fs-jetpack.utils.</span>prepareJetpackTestDir ()](#apidoc.element.fs-jetpack.utils.prepareJetpackTestDir)
1.  [function <span class="apidocSignatureSpan">fs-jetpack.utils.</span>showDifferenceInfo (jetpackTime, nativeTime)](#apidoc.element.fs-jetpack.utils.showDifferenceInfo)
1.  [function <span class="apidocSignatureSpan">fs-jetpack.utils.</span>startTimer (startMessage)](#apidoc.element.fs-jetpack.utils.startTimer)
1.  [function <span class="apidocSignatureSpan">fs-jetpack.utils.</span>waitAWhile ()](#apidoc.element.fs-jetpack.utils.waitAWhile)

#### [module fs-jetpack.write](#apidoc.module.fs-jetpack.write)
1.  [function <span class="apidocSignatureSpan">fs-jetpack.write.</span>async (path, data, options)](#apidoc.element.fs-jetpack.write.async)
1.  [function <span class="apidocSignatureSpan">fs-jetpack.write.</span>sync (path, data, options)](#apidoc.element.fs-jetpack.write.sync)
1.  [function <span class="apidocSignatureSpan">fs-jetpack.write.</span>validateInput (methodName, path, data, options)](#apidoc.element.fs-jetpack.write.validateInput)



# <a name="apidoc.module.fs-jetpack"></a>[module fs-jetpack](#apidoc.module.fs-jetpack)

#### <a name="apidoc.element.fs-jetpack.append"></a>[function <span class="apidocSignatureSpan">fs-jetpack.</span>append (path, data, options)](#apidoc.element.fs-jetpack.append)
- description and source-code
```javascript
append = function (path, data, options) {
  append.validateInput('append', path, data, options);
  append.sync(resolvePath(path), data, options);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.fs-jetpack.appendAsync"></a>[function <span class="apidocSignatureSpan">fs-jetpack.</span>appendAsync (path, data, options)](#apidoc.element.fs-jetpack.appendAsync)
- description and source-code
```javascript
appendAsync = function (path, data, options) {
  append.validateInput('appendAsync', path, data, options);
  return append.async(resolvePath(path), data, options);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.fs-jetpack.copy"></a>[function <span class="apidocSignatureSpan">fs-jetpack.</span>copy (from, to, options)](#apidoc.element.fs-jetpack.copy)
- description and source-code
```javascript
copy = function (from, to, options) {
  copy.validateInput('copy', from, to, options);
  copy.sync(resolvePath(from), resolvePath(to), options);
}
```
- example usage
```shell
...

**returns:**
Nothing.

**examples:**
'''javascript
// Copies a file (and replaces it if one already exists in 'foo' directory)
jetpack.copy('file.txt', 'foo/file.txt', { overwrite: true });

// Copies only '.md' files from 'foo' (and subdirectories of 'foo') to 'bar'.
jetpack.copy('foo', 'bar', { matching: '*.md' });
// Copies only '.md' and '.txt' files from 'foo' (and subdirectories of 'foo') to 'bar'.
jetpack.copy('foo', 'bar', { matching: ['*.md', '*.txt'] });

// You can filter previous matches by defining negated pattern further in the order:
...
```

#### <a name="apidoc.element.fs-jetpack.copyAsync"></a>[function <span class="apidocSignatureSpan">fs-jetpack.</span>copyAsync (from, to, options)](#apidoc.element.fs-jetpack.copyAsync)
- description and source-code
```javascript
copyAsync = function (from, to, options) {
  copy.validateInput('copyAsync', from, to, options);
  return copy.async(resolvePath(from), resolvePath(to), options);
}
```
- example usage
```shell
...

var test = function (testConfig) {
console.log('');

return utils.prepareFiles(toCopyDir, testConfig)
.then(utils.waitAWhile)
.then(function () {
  timer = utils.startTimer('jetpack.copyAsync()');
  return toCopyDir.copyAsync('.', testDir.path('copied-jetpack'));
})
.then(function () {
  jetpackTime = timer();
  return utils.waitAWhile();
})
.then(function () {
...
```

#### <a name="apidoc.element.fs-jetpack.createReadStream"></a>[function <span class="apidocSignatureSpan">fs-jetpack.</span>createReadStream (path, options)](#apidoc.element.fs-jetpack.createReadStream)
- description and source-code
```javascript
createReadStream = function (path, options) {
  return streams.createReadStream(resolvePath(path), options);
}
```
- example usage
```shell
...
// ---------------------------------------------------------
// Async
// ---------------------------------------------------------

var fileChecksumAsync = function (path, algo) {
return new Promise(function (resolve, reject) {
  var hash = crypto.createHash(algo);
  var s = fs.createReadStream(path);
  s.on('data', function (data) {
    hash.update(data);
  });
  s.on('end', function () {
    resolve(hash.digest('hex'));
  });
  s.on('error', reject);
...
```

#### <a name="apidoc.element.fs-jetpack.createWriteStream"></a>[function <span class="apidocSignatureSpan">fs-jetpack.</span>createWriteStream (path, options)](#apidoc.element.fs-jetpack.createWriteStream)
- description and source-code
```javascript
createWriteStream = function (path, options) {
  return streams.createWriteStream(resolvePath(path), options);
}
```
- example usage
```shell
...
},
copyAsync: function (from, to, options) {
  copy.validateInput('copyAsync', from, to, options);
  return copy.async(resolvePath(from), resolvePath(to), options);
},

createWriteStream: function (path, options) {
  return streams.createWriteStream(resolvePath(path), options);
},
createReadStream: function (path, options) {
  return streams.createReadStream(resolvePath(path), options);
},

dir: function (path, criteria) {
  var normalizedPath;
...
```

#### <a name="apidoc.element.fs-jetpack.cwd"></a>[function <span class="apidocSignatureSpan">fs-jetpack.</span>cwd ()](#apidoc.element.fs-jetpack.cwd)
- description and source-code
```javascript
cwd = function () {
  var args;
  var pathParts;

  // return current CWD if no arguments specified...
  if (arguments.length === 0) {
    return getCwdPath();
  }

  // ...create new CWD context otherwise
  args = Array.prototype.slice.call(arguments);
  pathParts = [getCwdPath()].concat(args);
  return jetpackContext(pathUtil.resolve.apply(null, pathParts));
}
```
- example usage
```shell
...
Just an alias to vanilla [fs.createWriteStream](http://nodejs.org/api/fs.html#fs_fs_createwritestream_path_options).



## cwd([path...])
Returns Current Working Directory (CWD) for this instance of jetpack, or creates new jetpack object with given path as its internal
 CWD.

**Note:** fs-jetpack never changes value of 'process.cwd()', the CWD we are talking about here is internal value inside every jetpack
 instance.

**arguments:**
'path...' (optional) path (or many path parts) to become new CWD. Could be absolute, or relative. If relative path given new CWD
 will be resolved basing on current CWD of this jetpack instance.

**returns:**
If 'path' not specified, returns CWD path of this jetpack object. For main instance of fs-jetpack it is always 'process.cwd()'.
If 'path' specified, returns new jetpack object (totally the same thing as main jetpack). The new object resolves paths according
 to its internal CWD, not the global one ('process.cwd()').
...
```

#### <a name="apidoc.element.fs-jetpack.dir"></a>[function <span class="apidocSignatureSpan">fs-jetpack.</span>dir (path, criteria)](#apidoc.element.fs-jetpack.dir)
- description and source-code
```javascript
dir = function (path, criteria) {
  var normalizedPath;
  dir.validateInput('dir', path, criteria);
  normalizedPath = resolvePath(path);
  dir.sync(normalizedPath, criteria);
  return cwd(normalizedPath);
}
```
- example usage
```shell
...
// jetpack.cwd() will always return the same value as process.cwd()
console.log(jetpack.cwd()); // '/one/two/three'

// Now let's create new CWD context...
var jetParent = jetpack.cwd('..');
console.log(jetParent.cwd()); // '/one/two'
// ...and use this new context.
jetParent.dir('four'); // we just created directory '/one/two/four'

// One CWD context can be used to create next CWD context.
var jetParentParent = jetParent.cwd('..');
console.log(jetParentParent.cwd()); // '/one'

// When many parameters specified they are treated as parts of path to resolve
var sillyCwd = jetpack.cwd('a', 'b', 'c');
...
```

#### <a name="apidoc.element.fs-jetpack.dirAsync"></a>[function <span class="apidocSignatureSpan">fs-jetpack.</span>dirAsync (path, criteria)](#apidoc.element.fs-jetpack.dirAsync)
- description and source-code
```javascript
dirAsync = function (path, criteria) {
  dir.validateInput('dirAsync', path, criteria);
  return new Promise(function (resolve, reject) {
    var normalizedPath = resolvePath(path);
    dir.async(normalizedPath, criteria)
    .then(function () {
      resolve(cwd(normalizedPath));
    }, reject);
  });
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.fs-jetpack.exists"></a>[function <span class="apidocSignatureSpan">fs-jetpack.</span>exists (path)](#apidoc.element.fs-jetpack.exists)
- description and source-code
```javascript
exists = function (path) {
  exists.validateInput('exists', path);
  return exists.sync(resolvePath(path));
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.fs-jetpack.existsAsync"></a>[function <span class="apidocSignatureSpan">fs-jetpack.</span>existsAsync (path)](#apidoc.element.fs-jetpack.existsAsync)
- description and source-code
```javascript
existsAsync = function (path) {
  exists.validateInput('existsAsync', path);
  return exists.async(resolvePath(path));
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.fs-jetpack.file"></a>[function <span class="apidocSignatureSpan">fs-jetpack.</span>file (path, criteria)](#apidoc.element.fs-jetpack.file)
- description and source-code
```javascript
file = function (path, criteria) {
  file.validateInput('file', path, criteria);
  file.sync(resolvePath(path), criteria);
  return this;
}
```
- example usage
```shell
...

**returns:**
Jetpack object you called this method on (self).

**examples:**
'''javascript
// Creates file if doesn't exist
jetpack.file('something.txt');

// Creates file with mode '777' and content 'Hello World!'
jetpack.file('hello.txt', { mode: '777', content: 'Hello World!' });
'''


## find([path], searchOptions)
...
```

#### <a name="apidoc.element.fs-jetpack.fileAsync"></a>[function <span class="apidocSignatureSpan">fs-jetpack.</span>fileAsync (path, criteria)](#apidoc.element.fs-jetpack.fileAsync)
- description and source-code
```javascript
fileAsync = function (path, criteria) {
  var that = this;
  file.validateInput('fileAsync', path, criteria);
  return new Promise(function (resolve, reject) {
    file.async(resolvePath(path), criteria)
    .then(function () {
      resolve(that);
    }, reject);
  });
}
```
- example usage
```shell
...

var prepareFiles = function (jetpackDir, creationConfig) {
  return new Promise(function (resolve, reject) {
var count = 0;
var content = new Buffer(creationConfig.size);

var makeOneFile = function () {
  jetpackDir.fileAsync(count + '.txt', { content: content })
  .then(function () {
    count += 1;
    if (count < creationConfig.files) {
      makeOneFile();
    } else {
      resolve();
    }
...
```

#### <a name="apidoc.element.fs-jetpack.find"></a>[function <span class="apidocSignatureSpan">fs-jetpack.</span>find (startPath, options)](#apidoc.element.fs-jetpack.find)
- description and source-code
```javascript
find = function (startPath, options) {
  // startPath is optional parameter, if not specified move rest of params
  // to proper places and default startPath to CWD.
  if (typeof options === 'undefined' && typeof startPath === 'object') {
    options = startPath;
    startPath = '.';
  }
  find.validateInput('find', startPath, options);
  return find.sync(resolvePath(startPath), normalizeOptions(options));
}
```
- example usage
```shell
...

**returns:**
'Array' of found paths.

**examples:**
'''javascript
// Finds all files which has 2015 in the name
jetpack.find('my-work', { matching: '*2015*' });

// Finds all '.txt' files inside 'foo/bar' directory and its subdirectories
jetpack.find('foo', { matching: 'bar/**/*.txt' });
// Finds all '.txt' files inside 'foo/bar' directory WITHOUT subdirectories
jetpack.find('foo', { matching: 'bar/*.txt' });

// Finds all '.js' files inside 'my-project' but excluding those in 'vendor' subtree.
...
```

#### <a name="apidoc.element.fs-jetpack.findAsync"></a>[function <span class="apidocSignatureSpan">fs-jetpack.</span>findAsync (startPath, options)](#apidoc.element.fs-jetpack.findAsync)
- description and source-code
```javascript
findAsync = function (startPath, options) {
  // startPath is optional parameter, if not specified move rest of params
  // to proper places and default startPath to CWD.
  if (typeof options === 'undefined' && typeof startPath === 'object') {
    options = startPath;
    startPath = '.';
  }
  find.validateInput('findAsync', startPath, options);
  return find.async(resolvePath(startPath), normalizeOptions(options));
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.fs-jetpack.inspect"></a>[function <span class="apidocSignatureSpan">fs-jetpack.</span>inspect (path, fieldsToInclude)](#apidoc.element.fs-jetpack.inspect)
- description and source-code
```javascript
inspect = function (path, fieldsToInclude) {
  inspect.validateInput('inspect', path, fieldsToInclude);
  return inspect.sync(resolvePath(path), fieldsToInclude);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.fs-jetpack.inspectAsync"></a>[function <span class="apidocSignatureSpan">fs-jetpack.</span>inspectAsync (path, fieldsToInclude)](#apidoc.element.fs-jetpack.inspectAsync)
- description and source-code
```javascript
inspectAsync = function (path, fieldsToInclude) {
  inspect.validateInput('inspectAsync', path, fieldsToInclude);
  return inspect.async(resolvePath(path), fieldsToInclude);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.fs-jetpack.inspectTree"></a>[function <span class="apidocSignatureSpan">fs-jetpack.</span>inspectTree (path, options)](#apidoc.element.fs-jetpack.inspectTree)
- description and source-code
```javascript
inspectTree = function (path, options) {
  inspectTree.validateInput('inspectTree', path, options);
  return inspectTree.sync(resolvePath(path), options);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.fs-jetpack.inspectTreeAsync"></a>[function <span class="apidocSignatureSpan">fs-jetpack.</span>inspectTreeAsync (path, options)](#apidoc.element.fs-jetpack.inspectTreeAsync)
- description and source-code
```javascript
inspectTreeAsync = function (path, options) {
  inspectTree.validateInput('inspectTreeAsync', path, options);
  return inspectTree.async(resolvePath(path), options);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.fs-jetpack.list"></a>[function <span class="apidocSignatureSpan">fs-jetpack.</span>list (path)](#apidoc.element.fs-jetpack.list)
- description and source-code
```javascript
list = function (path) {
  list.validateInput('list', path);
  return list.sync(resolvePath(path || '.'));
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.fs-jetpack.listAsync"></a>[function <span class="apidocSignatureSpan">fs-jetpack.</span>listAsync (path)](#apidoc.element.fs-jetpack.listAsync)
- description and source-code
```javascript
listAsync = function (path) {
  list.validateInput('listAsync', path);
  return list.async(resolvePath(path || '.'));
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.fs-jetpack.move"></a>[function <span class="apidocSignatureSpan">fs-jetpack.</span>move (from, to)](#apidoc.element.fs-jetpack.move)
- description and source-code
```javascript
move = function (from, to) {
  move.validateInput('move', from, to);
  move.sync(resolvePath(from), resolvePath(to));
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.fs-jetpack.moveAsync"></a>[function <span class="apidocSignatureSpan">fs-jetpack.</span>moveAsync (from, to)](#apidoc.element.fs-jetpack.moveAsync)
- description and source-code
```javascript
moveAsync = function (from, to) {
  move.validateInput('moveAsync', from, to);
  return move.async(resolvePath(from), resolvePath(to));
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.fs-jetpack.path"></a>[function <span class="apidocSignatureSpan">fs-jetpack.</span>path ()](#apidoc.element.fs-jetpack.path)
- description and source-code
```javascript
path = function () {
  // add CWD base path as first element of arguments array
  Array.prototype.unshift.call(arguments, getCwdPath());
  return pathUtil.resolve.apply(null, arguments);
}
```
- example usage
```shell
...

**returns:**
Resolved path as string.

**examples:**
'''javascript
jetpack.cwd(); // if it returns '/one/two'
jetpack.path(); // this will return the same '/one/two'
jetpack.path('three'); // this will return '/one/two/three'
jetpack.path('..', 'four'); // this will return '/one/four'
'''


## read(path, [returnAs])
asynchronous: **readAsync(path, [returnAs])**
...
```

#### <a name="apidoc.element.fs-jetpack.read"></a>[function <span class="apidocSignatureSpan">fs-jetpack.</span>read (path, returnAs)](#apidoc.element.fs-jetpack.read)
- description and source-code
```javascript
read = function (path, returnAs) {
  read.validateInput('read', path, returnAs);
  return read.sync(resolvePath(path), returnAs);
}
```
- example usage
```shell
...

Commonly used naming convention in Node world is reversed in this library (no 'method' and 'methodSync' naming). Asynchronous methods
 are those with 'Async' suffix, all methods without 'Async' in the name are synchronous. Reason behind this is that it gives very
 nice look to blocking API. And promise-based, non-blocking code is verbose anyway, so one more word is not much of a difference
.

Also it's just convenient...

If you don't see the word "Async" in method name it returns value immediately.
'''js
var data = jetpack.read('file.txt');
console.log(data);
'''

When you see "Async" that method returns promise which when resolved returns value.
'''js
jetpack.readAsync('file.txt')
.then(function (data) {
...
```

#### <a name="apidoc.element.fs-jetpack.readAsync"></a>[function <span class="apidocSignatureSpan">fs-jetpack.</span>readAsync (path, returnAs)](#apidoc.element.fs-jetpack.readAsync)
- description and source-code
```javascript
readAsync = function (path, returnAs) {
  read.validateInput('readAsync', path, returnAs);
  return read.async(resolvePath(path), returnAs);
}
```
- example usage
```shell
...
'''js
var data = jetpack.read('file.txt');
console.log(data);
'''

When you see "Async" that method returns promise which when resolved returns value.
'''js
jetpack.readAsync('file.txt')
.then(function (data) {
  console.log(data);
});
'''

# API
...
```

#### <a name="apidoc.element.fs-jetpack.remove"></a>[function <span class="apidocSignatureSpan">fs-jetpack.</span>remove (path)](#apidoc.element.fs-jetpack.remove)
- description and source-code
```javascript
remove = function (path) {
  remove.validateInput('remove', path);
  // If path not specified defaults to CWD
  remove.sync(resolvePath(path || '.'));
}
```
- example usage
```shell
...

**returns:**
Nothing.

**examples:**
'''javascript
// Deletes file
jetpack.remove('my_work/notes.txt');

// Deletes directory "important_stuff" and everything inside
jetpack.remove('my_work/important_stuff');

// Remove can be called with no parameters and will default to CWD then.
// In this example folder 'my_work' will cease to exist.
var myStuffDir = jetpack.cwd('my_stuff');
...
```

#### <a name="apidoc.element.fs-jetpack.removeAsync"></a>[function <span class="apidocSignatureSpan">fs-jetpack.</span>removeAsync (path)](#apidoc.element.fs-jetpack.removeAsync)
- description and source-code
```javascript
removeAsync = function (path) {
  remove.validateInput('removeAsync', path);
  // If path not specified defaults to CWD
  return remove.async(resolvePath(path || '.'));
}
```
- example usage
```shell
...

return utils.prepareFiles(dirJet, testConfig)
.then(function () {
  return utils.prepareFiles(dirNative, testConfig);
})
.then(utils.waitAWhile)
.then(function () {
  timer = utils.startTimer('jetpack.removeAsync()');
  return dirJet.removeAsync();
})
.then(function () {
  jetpackTime = timer();
  return utils.waitAWhile();
})
.then(function () {
...
```

#### <a name="apidoc.element.fs-jetpack.rename"></a>[function <span class="apidocSignatureSpan">fs-jetpack.</span>rename (path, newName)](#apidoc.element.fs-jetpack.rename)
- description and source-code
```javascript
rename = function (path, newName) {
  rename.validateInput('rename', path, newName);
  rename.sync(resolvePath(path), newName);
}
```
- example usage
```shell
...

**returns:**
Nothing.

**examples:**
'''javascript
// The file "my_work/important.md" will be renamed to "my_work/very_important.md"
jetpack.rename('my_work/important.txt', 'very_important.md');
'''

## symlink(symlinkValue, path)
asynchronous: **symlinkAsync(symlinkValue, path)**

Creates symbolic link.
...
```

#### <a name="apidoc.element.fs-jetpack.renameAsync"></a>[function <span class="apidocSignatureSpan">fs-jetpack.</span>renameAsync (path, newName)](#apidoc.element.fs-jetpack.renameAsync)
- description and source-code
```javascript
renameAsync = function (path, newName) {
  rename.validateInput('renameAsync', path, newName);
  return rename.async(resolvePath(path), newName);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.fs-jetpack.symlink"></a>[function <span class="apidocSignatureSpan">fs-jetpack.</span>symlink (symlinkValue, path)](#apidoc.element.fs-jetpack.symlink)
- description and source-code
```javascript
symlink = function (symlinkValue, path) {
  symlink.validateInput('symlink', symlinkValue, path);
  symlink.sync(symlinkValue, resolvePath(path));
}
```
- example usage
```shell
...

// ---------------------------------------------------------
// Async
// ---------------------------------------------------------

var symlinkAsync = function (symlinkValue, path) {
return new Promise(function (resolve, reject) {
  fs.symlink(symlinkValue, path)
  .then(resolve)
  .catch(function (err) {
    if (err.code === 'ENOENT') {
      // Parent directories don't exist. Just create them and rety.
      dir.createAsync(pathUtil.dirname(path))
      .then(function () {
        return fs.symlink(symlinkValue, path);
...
```

#### <a name="apidoc.element.fs-jetpack.symlinkAsync"></a>[function <span class="apidocSignatureSpan">fs-jetpack.</span>symlinkAsync (symlinkValue, path)](#apidoc.element.fs-jetpack.symlinkAsync)
- description and source-code
```javascript
symlinkAsync = function (symlinkValue, path) {
  symlink.validateInput('symlinkAsync', symlinkValue, path);
  return symlink.async(symlinkValue, resolvePath(path));
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.fs-jetpack.write"></a>[function <span class="apidocSignatureSpan">fs-jetpack.</span>write (path, data, options)](#apidoc.element.fs-jetpack.write)
- description and source-code
```javascript
write = function (path, data, options) {
  write.validateInput('write', path, data, options);
  write.sync(resolvePath(path), data, options);
}
```
- example usage
```shell
...
        humanReadableFileSize(creationConfig.size, true) + ' each)...');
    makeOneFile();
  });
};

var startTimer = function (startMessage) {
  var start = Date.now();
  process.stdout.write(startMessage + ' ... ');
  return function stop() {
    var time = Date.now() - start;
    console.log(time + 'ms');
    return time;
  };
};
...
```

#### <a name="apidoc.element.fs-jetpack.writeAsync"></a>[function <span class="apidocSignatureSpan">fs-jetpack.</span>writeAsync (path, data, options)](#apidoc.element.fs-jetpack.writeAsync)
- description and source-code
```javascript
writeAsync = function (path, data, options) {
  write.validateInput('writeAsync', path, data, options);
  return write.async(resolvePath(path), data, options);
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.fs-jetpack.append"></a>[module fs-jetpack.append](#apidoc.module.fs-jetpack.append)

#### <a name="apidoc.element.fs-jetpack.append.async"></a>[function <span class="apidocSignatureSpan">fs-jetpack.append.</span>async (path, data, options)](#apidoc.element.fs-jetpack.append.async)
- description and source-code
```javascript
async = function (path, data, options) {
  return new Promise(function (resolve, reject) {
    fs.appendFile(path, data, options)
    .then(resolve)
    .catch(function (err) {
      if (err.code === 'ENOENT') {
        // Parent directory doesn't exist, so just pass the task to 'write',
        // which will create the folder and file.
        write.async(path, data, options).then(resolve, reject);
      } else {
        reject(err);
      }
    });
  });
}
```
- example usage
```shell
...
  return new Promise(function (resolve, reject) {
    fs.appendFile(path, data, options)
    .then(resolve)
    .catch(function (err) {
      if (err.code === 'ENOENT') {
        // Parent directory doesn't exist, so just pass the task to 'write',
        // which will create the folder and file.
        write.async(path, data, options).then(resolve, reject);
      } else {
        reject(err);
      }
    });
  });
};
...
```

#### <a name="apidoc.element.fs-jetpack.append.sync"></a>[function <span class="apidocSignatureSpan">fs-jetpack.append.</span>sync (path, data, options)](#apidoc.element.fs-jetpack.append.sync)
- description and source-code
```javascript
sync = function (path, data, options) {
  try {
    fs.appendFileSync(path, data, options);
  } catch (err) {
    if (err.code === 'ENOENT') {
      // Parent directory doesn't exist, so just pass the task to 'write',
      // which will create the folder and file.
      write.sync(path, data, options);
    } else {
      throw err;
    }
  }
}
```
- example usage
```shell
...
var appendSync = function (path, data, options) {
  try {
    fs.appendFileSync(path, data, options);
  } catch (err) {
    if (err.code === 'ENOENT') {
      // Parent directory doesn't exist, so just pass the task to 'write',
      // which will create the folder and file.
      write.sync(path, data, options);
    } else {
      throw err;
    }
  }
};

// ---------------------------------------------------------
...
```

#### <a name="apidoc.element.fs-jetpack.append.validateInput"></a>[function <span class="apidocSignatureSpan">fs-jetpack.append.</span>validateInput (methodName, path, data, options)](#apidoc.element.fs-jetpack.append.validateInput)
- description and source-code
```javascript
validateInput = function (methodName, path, data, options) {
  var methodSignature = methodName + '(path, data, [options])';
  validate.argument(methodSignature, 'path', path, ['string']);
  validate.argument(methodSignature, 'data', data, ['string', 'buffer']);
  validate.options(methodSignature, 'options', options, {
    mode: ['string', 'number']
  });
}
```
- example usage
```shell
...
  // API

  var api = {
cwd: cwd,
path: getPath,

append: function (path, data, options) {
  append.validateInput('append', path, data, options);
  append.sync(resolvePath(path), data, options);
},
appendAsync: function (path, data, options) {
  append.validateInput('appendAsync', path, data, options);
  return append.async(resolvePath(path), data, options);
},
...
```



# <a name="apidoc.module.fs-jetpack.dir"></a>[module fs-jetpack.dir](#apidoc.module.fs-jetpack.dir)

#### <a name="apidoc.element.fs-jetpack.dir.async"></a>[function <span class="apidocSignatureSpan">fs-jetpack.dir.</span>async (path, passedCriteria)](#apidoc.element.fs-jetpack.dir.async)
- description and source-code
```javascript
async = function (path, passedCriteria) {
  return new Promise(function (resolve, reject) {
    var criteria = getCriteriaDefaults(passedCriteria);

    checkWhatAlreadyOccupiesPathAsync(path)
    .then(function (stat) {
      if (stat !== undefined) {
        return checkExistingDirectoryFulfillsCriteriaAsync(path, stat, criteria);
      }
      return createBrandNewDirectoryAsync(path, criteria);
    })
    .then(resolve, reject);
  });
}
```
- example usage
```shell
...
  return new Promise(function (resolve, reject) {
    fs.appendFile(path, data, options)
    .then(resolve)
    .catch(function (err) {
      if (err.code === 'ENOENT') {
        // Parent directory doesn't exist, so just pass the task to 'write',
        // which will create the folder and file.
        write.async(path, data, options).then(resolve, reject);
      } else {
        reject(err);
      }
    });
  });
};
...
```

#### <a name="apidoc.element.fs-jetpack.dir.createAsync"></a>[function <span class="apidocSignatureSpan">fs-jetpack.dir.</span>createAsync (path, opts)](#apidoc.element.fs-jetpack.dir.createAsync)
- description and source-code
```javascript
createAsync = function (path, opts) {
  var options = opts || {};

  return new Promise(function (resolve, reject) {
    fs.mkdir(path, options.mode)
    .then(resolve)
    .catch(function (err) {
      if (err.code === 'ENOENT') {
        // Parent directory doesn't exist. Need to create it first.
        createBrandNewDirectoryAsync(pathUtil.dirname(path), options)
        .then(function () {
          // Now retry creating this directory.
          return fs.mkdir(path, options.mode);
        })
        .then(resolve)
        .catch(function (err2) {
          if (err2.code === 'EEXIST') {
            // Hmm, something other have already created the directory?
            // No problem for us.
            resolve();
          } else {
            reject(err2);
          }
        });
      } else if (err.code === 'EEXIST') {
        // The path already exists. We're fine.
        resolve();
      } else {
        reject(err);
      }
    });
  });
}
```
- example usage
```shell
...

var ensureDestinationPathExistsAsync = function (to) {
return new Promise(function (resolve, reject) {
  var destDir = pathUtil.dirname(to);
  exists.async(destDir)
  .then(function (dstExists) {
    if (!dstExists) {
      dir.createAsync(destDir)
      .then(resolve, reject);
    } else {
      // Hah, no idea.
      reject();
    }
  })
  .catch(reject);
...
```

#### <a name="apidoc.element.fs-jetpack.dir.createSync"></a>[function <span class="apidocSignatureSpan">fs-jetpack.dir.</span>createSync (path, opts)](#apidoc.element.fs-jetpack.dir.createSync)
- description and source-code
```javascript
createSync = function (path, opts) {
  var options = opts || {};

  try {
    fs.mkdirSync(path, options.mode);
  } catch (err) {
    if (err.code === 'ENOENT') {
      // Parent directory doesn't exist. Need to create it first.
      createBrandNewDirectorySync(pathUtil.dirname(path), options);
      // Now retry creating this directory.
      fs.mkdirSync(path, options.mode);
    } else if (err.code === 'EEXIST') {
      // The path already exists. We're fine.
    } else {
      throw err;
    }
  }
}
```
- example usage
```shell
...
      // Ok, source or destination path doesn't exist.
      // Must do more investigation.
      if (!exists.sync(from)) {
        throw generateSourceDoesntExistError(from);
      }
      if (!exists.sync(to)) {
        // Some parent directory doesn't exist. Create it.
        dir.createSync(pathUtil.dirname(to));
        // Retry the attempt
        fs.renameSync(from, to);
      }
    }
  }
};
...
```

#### <a name="apidoc.element.fs-jetpack.dir.sync"></a>[function <span class="apidocSignatureSpan">fs-jetpack.dir.</span>sync (path, passedCriteria)](#apidoc.element.fs-jetpack.dir.sync)
- description and source-code
```javascript
sync = function (path, passedCriteria) {
  var criteria = getCriteriaDefaults(passedCriteria);
  var stat = checkWhatAlreadyOccupiesPathSync(path);
  if (stat) {
    checkExistingDirectoryFulfillsCriteriaSync(path, stat, criteria);
  } else {
    createBrandNewDirectorySync(path, criteria);
  }
}
```
- example usage
```shell
...
var appendSync = function (path, data, options) {
  try {
    fs.appendFileSync(path, data, options);
  } catch (err) {
    if (err.code === 'ENOENT') {
      // Parent directory doesn't exist, so just pass the task to 'write',
      // which will create the folder and file.
      write.sync(path, data, options);
    } else {
      throw err;
    }
  }
};

// ---------------------------------------------------------
...
```

#### <a name="apidoc.element.fs-jetpack.dir.validateInput"></a>[function <span class="apidocSignatureSpan">fs-jetpack.dir.</span>validateInput (methodName, path, criteria)](#apidoc.element.fs-jetpack.dir.validateInput)
- description and source-code
```javascript
validateInput = function (methodName, path, criteria) {
  var methodSignature = methodName + '(path, [criteria])';
  validate.argument(methodSignature, 'path', path, ['string']);
  validate.options(methodSignature, 'criteria', criteria, {
    empty: ['boolean'],
    mode: ['string', 'number']
  });
}
```
- example usage
```shell
...
  // API

  var api = {
cwd: cwd,
path: getPath,

append: function (path, data, options) {
  append.validateInput('append', path, data, options);
  append.sync(resolvePath(path), data, options);
},
appendAsync: function (path, data, options) {
  append.validateInput('appendAsync', path, data, options);
  return append.async(resolvePath(path), data, options);
},
...
```



# <a name="apidoc.module.fs-jetpack.exists"></a>[module fs-jetpack.exists](#apidoc.module.fs-jetpack.exists)

#### <a name="apidoc.element.fs-jetpack.exists.async"></a>[function <span class="apidocSignatureSpan">fs-jetpack.exists.</span>async (path)](#apidoc.element.fs-jetpack.exists.async)
- description and source-code
```javascript
async = function (path) {
  return new Promise(function (resolve, reject) {
    fs.stat(path, function (err, stat) {
      if (err) {
        if (err.code === 'ENOENT') {
          resolve(false);
        } else {
          reject(err);
        }
      } else if (stat.isDirectory()) {
        resolve('dir');
      } else if (stat.isFile()) {
        resolve('file');
      } else {
        resolve('other');
      }
    });
  });
}
```
- example usage
```shell
...
  return new Promise(function (resolve, reject) {
    fs.appendFile(path, data, options)
    .then(resolve)
    .catch(function (err) {
      if (err.code === 'ENOENT') {
        // Parent directory doesn't exist, so just pass the task to 'write',
        // which will create the folder and file.
        write.async(path, data, options).then(resolve, reject);
      } else {
        reject(err);
      }
    });
  });
};
...
```

#### <a name="apidoc.element.fs-jetpack.exists.sync"></a>[function <span class="apidocSignatureSpan">fs-jetpack.exists.</span>sync (path)](#apidoc.element.fs-jetpack.exists.sync)
- description and source-code
```javascript
sync = function (path) {
  var stat;
  try {
    stat = fs.statSync(path);
    if (stat.isDirectory()) {
      return 'dir';
    } else if (stat.isFile()) {
      return 'file';
    }
    return 'other';
  } catch (err) {
    if (err.code !== 'ENOENT') {
      throw err;
    }
  }

  return false;
}
```
- example usage
```shell
...
var appendSync = function (path, data, options) {
  try {
    fs.appendFileSync(path, data, options);
  } catch (err) {
    if (err.code === 'ENOENT') {
      // Parent directory doesn't exist, so just pass the task to 'write',
      // which will create the folder and file.
      write.sync(path, data, options);
    } else {
      throw err;
    }
  }
};

// ---------------------------------------------------------
...
```

#### <a name="apidoc.element.fs-jetpack.exists.validateInput"></a>[function <span class="apidocSignatureSpan">fs-jetpack.exists.</span>validateInput (methodName, path)](#apidoc.element.fs-jetpack.exists.validateInput)
- description and source-code
```javascript
validateInput = function (methodName, path) {
  var methodSignature = methodName + '(path)';
  validate.argument(methodSignature, 'path', path, ['string']);
}
```
- example usage
```shell
...
  // API

  var api = {
cwd: cwd,
path: getPath,

append: function (path, data, options) {
  append.validateInput('append', path, data, options);
  append.sync(resolvePath(path), data, options);
},
appendAsync: function (path, data, options) {
  append.validateInput('appendAsync', path, data, options);
  return append.async(resolvePath(path), data, options);
},
...
```



# <a name="apidoc.module.fs-jetpack.file"></a>[module fs-jetpack.file](#apidoc.module.fs-jetpack.file)

#### <a name="apidoc.element.fs-jetpack.file.async"></a>[function <span class="apidocSignatureSpan">fs-jetpack.file.</span>async (path, passedCriteria)](#apidoc.element.fs-jetpack.file.async)
- description and source-code
```javascript
async = function (path, passedCriteria) {
  return new Promise(function (resolve, reject) {
    var criteria = getCriteriaDefaults(passedCriteria);

    checkWhatAlreadyOccupiesPathAsync(path)
    .then(function (stat) {
      if (stat !== undefined) {
        return checkExistingFileFulfillsCriteriaAsync(path, stat, criteria);
      }
      return createBrandNewFileAsync(path, criteria);
    })
    .then(resolve, reject);
  });
}
```
- example usage
```shell
...
  return new Promise(function (resolve, reject) {
    fs.appendFile(path, data, options)
    .then(resolve)
    .catch(function (err) {
      if (err.code === 'ENOENT') {
        // Parent directory doesn't exist, so just pass the task to 'write',
        // which will create the folder and file.
        write.async(path, data, options).then(resolve, reject);
      } else {
        reject(err);
      }
    });
  });
};
...
```

#### <a name="apidoc.element.fs-jetpack.file.sync"></a>[function <span class="apidocSignatureSpan">fs-jetpack.file.</span>sync (path, passedCriteria)](#apidoc.element.fs-jetpack.file.sync)
- description and source-code
```javascript
sync = function (path, passedCriteria) {
  var criteria = getCriteriaDefaults(passedCriteria);
  var stat = checkWhatAlreadyOccupiesPathSync(path);
  if (stat !== undefined) {
    checkExistingFileFulfillsCriteriaSync(path, stat, criteria);
  } else {
    createBrandNewFileSync(path, criteria);
  }
}
```
- example usage
```shell
...
var appendSync = function (path, data, options) {
  try {
    fs.appendFileSync(path, data, options);
  } catch (err) {
    if (err.code === 'ENOENT') {
      // Parent directory doesn't exist, so just pass the task to 'write',
      // which will create the folder and file.
      write.sync(path, data, options);
    } else {
      throw err;
    }
  }
};

// ---------------------------------------------------------
...
```

#### <a name="apidoc.element.fs-jetpack.file.validateInput"></a>[function <span class="apidocSignatureSpan">fs-jetpack.file.</span>validateInput (methodName, path, criteria)](#apidoc.element.fs-jetpack.file.validateInput)
- description and source-code
```javascript
validateInput = function (methodName, path, criteria) {
  var methodSignature = methodName + '(path, [criteria])';
  validate.argument(methodSignature, 'path', path, ['string']);
  validate.options(methodSignature, 'criteria', criteria, {
    content: ['string', 'buffer', 'object', 'array'],
    jsonIndent: ['number'],
    mode: ['string', 'number']
  });
}
```
- example usage
```shell
...
  // API

  var api = {
cwd: cwd,
path: getPath,

append: function (path, data, options) {
  append.validateInput('append', path, data, options);
  append.sync(resolvePath(path), data, options);
},
appendAsync: function (path, data, options) {
  append.validateInput('appendAsync', path, data, options);
  return append.async(resolvePath(path), data, options);
},
...
```



# <a name="apidoc.module.fs-jetpack.find"></a>[module fs-jetpack.find](#apidoc.module.fs-jetpack.find)

#### <a name="apidoc.element.fs-jetpack.find.async"></a>[function <span class="apidocSignatureSpan">fs-jetpack.find.</span>async (path, options)](#apidoc.element.fs-jetpack.find.async)
- description and source-code
```javascript
async = function (path, options) {
  return inspect.async(path)
  .then(function (entryPointInspect) {
    if (entryPointInspect === undefined) {
      throw generatePathDoesntExistError(path);
    } else if (entryPointInspect.type !== 'dir') {
      throw generatePathNotDirectoryError(path);
    }
    return findAsync(path, normalizeOptions(options));
  });
}
```
- example usage
```shell
...
  return new Promise(function (resolve, reject) {
    fs.appendFile(path, data, options)
    .then(resolve)
    .catch(function (err) {
      if (err.code === 'ENOENT') {
        // Parent directory doesn't exist, so just pass the task to 'write',
        // which will create the folder and file.
        write.async(path, data, options).then(resolve, reject);
      } else {
        reject(err);
      }
    });
  });
};
...
```

#### <a name="apidoc.element.fs-jetpack.find.sync"></a>[function <span class="apidocSignatureSpan">fs-jetpack.find.</span>sync (path, options)](#apidoc.element.fs-jetpack.find.sync)
- description and source-code
```javascript
sync = function (path, options) {
  var entryPointInspect = inspect.sync(path);
  if (entryPointInspect === undefined) {
    throw generatePathDoesntExistError(path);
  } else if (entryPointInspect.type !== 'dir') {
    throw generatePathNotDirectoryError(path);
  }

  return findSync(path, normalizeOptions(options));
}
```
- example usage
```shell
...
var appendSync = function (path, data, options) {
  try {
    fs.appendFileSync(path, data, options);
  } catch (err) {
    if (err.code === 'ENOENT') {
      // Parent directory doesn't exist, so just pass the task to 'write',
      // which will create the folder and file.
      write.sync(path, data, options);
    } else {
      throw err;
    }
  }
};

// ---------------------------------------------------------
...
```

#### <a name="apidoc.element.fs-jetpack.find.validateInput"></a>[function <span class="apidocSignatureSpan">fs-jetpack.find.</span>validateInput (methodName, path, options)](#apidoc.element.fs-jetpack.find.validateInput)
- description and source-code
```javascript
validateInput = function (methodName, path, options) {
  var methodSignature = methodName + '([path], options)';
  validate.argument(methodSignature, 'path', path, ['string']);
  validate.options(methodSignature, 'options', options, {
    matching: ['string', 'array of string'],
    files: ['boolean'],
    directories: ['boolean'],
    recursive: ['boolean']
  });
}
```
- example usage
```shell
...
  // API

  var api = {
cwd: cwd,
path: getPath,

append: function (path, data, options) {
  append.validateInput('append', path, data, options);
  append.sync(resolvePath(path), data, options);
},
appendAsync: function (path, data, options) {
  append.validateInput('appendAsync', path, data, options);
  return append.async(resolvePath(path), data, options);
},
...
```



# <a name="apidoc.module.fs-jetpack.inspect"></a>[module fs-jetpack.inspect](#apidoc.module.fs-jetpack.inspect)

#### <a name="apidoc.element.fs-jetpack.inspect.async"></a>[function <span class="apidocSignatureSpan">fs-jetpack.inspect.</span>async (path, options)](#apidoc.element.fs-jetpack.inspect.async)
- description and source-code
```javascript
async = function (path, options) {
  return new Promise(function (resolve, reject) {
    var statOperation = fs.lstat;
    options = options || {};

    if (options.symlinks === 'follow') {
      statOperation = fs.stat;
    }

    statOperation(path)
    .then(function (stat) {
      var inspectObj = createInspectObj(path, options, stat);
      addExtraFieldsAsync(path, inspectObj, options)
      .then(resolve, reject);
    })
    .catch(function (err) {
      // Detection if path exists
      if (err.code === 'ENOENT') {
        // Doesn't exist. Return undefined instead of throwing.
        resolve(undefined);
      } else {
        reject(err);
      }
    });
  });
}
```
- example usage
```shell
...
  return new Promise(function (resolve, reject) {
    fs.appendFile(path, data, options)
    .then(resolve)
    .catch(function (err) {
      if (err.code === 'ENOENT') {
        // Parent directory doesn't exist, so just pass the task to 'write',
        // which will create the folder and file.
        write.async(path, data, options).then(resolve, reject);
      } else {
        reject(err);
      }
    });
  });
};
...
```

#### <a name="apidoc.element.fs-jetpack.inspect.sync"></a>[function <span class="apidocSignatureSpan">fs-jetpack.inspect.</span>sync (path, options)](#apidoc.element.fs-jetpack.inspect.sync)
- description and source-code
```javascript
sync = function (path, options) {
  var statOperation = fs.lstatSync;
  var stat;
  var inspectObj;
  options = options || {};

  if (options.symlinks === 'follow') {
    statOperation = fs.statSync;
  }

  try {
    stat = statOperation(path);
  } catch (err) {
    // Detection if path exists
    if (err.code === 'ENOENT') {
      // Doesn't exist. Return undefined instead of throwing.
      return undefined;
    }
    throw err;
  }

  inspectObj = createInspectObj(path, options, stat);
  addExtraFieldsSync(path, inspectObj, options);

  return inspectObj;
}
```
- example usage
```shell
...
var appendSync = function (path, data, options) {
  try {
    fs.appendFileSync(path, data, options);
  } catch (err) {
    if (err.code === 'ENOENT') {
      // Parent directory doesn't exist, so just pass the task to 'write',
      // which will create the folder and file.
      write.sync(path, data, options);
    } else {
      throw err;
    }
  }
};

// ---------------------------------------------------------
...
```

#### <a name="apidoc.element.fs-jetpack.inspect.validateInput"></a>[function <span class="apidocSignatureSpan">fs-jetpack.inspect.</span>validateInput (methodName, path, options)](#apidoc.element.fs-jetpack.inspect.validateInput)
- description and source-code
```javascript
validateInput = function (methodName, path, options) {
  var methodSignature = methodName + '(path, [options])';
  validate.argument(methodSignature, 'path', path, ['string']);
  validate.options(methodSignature, 'options', options, {
    checksum: ['string'],
    mode: ['boolean'],
    times: ['boolean'],
    absolutePath: ['boolean'],
    symlinks: ['string']
  });

  if (options && options.checksum !== undefined
    && supportedChecksumAlgorithms.indexOf(options.checksum) === -1) {
    throw new Error('Argument "options.checksum" passed to ' + methodSignature
      + ' must have one of values: ' + supportedChecksumAlgorithms.join(', '));
  }

  if (options && options.symlinks !== undefined
    && symlinkOptions.indexOf(options.symlinks) === -1) {
    throw new Error('Argument "options.symlinks" passed to ' + methodSignature
      + ' must have one of values: ' + symlinkOptions.join(', '));
  }
}
```
- example usage
```shell
...
  // API

  var api = {
cwd: cwd,
path: getPath,

append: function (path, data, options) {
  append.validateInput('append', path, data, options);
  append.sync(resolvePath(path), data, options);
},
appendAsync: function (path, data, options) {
  append.validateInput('appendAsync', path, data, options);
  return append.async(resolvePath(path), data, options);
},
...
```



# <a name="apidoc.module.fs-jetpack.inspect_tree"></a>[module fs-jetpack.inspect_tree](#apidoc.module.fs-jetpack.inspect_tree)

#### <a name="apidoc.element.fs-jetpack.inspect_tree.async"></a>[function <span class="apidocSignatureSpan">fs-jetpack.inspect_tree.</span>async (path, options)](#apidoc.element.fs-jetpack.inspect_tree.async)
- description and source-code
```javascript
async = function (path, options) {
  options = options || {};

  return inspectTreeNodeAsync(path, options);
}
```
- example usage
```shell
...
  return new Promise(function (resolve, reject) {
    fs.appendFile(path, data, options)
    .then(resolve)
    .catch(function (err) {
      if (err.code === 'ENOENT') {
        // Parent directory doesn't exist, so just pass the task to 'write',
        // which will create the folder and file.
        write.async(path, data, options).then(resolve, reject);
      } else {
        reject(err);
      }
    });
  });
};
...
```

#### <a name="apidoc.element.fs-jetpack.inspect_tree.sync"></a>[function <span class="apidocSignatureSpan">fs-jetpack.inspect_tree.</span>sync (path, options)](#apidoc.element.fs-jetpack.inspect_tree.sync)
- description and source-code
```javascript
sync = function (path, options) {
  options = options || {};

  return inspectTreeNodeSync(path, options, undefined);
}
```
- example usage
```shell
...
var appendSync = function (path, data, options) {
  try {
    fs.appendFileSync(path, data, options);
  } catch (err) {
    if (err.code === 'ENOENT') {
      // Parent directory doesn't exist, so just pass the task to 'write',
      // which will create the folder and file.
      write.sync(path, data, options);
    } else {
      throw err;
    }
  }
};

// ---------------------------------------------------------
...
```

#### <a name="apidoc.element.fs-jetpack.inspect_tree.validateInput"></a>[function <span class="apidocSignatureSpan">fs-jetpack.inspect_tree.</span>validateInput (methodName, path, options)](#apidoc.element.fs-jetpack.inspect_tree.validateInput)
- description and source-code
```javascript
validateInput = function (methodName, path, options) {
  var methodSignature = methodName + '(path, [options])';
  validate.argument(methodSignature, 'path', path, ['string']);
  validate.options(methodSignature, 'options', options, {
    checksum: ['string'],
    relativePath: ['boolean'],
    symlinks: ['string']
  });

  if (options && options.checksum !== undefined
    && inspect.supportedChecksumAlgorithms.indexOf(options.checksum) === -1) {
    throw new Error('Argument "options.checksum" passed to ' + methodSignature
      + ' must have one of values: ' + inspect.supportedChecksumAlgorithms.join(', '));
  }

  if (options && options.symlinks !== undefined
    && inspect.symlinkOptions.indexOf(options.symlinks) === -1) {
    throw new Error('Argument "options.symlinks" passed to ' + methodSignature
      + ' must have one of values: ' + inspect.symlinkOptions.join(', '));
  }
}
```
- example usage
```shell
...
  // API

  var api = {
cwd: cwd,
path: getPath,

append: function (path, data, options) {
  append.validateInput('append', path, data, options);
  append.sync(resolvePath(path), data, options);
},
appendAsync: function (path, data, options) {
  append.validateInput('appendAsync', path, data, options);
  return append.async(resolvePath(path), data, options);
},
...
```



# <a name="apidoc.module.fs-jetpack.list"></a>[module fs-jetpack.list](#apidoc.module.fs-jetpack.list)

#### <a name="apidoc.element.fs-jetpack.list.async"></a>[function <span class="apidocSignatureSpan">fs-jetpack.list.</span>async (path)](#apidoc.element.fs-jetpack.list.async)
- description and source-code
```javascript
async = function (path) {
  return new Promise(function (resolve, reject) {
    fs.readdir(path)
    .then(function (list) {
      resolve(list);
    })
    .catch(function (err) {
      if (err.code === 'ENOENT') {
        // Doesn't exist. Return undefined instead of throwing.
        resolve(undefined);
      } else {
        reject(err);
      }
    });
  });
}
```
- example usage
```shell
...
  return new Promise(function (resolve, reject) {
    fs.appendFile(path, data, options)
    .then(resolve)
    .catch(function (err) {
      if (err.code === 'ENOENT') {
        // Parent directory doesn't exist, so just pass the task to 'write',
        // which will create the folder and file.
        write.async(path, data, options).then(resolve, reject);
      } else {
        reject(err);
      }
    });
  });
};
...
```

#### <a name="apidoc.element.fs-jetpack.list.sync"></a>[function <span class="apidocSignatureSpan">fs-jetpack.list.</span>sync (path)](#apidoc.element.fs-jetpack.list.sync)
- description and source-code
```javascript
sync = function (path) {
  try {
    return fs.readdirSync(path);
  } catch (err) {
    if (err.code === 'ENOENT') {
      // Doesn't exist. Return undefined instead of throwing.
      return undefined;
    }
    throw err;
  }
}
```
- example usage
```shell
...
var appendSync = function (path, data, options) {
  try {
    fs.appendFileSync(path, data, options);
  } catch (err) {
    if (err.code === 'ENOENT') {
      // Parent directory doesn't exist, so just pass the task to 'write',
      // which will create the folder and file.
      write.sync(path, data, options);
    } else {
      throw err;
    }
  }
};

// ---------------------------------------------------------
...
```

#### <a name="apidoc.element.fs-jetpack.list.validateInput"></a>[function <span class="apidocSignatureSpan">fs-jetpack.list.</span>validateInput (methodName, path)](#apidoc.element.fs-jetpack.list.validateInput)
- description and source-code
```javascript
validateInput = function (methodName, path) {
  var methodSignature = methodName + '(path)';
  validate.argument(methodSignature, 'path', path, ['string', 'undefined']);
}
```
- example usage
```shell
...
  // API

  var api = {
cwd: cwd,
path: getPath,

append: function (path, data, options) {
  append.validateInput('append', path, data, options);
  append.sync(resolvePath(path), data, options);
},
appendAsync: function (path, data, options) {
  append.validateInput('appendAsync', path, data, options);
  return append.async(resolvePath(path), data, options);
},
...
```



# <a name="apidoc.module.fs-jetpack.move"></a>[module fs-jetpack.move](#apidoc.module.fs-jetpack.move)

#### <a name="apidoc.element.fs-jetpack.move.async"></a>[function <span class="apidocSignatureSpan">fs-jetpack.move.</span>async (from, to)](#apidoc.element.fs-jetpack.move.async)
- description and source-code
```javascript
async = function (from, to) {
  return new Promise(function (resolve, reject) {
    fs.rename(from, to)
    .then(resolve)
    .catch(function (err) {
      if (err.code !== 'ENOENT') {
        // Something unknown. Rethrow original error.
        reject(err);
      } else {
        // Ok, source or destination path doesn't exist.
        // Must do more investigation.
        exists.async(from)
        .then(function (srcExists) {
          if (!srcExists) {
            reject(generateSourceDoesntExistError(from));
          } else {
            ensureDestinationPathExistsAsync(to)
            .then(function () {
              // Retry the attempt
              return fs.rename(from, to);
            })
            .then(resolve, reject);
          }
        })
        .catch(reject);
      }
    });
  });
}
```
- example usage
```shell
...
  return new Promise(function (resolve, reject) {
    fs.appendFile(path, data, options)
    .then(resolve)
    .catch(function (err) {
      if (err.code === 'ENOENT') {
        // Parent directory doesn't exist, so just pass the task to 'write',
        // which will create the folder and file.
        write.async(path, data, options).then(resolve, reject);
      } else {
        reject(err);
      }
    });
  });
};
...
```

#### <a name="apidoc.element.fs-jetpack.move.sync"></a>[function <span class="apidocSignatureSpan">fs-jetpack.move.</span>sync (from, to)](#apidoc.element.fs-jetpack.move.sync)
- description and source-code
```javascript
sync = function (from, to) {
  try {
    fs.renameSync(from, to);
  } catch (err) {
    if (err.code !== 'ENOENT') {
      // We can't make sense of this error. Rethrow it.
      throw err;
    } else {
      // Ok, source or destination path doesn't exist.
      // Must do more investigation.
      if (!exists.sync(from)) {
        throw generateSourceDoesntExistError(from);
      }
      if (!exists.sync(to)) {
        // Some parent directory doesn't exist. Create it.
        dir.createSync(pathUtil.dirname(to));
        // Retry the attempt
        fs.renameSync(from, to);
      }
    }
  }
}
```
- example usage
```shell
...
var appendSync = function (path, data, options) {
  try {
    fs.appendFileSync(path, data, options);
  } catch (err) {
    if (err.code === 'ENOENT') {
      // Parent directory doesn't exist, so just pass the task to 'write',
      // which will create the folder and file.
      write.sync(path, data, options);
    } else {
      throw err;
    }
  }
};

// ---------------------------------------------------------
...
```

#### <a name="apidoc.element.fs-jetpack.move.validateInput"></a>[function <span class="apidocSignatureSpan">fs-jetpack.move.</span>validateInput (methodName, from, to)](#apidoc.element.fs-jetpack.move.validateInput)
- description and source-code
```javascript
validateInput = function (methodName, from, to) {
  var methodSignature = methodName + '(from, to)';
  validate.argument(methodSignature, 'from', from, ['string']);
  validate.argument(methodSignature, 'to', to, ['string']);
}
```
- example usage
```shell
...
  // API

  var api = {
cwd: cwd,
path: getPath,

append: function (path, data, options) {
  append.validateInput('append', path, data, options);
  append.sync(resolvePath(path), data, options);
},
appendAsync: function (path, data, options) {
  append.validateInput('appendAsync', path, data, options);
  return append.async(resolvePath(path), data, options);
},
...
```



# <a name="apidoc.module.fs-jetpack.read"></a>[module fs-jetpack.read](#apidoc.module.fs-jetpack.read)

#### <a name="apidoc.element.fs-jetpack.read.async"></a>[function <span class="apidocSignatureSpan">fs-jetpack.read.</span>async (path, returnAs)](#apidoc.element.fs-jetpack.read.async)
- description and source-code
```javascript
async = function (path, returnAs) {
  return new Promise(function (resolve, reject) {
    var retAs = returnAs || 'utf8';
    var encoding = 'utf8';
    if (retAs === 'buffer') {
      encoding = null;
    }

    fs.readFile(path, { encoding: encoding })
    .then(function (data) {
      // Make final parsing of the data before returning.
      try {
        if (retAs === 'json') {
          resolve(JSON.parse(data));
        } else if (retAs === 'jsonWithDates') {
          resolve(JSON.parse(data, jsonDateParser));
        } else {
          resolve(data);
        }
      } catch (err) {
        reject(makeNicerJsonParsingError(path, err));
      }
    })
    .catch(function (err) {
      if (err.code === 'ENOENT') {
        // If file doesn't exist return undefined instead of throwing.
        resolve(undefined);
      } else {
        // Otherwise throw
        reject(err);
      }
    });
  });
}
```
- example usage
```shell
...
  return new Promise(function (resolve, reject) {
    fs.appendFile(path, data, options)
    .then(resolve)
    .catch(function (err) {
      if (err.code === 'ENOENT') {
        // Parent directory doesn't exist, so just pass the task to 'write',
        // which will create the folder and file.
        write.async(path, data, options).then(resolve, reject);
      } else {
        reject(err);
      }
    });
  });
};
...
```

#### <a name="apidoc.element.fs-jetpack.read.sync"></a>[function <span class="apidocSignatureSpan">fs-jetpack.read.</span>sync (path, returnAs)](#apidoc.element.fs-jetpack.read.sync)
- description and source-code
```javascript
sync = function (path, returnAs) {
  var retAs = returnAs || 'utf8';
  var data;

  var encoding = 'utf8';
  if (retAs === 'buffer') {
    encoding = null;
  }

  try {
    data = fs.readFileSync(path, { encoding: encoding });
  } catch (err) {
    if (err.code === 'ENOENT') {
      // If file doesn't exist return undefined instead of throwing.
      return undefined;
    }
    // Otherwise rethrow the error
    throw err;
  }

  try {
    if (retAs === 'json') {
      data = JSON.parse(data);
    } else if (retAs === 'jsonWithDates') {
      data = JSON.parse(data, jsonDateParser);
    }
  } catch (err) {
    throw makeNicerJsonParsingError(path, err);
  }

  return data;
}
```
- example usage
```shell
...
var appendSync = function (path, data, options) {
  try {
    fs.appendFileSync(path, data, options);
  } catch (err) {
    if (err.code === 'ENOENT') {
      // Parent directory doesn't exist, so just pass the task to 'write',
      // which will create the folder and file.
      write.sync(path, data, options);
    } else {
      throw err;
    }
  }
};

// ---------------------------------------------------------
...
```

#### <a name="apidoc.element.fs-jetpack.read.validateInput"></a>[function <span class="apidocSignatureSpan">fs-jetpack.read.</span>validateInput (methodName, path, returnAs)](#apidoc.element.fs-jetpack.read.validateInput)
- description and source-code
```javascript
validateInput = function (methodName, path, returnAs) {
  var methodSignature = methodName + '(path, returnAs)';
  validate.argument(methodSignature, 'path', path, ['string']);
  validate.argument(methodSignature, 'returnAs', returnAs, ['string', 'undefined']);

  if (returnAs && supportedReturnAs.indexOf(returnAs) === -1) {
    throw new Error('Argument "returnAs" passed to ' + methodSignature
      + ' must have one of values: ' + supportedReturnAs.join(', '));
  }
}
```
- example usage
```shell
...
  // API

  var api = {
cwd: cwd,
path: getPath,

append: function (path, data, options) {
  append.validateInput('append', path, data, options);
  append.sync(resolvePath(path), data, options);
},
appendAsync: function (path, data, options) {
  append.validateInput('appendAsync', path, data, options);
  return append.async(resolvePath(path), data, options);
},
...
```



# <a name="apidoc.module.fs-jetpack.rename"></a>[module fs-jetpack.rename](#apidoc.module.fs-jetpack.rename)

#### <a name="apidoc.element.fs-jetpack.rename.async"></a>[function <span class="apidocSignatureSpan">fs-jetpack.rename.</span>async (path, newName)](#apidoc.element.fs-jetpack.rename.async)
- description and source-code
```javascript
async = function (path, newName) {
  var newPath = pathUtil.join(pathUtil.dirname(path), newName);
  return move.async(path, newPath);
}
```
- example usage
```shell
...
  return new Promise(function (resolve, reject) {
    fs.appendFile(path, data, options)
    .then(resolve)
    .catch(function (err) {
      if (err.code === 'ENOENT') {
        // Parent directory doesn't exist, so just pass the task to 'write',
        // which will create the folder and file.
        write.async(path, data, options).then(resolve, reject);
      } else {
        reject(err);
      }
    });
  });
};
...
```

#### <a name="apidoc.element.fs-jetpack.rename.sync"></a>[function <span class="apidocSignatureSpan">fs-jetpack.rename.</span>sync (path, newName)](#apidoc.element.fs-jetpack.rename.sync)
- description and source-code
```javascript
sync = function (path, newName) {
  var newPath = pathUtil.join(pathUtil.dirname(path), newName);
  move.sync(path, newPath);
}
```
- example usage
```shell
...
var appendSync = function (path, data, options) {
  try {
    fs.appendFileSync(path, data, options);
  } catch (err) {
    if (err.code === 'ENOENT') {
      // Parent directory doesn't exist, so just pass the task to 'write',
      // which will create the folder and file.
      write.sync(path, data, options);
    } else {
      throw err;
    }
  }
};

// ---------------------------------------------------------
...
```

#### <a name="apidoc.element.fs-jetpack.rename.validateInput"></a>[function <span class="apidocSignatureSpan">fs-jetpack.rename.</span>validateInput (methodName, path, newName)](#apidoc.element.fs-jetpack.rename.validateInput)
- description and source-code
```javascript
validateInput = function (methodName, path, newName) {
  var methodSignature = methodName + '(path, newName)';
  validate.argument(methodSignature, 'path', path, ['string']);
  validate.argument(methodSignature, 'newName', newName, ['string']);
}
```
- example usage
```shell
...
  // API

  var api = {
cwd: cwd,
path: getPath,

append: function (path, data, options) {
  append.validateInput('append', path, data, options);
  append.sync(resolvePath(path), data, options);
},
appendAsync: function (path, data, options) {
  append.validateInput('appendAsync', path, data, options);
  return append.async(resolvePath(path), data, options);
},
...
```



# <a name="apidoc.module.fs-jetpack.streams"></a>[module fs-jetpack.streams](#apidoc.module.fs-jetpack.streams)

#### <a name="apidoc.element.fs-jetpack.streams.createReadStream"></a>[function <span class="apidocSignatureSpan">fs-jetpack.streams.</span>createReadStream (path, options)](#apidoc.element.fs-jetpack.streams.createReadStream)
- description and source-code
```javascript
createReadStream = function (path, options) {
  return new ReadStream(path, options);
}
```
- example usage
```shell
...
// ---------------------------------------------------------
// Async
// ---------------------------------------------------------

var fileChecksumAsync = function (path, algo) {
return new Promise(function (resolve, reject) {
  var hash = crypto.createHash(algo);
  var s = fs.createReadStream(path);
  s.on('data', function (data) {
    hash.update(data);
  });
  s.on('end', function () {
    resolve(hash.digest('hex'));
  });
  s.on('error', reject);
...
```

#### <a name="apidoc.element.fs-jetpack.streams.createWriteStream"></a>[function <span class="apidocSignatureSpan">fs-jetpack.streams.</span>createWriteStream (path, options)](#apidoc.element.fs-jetpack.streams.createWriteStream)
- description and source-code
```javascript
createWriteStream = function (path, options) {
  return new WriteStream(path, options);
}
```
- example usage
```shell
...
},
copyAsync: function (from, to, options) {
  copy.validateInput('copyAsync', from, to, options);
  return copy.async(resolvePath(from), resolvePath(to), options);
},

createWriteStream: function (path, options) {
  return streams.createWriteStream(resolvePath(path), options);
},
createReadStream: function (path, options) {
  return streams.createReadStream(resolvePath(path), options);
},

dir: function (path, criteria) {
  var normalizedPath;
...
```



# <a name="apidoc.module.fs-jetpack.symlink"></a>[module fs-jetpack.symlink](#apidoc.module.fs-jetpack.symlink)

#### <a name="apidoc.element.fs-jetpack.symlink.async"></a>[function <span class="apidocSignatureSpan">fs-jetpack.symlink.</span>async (symlinkValue, path)](#apidoc.element.fs-jetpack.symlink.async)
- description and source-code
```javascript
async = function (symlinkValue, path) {
  return new Promise(function (resolve, reject) {
    fs.symlink(symlinkValue, path)
    .then(resolve)
    .catch(function (err) {
      if (err.code === 'ENOENT') {
        // Parent directories don't exist. Just create them and rety.
        dir.createAsync(pathUtil.dirname(path))
        .then(function () {
          return fs.symlink(symlinkValue, path);
        })
        .then(resolve, reject);
      } else {
        reject(err);
      }
    });
  });
}
```
- example usage
```shell
...
  return new Promise(function (resolve, reject) {
    fs.appendFile(path, data, options)
    .then(resolve)
    .catch(function (err) {
      if (err.code === 'ENOENT') {
        // Parent directory doesn't exist, so just pass the task to 'write',
        // which will create the folder and file.
        write.async(path, data, options).then(resolve, reject);
      } else {
        reject(err);
      }
    });
  });
};
...
```

#### <a name="apidoc.element.fs-jetpack.symlink.sync"></a>[function <span class="apidocSignatureSpan">fs-jetpack.symlink.</span>sync (symlinkValue, path)](#apidoc.element.fs-jetpack.symlink.sync)
- description and source-code
```javascript
sync = function (symlinkValue, path) {
  try {
    fs.symlinkSync(symlinkValue, path);
  } catch (err) {
    if (err.code === 'ENOENT') {
      // Parent directories don't exist. Just create them and rety.
      dir.createSync(pathUtil.dirname(path));
      fs.symlinkSync(symlinkValue, path);
    } else {
      throw err;
    }
  }
}
```
- example usage
```shell
...
var appendSync = function (path, data, options) {
  try {
    fs.appendFileSync(path, data, options);
  } catch (err) {
    if (err.code === 'ENOENT') {
      // Parent directory doesn't exist, so just pass the task to 'write',
      // which will create the folder and file.
      write.sync(path, data, options);
    } else {
      throw err;
    }
  }
};

// ---------------------------------------------------------
...
```

#### <a name="apidoc.element.fs-jetpack.symlink.validateInput"></a>[function <span class="apidocSignatureSpan">fs-jetpack.symlink.</span>validateInput (methodName, symlinkValue, path)](#apidoc.element.fs-jetpack.symlink.validateInput)
- description and source-code
```javascript
validateInput = function (methodName, symlinkValue, path) {
  var methodSignature = methodName + '(symlinkValue, path)';
  validate.argument(methodSignature, 'symlinkValue', symlinkValue, ['string']);
  validate.argument(methodSignature, 'path', path, ['string']);
}
```
- example usage
```shell
...
  // API

  var api = {
cwd: cwd,
path: getPath,

append: function (path, data, options) {
  append.validateInput('append', path, data, options);
  append.sync(resolvePath(path), data, options);
},
appendAsync: function (path, data, options) {
  append.validateInput('appendAsync', path, data, options);
  return append.async(resolvePath(path), data, options);
},
...
```



# <a name="apidoc.module.fs-jetpack.utils"></a>[module fs-jetpack.utils](#apidoc.module.fs-jetpack.utils)

#### <a name="apidoc.element.fs-jetpack.utils.cleanAfterTest"></a>[function <span class="apidocSignatureSpan">fs-jetpack.utils.</span>cleanAfterTest ()](#apidoc.element.fs-jetpack.utils.cleanAfterTest)
- description and source-code
```javascript
cleanAfterTest = function () {
  console.log('Cleaning up after test...');
  return jetpack.removeAsync(testDirPath());
}
```
- example usage
```shell
...
  .then(function () {
    timer = utils.startTimer('Native cp -R');
    return utils.exec('cp -R ' + toCopyDir.path() + ' ' + testDir.path('copied-native'));
  })
  .then(function () {
    nativeTime = timer();
    utils.showDifferenceInfo(jetpackTime, nativeTime);
    return utils.cleanAfterTest();
  })
  .catch(function (err) {
    console.log(err);
  });
};

var testConfigs = [
...
```

#### <a name="apidoc.element.fs-jetpack.utils.exec"></a>[function <span class="apidocSignatureSpan">fs-jetpack.utils.</span>exec ()](#apidoc.element.fs-jetpack.utils.exec)
- description and source-code
```javascript
exec = function () {
  var i = 0;
  var length = arguments.length;
  var args = new Array(length);

  for (; i < length; i++) {
    args[i] = arguments[i];
  }

  return new Promise(function (resolve, reject) {
    args.push(function (err, data) {
      if (err) {
        reject(err);
      } else {
        resolve(data);
      }
    });

    fn.apply(null, args);
  });
}
```
- example usage
```shell
...
})
.then(function () {
  jetpackTime = timer();
  return utils.waitAWhile();
})
.then(function () {
  timer = utils.startTimer('Native cp -R');
  return utils.exec('cp -R ' + toCopyDir.path() + ' ' + testDir.path('copied-native'));
})
.then(function () {
  nativeTime = timer();
  utils.showDifferenceInfo(jetpackTime, nativeTime);
  return utils.cleanAfterTest();
})
.catch(function (err) {
...
```

#### <a name="apidoc.element.fs-jetpack.utils.prepareFiles"></a>[function <span class="apidocSignatureSpan">fs-jetpack.utils.</span>prepareFiles (jetpackDir, creationConfig)](#apidoc.element.fs-jetpack.utils.prepareFiles)
- description and source-code
```javascript
prepareFiles = function (jetpackDir, creationConfig) {
  return new Promise(function (resolve, reject) {
    var count = 0;
    var content = new Buffer(creationConfig.size);

    var makeOneFile = function () {
      jetpackDir.fileAsync(count + '.txt', { content: content })
      .then(function () {
        count += 1;
        if (count < creationConfig.files) {
          makeOneFile();
        } else {
          resolve();
        }
      }, reject);
    };

    console.log('Preparing ' + creationConfig.files + ' test files (' +
        humanReadableFileSize(creationConfig.size, true) + ' each)...');
    makeOneFile();
  });
}
```
- example usage
```shell
...
var timer;
var jetpackTime;
var nativeTime;

var test = function (testConfig) {
console.log('');

return utils.prepareFiles(toCopyDir, testConfig)
.then(utils.waitAWhile)
.then(function () {
  timer = utils.startTimer('jetpack.copyAsync()');
  return toCopyDir.copyAsync('.', testDir.path('copied-jetpack'));
})
.then(function () {
  jetpackTime = timer();
...
```

#### <a name="apidoc.element.fs-jetpack.utils.prepareJetpackTestDir"></a>[function <span class="apidocSignatureSpan">fs-jetpack.utils.</span>prepareJetpackTestDir ()](#apidoc.element.fs-jetpack.utils.prepareJetpackTestDir)
- description and source-code
```javascript
prepareJetpackTestDir = function () {
  return jetpack.dir(testDirPath(), { empty: true });
}
```
- example usage
```shell
...

/* eslint no-console: 0 */

'use strict';

var utils = require('./utils');

var testDir = utils.prepareJetpackTestDir();
var toCopyDir = testDir.dir('to-copy');
var timer;
var jetpackTime;
var nativeTime;

var test = function (testConfig) {
console.log('');
...
```

#### <a name="apidoc.element.fs-jetpack.utils.showDifferenceInfo"></a>[function <span class="apidocSignatureSpan">fs-jetpack.utils.</span>showDifferenceInfo (jetpackTime, nativeTime)](#apidoc.element.fs-jetpack.utils.showDifferenceInfo)
- description and source-code
```javascript
showDifferenceInfo = function (jetpackTime, nativeTime) {
  var perc = Math.round(jetpackTime / nativeTime * 100) - 100;
  console.log('Jetpack is ' + perc + '% slower than native');
}
```
- example usage
```shell
...
  })
  .then(function () {
    timer = utils.startTimer('Native cp -R');
    return utils.exec('cp -R ' + toCopyDir.path() + ' ' + testDir.path('copied-native'));
  })
  .then(function () {
    nativeTime = timer();
    utils.showDifferenceInfo(jetpackTime, nativeTime);
    return utils.cleanAfterTest();
  })
  .catch(function (err) {
    console.log(err);
  });
};
...
```

#### <a name="apidoc.element.fs-jetpack.utils.startTimer"></a>[function <span class="apidocSignatureSpan">fs-jetpack.utils.</span>startTimer (startMessage)](#apidoc.element.fs-jetpack.utils.startTimer)
- description and source-code
```javascript
startTimer = function (startMessage) {
  var start = Date.now();
  process.stdout.write(startMessage + ' ... ');
  return function stop() {
    var time = Date.now() - start;
    console.log(time + 'ms');
    return time;
  };
}
```
- example usage
```shell
...

var test = function (testConfig) {
console.log('');

return utils.prepareFiles(toCopyDir, testConfig)
.then(utils.waitAWhile)
.then(function () {
  timer = utils.startTimer('jetpack.copyAsync()');
  return toCopyDir.copyAsync('.', testDir.path('copied-jetpack'));
})
.then(function () {
  jetpackTime = timer();
  return utils.waitAWhile();
})
.then(function () {
...
```

#### <a name="apidoc.element.fs-jetpack.utils.waitAWhile"></a>[function <span class="apidocSignatureSpan">fs-jetpack.utils.</span>waitAWhile ()](#apidoc.element.fs-jetpack.utils.waitAWhile)
- description and source-code
```javascript
waitAWhile = function () {
  return new Promise(function (resolve) {
    console.log('Waiting 5s to allow hardware buffers be emptied...');
    setTimeout(resolve, 5000);
  });
}
```
- example usage
```shell
...
.then(utils.waitAWhile)
.then(function () {
  timer = utils.startTimer('jetpack.copyAsync()');
  return toCopyDir.copyAsync('.', testDir.path('copied-jetpack'));
})
.then(function () {
  jetpackTime = timer();
  return utils.waitAWhile();
})
.then(function () {
  timer = utils.startTimer('Native cp -R');
  return utils.exec('cp -R ' + toCopyDir.path() + ' ' + testDir.path('copied-native'));
})
.then(function () {
  nativeTime = timer();
...
```



# <a name="apidoc.module.fs-jetpack.write"></a>[module fs-jetpack.write](#apidoc.module.fs-jetpack.write)

#### <a name="apidoc.element.fs-jetpack.write.async"></a>[function <span class="apidocSignatureSpan">fs-jetpack.write.</span>async (path, data, options)](#apidoc.element.fs-jetpack.write.async)
- description and source-code
```javascript
async = function (path, data, options) {
  var opts = options || {};
  var processedData = serializeToJsonMaybe(data, opts.jsonIndent);

  var writeStrategy = writeFileAsync;
  if (opts.atomic) {
    writeStrategy = writeAtomicAsync;
  }
  return writeStrategy(path, processedData, { mode: opts.mode });
}
```
- example usage
```shell
...
  return new Promise(function (resolve, reject) {
    fs.appendFile(path, data, options)
    .then(resolve)
    .catch(function (err) {
      if (err.code === 'ENOENT') {
        // Parent directory doesn't exist, so just pass the task to 'write',
        // which will create the folder and file.
        write.async(path, data, options).then(resolve, reject);
      } else {
        reject(err);
      }
    });
  });
};
...
```

#### <a name="apidoc.element.fs-jetpack.write.sync"></a>[function <span class="apidocSignatureSpan">fs-jetpack.write.</span>sync (path, data, options)](#apidoc.element.fs-jetpack.write.sync)
- description and source-code
```javascript
sync = function (path, data, options) {
  var opts = options || {};
  var processedData = serializeToJsonMaybe(data, opts.jsonIndent);

  var writeStrategy = writeFileSync;
  if (opts.atomic) {
    writeStrategy = writeAtomicSync;
  }
  writeStrategy(path, processedData, { mode: opts.mode });
}
```
- example usage
```shell
...
var appendSync = function (path, data, options) {
  try {
    fs.appendFileSync(path, data, options);
  } catch (err) {
    if (err.code === 'ENOENT') {
      // Parent directory doesn't exist, so just pass the task to 'write',
      // which will create the folder and file.
      write.sync(path, data, options);
    } else {
      throw err;
    }
  }
};

// ---------------------------------------------------------
...
```

#### <a name="apidoc.element.fs-jetpack.write.validateInput"></a>[function <span class="apidocSignatureSpan">fs-jetpack.write.</span>validateInput (methodName, path, data, options)](#apidoc.element.fs-jetpack.write.validateInput)
- description and source-code
```javascript
validateInput = function (methodName, path, data, options) {
  var methodSignature = methodName + '(path, data, [options])';
  validate.argument(methodSignature, 'path', path, ['string']);
  validate.argument(methodSignature, 'data', data, ['string', 'buffer', 'object', 'array']);
  validate.options(methodSignature, 'options', options, {
    atomic: ['boolean'],
    jsonIndent: ['number']
  });
}
```
- example usage
```shell
...
  // API

  var api = {
cwd: cwd,
path: getPath,

append: function (path, data, options) {
  append.validateInput('append', path, data, options);
  append.sync(resolvePath(path), data, options);
},
appendAsync: function (path, data, options) {
  append.validateInput('appendAsync', path, data, options);
  return append.async(resolvePath(path), data, options);
},
...
```



# misc
- this document was created with [utility2](https://github.com/kaizhu256/node-utility2)
