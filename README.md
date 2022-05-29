Language : 🇺🇸 | [🇨🇳](./README.zh-CN.md)
# web-layout-debugger
Using the ` web-layout-debugger` plug-in, you can visually see the web page layout, whether there are layout bugs, whether the layout is standardized, whether the margin and padding spacing are standardized, whether the text alignment is standardized, and whether the button hot zone size is standardized. It can be used in various frameworks such as `Vue` and `react` and `electron`
## web-layout-debugger
![npm](https://raw.githubusercontent.com/hero8080/web_layout_debugger/main/npm.png)
![git](https://raw.githubusercontent.com/hero8080/web_layout_debugger/main/git.png)

##Install
`npm i web-layout-debugger --save`

##Use in vite

####Edit `min.js`file
```js
import { createApp } from 'vue'
//vue
import App from './App.vue'

//web-layout-debugger
import {loadLayoutDebugger} from 'web-layout-debugger'

//Start web-layout-debugger in development environment
if(import.meta.env.DEV){
    loadLayoutDebugger()
}

createApp(App).mount('#app');
```

##Use in webpack

####Edit `min.js`file
```js
import Vue from 'vue'
import App from './App'

import {loadLayoutDebugger} from 'web-layout-debugger'

//Start web-layout-debugger in development environment
if(process.env.NODE_ENV=='development'){
  loadLayoutDebugger()
}

new Vue({
  render: (h) => h(App)
}).$mount('#app')
```
##Use in react

####Edit `index.js`file
```js
import React from 'react';
import ReactDOM from 'react-dom';
import './index.css';
import App from './App';

import {loadLayoutDebugger} from "web-layout-debugger";

//Start web-layout-debugger in development environment
if(process.env.NODE_ENV=='development'){
    loadLayoutDebugger()
}

ReactDOM.render(
    <App />,
    document.getElementById('root')
);
```
