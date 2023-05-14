---
title: Autoimport React using Webpack’s ProvidePlugin
category: Frontend Cheetseat
date: 2021-10-29
tags: ['Webpack']
author: Suresh Kumar Mukhiya
thumbnailText: 'Autoimport React'
---

### Problem:
```js
import React from 'react';
```

It is common to import the above line if you are working with any ReactJS project. Over time, I found it repetitive and cumbersome. I started to see if the import could be done automatically, and guess what? We can by using [ProvidePlugin](https://webpack.js.org/plugins/provide-plugin/) from the webpack.

To get it working, here is what you should do. First, configure your webpack.config.js file as shown below:

### webpack.config.js [Webpack]

```js
var path = require('path')
var webpack = require('webpack')

module.exports = {
  devtool: 'eval',
  entry: [
    'webpack-dev-server/client?http://localhost:3000',
    'webpack/hot/only-dev-server',
    './src/index'
  ],
  output: {
    path: path.join(__dirname, 'dist'),
    filename: 'bundle.js',
    publicPath: '/'
  },
  plugins: [
    new webpack.HotModuleReplacementPlugin(),
    new webpack.ProvidePlugin({
      React: 'react'
    })
  ],
  module: {
    loaders: [
      {
        test: /\.js$/,
        loaders: ['react-hot', 'babel'],
        include: path.join(__dirname, 'src')
      }
    ]
  }
}
```

### jest.setup.js [JEST]

```js
// ProvidePlugin for our tests using a global variable
window.React = require('react')

// other jest setup
```

### tsconfig.json [TypeScript]

If you have TypeScript setup, we want to make it work with the ProvidePlugin.

```js
{
"compilerOptions": {
"allowUmdGlobalAccess": true, // make typescript work with ProvidePlugin
// other compiler options
},

// other ts config
}
```

### .eslintrc.js [ESLINT]

Once React is auto imported on all files, we often warn developers not to import React in each file. We can throw eslint warning or errors by setting up a rule as follows:

```js
module.exports = {
  rules: {
    // Prevent default react imports like import React from 'react'
    // but still allows other named react imports.
    'no-restricted-imports': [
      'error',
      {
        paths: [
          {
            name: 'react',
            importNames: ['default'],
            message: 'React default is automatically imported by webpack.'
          }
        ]
      }
    ]

    // other eslint rules
  }
}
```

These configurations saved a lot of time and became handy over time. I hope someone finds this interesting and helpful. Happy Coding!
