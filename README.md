# service-client
Client code for service discovery and invocation

## Example

```javascript
var serviceClient = require('../index');

var config = {
  host: 'my.consul.com', // e.g 172.x.x.x:8500
  serviceName: 'users',
  endpoint: 'users',
  method: 'POST',
  body: {
    username: 'foo',
    password: 'bar'
  }
};

// Posts a new user to the users' service /users route.
serviceClient(config)
  .then(console.log)
  .catch(console.log);
```
