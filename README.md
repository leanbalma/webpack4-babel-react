# Testing Webpack 4 + Babel + React

# Webpack

Webpack [main concepts](https://webpack.js.org/concepts/).

## Webpack 4 with no configuration file

By default, Webpack 4 doesn't need a configuration file. It will use `./src/index.js` as the entry point and will put the bundle in `./dist/main.js`.
Also, we can specify a `mode` to use optimizations out of the box:
- `development`: Sets `process.env.NODE_ENV` to `development`. Enables `NamedChunksPlugin` and `NamedModulesPlugin`.
- `production`: Sets `process.env.NODE_ENV` to `production`. Enables `FlagDependencyUsagePlugin`, `FlagIncludedChunksPlugin`, [`ModuleConcatenationPlugin`](https://webpack.js.org/plugins/module-concatenation-plugin/), [`NoEmitOnErrorsPlugin`](https://webpack.js.org/configuration/optimization/#optimizationnoemitonerrors), `OccurrenceOrderPlugin`, [`SideEffectsFlagPlugin`](https://webpack.js.org/guides/tree-shaking/) and [`TerserPlugin`](https://webpack.js.org/plugins/terser-webpack-plugin/).

Go to the `simple-configuration` branch and run `npm run dev` and `npm run build` to see the differences in `./dist/main.js`.

## References
- https://www.valentinog.com/blog/webpack/
- https://webpack.js.org/
