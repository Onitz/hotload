### Steps for running ### 
  1. `npm install`
  2. `npm run dev` 
  3. Go to http://localhost:8080
  4. Edit/save index.html
  5. Profit!

### How to setup a project like this ###
Command                       | Explanation
----------------------------- | --------------------------------------------------
`npm init`                    | Init npm
nmp i -d webpack              | Init webpack
npm i -d webpack-dev-server   | Needed to run up our local server with hot deploy
npm i -d webpack-cli          | Needed to run webpack from command line
npm i -d html-webpack-plugin  | Needed to load .html instead of .js application

### package.json ###
```json
  {
    "name": "hotload",
    "version": "1.0.0",
    "scripts": {
      "dev": "webpack-dev-server"
    },
    "devDependencies": {
      "webpack": "^4.15.1",
      "webpack-cli": "^3.0.8",
      "html-webpack-plugin": "^3.2.0",
      "webpack-dev-server": "^3.1.4"
    }
  }
```

### webpack.config.js ###
```javascript
  let HtmlWebpackPlugin = require('html-webpack-plugin');
  module.exports = {
    entry: [],
    output: {},
    mode: "development",
    plugins: [ new HtmlWebpackPlugin({template:"./index.html"})]
  };
```