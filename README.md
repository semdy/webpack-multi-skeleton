# webpack 多页面骨架
![building](https://www.travis-ci.org/CavinHuang/webpack-multi-skeleton.svg?branch=master "build status")
---
>config目录下都是webpack相关配置
包含开发环境配置、打包配置、jsLint配置

>在app html下，增加html后在js下增加相应名字的js，在config/htmlEntry添加相应的html名字，不用带后缀
lib下可以放置框架文件，如jquery等

## Build Setup

``` bash
# install dependencies
$ npm install # Or yarn install*[see note below]

# serve with hot reload at localhost:3000
$ npm run dev

# build for production and launch server
$ npm run build
$ npm start

```
## 更新(18/1/11)
- 去除原先的手动添加模块的配置
- 添加自动注入模块
- 调整目录结构
  - static 调整为公共静态资源
  - libs 调整为第三方插件静态资源

## 完整的目录结构如下：
```

├─app
│  ├─libs
│  │      common.js
│  │      test.css
│  │      
│  ├─static
│  │  ├─css
│  │  ├─img
│  │  │      1.jpg
│  │  │      
│  │  └─js
│  │      └─test
│  │              index.js
│  │              
│  └─templates
│      ├─test
│      │  │  index.js
│      │  │  
│      │  ├─css
│      │  │      index.css
│      │  │      
│      │  └─html
│      │          index.pug
│      │          
│      └─test0
│          │  index.js
│          │  
│          ├─css
│          │      index.css
│          │      
│          └─html
│                  index.pug
│                  
├─config
│      config.js
│      webpack.config.base.js
│      webpack.config.dev.js
│      webpack.config.lint.js
│      webpack.config.prod.js
│      
├─  .babelrc
├─  .eslintrc.js
├─  .gitignore
├─  .travis.yml
├─  package-lock.json
├─  package.json
├─  postcss.config.js
├─  README.md
├─  webpack.config.js
├─  yarn.lock
```
