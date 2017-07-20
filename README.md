# Minami

A clean, responsive documentation template theme for JSDoc 3.

![Minami Screenshot](http://i.imgur.com/rPCIFqT.png)


## Changes in this fork (GDixon/Minami)

 - Disables sorting of methods in classes [(cb32c8a)](https://github.com/gdixon/minami/commit/cb32c8ada85b8e9ac77bfef91a98e9ef7d0a3e6a)
 - Moves 'namespaces' above 'classes' in nav and patches linkto for namespace methods [(2c4e81)](https://github.com/gdixon/minami/commit/02c4e816785aa5500fca2d787713f9b75fd39fe9)
 - Adds copyright text to the footer element [(62dc618)](https://github.com/gdixon/minami/commit/62dc6184cf38131e9d29640e689e72d51a06531b)
 - Adds favicon.ico link element in head [(b1df1971)](https://github.com/gdixon/minami/commit/b1df1971af0b16cae87c68e2343d389e37e56fc8)
 - Fixes formatting line-height issues for h1 and h2's [(daf9e91)](https://github.com/gdixon/minami/commit/daf9e91ca7ddf5bc5ca486bb26390aab3c9fccd1)  
 - Adds id to the h2 element in header section [(d25fec1)](https://github.com/gdixon/minami/commit/d25fec108b5faf8d6b3eec261852924230bf904c)  
 - Alters margin on H2 element [(e740797)](https://github.com/gdixon/minami/commit/e7407975ebbb00f82c064eb27dd70804da69a362)
 - Adds optional (manual) menu which can be used to define nav items for the readme.md - to use add items to extraNavDetails in config handed to jsdoc [(b49d6ad)](https://github.com/gdixon/minami/commit/b49d6ad2071c1ff0f221a09d76e2df4921eb1f31)

 * to use this version of Minami in your project: follow the install directions in this document, then replace the defined version with "https://github.com/gdixon/minami/tarball/master" in your package.json file.

 ```json
 ...
     "devDependencies": {
        "minami": "https://github.com/gdixon/minami/tarball/master"
     }
 ...
 ```

## Uses

- [the Taffy Database library](http://taffydb.com/)
- [Underscore Template library](http://underscorejs.org/#template)
- [Montserrat](https://fonts.google.com/specimen/Montserrat) & Helvetica Neue


## Install

```bash
$ npm install --save-dev minami
```


## Usage

Clone repository to your designated `jsdoc` template directory, then:

```bash
$ jsdoc entry-file.js -t path/to/minami
```


### Node.js Dependency

In your projects `package.json` file add a generate script:

```json
"script": {
  "generate-docs": "node_modules/.bin/jsdoc --configure .jsdoc.json --verbose"
}
```

In your `.jsdoc.json` file, add a template option.

```json
"opts": {
  "template": "node_modules/minami"
}
```


### Example JSDoc Config

```json
{
    "tags": {
        "allowUnknownTags": true,
        "dictionaries": ["jsdoc"]
    },
    "source": {
        "include": ["lib", "package.json", "README.md"],
        "includePattern": ".js$",
        "excludePattern": "(node_modules/|docs)"
    },
    "plugins": [
        "plugins/markdown"
    ],
    "templates": {
        "cleverLinks": false,
        "monospaceLinks": true,
        "useLongnameInNav": false,
        "showInheritedInNav": true
    },
    "opts": {
        "destination": "./docs/",
        "encoding": "utf8",
        "private": true,
        "recurse": true,
        "template": "./node_modules/minami"
    }
}
```

Specifying a number for useLongnameInNav it will be the max number of path elements to show in nav (starting from Class).


## License

Licensed under the Apache2 license.
