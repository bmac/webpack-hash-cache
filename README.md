# HashCachePlugin

An experimental incremental build plugin for Webpack.

Incremental builds increase the speed of the development workflow by avoiding rebuilding unchanged entries. However, in large projects, the caching process can be expensive. HashCachePlugin uses Rust for resource-intensive caching, which accelerates the caching process.

Built with [napi-rs](https://github.com/napi-rs/napi-rs)!

## Installation

```
yarn add -D webpack-hash-cache
npm install --save-dev webpack-hash-cache
```

## Usage

```js
import { HashCachePlugin } from 'webpack-hash-cache';
```

Add instance to the plugins array in webpack config:
```js
plugins: [
    new HashCachePlugin()
]
```

Currently, you must specify a cache directory, either as an environment variable, CACHE_DIR, or as an option passed to plugin constructor.
