# How to create an Arini Project on Ubuntu with npm.

## First, make a directory for your project.

`mkdir project`{{execute}}

## Now, enter that directory

`cd project`{{execute}}

## Once you're in there, run npm init and install arini

`npm init && npm i --save arini`{{execute}}

Follow the directions from npm to initialize your Node.JS prackage.

Now try the code below:

```
  const arini = require('arini');
  arini.parse(`return include "./program.ari";`);
  module.exports = arini.eval();
```

