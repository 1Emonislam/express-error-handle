# express-error-handle

#### A graceful error handle for Express applications. This also patches a DOS exploit where users can manually trigger bad request errors that shut down your app.

# Installation

npm i --save express-error-handle

# Express express-error-handle

```
const express = require('express');
const {errorLog,errorHandlerNotify} = require("express-error-handle")
const app = express()
const port = process.env.PORT || 5000;

app.get('/a-typical-route',async function(req, res, next) {
try{

//your code here

}
catch(error){
next(error)
}

});


app.listen(port, () => {
console.log(`Example app listening on port ${port}`)
})

//handling error using at the end of last routes
app.use(errorLog);
app.use(errorHandlerNotify);
```

## Supported environment variables

### create root path .env file and then put here

### open project folder and create

` touch .env`

### only use developemnt purpose

```
NODE_ENV=development
```

### production serve using applications

### only use production purpose

```
NODE_ENV=production
```

# express-error-handle
