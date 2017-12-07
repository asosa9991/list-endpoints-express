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
someRouter consists of routes to handle POST & GET using 'v1' context.

## Output

```JSON
[
  {
    "method": "POST",
    "paths": [
      "/about/v1",
      "/help/v1",
      "/:uriParam/help/v1",
      "/view/v1",
      "/viewHelp/v1",
      "/view/help/v1"
    ]
  },
  {
    "method": "GET",
    "paths": [
    "/about/v1",
    "/help/v1",
    "/:uriParam/help/v1",
    "/view/v1",
    "/viewHelp/v1",
    "/view/help/v1"
    ]
    }
  ]
  ```

## license

MIT
