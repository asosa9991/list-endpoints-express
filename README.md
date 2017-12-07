# list-endpoints-express
lists endpoints that are registered in a express app

## Usage

```javascript
const listEndpoints = require('list-endpoints-express')

let app = require('express')();

app.use('/about', someRouter);
app.use(['/help', '/:uriParam/help'], someRouter);
app.use(['/view', '/viewHelp', '/view/help'], someRouter);


console.log(JSON.stringify(listEndpoints(app), null, 2));

```

## Arguments

### `app` - Express `app`

your app instance (`app`).

## license

MIT
