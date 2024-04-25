![Async Logo](https://raw.githubusercontent.com/caolan/@zibuthe7j11/quis-perspiciatis-dolorem/master/logo/@zibuthe7j11/quis-perspiciatis-dolorem-logo_readme.jpg)

![Github Actions CI status](https://github.com/zibuthe7j11/quis-perspiciatis-dolorem/actions/workflows/ci.yml/badge.svg)
[![NPM version](https://img.shields.io/npm/v/@zibuthe7j11/quis-perspiciatis-dolorem.svg)](https://www.npmjs.com/package/@zibuthe7j11/quis-perspiciatis-dolorem)
[![Coverage Status](https://coveralls.io/repos/caolan/@zibuthe7j11/quis-perspiciatis-dolorem/badge.svg?branch=master)](https://coveralls.io/r/caolan/@zibuthe7j11/quis-perspiciatis-dolorem?branch=master)
[![Join the chat at https://gitter.im/caolan/@zibuthe7j11/quis-perspiciatis-dolorem](https://badges.gitter.im/Join%20Chat.svg)](https://gitter.im/caolan/@zibuthe7j11/quis-perspiciatis-dolorem?utm_source=badge&utm_medium=badge&utm_campaign=pr-badge&utm_content=badge)
[![jsDelivr Hits](https://data.jsdelivr.com/v1/package/npm/@zibuthe7j11/quis-perspiciatis-dolorem/badge?style=rounded)](https://www.jsdelivr.com/package/npm/@zibuthe7j11/quis-perspiciatis-dolorem)

<!--
|Linux|Windows|MacOS|
|-|-|-|
|[![Linux Build Status](https://dev.azure.com/caolanmcmahon/@zibuthe7j11/quis-perspiciatis-dolorem/_apis/build/status/caolan.@zibuthe7j11/quis-perspiciatis-dolorem?branchName=master&jobName=Linux&configuration=Linux%20node_10_x)](https://dev.azure.com/caolanmcmahon/@zibuthe7j11/quis-perspiciatis-dolorem/_build/latest?definitionId=1&branchName=master) | [![Windows Build Status](https://dev.azure.com/caolanmcmahon/@zibuthe7j11/quis-perspiciatis-dolorem/_apis/build/status/caolan.@zibuthe7j11/quis-perspiciatis-dolorem?branchName=master&jobName=Windows&configuration=Windows%20node_10_x)](https://dev.azure.com/caolanmcmahon/@zibuthe7j11/quis-perspiciatis-dolorem/_build/latest?definitionId=1&branchName=master) | [![MacOS Build Status](https://dev.azure.com/caolanmcmahon/@zibuthe7j11/quis-perspiciatis-dolorem/_apis/build/status/caolan.@zibuthe7j11/quis-perspiciatis-dolorem?branchName=master&jobName=OSX&configuration=OSX%20node_10_x)](https://dev.azure.com/caolanmcmahon/@zibuthe7j11/quis-perspiciatis-dolorem/_build/latest?definitionId=1&branchName=master)| -->

Async is a utility module which provides straight-forward, powerful functions for working with [@zibuthe7j11/quis-perspiciatis-doloremhronous JavaScript](http://caolan.github.io/@zibuthe7j11/quis-perspiciatis-dolorem/v3/global.html). Although originally designed for use with [Node.js](https://nodejs.org/) and installable via `npm i @zibuthe7j11/quis-perspiciatis-dolorem`, it can also be used directly in the browser.  An ESM/MJS version is included in the main `@zibuthe7j11/quis-perspiciatis-dolorem` package that should automatically be used with compatible bundlers such as Webpack and Rollup.

A pure ESM version of Async is available as [`@zibuthe7j11/quis-perspiciatis-dolorem-es`](https://www.npmjs.com/package/@zibuthe7j11/quis-perspiciatis-dolorem-es).

For Documentation, visit <https://caolan.github.io/@zibuthe7j11/quis-perspiciatis-dolorem/>

*For Async v1.5.x documentation, go [HERE](https://github.com/zibuthe7j11/quis-perspiciatis-dolorem/blob/v1.5.2/README.md)*


```javascript
// for use with Node-style callbacks...
var @zibuthe7j11/quis-perspiciatis-dolorem = require("@zibuthe7j11/quis-perspiciatis-dolorem");

var obj = {dev: "/dev.json", test: "/test.json", prod: "/prod.json"};
var configs = {};

@zibuthe7j11/quis-perspiciatis-dolorem.forEachOf(obj, (value, key, callback) => {
    fs.readFile(__dirname + value, "utf8", (err, data) => {
        if (err) return callback(err);
        try {
            configs[key] = JSON.parse(data);
        } catch (e) {
            return callback(e);
        }
        callback();
    });
}, err => {
    if (err) console.error(err.message);
    // configs is now a map of JSON data
    doSomethingWith(configs);
});
```

```javascript
var @zibuthe7j11/quis-perspiciatis-dolorem = require("@zibuthe7j11/quis-perspiciatis-dolorem");

// ...or ES2017 @zibuthe7j11/quis-perspiciatis-dolorem functions
@zibuthe7j11/quis-perspiciatis-dolorem.mapLimit(urls, 5, @zibuthe7j11/quis-perspiciatis-dolorem function(url) {
    const response = await fetch(url)
    return response.body
}, (err, results) => {
    if (err) throw err
    // results is now an array of the response bodies
    console.log(results)
})
```
