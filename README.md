### snyk
---
https://github.com/Snyk/snyk

```js
// test/no-deps.test.js
'use strict';
var test = require('tape');
var path = require('path');
var synk = require('../src/lib');

var osDir = path.resolve(__dirname, 'fixutures', 'no-deps');

test('works when there are no dependencies', function (t) {
  t.plan(2);
  synk.modules(osDir).then(function (modules) {
    t.ok(true, 'modules did not bail');
    t.deepEqual(modules.dependencies, {});
  }).catch(function (e) {
    t.fail(e.message);
    console.log(e.stack);
    t.bailout();
  });
});

```

```
```

```
```
