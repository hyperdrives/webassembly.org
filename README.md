webassembly.org
===============

[HyperDrive](https://github.com/mafintosh/hyperdrive) Archive from webassembly.org

![www.webassembly.org](webassembly.org/webassembly.svg)

## Installation

```sh
$ npm install @hyperdrives/webassembly.org
```

or (Github):

```sh
$ npm install hyperdrives/webassembly.org
```

## Usage

You can read the archive directly by simply requiring and initializing
the hyperdrive with the correct public key.

```js
const storage = require.resolve('@hyperdrives/webassembly.org')
const webassembly = require('hyperdrive')(storage, key, opts)
```

or using a convenient wrapper:

```js
const webassembly = require('@hyperdrives/webassembly.org')(key, opts)
```

You can also leverage [random-access-http](
https://github.com/random-access-storage/random-access-http) to read the
archive from the public Github repository.

```js
'use strict'

const hyperdrive = require('hyperdrive')
const http = require('random-access-http')

const prefix = 'https://github.com/hyperdrives/webassembly.org/raw/master/'
const key ='082dc40709a26a382194c14db1e1cee90156d4671300b19282df1cb9bcf1d24c'
const drive = hyperdrive((filename) => http(prefix + filename), key)

webassembly.readdir('/', console.log)
```

## Archive

The webassembly archive represents an offline archive of
http://webassembly.org/

### Public Key

```
082dc40709a26a382194c14db1e1cee90156d4671300b19282df1cb9bcf1d24c
```

## Credits

See http://www.webassembly.org/
