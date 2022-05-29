# web-layout-debugger

##图片占位
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

