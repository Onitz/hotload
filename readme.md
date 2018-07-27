### How to setup a project like this ###
  npm init 
  nmp i -d webpack                   // webpack project
  npm i -d webpack-dev-server        // needed to run up our local server with hot deploy
  npm i -d webpack-cli               // needed to run webpack from command line
  npm i -d html-webpack-plugin       // needed to load .html instead of .js application


### Steps for running ### 
  npm install 
  npm run dev 
  go to http://localhost:8080
  edit/save index.html
  profit

### PACKAGE.JSON ###
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

### WEBPACK.CONFIG.JS ###
  let HtmlWebpackPlugin = require('html-webpack-plugin');
  module.exports = {
    entry: [],
    output: {},
    mode: "development",
    plugins: [ new HtmlWebpackPlugin({template:"./index.html"})]
  };