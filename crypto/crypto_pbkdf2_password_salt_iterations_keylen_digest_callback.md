###crypto.pbkdf2(password, salt, iterations, keylen, digest, callback)

Provides an asynchronous Password-Based Key Derivation Function 2 (PBKDF2)
implementation. A selected HMAC digest algorithm specified by `digest` is
applied to derive a key of the requested byte length (`keylen`) from the
`password`, `salt` and `iterations`.

The supplied `callback` function is called with two arguments: `err` and
`derivedKey`. If an error occurs, `err` will be set; otherwise `err` will be
null. The successfully generated `derivedKey` will be passed as a [`Buffer`][].

The `iterations` argument must be a number set as high as possible. The
higher the number of iterations, the more secure the derived key will be,
but will take a longer amount of time to complete.

The `salt` should also be as unique as possible. It is recommended that the
salts are random and their lengths are greater than 16 bytes. See
[NIST SP 800-132][] for details.

Example:

```js
const crypto = require('crypto');
crypto.pbkdf2('secret', 'salt', 100000, 512, 'sha512', (err, key) => {
  if (err) throw err;
  console.log(key.toString('hex'));  // '3745e48...aa39b34'
});
```

An array of supported digest functions can be retrieved using
[`crypto.getHashes()`][].

