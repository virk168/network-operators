# Network Operators

A package for query network operators in Cambodia.

[![test](https://github.com/seanghay/network-operators/actions/workflows/test.yml/badge.svg)](https://github.com/seanghay/network-operators/actions/workflows/test.yml)

## Install

```
npm install network-operators
```

## Usage

```js
// ESM
import { prefixInfo, phoneNumberInfo, networkOperators, parsePhoneNumber } from 'network-operators'

// CJS
const { prefixInfo, phoneNumberInfo, networkOperators, parsePhoneNumber } = require('network-operators')

console.log(prefixInfo('012'))
// { operator: 'Cellcard', length: [ 6, 7 ] }

console.log(phoneNumberInfo('012123123'))
// {
//   operator: 'Cellcard',
//   length: [ 6, 7 ],
//   prefix: '012',
//   suffix: '123123',
//   number: '012123123'
// }

console.log(networkOperators())
// [
//   'Cellcard', 'CooTel',
//   'Kingtel',  'Seatel',
//   'Metfone',  'qb',
//   'Smart'
// ]

console.log(parsePhoneNumber('010123123'))
// { prefix: '010', suffix: '123123', number: '010123123' }
```


## License

Apache-2.0