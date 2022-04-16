# ESM `defer`

This repository provides an implementation of a `defer` function compatible with
ESM.

This function used to be available in browsers using `Promise.defer`, but is not
anymore. I've found many use-cases where I need to resolve or reject a promise
from outside of its constructor, hence the return of the defer pattern through
this implementation.

## Installation & Usage

Use `--experimental-network-imports` with Node for HTTP(S) ESM URL support:

https://nodejs.org/api/esm.html#https-and-http-imports

```javascript
import defer from 'https://tomashubelbauer.github.io/esm-defer/index.js';

const deferrer = defer();

await deferrer.promise;

// elsewhere
deferred.resolve();
deferred.reject();
```
