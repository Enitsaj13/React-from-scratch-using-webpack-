# React-From-Scratch-Using-Webpack with Dark Mode theme❕❕

You can try it by yourself using the tutorial below or just clone it in this repository for convenience.❕❕

Why webpack instead of CRA or just simply use the Create React App ? 😎

Webpack is a fast and lightweight module bundler ✔

Webpack reduces the file size of standard CRA ✔

CRA is 260+ Mb vs 80+ Mb (without git) using webpack ✔

Webpack dev-server is smooth and compared to the server of CRA. ✔

Webpack lessen the unnecessary file in your react-app ✔

Here are the step by step tutorial on how to setup and configure your react app using webpack. ❕❕❕

🔸 Step 1: Create a folder and initialize the npm and open it using any IDE like vs code

▫ mkdir react-folder
▫ npm init - y
▫ code . ( to open the folder instantly)

🔸 Step 2: Go to the folder and install the react and react-dom

▫ cd react-folder
▫ npm i react react-dom

🔸 Step 3: Install all these packages of webpack and babel

▫ npm i -D @babel/core @babel/cli @babel/plugin-transform-runtime @babel/preset-env @babel/preset-react @babel/runtime babel-eslint babel-loader webpack webpack-cli webpack-dev-server

🔸 Step 4: Create .babelrc file and add this line
{
"presets": ["@babel/preset-env", "@babel/preset-react"]
"plugins": ["@babel/plugin-transform-runtime"]
}

🔸 Step 5: Create a webpack.config.js file and add this line

const path = require("path");

module.exports = {
mode: "development",
entry: "./index.js",
output: {
path: path.resolve(\_\_dirname, "public"),
filename: "main.js",
},

target: "web",
devServer: {
port: "3000",
static: ["./public"],
open: true,
hot: true,
liveReload: true,
},
resolve: {
extensions: [".js", ".jsx", ".json", ".ts"],
},
module: {
rules: [
{
test: /\.(js|jsx)$/,
exclude: /node_modules/,
use: "babel-loader",
},
],
},
};

🔸 Step 6: Create public folder (inside your react-folder) and create index.html file

▫ mkdir public
▫ touch public/index.html

🔸 Step 7: Create src folder (inside your react-folder) and create index.js file

▫ mkdir src
▫ touch src/index.js

🔸 Step 8: Open package.json file and add this line

"scripts": {
"start": "webpack-dev-server .",
"build": "Webpack ."
}

Find the line "main" and change it to
"main": "./src/index.js"

🔸 Step 9: Test your react app by simple typing

▫ npm run build
▫ npx serve build
▫ npm start

That's all and see if it's working. 🙏
This example is intended for people who want to create
a react app from scratch using webpack and lessen the file size of it.

I hope you learn something new in this step-by-step tutorial. 🤍

Thank you very much! 🤍
