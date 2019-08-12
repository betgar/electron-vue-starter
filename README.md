# electron-vue-starter

> An electron project powered by electron-vue

## Build Setup

``` bash
# install dependencies
npm install

# serve with hot reload at localhost:9080
npm run dev

# build electron application for production
npm run build

# run unit & end-to-end tests
npm test


# lint all JS/Vue component files in `src/`
npm run lint

```

## update dependencies
> 更新了项目的依赖信息

- electron

  > electron v5.x

  ```javascript
  // electron v5.x的break change
  mainWindow = new BrowserWindow({
    height: 563,
    useContentSize: true,
    width: 1000,
    webPreferences: {
      // @see https://electronjs.org/releases/stable?version=5&page=2#release-notes-for-v500
      // @see issues https://github.com/electron/electron/pull/16235
      // electron v5.x 修改配置默认nodeIntegration: false
      // WARNNING: 当设置为false时不能在renderer进程使用require
      nodeIntegration: true
    }
  })
  ```

  
## learn source
- [electron-vue开发实战](https://molunerfinn.com/tags/Electron-vue/)
- [electron-vue中文文档](https://simulatedgreg.gitbooks.io/electron-vue/content/cn/)

## download dependencies failed resolution
- chrome driver

  > https://www.npmjs.com/package/chromedriver

  ```bash
  # 安装指定地址
  npm install chromedriver --chromedriver_cdnurl=https://npm.taobao.org/mirrors/chromedriver

  # 直接设置`.npmrc`变量
  npm config set chromedriver_cdnurl "https://npm.taobao.org/mirrors/chromedriver"
  ```

  ```bash
  # 添加环境变量 CHROMEDRIVER_CDNURL
  CHROMEDRIVER_CDNURL=https://npm.taobao.org/mirrors/chromedriver npm install chromedriver
  ```

- electron

  > https://npm.taobao.org/mirrors/electron/

  ```bash
  npm config set electron_mirror https://npm.taobao.org/mirrors/electron/

  # 或者
  ELECTRON_MIRROR="https://npm.taobao.org/mirrors/electron/" npm i electron
  ```

- phantomjs

  > https://github.com/Medium/phantomjs

  ```bash
  npm install phantomjs-prebuilt --phantomjs_cdnurl=https://npm.taobao.org/mirrors/phantomjs/

  # .npmrc 方式
  npm config set phantomjs_cdnurl https://npm.taobao.org/mirrors/phantomjs/

  # PATH
  PHANTOMJS_CDNURL=https://npm.taobao.org/mirrors/phantomjs/
  ```

- node-sass

  > https://github.com/sass/node-sass

  ```bash
  npm install -g mirror-config-china --registry=http://registry.npm.taobao.org
  # .npmrc
  npm config set sass_binary_site https://npm.taobao.org/mirrors/node-sass/
  ```

- [electron-vue的正确build姿势](https://segmentfault.com/a/1190000013473230)



---

This project was generated with [electron-vue](https://github.com/SimulatedGREG/electron-vue)@[8fae476](https://github.com/SimulatedGREG/electron-vue/tree/8fae4763e9d225d3691b627e83b9e09b56f6c935) using [vue-cli](https://github.com/vuejs/vue-cli). Documentation about the original structure can be found [here](https://simulatedgreg.gitbooks.io/electron-vue/content/index.html).
