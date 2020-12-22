# Evaluate A News Article with Natural Language Processing

The goal of this project is:
- Setting up Webpack
- Sass styles
- Webpack Loaders and Plugins
- Creating layouts and page design
- Service workers
- Use APIs and create requests to external urls

This project is a web tool that allows users to run Natural Language Processing (NLP) on articles or blogs found on other websites. Using an exciting api called meaningcloud, we can build a simple web interface to interact with their NLP system.

> Natural language processing (NLP) is a subfield of computer science, information engineering, and artificial intelligence
concerned with the interactions between computers and human (natural) languages, in particular how to program computers to
process and analyze large amounts of natural language data.

## Getting started

Make sure Node and NPM are installed from the terminal.
- `node -v`
- `npm -v`

Clone the repo
- `git clone <repo>`

Remember that once you clone, you will still need to install everything:

`cd` into your new folder and run:
- `npm install`

Install loaders and plugins
- `npm i -D @babel/core @babel/preset-env babel-loader`
- `npm i -D style-loader node-sass css-loader sass-loader`
- `npm i -D clean-webpack-plugin`
- `npm i -D html-webpack-plugin`
- `npm i -D mini-css-extract-plugin`
- `npm i -D optimize-css-assets-webpack-plugin terser-webpack-plugin`

## Setting up the API

### Signup for an API key
Signup meaningcloud.com for a license key to start using the API.

### Environment Variables
 * Use npm to install the dotenv package `npm install dotenv`.

 * Create a new `.env` file in the root of your project

 * Fill the `.env` file with your API key like this:

`API_KEY=**************************`

 * Add this code to the very top of your server/index.js file:
    `const dotenv = require('dotenv')`
    `dotenv.config()`

 * Reference variables you created in the `.env` file by putting `process.env` in front of the variable name in the server/index.js file, an example might look like this:
`console.log(`Your API key is ${process.env.API_KEY}`)`

This means that our updated API credential settings will look like this:

`const API_KEY = process.env.API_KEY`

### Using the API
We use the [Sentiment Analysis API](https://www.meaningcloud.com/developer/sentiment-analysis) for this project.

## Start the project

Command  | Action
------------- | -------------
`npm run build-prod`  |   Build project
`npm start`  |   Run project

http://localhost:8081