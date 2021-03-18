# ESM `defer`

This repository provides an implementation of a `defer` function compatible with
ESM.

This function used to be available in browsers using `Promise.defer`, but is not
anymore. I've found many use-cases where I need to resolve or reject a promise
from outside of its constructor, hence the return of the defer pattern through
this implementation.

## Installation & Usage

### Browser

```javascript
import delay from 'https://github.com/tomashubelbauer/esm-defer/index.js';

const deferrer = defer();

await deferrer.promise;

// elsewhere
deferred.resolve();
deferred.reject();
```

### Node

```bash
git submodule add https://github.com/tomashubelbauer/esm-delay vendor/esm-delay
```

```javascript
import delay from './vendor/esm-delay/index.js';

const deferrer = defer();

await deferrer.promise;

// elsewhere
deferred.resolve();
deferred.reject();
```
