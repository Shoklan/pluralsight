# Single Page Applications with Vue.js
## Bill Stavroulakis

# Environment Setup - Build Process
- Vue.js can be a small component to manipulate the DOM.
- As well as modern single page web pages.
- This is not a fundamentals course.
- A project should include:
  1. A License File.
  2. A README.MD file.
  3. An index.html file.
- There are three favored ways to handle package management:
  1. bower
  2. jspm
  3. npm
- Once installed, you can run `npm init -y` to start working and configure settings.
- This will create a *package.json* file which is where all the dependencies will be contained.
- Two keys to pay attention to are `dependencies` and `devDependencies` which control what is needed in dev and prod respectively.
- There are a few ways to get Vue.js into our project.
  1. With a CDN include.
  2. [Recommended] Install with npm.
- The argument `--save` creates a `node_modules/vue/dist` with all the files.
- It will also add it as a dependency in the *package.json* file.
- There are also many choices of web servers but we're going to use *express.js*.
- You will install it with `npm install express --save`
- Then, create a file called *server.js*.
```js
const express = require('express');
const app = express();

app.get('*', (req, res) =>{
  res.write('Maor Turtles');
  res.end();
});

const port = process.env.PORT || 3000;
app.listen( port, () => {
  console.log('turtles!')
})
```
- We'll want to serve the file system node module to serve the page itself.
```js
const fs = requires('fs');
const path = requires('path');

const indexHTML = (() => {
  return fs.readFileSync( path.resolve( __dirname, "./index.html"), "utf-8");
})();

//..
res.write(indexHTML)

```
- No, instead of remembering the paths of our scripts, we'll create a shortcut.
- We'll add `"start": "node server"` to the *package.json* file.
- The thing with modules is that they are not supported on all browsers.
- The two most common polypher is *browersify* and *webpack*.
- We'll be using *webpack*.
- We'll need to create a folder called *build* with a file in it called `webpack.base.config.js`
- Then, we'll install it with `npm install webpack --save-dev`.
- Now we'll need to include all the modules needed for webpack.
- Webpack modules start with entry points.
![ Build Process](images/build-process.png)
```js
const path = require('path');

const config = {
  entry: {
    app: path.resolve(__dirname, "../src/client-entry.js")
  },
  output: {
    path: path.resolve(__dirname, "../dist"),
    publicPath: "/",
    filename: "assets/js/[name].js"
  }
};

module.exports = config;
```
![Compile webpack](images/webpack-compile.png)
- Now we'll add vue to the app.js file.
```js
import Vue from "vue";

const app = new Vue({
  data: {
    hello: 'hey turtles'
  }
});

export { app };
```
- Once it's loaded, you can then mount it in the *client-entry.js* file.
- Don't forget to mount it and add the appropriate attribute.
- Starting and stopping the server is annoying so we're going to install two modules to assist:
  * `npm install webpack-dev-middleware --save-dev`
  * `npm install webpack-hot-middleware --save-dev`
- This will allow them to be stored in memory and updated when changes are detected.
- **Linting** enforces coding standards on events - usually saving.


# Single File Components

# Routing

# API Communication

# State Management

# Server-side Rendering

# Testing

# Deploying

# Reference:
- [Project Github Page](https://github.com/bstavroulakis/vue-spa)
- [EditorConfig](https://editorconfig.org)

# Research:
