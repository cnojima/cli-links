# term-link
Parses text for HTTP/S protocol links and ANSI escapes them to make them clickable in stdout output.

Simple usage:

const termLink = require('term-link');

```javascript
// decorate console.log
const log = console.log;
console.log = () => {
  [ ...arguments ] = arguments.forEach(a => {
    return termLink(a);
  });
  log().apply(arguments);
};
```
