###diffieHellman.setPublicKey(public_key[, encoding])

Sets the Diffie-Hellman public key. If the `encoding` argument is provided
and is either `'latin1'`, `'hex'` or `'base64'`, `public_key` is expected
to be a string. If no `encoding` is provided, `public_key` is expected
to be a [`Buffer`][].

