## 创建项目

vite + vue3 + ts + pinia

#### npm

````js
npm init vite@latest
   ```
````

创建项目名 ==> Project name
Select a framework ==> vue (默认 vue3)
Select a variant ==> typeScript (ts)

````js
npm init vite@latest
   ```
````

#### 项目

npm run dev 跑项目
npm run build 打包

**注意**
App.vue 页面报红，ts 检测语法 import App from './App.vue' 检测.vue 文件类型
解决报红方法：
新建 src/vue-shims.d.ts

````js
declare module '\*.vue' {
import { ComponentOptions } from 'vue'
const componentOptions: ComponentOptions
export default componentOptions
}
    ```
````
