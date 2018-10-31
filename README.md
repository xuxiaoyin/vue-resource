# vue04

> A Vue.js project

## Build Setup

``` bash
# install dependencies
npm install

# serve with hot reload at localhost:8080
npm run dev

# build for production with minification
npm run build
```

/*使用vue-resource请求数据的步骤

1、需要安装vue-resource模块，  注意加上  --save

  npm install vue-resource --save /  cnpm install vue-resource --save  

2、main.js引入 vue-resource

    import VueResource from 'vue-resource';

3、main.js  Vue.use(VueResource);


4、在组件里面直接使用

    this.$http.get(地址).then(function(){

    })

*/
