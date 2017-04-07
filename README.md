# api documentation for  [node-persist (v2.0.10)](https://github.com/simonlast/node-persist#readme)  [![npm package](https://img.shields.io/npm/v/npmdoc-node-persist.svg?style=flat-square)](https://www.npmjs.org/package/npmdoc-node-persist) [![travis-ci.org build-status](https://api.travis-ci.org/npmdoc/node-npmdoc-node-persist.svg)](https://travis-ci.org/npmdoc/node-npmdoc-node-persist)
#### Super-easy (and fast) persistent data structures in Node.js, modeled after HTML5 localStorage

[![NPM](https://nodei.co/npm/node-persist.png?downloads=true)](https://www.npmjs.com/package/node-persist)

[![apidoc](https://npmdoc.github.io/node-npmdoc-node-persist/build/screenCapture.buildNpmdoc.browser._2Fhome_2Ftravis_2Fbuild_2Fnpmdoc_2Fnode-npmdoc-node-persist_2Ftmp_2Fbuild_2Fapidoc.html.png)](https://npmdoc.github.io/node-npmdoc-node-persist/build/apidoc.html)

![npmPackageListing](https://npmdoc.github.io/node-npmdoc-node-persist/build/screenCapture.npmPackageListing.svg)

![npmPackageDependencyTree](https://npmdoc.github.io/node-npmdoc-node-persist/build/screenCapture.npmPackageDependencyTree.svg)



# package.json

```json

{
    "bugs": {
        "url": "https://github.com/simonlast/node-persist/issues"
    },
    "contributors": [
        {
            "name": "Simon Last",
            "email": "hello@simonlast.org",
            "url": "http://simonlast.org/"
        },
        {
            "name": "Ben Monro",
            "url": "https://github.com/benmonro"
        },
        {
            "name": "Aziz Khoury",
            "url": "https://github.com/akhoury"
        }
    ],
    "dependencies": {
        "mkdirp": "~0.5.1",
        "q": "~1.1.1"
    },
    "description": "Super-easy (and fast) persistent data structures in Node.js, modeled after HTML5 localStorage",
    "devDependencies": {
        "chai": "^3.5.0",
        "mocha": "^2.3.3",
        "rimraf": "^2.4.3"
    },
    "directories": {
        "example": "examples"
    },
    "dist": {
        "shasum": "78f5a44b267fa9146ab297048e942cb4b9c1a32a",
        "tarball": "https://registry.npmjs.org/node-persist/-/node-persist-2.0.10.tgz"
    },
    "gitHead": "6c9b64fe51d0b9f6d133f0aed1346821115e3882",
    "homepage": "https://github.com/simonlast/node-persist#readme",
    "keywords": [
        "node",
        "persist",
        "storage"
    ],
    "license": "MIT",
    "main": "./src/node-persist.js",
    "maintainers": [
        {
            "name": "akhoury",
            "email": "bentael@gmail.com"
        },
        {
            "name": "benmonro",
            "email": "ben.monro@gmail.com"
        },
        {
            "name": "slast",
            "email": "hello@simonlast.org"
        }
    ],
    "name": "node-persist",
    "optionalDependencies": {},
    "readme": "ERROR: No README data found!",
    "repository": {
        "type": "git",
        "url": "git+https://github.com/simonlast/node-persist.git"
    },
    "scripts": {
        "test": "./node_modules/mocha/bin/mocha tests/"
    },
    "version": "2.0.10"
}
```



# <a name="apidoc.tableOfContents"></a>[table of contents](#apidoc.tableOfContents)

#### [module node-persist](#apidoc.module.node-persist)
1.  [function <span class="apidocSignatureSpan">node-persist.</span>create (userOptions)](#apidoc.element.node-persist.create)
1.  [function <span class="apidocSignatureSpan">node-persist.</span>init (userOptions, callback)](#apidoc.element.node-persist.init)
1.  [function <span class="apidocSignatureSpan">node-persist.</span>initSync (userOptions)](#apidoc.element.node-persist.initSync)
1.  [function <span class="apidocSignatureSpan">node-persist.</span>local_storage (userOptions)](#apidoc.element.node-persist.local_storage)
1.  object <span class="apidocSignatureSpan">node-persist.</span>local_storage.prototype

#### [module node-persist.local_storage](#apidoc.module.node-persist.local_storage)
1.  [function <span class="apidocSignatureSpan">node-persist.</span>local_storage (userOptions)](#apidoc.element.node-persist.local_storage.local_storage)

#### [module node-persist.local_storage.prototype](#apidoc.module.node-persist.local_storage.prototype)
1.  [function <span class="apidocSignatureSpan">node-persist.local_storage.prototype.</span>calcTTL (ttl)](#apidoc.element.node-persist.local_storage.prototype.calcTTL)
1.  [function <span class="apidocSignatureSpan">node-persist.local_storage.prototype.</span>clear (callback)](#apidoc.element.node-persist.local_storage.prototype.clear)
1.  [function <span class="apidocSignatureSpan">node-persist.local_storage.prototype.</span>clearSync ()](#apidoc.element.node-persist.local_storage.prototype.clearSync)
1.  [function <span class="apidocSignatureSpan">node-persist.local_storage.prototype.</span>del (key, callback)](#apidoc.element.node-persist.local_storage.prototype.del)
1.  [function <span class="apidocSignatureSpan">node-persist.local_storage.prototype.</span>forEach (callback)](#apidoc.element.node-persist.local_storage.prototype.forEach)
1.  [function <span class="apidocSignatureSpan">node-persist.local_storage.prototype.</span>get (key, callback)](#apidoc.element.node-persist.local_storage.prototype.get)
1.  [function <span class="apidocSignatureSpan">node-persist.local_storage.prototype.</span>getItem (key, callback)](#apidoc.element.node-persist.local_storage.prototype.getItem)
1.  [function <span class="apidocSignatureSpan">node-persist.local_storage.prototype.</span>getItemSync (key)](#apidoc.element.node-persist.local_storage.prototype.getItemSync)
1.  [function <span class="apidocSignatureSpan">node-persist.local_storage.prototype.</span>init (userOptions, callback)](#apidoc.element.node-persist.local_storage.prototype.init)
1.  [function <span class="apidocSignatureSpan">node-persist.local_storage.prototype.</span>initSync (userOptions)](#apidoc.element.node-persist.local_storage.prototype.initSync)
1.  [function <span class="apidocSignatureSpan">node-persist.local_storage.prototype.</span>isExpired (key)](#apidoc.element.node-persist.local_storage.prototype.isExpired)
1.  [function <span class="apidocSignatureSpan">node-persist.local_storage.prototype.</span>keys ()](#apidoc.element.node-persist.local_storage.prototype.keys)
1.  [function <span class="apidocSignatureSpan">node-persist.local_storage.prototype.</span>length ()](#apidoc.element.node-persist.local_storage.prototype.length)
1.  [function <span class="apidocSignatureSpan">node-persist.local_storage.prototype.</span>log ()](#apidoc.element.node-persist.local_storage.prototype.log)
1.  [function <span class="apidocSignatureSpan">node-persist.local_storage.prototype.</span>md5 (data)](#apidoc.element.node-persist.local_storage.prototype.md5)
1.  [function <span class="apidocSignatureSpan">node-persist.local_storage.prototype.</span>parse (str)](#apidoc.element.node-persist.local_storage.prototype.parse)
1.  [function <span class="apidocSignatureSpan">node-persist.local_storage.prototype.</span>parseFile (filename, callback)](#apidoc.element.node-persist.local_storage.prototype.parseFile)
1.  [function <span class="apidocSignatureSpan">node-persist.local_storage.prototype.</span>parseFileSync (filename)](#apidoc.element.node-persist.local_storage.prototype.parseFileSync)
1.  [function <span class="apidocSignatureSpan">node-persist.local_storage.prototype.</span>parseStorageDir (callback)](#apidoc.element.node-persist.local_storage.prototype.parseStorageDir)
1.  [function <span class="apidocSignatureSpan">node-persist.local_storage.prototype.</span>parseStorageDirSync ()](#apidoc.element.node-persist.local_storage.prototype.parseStorageDirSync)
1.  [function <span class="apidocSignatureSpan">node-persist.local_storage.prototype.</span>persist (callback)](#apidoc.element.node-persist.local_storage.prototype.persist)
1.  [function <span class="apidocSignatureSpan">node-persist.local_storage.prototype.</span>persistKey (key, callback)](#apidoc.element.node-persist.local_storage.prototype.persistKey)
1.  [function <span class="apidocSignatureSpan">node-persist.local_storage.prototype.</span>persistKeySync (key)](#apidoc.element.node-persist.local_storage.prototype.persistKeySync)
1.  [function <span class="apidocSignatureSpan">node-persist.local_storage.prototype.</span>persistSync ()](#apidoc.element.node-persist.local_storage.prototype.persistSync)
1.  [function <span class="apidocSignatureSpan">node-persist.local_storage.prototype.</span>removeExpiredItems (callback)](#apidoc.element.node-persist.local_storage.prototype.removeExpiredItems)
1.  [function <span class="apidocSignatureSpan">node-persist.local_storage.prototype.</span>removeItem (key, callback)](#apidoc.element.node-persist.local_storage.prototype.removeItem)
1.  [function <span class="apidocSignatureSpan">node-persist.local_storage.prototype.</span>removeItemSync (key)](#apidoc.element.node-persist.local_storage.prototype.removeItemSync)
1.  [function <span class="apidocSignatureSpan">node-persist.local_storage.prototype.</span>removePersistedKey (key, callback)](#apidoc.element.node-persist.local_storage.prototype.removePersistedKey)
1.  [function <span class="apidocSignatureSpan">node-persist.local_storage.prototype.</span>removePersistedKeySync (key)](#apidoc.element.node-persist.local_storage.prototype.removePersistedKeySync)
1.  [function <span class="apidocSignatureSpan">node-persist.local_storage.prototype.</span>resolveDir (dir)](#apidoc.element.node-persist.local_storage.prototype.resolveDir)
1.  [function <span class="apidocSignatureSpan">node-persist.local_storage.prototype.</span>rm (key, callback)](#apidoc.element.node-persist.local_storage.prototype.rm)
1.  [function <span class="apidocSignatureSpan">node-persist.local_storage.prototype.</span>set (key, value, options, callback)](#apidoc.element.node-persist.local_storage.prototype.set)
1.  [function <span class="apidocSignatureSpan">node-persist.local_storage.prototype.</span>setItem (key, value, options, callback)](#apidoc.element.node-persist.local_storage.prototype.setItem)
1.  [function <span class="apidocSignatureSpan">node-persist.local_storage.prototype.</span>setItemSync (key, value, options)](#apidoc.element.node-persist.local_storage.prototype.setItemSync)
1.  [function <span class="apidocSignatureSpan">node-persist.local_storage.prototype.</span>setOptions (userOptions)](#apidoc.element.node-persist.local_storage.prototype.setOptions)
1.  [function <span class="apidocSignatureSpan">node-persist.local_storage.prototype.</span>startExpiredKeysInterval ()](#apidoc.element.node-persist.local_storage.prototype.startExpiredKeysInterval)
1.  [function <span class="apidocSignatureSpan">node-persist.local_storage.prototype.</span>startPersistInterval (persistFunction)](#apidoc.element.node-persist.local_storage.prototype.startPersistInterval)
1.  [function <span class="apidocSignatureSpan">node-persist.local_storage.prototype.</span>stopExpiredKeysInterval ()](#apidoc.element.node-persist.local_storage.prototype.stopExpiredKeysInterval)
1.  [function <span class="apidocSignatureSpan">node-persist.local_storage.prototype.</span>stopPersistInterval ()](#apidoc.element.node-persist.local_storage.prototype.stopPersistInterval)
1.  [function <span class="apidocSignatureSpan">node-persist.local_storage.prototype.</span>stringify (obj)](#apidoc.element.node-persist.local_storage.prototype.stringify)
1.  [function <span class="apidocSignatureSpan">node-persist.local_storage.prototype.</span>values ()](#apidoc.element.node-persist.local_storage.prototype.values)
1.  [function <span class="apidocSignatureSpan">node-persist.local_storage.prototype.</span>valuesWithKeyMatch (match)](#apidoc.element.node-persist.local_storage.prototype.valuesWithKeyMatch)



# <a name="apidoc.module.node-persist"></a>[module node-persist](#apidoc.module.node-persist)

#### <a name="apidoc.element.node-persist.create"></a>[function <span class="apidocSignatureSpan">node-persist.</span>create (userOptions)](#apidoc.element.node-persist.create)
- description and source-code
```javascript
create = function (userOptions) {
    return LocalStorage(userOptions);
}
```
- example usage
```shell
...
If you choose to create multiple instances of storage, you can. Just avoid using the same 'dir' for the storage location.
__You still have to call 'init' or 'initSync' after 'create'__ - you can pass your configs to either 'create' or 'init/Sync'

The reason we don't call 'init' in the constructor (or when you 'create') because we can only do so for the 'initSync' version,
the async 'init' returns a promise, and in order to maintain that API, we cannot return the promise in the constructor, so 'init
' must be called on the instance of new LocalStorage();

'''javascript
var storage = require('node-persist');
var myStorage = storage.create({dir: 'myDir', ttl: 3000});
myStorage.init().then(function() { // or you can use initSync()
   // ...
});
'''

### Contributing
...
```

#### <a name="apidoc.element.node-persist.init"></a>[function <span class="apidocSignatureSpan">node-persist.</span>init (userOptions, callback)](#apidoc.element.node-persist.init)
- description and source-code
```javascript
init = function (userOptions, callback) {
    localStorage = nodePersist.defaultInstance = nodePersist.create(userOptions);
    var ret = localStorage.init(callback);
    mixin(nodePersist, localStorage, {skip: ['init', 'initSync', 'create']});
    return ret;
}
```
- example usage
```shell
...

## Basic Example

Async example
'''js
//you must first call storage.init

storage.init( /* options ... */ ).then(function() {
//then start using it
storage.setItem('name','yourname')
.then(function() {

  return storage.getItem('name')
})
.then(function(value) {
...
```

#### <a name="apidoc.element.node-persist.initSync"></a>[function <span class="apidocSignatureSpan">node-persist.</span>initSync (userOptions)](#apidoc.element.node-persist.initSync)
- description and source-code
```javascript
initSync = function (userOptions) {
    localStorage = nodePersist.defaultInstance = nodePersist.create(userOptions);
    var ret = localStorage.initSync();
    mixin(nodePersist, localStorage, {skip: ['init', 'initSync', 'create']});
    return ret;
}
```
- example usage
```shell
...
});

'''

Sync example
'''
//you must first call storage.initSync
storage.initSync();

//then start using it
storage.setItemSync('name','yourname');
console.log(storage.getItemSync('name')); // yourname

'''
...
```

#### <a name="apidoc.element.node-persist.local_storage"></a>[function <span class="apidocSignatureSpan">node-persist.</span>local_storage (userOptions)](#apidoc.element.node-persist.local_storage)
- description and source-code
```javascript
local_storage = function (userOptions) {
    if(!(this instanceof LocalStorage)) {
        return new LocalStorage(userOptions);
    }
    this.data = {};
    this.changes = {};
    this.setOptions(userOptions);

    // we don't call init in the constructor because we can only do so for the initSync
    // for init async, it returns a promise, and in order to maintain that API, we cannot return the promise in the constructor
    // so init must be called, separately, on the instance of new LocalStorage();
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.node-persist.local_storage"></a>[module node-persist.local_storage](#apidoc.module.node-persist.local_storage)

#### <a name="apidoc.element.node-persist.local_storage.local_storage"></a>[function <span class="apidocSignatureSpan">node-persist.</span>local_storage (userOptions)](#apidoc.element.node-persist.local_storage.local_storage)
- description and source-code
```javascript
local_storage = function (userOptions) {
    if(!(this instanceof LocalStorage)) {
        return new LocalStorage(userOptions);
    }
    this.data = {};
    this.changes = {};
    this.setOptions(userOptions);

    // we don't call init in the constructor because we can only do so for the initSync
    // for init async, it returns a promise, and in order to maintain that API, we cannot return the promise in the constructor
    // so init must be called, separately, on the instance of new LocalStorage();
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.node-persist.local_storage.prototype"></a>[module node-persist.local_storage.prototype](#apidoc.module.node-persist.local_storage.prototype)

#### <a name="apidoc.element.node-persist.local_storage.prototype.calcTTL"></a>[function <span class="apidocSignatureSpan">node-persist.local_storage.prototype.</span>calcTTL (ttl)](#apidoc.element.node-persist.local_storage.prototype.calcTTL)
- description and source-code
```javascript
calcTTL = function (ttl) {
    // only check for undefined, if null was passed in setItem then we probably didn't want to use the this.options.ttl
    if (typeof ttl == 'undefined') {
        ttl = this.options.ttl;
    } else {
        ttl = ttl ? isNumber(ttl) && ttl > 0 ? ttl : defaultTTL : false;
    }
    return ttl ? new Date().getTime() + ttl : undefined;
}
```
- example usage
```shell
...

var logmsg = "set (" + key + ": " + this.stringify(value) + ")";

var deferred = Q.defer();
var deferreds = [];

// ttl is different that the other options because we can pass a different for each setItem, as well as have a default one.
var ttl = this.calcTTL(options.ttl);
this.data[key] = {value: value, ttl: ttl};

var instanceOptions = this.options;
var result = {key: key, value: value, ttl: ttl, queued: !!instanceOptions.interval, manual: !instanceOptions.interval && !instanceOptions
.continuous};

var onSuccess = function () {
    callback(null, result);
...
```

#### <a name="apidoc.element.node-persist.local_storage.prototype.clear"></a>[function <span class="apidocSignatureSpan">node-persist.local_storage.prototype.</span>clear (callback)](#apidoc.element.node-persist.local_storage.prototype.clear)
- description and source-code
```javascript
clear = function (callback) {
    callback = isFunction(callback) ? callback : noop;

    var deferred = Q.defer();
    var deferreds = [];

    var keys = this.keys();
    for (var i = 0; i < keys.length; i++) {
        deferreds.push(this.removePersistedKey(keys[i]));
    }

    Q.all(deferreds).then(
        function() {
            this.data = {};
            this.changes = {};
            deferred.resolve();
            callback();
        }.bind(this),
        function(err) {
            deferred.reject(err);
            callback(err);
        });

    return deferred.promise;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.node-persist.local_storage.prototype.clearSync"></a>[function <span class="apidocSignatureSpan">node-persist.local_storage.prototype.</span>clearSync ()](#apidoc.element.node-persist.local_storage.prototype.clearSync)
- description and source-code
```javascript
clearSync = function () {
    var keys = this.keys(true);
    for (var i = 0; i < keys.length; i++) {
        this.removePersistedKeySync(keys[i]);
    }
    this.data = {};
    this.changes = {};
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.node-persist.local_storage.prototype.del"></a>[function <span class="apidocSignatureSpan">node-persist.local_storage.prototype.</span>del (key, callback)](#apidoc.element.node-persist.local_storage.prototype.del)
- description and source-code
```javascript
del = function (key, callback) {
    return this.removeItem(key, callback);
}
```
- example usage
```shell
...
* 'storage.getItem()' now returns a promise
* 'storage.valuesWithKeyMatch()' no longer accepts a callback
* 'storage.values()' no longer accepts a callback
* 'storage.key()' is gone
* The default 'dir' is now 'process.cwd() + (dir || '.node-persist/storage')', unless you use an absolute path
* added 'storage.get()', alias to 'getItem()'
* added 'storage.set()', alias to 'setItem()'
* added 'storage.del()', 'storage.rm()', as aliases to 'removeItem()'
* Keys, on the file system are base64 encoded with the replacement of the '/'

## API Documentation

#### 'init(options, [callback])' - asynchronous*, returns Promise
This function reads what's on disk and loads it into memory, if the storage dir is new, it will create it
##### Options
...
```

#### <a name="apidoc.element.node-persist.local_storage.prototype.forEach"></a>[function <span class="apidocSignatureSpan">node-persist.local_storage.prototype.</span>forEach (callback)](#apidoc.element.node-persist.local_storage.prototype.forEach)
- description and source-code
```javascript
forEach = function (callback) {
    return this.keys().forEach(function(key) {
        callback(key, this.data[key].value);
    }.bind(this));
}
```
- example usage
```shell
...
This function returns the number of keys stored in the database.

#### 'forEach(callback)' - synchronous, assuming callback is as well.

This function iterates over each key/value pair and executes a callback.

'''javascript
storage.forEach(function(key, value) {
	// use key and value
});
'''

### Fine-grained control
Make sure you set 'continuous:false' in the 'options' hash, and you don't set an 'interval'
...
```

#### <a name="apidoc.element.node-persist.local_storage.prototype.get"></a>[function <span class="apidocSignatureSpan">node-persist.local_storage.prototype.</span>get (key, callback)](#apidoc.element.node-persist.local_storage.prototype.get)
- description and source-code
```javascript
get = function (key, callback) {
    return this.getItem(key, callback);
}
```
- example usage
```shell
...
Mostly non-backward changes

* 'storage.getItem()' now returns a promise
* 'storage.valuesWithKeyMatch()' no longer accepts a callback
* 'storage.values()' no longer accepts a callback
* 'storage.key()' is gone
* The default 'dir' is now 'process.cwd() + (dir || '.node-persist/storage')', unless you use an absolute path
* added 'storage.get()', alias to 'getItem()'
* added 'storage.set()', alias to 'setItem()'
* added 'storage.del()', 'storage.rm()', as aliases to 'removeItem()'
* Keys, on the file system are base64 encoded with the replacement of the '/'

## API Documentation

#### 'init(options, [callback])' - asynchronous*, returns Promise
...
```

#### <a name="apidoc.element.node-persist.local_storage.prototype.getItem"></a>[function <span class="apidocSignatureSpan">node-persist.local_storage.prototype.</span>getItem (key, callback)](#apidoc.element.node-persist.local_storage.prototype.getItem)
- description and source-code
```javascript
getItem = function (key, callback) {
    callback = isFunction(callback) ? callback : noop;
    var deferred = Q.defer();

    if (this.isExpired(key)) {
        this.log(key + ' has expired');
        if (this.options.interval || !this.options.continuous) {
            callback(null, null);
            return deferred.resolve(null);
        }
        return this.removeItem(key).then(function() {
            callback(null, null);
            return null;
        }, callback);
    } else {
        callback(null, this.data[key] && this.data[key].value);
        deferred.resolve(this.data[key] && this.data[key].value);
    }
    return deferred.promise;
}
```
- example usage
```shell
...
//you must first call storage.init

storage.init( /* options ... */ ).then(function() {
  //then start using it
  storage.setItem('name','yourname')
  .then(function() {

    return storage.getItem('name')
  })
  .then(function(value) {

    console.log(value); // yourname
  })
});
...
```

#### <a name="apidoc.element.node-persist.local_storage.prototype.getItemSync"></a>[function <span class="apidocSignatureSpan">node-persist.local_storage.prototype.</span>getItemSync (key)](#apidoc.element.node-persist.local_storage.prototype.getItemSync)
- description and source-code
```javascript
getItemSync = function (key) {
    if (this.isExpired(key)) {
        this.removeItemSync(key);
    } else {
        return this.data[key] && this.data[key].value;
    }
}
```
- example usage
```shell
...
Sync example
'''
//you must first call storage.initSync
storage.initSync();

//then start using it
storage.setItemSync('name','yourname');
console.log(storage.getItemSync('name')); // yourname

'''

## Run the examples:

'''sh
$ cd examples/examplename
...
```

#### <a name="apidoc.element.node-persist.local_storage.prototype.init"></a>[function <span class="apidocSignatureSpan">node-persist.local_storage.prototype.</span>init (userOptions, callback)](#apidoc.element.node-persist.local_storage.prototype.init)
- description and source-code
```javascript
init = function (userOptions, callback) {
    if (isFunction(userOptions)) {
        callback = userOptions;
        userOptions = null;
    }
    if (userOptions) {
        this.setOptions(userOptions);
    }
    callback = isFunction(callback) ? callback : noop;

    var deferred = Q.defer();
    var deferreds = [];

    var options = this.options;

    var result = {dir: options.dir};
    deferreds.push(this.parseStorageDir());

    //start persisting
    if (options.interval && options.interval > 0) {
        this.startPersistInterval(this.persist.bind(this));
    }

    if (options.expiredInterval) {
        this.startExpiredKeysInterval();
    }

    Q.all(deferreds).then(
        function() {
            deferred.resolve(result);
            callback(null, result);
        },
        function(err) {
            deferred.reject(err);
            callback(err);
        });

    return deferred.promise;
}
```
- example usage
```shell
...

## Basic Example

Async example
'''js
//you must first call storage.init

storage.init( /* options ... */ ).then(function() {
//then start using it
storage.setItem('name','yourname')
.then(function() {

  return storage.getItem('name')
})
.then(function(value) {
...
```

#### <a name="apidoc.element.node-persist.local_storage.prototype.initSync"></a>[function <span class="apidocSignatureSpan">node-persist.local_storage.prototype.</span>initSync (userOptions)](#apidoc.element.node-persist.local_storage.prototype.initSync)
- description and source-code
```javascript
initSync = function (userOptions) {
    if (userOptions) {
        this.setOptions(userOptions);
    }

    var options = this.options;

    if (options.logging) {
        this.log("options:");
        this.log(this.stringify(options));
    }

    this.parseStorageDirSync();
    if (options.expiredInterval) {
        this.startExpiredKeysInterval();
    }
    //start synchronous persisting,
    if (options.interval && options.interval > 0) {
        this._persistInterval = setInterval(this.persistSync.bind(this), options.interval);
    }
}
```
- example usage
```shell
...
});

'''

Sync example
'''
//you must first call storage.initSync
storage.initSync();

//then start using it
storage.setItemSync('name','yourname');
console.log(storage.getItemSync('name')); // yourname

'''
...
```

#### <a name="apidoc.element.node-persist.local_storage.prototype.isExpired"></a>[function <span class="apidocSignatureSpan">node-persist.local_storage.prototype.</span>isExpired (key)](#apidoc.element.node-persist.local_storage.prototype.isExpired)
- description and source-code
```javascript
isExpired = function (key) {
    return this.data[key] && this.data[key].ttl && this.data[key].ttl < (new Date()).getTime();
}
```
- example usage
```shell
...
return this.getItem(key, callback);
    },

    getItem: function (key, callback) {
callback = isFunction(callback) ? callback : noop;
var deferred = Q.defer();

if (this.isExpired(key)) {
    this.log(key + ' has expired');
    if (this.options.interval || !this.options.continuous) {
        callback(null, null);
        return deferred.resolve(null);
    }
    return this.removeItem(key).then(function() {
        callback(null, null);
...
```

#### <a name="apidoc.element.node-persist.local_storage.prototype.keys"></a>[function <span class="apidocSignatureSpan">node-persist.local_storage.prototype.</span>keys ()](#apidoc.element.node-persist.local_storage.prototype.keys)
- description and source-code
```javascript
keys = function () {
    return Object.keys(this.data);
}
```
- example usage
```shell
...
    //start synchronous persisting,
    if (options.interval && options.interval > 0) {
        this._persistInterval = setInterval(this.persistSync.bind(this), options.interval);
    }
},

keys: function () {
    return Object.keys(this.data);
},

length: function () {
    return this.keys().length;
},

forEach: function(callback) {
...
```

#### <a name="apidoc.element.node-persist.local_storage.prototype.length"></a>[function <span class="apidocSignatureSpan">node-persist.local_storage.prototype.</span>length ()](#apidoc.element.node-persist.local_storage.prototype.length)
- description and source-code
```javascript
length = function () {
    return this.keys().length;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.node-persist.local_storage.prototype.log"></a>[function <span class="apidocSignatureSpan">node-persist.local_storage.prototype.</span>log ()](#apidoc.element.node-persist.local_storage.prototype.log)
- description and source-code
```javascript
log = function () {
    this.options && this.options.logging && console.log.apply(console, arguments);
}
```
- example usage
```shell
...
  storage.setItem('name','yourname')
  .then(function() {

    return storage.getItem('name')
  })
  .then(function(value) {

    console.log(value); // yourname
  })
});

'''

Sync example
'''
...
```

#### <a name="apidoc.element.node-persist.local_storage.prototype.md5"></a>[function <span class="apidocSignatureSpan">node-persist.local_storage.prototype.</span>md5 (data)](#apidoc.element.node-persist.local_storage.prototype.md5)
- description and source-code
```javascript
md5 = function (data) {
    return crypto.createHash('md5').update(data).digest("hex");
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.node-persist.local_storage.prototype.parse"></a>[function <span class="apidocSignatureSpan">node-persist.local_storage.prototype.</span>parse (str)](#apidoc.element.node-persist.local_storage.prototype.parse)
- description and source-code
```javascript
parse = function (str){
    try {
        return this.options.parse(str);
    } catch(e) {
        this.log("parse error: ", this.stringify(e));
        return undefined;
    }
}
```
- example usage
```shell
...

stringify: function (obj) {
    return this.options.stringify(obj);
},

parse: function(str){
    try {
        return this.options.parse(str);
    } catch(e) {
        this.log("parse error: ", this.stringify(e));
        return undefined;
    }
},

parseStorageDir: function(callback) {
...
```

#### <a name="apidoc.element.node-persist.local_storage.prototype.parseFile"></a>[function <span class="apidocSignatureSpan">node-persist.local_storage.prototype.</span>parseFile (filename, callback)](#apidoc.element.node-persist.local_storage.prototype.parseFile)
- description and source-code
```javascript
parseFile = function (filename, callback) {
    callback = isFunction(callback) ? callback : noop;

    var deferred = Q.defer();
    var self = this;
    var options = this.options;
    var dir = this.options.dir;
    var file = path.join(dir, filename);

    var error = function (err) {
        deferred.reject(err);
        return callback(err);
    };

    var done = function (input) {
        deferred.resolve(input);
        callback(null, input);
    };

    fs.readFile(file, options.encoding, function (err, text) {
        if (err) {
            return error(err);
        }
        var input = self.parse(text);
        if (!isValidStorageFileContent(input)) {
            return options.forgiveParseErrors ? done() : error(new Error('[PARSE-ERROR] ' + file + ' does not look like a valid
storage file!'));
        }
        self.data[input.key] = input;
        self.log("loaded: " + dir + "/" + input.key);
        done(input);
    });

    return deferred.promise;
}
```
- example usage
```shell
...
    deferred.reject(err);
    callback(err);
}

for (var i in arr) {
    var currentFile = arr[i];
    if (currentFile[0] !== '.') {
        deferreds.push(self.parseFile(currentFile));
    }
}

Q.all(deferreds).then(
    function() {
        deferred.resolve(result);
        callback(null, result);
...
```

#### <a name="apidoc.element.node-persist.local_storage.prototype.parseFileSync"></a>[function <span class="apidocSignatureSpan">node-persist.local_storage.prototype.</span>parseFileSync (filename)](#apidoc.element.node-persist.local_storage.prototype.parseFileSync)
- description and source-code
```javascript
parseFileSync = function (filename) {
    var dir = this.options.dir;
    var file = path.join(dir, filename);
    var input = this.parse(fs.readFileSync(file, this.options.encoding));
    if (!isValidStorageFileContent(input)) {
        if (this.options.forgiveParseErrors) {
            return;
        }
        throw Error('[PARSE-ERROR] ' + file + ' does not look like a valid storage file!');
    }
    this.data[input.key] = input;
    this.log("loaded: " + dir + "/" + input.key);
    return this.data[input.key];
}
```
- example usage
```shell
...
    var exists = fs.existsSync(dir);

    if (exists) { //load data
        var arr = fs.readdirSync(dir);
        for (var i = 0; i < arr.length; i++) {
            var currentFile = arr[i];
            if (arr[i] && currentFile[0] !== '.') {
                this.parseFileSync(currentFile);
            }
        }
    } else { //create the directory
        mkdirp.sync(dir);
    }
},
...
```

#### <a name="apidoc.element.node-persist.local_storage.prototype.parseStorageDir"></a>[function <span class="apidocSignatureSpan">node-persist.local_storage.prototype.</span>parseStorageDir (callback)](#apidoc.element.node-persist.local_storage.prototype.parseStorageDir)
- description and source-code
```javascript
parseStorageDir = function (callback) {
    callback = isFunction(callback) ? callback : noop;

    var deferred = Q.defer();
    var deferreds = [];

    var dir = this.options.dir;
    var self = this;
    var result = {dir: dir};

    //check to see if dir is present
    fs.exists(dir, function (exists) {
        if (exists) {
            //load data
            fs.readdir(dir, function (err, arr) {
                if (err) {
                    deferred.reject(err);
                    callback(err);
                }

                for (var i in arr) {
                    var currentFile = arr[i];
                    if (currentFile[0] !== '.') {
                        deferreds.push(self.parseFile(currentFile));
                    }
                }

                Q.all(deferreds).then(
                    function() {
                        deferred.resolve(result);
                        callback(null, result);
                    },
                    function(err) {
                        deferred.reject(err);
                        callback(err);
                    });
            });
        } else {
            //create the directory
            mkdirp(dir, function (err) {
                if (err) {
                    console.error(err);
                    deferred.reject(err);
                    callback(err);
                } else {
                    self.log('created ' + dir);
                    deferred.resolve(result);
                    callback(null, result);
                }
            });
        }
    });

    return deferred.promise;
}
```
- example usage
```shell
...

var deferred = Q.defer();
var deferreds = [];

var options = this.options;

var result = {dir: options.dir};
deferreds.push(this.parseStorageDir());

//start persisting
if (options.interval && options.interval > 0) {
    this.startPersistInterval(this.persist.bind(this));
}

if (options.expiredInterval) {
...
```

#### <a name="apidoc.element.node-persist.local_storage.prototype.parseStorageDirSync"></a>[function <span class="apidocSignatureSpan">node-persist.local_storage.prototype.</span>parseStorageDirSync ()](#apidoc.element.node-persist.local_storage.prototype.parseStorageDirSync)
- description and source-code
```javascript
parseStorageDirSync = function () {
    var dir = this.options.dir;
    var exists = fs.existsSync(dir);

    if (exists) { //load data
        var arr = fs.readdirSync(dir);
        for (var i = 0; i < arr.length; i++) {
            var currentFile = arr[i];
            if (arr[i] && currentFile[0] !== '.') {
                this.parseFileSync(currentFile);
            }
        }
    } else { //create the directory
        mkdirp.sync(dir);
    }
}
```
- example usage
```shell
...
var options = this.options;

if (options.logging) {
    this.log("options:");
    this.log(this.stringify(options));
}

this.parseStorageDirSync();
if (options.expiredInterval) {
    this.startExpiredKeysInterval();
}
//start synchronous persisting,
if (options.interval && options.interval > 0) {
    this._persistInterval = setInterval(this.persistSync.bind(this), options.interval);
}
...
```

#### <a name="apidoc.element.node-persist.local_storage.prototype.persist"></a>[function <span class="apidocSignatureSpan">node-persist.local_storage.prototype.</span>persist (callback)](#apidoc.element.node-persist.local_storage.prototype.persist)
- description and source-code
```javascript
persist = function (callback) {
    callback = isFunction(callback) ? callback : noop;

    var deferred = Q.defer();
    var result;
    var deferreds = [];

    for (var key in this.data) {
        if (this.changes[key]) {
            deferreds.push(this.persistKey(key));
        }
    }

    Q.all(deferreds).then(
        function(result) {
            deferred.resolve(result);
            callback(null, result);
            this.log('persist done');
        }.bind(this),
        function(err) {
            deferred.reject(result);
            callback(err);
        });

    return deferred.promise;
}
```
- example usage
```shell
...

### Fine-grained control
Make sure you set 'continuous:false' in the 'options' hash, and you don't set an 'interval'

#### 'persist([callback])' - asynchronous, returns Promise
These function can be used to manually persist the database
'''js
storage.persist( /* optional callback */ function(err) {
    // when done
}).then(onSuccess, onError); // or you can use the promise
'''
#### 'persistSync()' - synchronous, throws Error on failure
like 'persist()' but synchronous
'''js
storage.persistSync();
...
```

#### <a name="apidoc.element.node-persist.local_storage.prototype.persistKey"></a>[function <span class="apidocSignatureSpan">node-persist.local_storage.prototype.</span>persistKey (key, callback)](#apidoc.element.node-persist.local_storage.prototype.persistKey)
- description and source-code
```javascript
persistKey = function (key, callback) {
    callback = isFunction(callback) ? callback : noop;

    var self = this;
    var options = this.options;
    var file = path.join(options.dir, md5(key));

    var deferred = Q.defer();
    var output = {key: key, value: this.data[key] && this.data[key].value, ttl: this.data[key] && this.data[key].ttl};

    fs.writeFile(file, this.stringify(output), options.encoding, function(err) {
        if (err) {
            self.changes[key] && self.changes[key].onError && self.changes[key].onError(err);
            deferred.reject(err);
            return callback(err);
        }

        self.changes[key] && self.changes[key].onSuccess && self.changes[key].onSuccess();
        delete self.changes[key];
        deferred.resolve(output);
        callback(null, output);
        self.log("wrote: " + key);
    });

    return deferred.promise;
}
```
- example usage
```shell
...
##### note:
Both 'persist()', 'persistSync()', 'persistKey()', and 'persistKeySync()' will automatically persist the ttl keys/values in the
persistance process

#### 'persistKey(key, [callback])' - asynchronous, returns Promise
This function manually persist a 'key' within the database
'''js
storage.setItem('name','myname');
storage.persistKey('name', /* optional callback */ function(err) {
    // when done
}).then(onSuccess, onError); // or you can use the promise
'''

#### 'persistKeySync(key)'
like 'persistKey()' but synchronous
'''js
...
```

#### <a name="apidoc.element.node-persist.local_storage.prototype.persistKeySync"></a>[function <span class="apidocSignatureSpan">node-persist.local_storage.prototype.</span>persistKeySync (key)](#apidoc.element.node-persist.local_storage.prototype.persistKeySync)
- description and source-code
```javascript
persistKeySync = function (key) {
    var options = this.options;
    var file = path.join(options.dir, md5(key));

    var output = {key: key, value: this.data[key] && this.data[key].value, ttl: this.data[key] && this.data[key].ttl};
    try {
        fs.writeFileSync(file, this.stringify(output));
        this.changes[key] && this.changes[key].onSuccess && this.changes[key].onSuccess();
    } catch (err) {
        this.changes[key] && this.changes[key].onError && this.changes[key].onError(err);
        throw err;
    }
    delete this.changes[key];
    this.log("wrote: " + key);
}
```
- example usage
```shell
...
}).then(onSuccess, onError); // or you can use the promise
'''

#### 'persistKeySync(key)'
like 'persistKey()' but synchronous
'''js
storage.setItem('name','myname');
storage.persistKeySync('name');
'''

### Factory method

#### 'create(options)' - synchronous, static method

If you choose to create multiple instances of storage, you can. Just avoid using the same 'dir' for the storage location.
...
```

#### <a name="apidoc.element.node-persist.local_storage.prototype.persistSync"></a>[function <span class="apidocSignatureSpan">node-persist.local_storage.prototype.</span>persistSync ()](#apidoc.element.node-persist.local_storage.prototype.persistSync)
- description and source-code
```javascript
persistSync = function () {
    for (var key in this.data) {
        if (this.changes[key]) {
            this.persistKeySync(key);
        }
    }
    this.log('persistSync done');
}
```
- example usage
```shell
...
storage.persist( /* optional callback */ function(err) {
    // when done
}).then(onSuccess, onError); // or you can use the promise
'''
#### 'persistSync()' - synchronous, throws Error on failure
like 'persist()' but synchronous
'''js
storage.persistSync();
'''
##### note:
Both 'persist()', 'persistSync()', 'persistKey()', and 'persistKeySync()' will automatically persist the ttl keys/values in the
persistance process

#### 'persistKey(key, [callback])' - asynchronous, returns Promise
This function manually persist a 'key' within the database
'''js
...
```

#### <a name="apidoc.element.node-persist.local_storage.prototype.removeExpiredItems"></a>[function <span class="apidocSignatureSpan">node-persist.local_storage.prototype.</span>removeExpiredItems (callback)](#apidoc.element.node-persist.local_storage.prototype.removeExpiredItems)
- description and source-code
```javascript
removeExpiredItems = function (callback) {
    callback = isFunction(callback) ? callback : noop;
    var deferred = Q.defer();
    var deferreds = [];

    var keys = this.keys();
    for (var i = 0; i < keys.length; i++) {
        if (this.isExpired(keys[i])) {
            deferreds.push(this.removeItem(keys[i]));
        }
    }
    Q.all(deferreds).then(
        function() {
            deferred.resolve();
            callback();
        },
        function(err) {
            deferred.reject(err);
            callback(err);
        });

    return deferred.promise;

}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.node-persist.local_storage.prototype.removeItem"></a>[function <span class="apidocSignatureSpan">node-persist.local_storage.prototype.</span>removeItem (key, callback)](#apidoc.element.node-persist.local_storage.prototype.removeItem)
- description and source-code
```javascript
removeItem = function (key, callback) {
    callback = isFunction(callback) ? callback : noop;

    var deferred = Q.defer();
    var deferreds = [];

    deferreds.push(this.removePersistedKey(key));

    Q.all(deferreds).then(
        function() {
            var value = this.data[key] && this.data[key].value;
            delete this.data[key];
            this.log('removed: ' + key);
            callback(null, value);
            deferred.resolve(value);
        }.bind(this),
        function(err) {
            callback(err);
            deferred.reject(err);
        }
    );
    return deferred.promise;
}
```
- example usage
```shell
...
storage.setItemSync('foo', 'bar');
storage.setItemSync('hello', 'world', {ttl: 1000 * 60 /* ttl 1 minute */})
'''
#### 'removeItem(key, [callback])' - asynchronous, returns Promise
This function removes key in the database if it is present, and immediately deletes it from the file system asynchronously. If ttl
 is used, the corrresponding ttl-key is removed as well

'''js
storage.removeItem('me', /* optional callback */ function(err) {
  // done
}).then(onSuccess, onError); // or use the promise
'''
#### 'removeItemSync(key)' - synchronous,  throws Error on failure
just like removeItem, but synchronous
'''js
storage.removeItemSync('me');
...
```

#### <a name="apidoc.element.node-persist.local_storage.prototype.removeItemSync"></a>[function <span class="apidocSignatureSpan">node-persist.local_storage.prototype.</span>removeItemSync (key)](#apidoc.element.node-persist.local_storage.prototype.removeItemSync)
- description and source-code
```javascript
removeItemSync = function (key) {
    var value = this.data[key] && this.data[key].value;
    this.removePersistedKeySync(key);
    delete this.data[key];
    this.log('removed: ' + key);
    return value;
}
```
- example usage
```shell
...
storage.removeItem('me', /* optional callback */ function(err) {
  // done
}).then(onSuccess, onError); // or use the promise
'''
#### 'removeItemSync(key)' - synchronous,  throws Error on failure
just like removeItem, but synchronous
'''js
storage.removeItemSync('me');
'''
#### 'clear([callback])' - asynchronous, returns Promise
This function removes all keys in the database, and immediately deletes all keys from the file system asynchronously.
#### 'clearSync()' - synchronous, throws Error on failure
like 'clear()' but synchronous

#### 'values()' -  synchronous, returns array
...
```

#### <a name="apidoc.element.node-persist.local_storage.prototype.removePersistedKey"></a>[function <span class="apidocSignatureSpan">node-persist.local_storage.prototype.</span>removePersistedKey (key, callback)](#apidoc.element.node-persist.local_storage.prototype.removePersistedKey)
- description and source-code
```javascript
removePersistedKey = function (key, callback) {
    callback = isFunction(callback) ? callback : noop;

    var options = this.options;
    var deferred = Q.defer();
    var result;

    //check to see if key has been persisted
    var file = path.join(options.dir, md5(key));
    fs.exists(file, function (exists) {
        if (exists) {
            fs.unlink(file, function (err) {
                result = {key: key, removed: !err, existed: exists};
                if (err && err.code != 'ENOENT') {<span class="apidocCodeCommentSpan"> /* Only throw the error if the error is something else */
</span>                    deferred.reject(err);
                    return callback(err);
                }
                err && this.log('Failed to remove file:' + file + ' because it doesn\'t exist anymore.');
                deferred.resolve(result);
                callback(null, result);
            }.bind(this));
        } else {
            result = {key: key, removed: false, existed: exists};
            deferred.resolve(result);
            callback(null, result);
        }
    }.bind(this));

    return deferred.promise;
}
```
- example usage
```shell
...

    removeItem: function (key, callback) {
callback = isFunction(callback) ? callback : noop;

var deferred = Q.defer();
var deferreds = [];

deferreds.push(this.removePersistedKey(key));

Q.all(deferreds).then(
    function() {
        var value = this.data[key] && this.data[key].value;
        delete this.data[key];
        this.log('removed: ' + key);
        callback(null, value);
...
```

#### <a name="apidoc.element.node-persist.local_storage.prototype.removePersistedKeySync"></a>[function <span class="apidocSignatureSpan">node-persist.local_storage.prototype.</span>removePersistedKeySync (key)](#apidoc.element.node-persist.local_storage.prototype.removePersistedKeySync)
- description and source-code
```javascript
removePersistedKeySync = function (key) {
    var options = this.options;
    var file = path.join(options.dir, md5(key));
    if (fs.existsSync(file)) {
        try {
            fs.unlinkSync(file);
        } catch (err) {
            if (err.code != 'ENOENT') {<span class="apidocCodeCommentSpan"> /* Only throw the error if the error is something else */
</span>                throw err;
            }
            this.log('Failed to remove file:' + file + ' because it doesn\'t exist anymore.');
        }
        return {key: key, removed: true, existed: true};
    }
    return {key: key, removed: false, existed: false};
}
```
- example usage
```shell
...
        }
    );
    return deferred.promise;
},

removeItemSync: function (key) {
    var value = this.data[key] && this.data[key].value;
    this.removePersistedKeySync(key);
    delete this.data[key];
    this.log('removed: ' + key);
    return value;
},

removeExpiredItems: function (callback) {
    callback = isFunction(callback) ? callback : noop;
...
```

#### <a name="apidoc.element.node-persist.local_storage.prototype.resolveDir"></a>[function <span class="apidocSignatureSpan">node-persist.local_storage.prototype.</span>resolveDir (dir)](#apidoc.element.node-persist.local_storage.prototype.resolveDir)
- description and source-code
```javascript
resolveDir = function (dir) {
    dir = path.normalize(dir);
    if (path.isAbsolute(dir)) {
        return dir;
    }
    return path.join(process.cwd(), dir);
}
```
- example usage
```shell
...
        if (userOptions.hasOwnProperty(key)) {
            options[key] = userOptions[key];
        } else {
            options[key] = defaults[key];
        }
    }

    options.dir = this.resolveDir(options.dir);
    options.ttl = options.ttl ? isNumber(options.ttl) && options.ttl > 0 ? options.ttl : defaultTTL : false;
}

// Check to see if we received an external logging function
if (isFunction(options.logging)) {
    // Overwrite log function with external logging function
    this.log = options.logging;
...
```

#### <a name="apidoc.element.node-persist.local_storage.prototype.rm"></a>[function <span class="apidocSignatureSpan">node-persist.local_storage.prototype.</span>rm (key, callback)](#apidoc.element.node-persist.local_storage.prototype.rm)
- description and source-code
```javascript
rm = function (key, callback) {
    return this.removeItem(key, callback);
}
```
- example usage
```shell
...
* 'storage.getItem()' now returns a promise
* 'storage.valuesWithKeyMatch()' no longer accepts a callback
* 'storage.values()' no longer accepts a callback
* 'storage.key()' is gone
* The default 'dir' is now 'process.cwd() + (dir || '.node-persist/storage')', unless you use an absolute path
* added 'storage.get()', alias to 'getItem()'
* added 'storage.set()', alias to 'setItem()'
* added 'storage.del()', 'storage.rm()', as aliases to 'removeItem()'
* Keys, on the file system are base64 encoded with the replacement of the '/'

## API Documentation

#### 'init(options, [callback])' - asynchronous*, returns Promise
This function reads what's on disk and loads it into memory, if the storage dir is new, it will create it
##### Options
...
```

#### <a name="apidoc.element.node-persist.local_storage.prototype.set"></a>[function <span class="apidocSignatureSpan">node-persist.local_storage.prototype.</span>set (key, value, options, callback)](#apidoc.element.node-persist.local_storage.prototype.set)
- description and source-code
```javascript
set = function (key, value, options, callback) {
    return this.setItem(key, value, options, callback);
}
```
- example usage
```shell
...

* 'storage.getItem()' now returns a promise
* 'storage.valuesWithKeyMatch()' no longer accepts a callback
* 'storage.values()' no longer accepts a callback
* 'storage.key()' is gone
* The default 'dir' is now 'process.cwd() + (dir || '.node-persist/storage')', unless you use an absolute path
* added 'storage.get()', alias to 'getItem()'
* added 'storage.set()', alias to 'setItem()'
* added 'storage.del()', 'storage.rm()', as aliases to 'removeItem()'
* Keys, on the file system are base64 encoded with the replacement of the '/'

## API Documentation

#### 'init(options, [callback])' - asynchronous*, returns Promise
This function reads what's on disk and loads it into memory, if the storage dir is new, it will create it
...
```

#### <a name="apidoc.element.node-persist.local_storage.prototype.setItem"></a>[function <span class="apidocSignatureSpan">node-persist.local_storage.prototype.</span>setItem (key, value, options, callback)](#apidoc.element.node-persist.local_storage.prototype.setItem)
- description and source-code
```javascript
setItem = function (key, value, options, callback) {
    if (typeof options == 'function') {
        callback = options;
        options = null;
    }
    options = options || {};
    callback = isFunction(callback) ? callback : noop;

    var logmsg = "set (" + key + ": " + this.stringify(value) + ")";

    var deferred = Q.defer();
    var deferreds = [];

    // ttl is different that the other options because we can pass a different for each setItem, as well as have a default one.
    var ttl = this.calcTTL(options.ttl);
    this.data[key] = {value: value, ttl: ttl};

    var instanceOptions = this.options;
    var result = {key: key, value: value, ttl: ttl, queued: !!instanceOptions.interval, manual: !instanceOptions.interval && !instanceOptions
.continuous};

    var onSuccess = function () {
        callback(null, result);
        deferred.resolve(result);
    };

    var onError = function (err) {
        callback(err);
        deferred.reject(err);
    };

    this.log(logmsg);

    if (instanceOptions.interval || !instanceOptions.continuous) {
        this.changes[key] = {onSuccess: onSuccess, onError: onError};
    } else {
        deferreds.push(this.persistKey(key));

        Q.all(deferreds).then(
            function(result) {
                deferred.resolve(result);
                callback(null, result);
            }.bind(this),
            function(err) {
                deferred.reject(err);
                callback(err);
            });
    }

    return deferred.promise;
}
```
- example usage
```shell
...

Async example
'''js
//you must first call storage.init

storage.init( /* options ... */ ).then(function() {
  //then start using it
  storage.setItem('name','yourname')
  .then(function() {

return storage.getItem('name')
  })
  .then(function(value) {

console.log(value); // yourname
...
```

#### <a name="apidoc.element.node-persist.local_storage.prototype.setItemSync"></a>[function <span class="apidocSignatureSpan">node-persist.local_storage.prototype.</span>setItemSync (key, value, options)](#apidoc.element.node-persist.local_storage.prototype.setItemSync)
- description and source-code
```javascript
setItemSync = function (key, value, options) {
    options = options || {};
    var ttl = this.calcTTL(options.ttl);
    this.data[key] = {key: key, value: value, ttl: ttl};
    this.persistKeySync(key);
    this.log("set (" + key + ": " + this.stringify(value) + ")");
}
```
- example usage
```shell
...

Sync example
'''
//you must first call storage.initSync
storage.initSync();

//then start using it
storage.setItemSync('name','yourname');
console.log(storage.getItemSync('name')); // yourname

'''

## Run the examples:

'''sh
...
```

#### <a name="apidoc.element.node-persist.local_storage.prototype.setOptions"></a>[function <span class="apidocSignatureSpan">node-persist.local_storage.prototype.</span>setOptions (userOptions)](#apidoc.element.node-persist.local_storage.prototype.setOptions)
- description and source-code
```javascript
setOptions = function (userOptions) {
    var options = {};

    if (!userOptions) {
        options = defaults;
    } else {
        for (var key in defaults) {
            if (userOptions.hasOwnProperty(key)) {
                options[key] = userOptions[key];
            } else {
                options[key] = defaults[key];
            }
        }

        options.dir = this.resolveDir(options.dir);
        options.ttl = options.ttl ? isNumber(options.ttl) && options.ttl > 0 ? options.ttl : defaultTTL : false;
    }

    // Check to see if we received an external logging function
    if (isFunction(options.logging)) {
        // Overwrite log function with external logging function
        this.log = options.logging;
        options.logging = true;
    }

    this.options = options;
}
```
- example usage
```shell
...

var LocalStorage = function (userOptions) {
    if(!(this instanceof LocalStorage)) {
        return new LocalStorage(userOptions);
    }
    this.data = {};
    this.changes = {};
    this.setOptions(userOptions);

    // we don't call init in the constructor because we can only do so for the initSync
    // for init async, it returns a promise, and in order to maintain that API, we cannot return the promise in the constructor
    // so init must be called, separately, on the instance of new LocalStorage();
};

LocalStorage.prototype = {
...
```

#### <a name="apidoc.element.node-persist.local_storage.prototype.startExpiredKeysInterval"></a>[function <span class="apidocSignatureSpan">node-persist.local_storage.prototype.</span>startExpiredKeysInterval ()](#apidoc.element.node-persist.local_storage.prototype.startExpiredKeysInterval)
- description and source-code
```javascript
startExpiredKeysInterval = function () {
    this.stopExpiredKeysInterval();
    this._expiredKeysInterval = setInterval(this.removeExpiredItems.bind(this), this.options.expiredInterval);
    this._expiredKeysInterval.unref();
}
```
- example usage
```shell
...

//start persisting
if (options.interval && options.interval > 0) {
    this.startPersistInterval(this.persist.bind(this));
}

if (options.expiredInterval) {
    this.startExpiredKeysInterval();
}

Q.all(deferreds).then(
    function() {
        deferred.resolve(result);
        callback(null, result);
    },
...
```

#### <a name="apidoc.element.node-persist.local_storage.prototype.startPersistInterval"></a>[function <span class="apidocSignatureSpan">node-persist.local_storage.prototype.</span>startPersistInterval (persistFunction)](#apidoc.element.node-persist.local_storage.prototype.startPersistInterval)
- description and source-code
```javascript
startPersistInterval = function (persistFunction) {
    this.stopPersistInterval();
    this._persistInterval = setInterval(persistFunction || this.persist.bind(this), this.options.interval);
    this._persistInterval.unref();
}
```
- example usage
```shell
...
var options = this.options;

var result = {dir: options.dir};
deferreds.push(this.parseStorageDir());

//start persisting
if (options.interval && options.interval > 0) {
    this.startPersistInterval(this.persist.bind(this));
}

if (options.expiredInterval) {
    this.startExpiredKeysInterval();
}

Q.all(deferreds).then(
...
```

#### <a name="apidoc.element.node-persist.local_storage.prototype.stopExpiredKeysInterval"></a>[function <span class="apidocSignatureSpan">node-persist.local_storage.prototype.</span>stopExpiredKeysInterval ()](#apidoc.element.node-persist.local_storage.prototype.stopExpiredKeysInterval)
- description and source-code
```javascript
stopExpiredKeysInterval = function () {
    clearInterval(this._expiredKeysInterval);
}
```
- example usage
```shell
...
},

stopPersistInterval: function () {
    clearInterval(this._persistInterval);
},

startExpiredKeysInterval: function () {
    this.stopExpiredKeysInterval();
    this._expiredKeysInterval = setInterval(this.removeExpiredItems.bind(this), this.options.expiredInterval);
    this._expiredKeysInterval.unref();
},

stopExpiredKeysInterval: function () {
    clearInterval(this._expiredKeysInterval);
},
...
```

#### <a name="apidoc.element.node-persist.local_storage.prototype.stopPersistInterval"></a>[function <span class="apidocSignatureSpan">node-persist.local_storage.prototype.</span>stopPersistInterval ()](#apidoc.element.node-persist.local_storage.prototype.stopPersistInterval)
- description and source-code
```javascript
stopPersistInterval = function () {
    clearInterval(this._persistInterval);
}
```
- example usage
```shell
...
    if (path.isAbsolute(dir)) {
        return dir;
    }
    return path.join(process.cwd(), dir);
},

startPersistInterval: function (persistFunction) {
    this.stopPersistInterval();
    this._persistInterval = setInterval(persistFunction || this.persist.bind(this), this.options.interval);
    this._persistInterval.unref();
},

stopPersistInterval: function () {
    clearInterval(this._persistInterval);
},
...
```

#### <a name="apidoc.element.node-persist.local_storage.prototype.stringify"></a>[function <span class="apidocSignatureSpan">node-persist.local_storage.prototype.</span>stringify (obj)](#apidoc.element.node-persist.local_storage.prototype.stringify)
- description and source-code
```javascript
stringify = function (obj) {
    return this.options.stringify(obj);
}
```
- example usage
```shell
...
    this.setOptions(userOptions);
}

var options = this.options;

if (options.logging) {
    this.log("options:");
    this.log(this.stringify(options));
}

this.parseStorageDirSync();
if (options.expiredInterval) {
    this.startExpiredKeysInterval();
}
//start synchronous persisting,
...
```

#### <a name="apidoc.element.node-persist.local_storage.prototype.values"></a>[function <span class="apidocSignatureSpan">node-persist.local_storage.prototype.</span>values ()](#apidoc.element.node-persist.local_storage.prototype.values)
- description and source-code
```javascript
values = function () {
    return this.keys().map(function(k) {
        return this.data[k].value;
    }.bind(this));
}
```
- example usage
```shell
...

## 1.0.0 change logs

Mostly non-backward changes

* 'storage.getItem()' now returns a promise
* 'storage.valuesWithKeyMatch()' no longer accepts a callback
* 'storage.values()' no longer accepts a callback
* 'storage.key()' is gone
* The default 'dir' is now 'process.cwd() + (dir || '.node-persist/storage')', unless you use an absolute path
* added 'storage.get()', alias to 'getItem()'
* added 'storage.set()', alias to 'setItem()'
* added 'storage.del()', 'storage.rm()', as aliases to 'removeItem()'
* Keys, on the file system are base64 encoded with the replacement of the '/'
...
```

#### <a name="apidoc.element.node-persist.local_storage.prototype.valuesWithKeyMatch"></a>[function <span class="apidocSignatureSpan">node-persist.local_storage.prototype.</span>valuesWithKeyMatch (match)](#apidoc.element.node-persist.local_storage.prototype.valuesWithKeyMatch)
- description and source-code
```javascript
valuesWithKeyMatch = function (match) {
    match = match || /.*/;

    var filter = match instanceof RegExp ?
        function(key) {
            return match.test(key);
        } :
        function(key) {
            return key.indexOf(match) !== -1;
        };

    var values = [];
    this.keys().forEach(function(k) {
        if (filter(k)) {
            values.push(this.data[k].value);
        }
    }.bind(this));

    return values;
}
```
- example usage
```shell
...
* added 'forgiveParseErrors' option

## 1.0.0 change logs

Mostly non-backward changes

* 'storage.getItem()' now returns a promise
* 'storage.valuesWithKeyMatch()' no longer accepts a callback
* 'storage.values()' no longer accepts a callback
* 'storage.key()' is gone
* The default 'dir' is now 'process.cwd() + (dir || '.node-persist/storage')', unless you use an absolute path
* added 'storage.get()', alias to 'getItem()'
* added 'storage.set()', alias to 'setItem()'
* added 'storage.del()', 'storage.rm()', as aliases to 'removeItem()'
* Keys, on the file system are base64 encoded with the replacement of the '/'
...
```



# misc
- this document was created with [utility2](https://github.com/kaizhu256/node-utility2)
