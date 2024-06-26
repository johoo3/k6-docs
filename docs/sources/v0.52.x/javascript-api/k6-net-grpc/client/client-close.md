---
title: 'Client.close()'
description: 'Close the connection to the gRPC service. Tear down all underlying connections.'
weight: 40
aliases:
  - ../../k6-experimental/grpc/client/client-close/ # docs/k6/<K6_VERSION>/javascript-api/k6-experimental/grpc/client/client-close/
---

# Client.close()

Close the connection to the gRPC service. Tear down all underlying connections.

### Examples

<div class="code-group" data-props='{"labels": ["Simple example"], "lineNumbers": [true]}'>

```javascript
import grpc from 'k6/net/grpc';

const client = new grpc.Client();
client.load(['definitions'], 'hello.proto');

export default () => {
  client.connect('localhost:8080');
  client.close();
};
```

</div>