###Event: 'listening'

* `address` {Object}

Similar to the `cluster.on('listening')` event, but specific to this worker.

```js
cluster.fork().on('listening', (address) => {
  // Worker is listening
});
```

It is not emitted in the worker.

