# RC4 TS

## Usage

```js
npm i rc4-ts
# or
yarn add rc4-ts

import RC4 from 'rc4-ts';

const encryptKey = '123456';
const rc4 = new RC4(encryptKey);

const needEncryptData = 'abcde';
const base64Data = window.btoa(window.unescape(window.encodeURIComponent(needEncryptData)));
const encryptResult = rc4.encrypt(base64Data);

const decryptResult = rc4.decrypt(encryptResult);
const finalResult = window.decodeURIComponent(window.escape(window.atob(decryptResult)));
```

## For what

- Encrypt http req entity
- localStorage user infomation
