###diffieHellman.generateKeys([encoding])

Generates private and public Diffie-Hellman key values, and returns
the public key in the specified `encoding`. This key should be
transferred to the other party. Encoding can be `'latin1'`, `'hex'`,
or `'base64'`. If `encoding` is provided a string is returned; otherwise a
[`Buffer`][] is returned.

