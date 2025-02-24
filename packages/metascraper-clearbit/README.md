# metascraper-clearbit

[![npm](https://img.shields.io/npm/v/metascraper-clearbit.svg?style=flat-square)](https://www.npmjs.com/package/metascraper-clearbit)
[![Dependency Status](https://david-dm.org/microlinkhq/metascraper.svg?path=packages/metascraper-clearbit&style=flat-square)](https://david-dm.org/microlinkhq/metascraper?path=packages/metascraper-clearbit)

> Metascraper integration with Clearbit Logo API.

## Install

```bash
$ npm install metascraper-clearbit --save
```

## API

### metascraper-clearbit([options])

#### options

##### gotOpts

Any option provided here will passed to [got#options](https://github.com/sindresorhus/got#options).

In addition, these options are set by default:

```json
{
  "responseType": "json"
}
```

##### keyvOpts

Type: `object`

Any option provided here will passed to [@keyvhq/memoize#options](https://github.com/microlinkhq/keyv/tree/master/packages/memoize#keyvoptions).

#### logoOpts

Any option provided here will passed to [Clearbit Logo API](https://clearbit.com/docs#logo-api).

## License

**metascraper-clearbit** © [Microlink](https://microlink.io), Released under the [MIT](https://github.com/microlinkhq/metascraper/blob/master/LICENSE.md) License.<br>
Authored and maintained by [Microlink](https://microlink.io) with help from [contributors](https://github.com/microlinkhq/metascraper/contributors).

> [microlink.io](https://microlink.io) · GitHub [@microlink.io](https://github.com/microlinkhq) · Twitter [@microlinkhq](https://twitter.com/microlinkhq)
