##Event: 'exit'
* `worker` {cluster.Worker}
* `code` {Number} the exit code, if it exited normally.
* `signal` {String} the name of the signal (e.g. `'SIGHUP'`) that caused
  the process to be killed.

When any of the workers die the cluster module will emit the `'exit'` event.

This can be used to restart the worker by calling `.fork()` again.

```js
cluster.on('exit', (worker, code, signal) => {
  console.log('worker %d died (%s). restarting...',
    worker.process.pid, signal || code);
  cluster.fork();
});
```

See [child_process event: 'exit'][].

