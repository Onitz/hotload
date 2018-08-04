### Steps for running ### 
  1. `npm install`
  2. `npm run dev` 
  3. Go to http://localhost:8080
  4. Edit/save index.html
  5. Profit!

### package.json ###
```json
  {
    "name": "hotload",
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

### How to setup a project like this ###
Command                         | Explanation
------------------------------- | --------------------------------------------------
`npm init`                      | Setup an npm project
`nmp i -D webpack`              | Add webpack
`npm i -D webpack-dev-server`   | Needed to run up our local server with hot deploy
`npm i -D webpack-cli`          | Needed to run webpack from command line
`npm i -D html-webpack-plugin`  | Needed to load .html instead of .js application

### ..Alternatively ### 
You can use /fancy for a barebones project with some more features (sass compilation, minify dev/prod mode)