语言 : [英文](./README.md)| 中文
# web-layout-debugger
使用网页布局调试插件可以直观的看到网页布局，是否存在布局bug,布局是否规范,margin和padding间距是否规范,文本对齐是否规范，按钮热区大小是否规范，可用在`vue`,`react`和`electron`等各种框架中
#网页布局调试
![npm](https://raw.githubusercontent.com/hero8080/web_layout_debugger/main/npm.png)
![git](https://raw.githubusercontent.com/hero8080/web_layout_debugger/main/git.png)

###安装
`npm i web-layout-debugger --save`

#在vite中使用
###修改 `min.js`文件
```js
import { createApp } from 'vue'
//vue
import App from './App.vue'

//web-layout-debugger
import {loadLayoutDebugger} from 'web-layout-debugger'

//开发环境启动web布局调试
if(import.meta.env.DEV){
    loadLayoutDebugger()
}

createApp(App).mount('#app');
```

#在webpack中使用
###修改 `min.js`文件
```js
import Vue from 'vue'
import App from './App'

import {loadLayoutDebugger} from 'web-layout-debugger'

//开发环境启动web布局调试
if(process.env.NODE_ENV=='development'){
  loadLayoutDebugger()
}

new Vue({
  render: (h) => h(App)
}).$mount('#app')
```
#在react中使用
###修改 `index.js`文件
```js
import React from 'react';
import ReactDOM from 'react-dom';
import './index.css';
import App from './App';

import {loadLayoutDebugger} from "web-layout-debugger";

//开发环境启动web布局调试
if(process.env.NODE_ENV=='development'){
    loadLayoutDebugger()
}

ReactDOM.render(
    <App />,
    document.getElementById('root')
);
```
