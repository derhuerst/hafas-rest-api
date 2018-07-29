# hafas-rest-api

**Expose a [`hafas-client`](https://github.com/public-transport/hafas-client/tree/0466e570ad3fcdc952dc99da1ef30a084ab79f13) instance as an HTTP REST API.**

[![npm version](https://img.shields.io/npm/v/hafas-rest-api.svg)](https://www.npmjs.com/package/hafas-rest-api)
[![build status](https://api.travis-ci.org/derhuerst/hafas-rest-api.svg?branch=master)](https://travis-ci.org/derhuerst/hafas-rest-api)
![ISC-licensed](https://img.shields.io/github/license/derhuerst/hafas-rest-api.svg)
[![chat on gitter](https://badges.gitter.im/derhuerst.svg)](https://gitter.im/derhuerst)
[![support me on Patreon](https://img.shields.io/badge/support%20me-on%20patreon-fa7664.svg)](https://patreon.com/derhuerst)


## Installing

```shell
npm install hafas-rest-api
```


## Usage

```js
const createHafas = require('hafas-client')
const dbProfile = require('hafas-client/p/db')

const createApi = require('.')

const config = {
	hostname: 'example.org',
	port: 3000,
	name: 'my-hafas-rest-api',
	homepage: 'https://github.com/someone/my-hafas-rest-api'
}

const hafas = createHafas(dbProfile, 'my-hafas-rest-api')
const api = createApi(hafas, config)

api.listen(config.port, (err) => {
	if (err) console.error(err)
})
```


## Contributing

If you have a question or have difficulties using `hafas-rest-api`, please double-check your code and setup first. If you think you have found a bug or want to propose a feature, refer to [the issues page](https://github.com/derhuerst/hafas-rest-api/issues).
