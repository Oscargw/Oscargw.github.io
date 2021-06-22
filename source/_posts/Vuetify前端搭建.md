---
title: Vuetify前端搭建
date: 2020-12-31 15:00:04
tags:
- Vuetify
- Vue
---



### 开始

1. 启动vue-cli：
```shell
输入：vue ui
```
2. 参考：
    https://blog.csdn.net/qq_42711864/article/details/85704099

3. 添加vuetify：
```shell
选择：vue add vuetify
```
4. main.ts代码：
```shell
import Vue from "vue";
// import Vuetify from "vuetify";
import App from "./App.vue";
import Test from './views/Test.vue';
import router from "./router";
import store from "./store";
import "vuetify/dist/vuetify.min.css"; //css 需引入
import "material-design-icons-iconfont/dist/material-design-icons.css"; //vuetify依赖的图标
import vuetify from "./plugins/vuetify";

// Vue.use(Vuetify);
Vue.config.productionTip = false;

new Vue({
  router,
  store,
  vuetify,
  render: h => h(Test)
}).$mount("#app");
```


##### 参考链接
- [Vue官网](https://vuetifyjs.com/en/getting-started/installation/#vue-cli-install)
- [vue+vuetify+typescript中添加vuetify声明](https://blog.csdn.net/u011737005/article/details/105822944)
- [TypeScript+Vue+vuetify的项目搭建](https://blog.csdn.net/qq_42711864/article/details/85704099)