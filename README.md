[![NPM version](https://img.shields.io/npm/v/gatsby-plugin-postcss.svg)](https://www.npmjs.org/package/gatsby-plugin-postcss)
[![Travis build status](https://travis-ci.org/mdreizin/gatsby-plugin-postcss.svg?branch=master)](https://travis-ci.org/mdreizin/gatsby-plugin-postcss)
[![AppVeyor build status](https://ci.appveyor.com/api/projects/status/yhylaug8h5lrddo9/branch/master?svg=true)](https://ci.appveyor.com/project/mdreizin/gatsby-plugin-postcss/branch/master)
[![Maintainability](https://api.codeclimate.com/v1/badges/9961f28042daadd06dad/maintainability)](https://codeclimate.com/github/mdreizin/gatsby-plugin-postcss/maintainability)
[![Test Coverage](https://api.codeclimate.com/v1/badges/9961f28042daadd06dad/test_coverage)](https://codeclimate.com/github/mdreizin/gatsby-plugin-postcss/test_coverage)
[![Dependency Status](https://img.shields.io/david/mdreizin/gatsby-plugin-postcss.svg)](https://david-dm.org/mdreizin/gatsby-plugin-postcss)
[![Development Dependency Status](https://img.shields.io/david/dev/mdreizin/gatsby-plugin-postcss.svg)](https://david-dm.org/mdreizin/gatsby-plugin-postcss#info=devDependencies)

# gatsby-plugin-postcss

> Gatsby plugin to handle PostCSS.

## Install

`yarn add gatsby-plugin-postcss`

or

`npm install --save gatsby-plugin-postcss`

## How to Use

`gatsby-config.js`

```js
module.exports = {
  plugins: ['gatsby-plugin-postcss']
};
```

This plugin uses [`postcss-loader`](https://github.com/postcss/postcss-loader) with its default options that means you can use your own `postcss.config.js`:

`postcss.config.js`

```js
const postcssPresetEnv = require('postcss-preset-env');

module.exports = () => ({
  plugins: [
    postcssPresetEnv({
      stage: 0
    })
  ]
});
```

## Options

You can use any allowed [`postcss-loader`](https://github.com/postcss/postcss-loader#options) options using `postcss` property:

`gatsby-config.js`

```js
module.exports = {
  plugins: [
    {
      resolve: 'gatsby-plugin-postcss',
      options: {
        postcss: {
          plugins: () => [require('postcss-preset-env')({ stage: 0 })]
        }
      }
    }
  ]
};
```
