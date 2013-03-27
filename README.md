console-ten
===========

Console-TEN is a simple console Timestamp Extension for Node.js

It prepends a timestamp and log type for console.log type functions (error, warn, info, log)
Tt also allows disabling some logging by setting a log level

Install
-------
```bash
> npm install console-ten
```

Usage
-----
```javascript
require('console-ten').init(console);
console.log("Hello Node!", {'i':'love','json':'!'});
```

Example Output
--------------
```bash
> 2013-01-01T00:00:00.000Z [LOG] :  Hello Node! { i: 'love', json: '!' }
```

Log Levels
----------
Console-TEN will default to show all logs, you can limit which logs are shown by passing in a level in the init method:

```javascript
var consoleTEN = require('console-ten');
consoleTEN.init(console, consoleTEN.LEVELS.LOG);
console.log("This will be sent to the console.");
console.info("But this will not be shown.");
```

Here are the log levels currently defined:

```javascript
LEVELS = {
    'ERROR':1,
    'WARNING':2,
    'LOG':3,
    'INFO':4,
    'DEBUG':5,
    'ALL':6,
};
```


