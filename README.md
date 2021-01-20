# Multimirror Js

This library represents a custom connector to socket-io

## Usage

1st: Use multimirror connector in your bootstrap.js

```js
import Echo from "laravel-echo";

import Multimirror from "multimirror-js"

window.io = require("socket.io-client");
window.Echo = new Echo({
    broadcaster: Multimirror,
    host: 'http://socket.kamal.guru',
    app_key: process.env.MIX_MULTIMIRROR_APP_KEY
});
```

```js
Echo.private('test-channel')
.listen('TestEvent', msg => {
    console.log('new private event');
})
```