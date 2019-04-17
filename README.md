# element-samples

> element-ui 各种组件使用的小例子，希望可以依此熟悉element-ui 组件的基本使用

### Build Setup

``` bash
# install dependencies
npm install

# serve with hot reload at localhost:8080
npm run dev

# build for production with minification
npm run build

# build for production and view the bundle analyzer report
npm run build --report
```

### 1.使用vue脚手架创建webpack项目

```
vue init webpack
```

### 2.添加element

```
npm i element-ui -S
```

### 3.element-ui搭建

#### 3.1完整引入

在main.js中修改如下：

```
import Vue from 'vue'
import App from './App'
import router from './router'

import ElementUI from 'element-ui';//+
import 'element-ui/lib/theme-chalk/index.css';//+

Vue.use(ElementUI);//+

Vue.config.productionTip = false

/* eslint-disable no-new */
new Vue({
  el: '#app',
  router,
  components: { App },
  template: '<App/>'
})

```

#### 3.2按需引入

##### 3.2.1安装

```
npm install babel-plugin-component -D
```

##### 3.2.2配置

```
{
  "presets": [["es2015", { "modules": false }]],
  "plugins": [
    [
      "component",
      {
        "libraryName": "element-ui",
        "styleLibraryName": "theme-chalk"
      }
    ]
  ]
}
```

