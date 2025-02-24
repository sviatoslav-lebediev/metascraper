# metascraper-media-provider

[![npm](https://img.shields.io/npm/v/metascraper-media-provider.svg?style=flat-square)](https://www.npmjs.com/package/metascraper-media-provider)
[![Dependency Status](https://david-dm.org/microlinkhq/metascraper.svg?path=packages/metascraper-media-provider&style=flat-square)](https://david-dm.org/microlinkhq/metascraper?path=packages/metascraper-media-provider)

> Get specific video provider url (Facebook/Twitter/Vimeo/etc).

## Install

```bash
$ npm install metascraper-media-provider --save
```

## API

### metascraper-media-provider([options])

#### options

##### cacheDir

Type: `string`

It specifies cache based on file system to be used by [youtube-dl](youtube-dl).

##### getProxy

Type: `function`

It will be called to determinate if a proxy should be used for resolving the next request URL.

```js
const getProxy = ({ url, retryCount }) => {
  if (retryCount === 0) return false
  return 'http://user:pwd@proxy:8001'
}
```

##### getAgent

Type: `function`

It receives as input the output from `.getProxy`. The output will be passed to `.gotOpts`.

##### gotOpts

Type: `object`

Any option provided here will passed to [got#options](https://github.com/sindresorhus/got#options).

##### retry

Type: `number`<br>
Default: `5`

The maximum number of retries allowed to perform.

##### timeout

Type: `number`<br>
Default: `30000`

The maximum time allowed to wait until considering the request as timed out.

##### populators

Type: `object`

Each value of the object should be a function that returns required information. 
Function will receive a `raw` data related to the url as a param.
Key names will be added to the result.
For example:

```js
{
  populators: {
     videoQuality(data) {
       ...
       return ...
     }
  }
}
```

## License

**metascraper-media-provider** © [Microlink](https://microlink.io), Released under the [MIT](https://github.com/microlinkhq/metascraper/blob/master/LICENSE.md) License.<br>
Authored and maintained by [Microlink](https://microlink.io) with help from [contributors](https://github.com/microlinkhq/metascraper/contributors).

> [microlink.io](https://microlink.io) · GitHub [@microlink.io](https://github.com/microlinkhq) · Twitter [@microlinkhq](https://twitter.com/microlinkhq)
