# Webpack 5.x-2-5-Optimization

### `optimization.moduleIds` [:book:](https://webpack.js.org/configuration/optimization/#optimizationmoduleids)

### `optimization.chunkIds` [:book:](https://webpack.js.org/configuration/optimization/#optimizationchunkids)

`boolean = false string: 'natural' | 'named' | 'size' | 'total-size' | 'deterministic'`

chunkIds 演算法在 Webpck 5 版本開放給使用者設定 [:book:](https://webpack.docschina.org/blog/2020-10-10-webpack-5-release/)。

在 mode develope 下，預設是 'named' 演算法
在 mode product 下，預設是 'deterministic' 演算法，產生的固定的短 id 為命名。如果需求可調 id 長度(webpack.ids.DeterministicChunkIdsPlugin)

目前測得 deterministic 演算法會根據，引用模組 + 模組檔案名稱變動，同時不會因為檔案大小而改變。
