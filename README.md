# vue-playlist

> Vue基础知识

## Build Setup

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

For a detailed explanation on how things work, check out the [guide](http://vuejs-templates.github.io/webpack/) and [docs for vue-loader](http://vuejs.github.io/vue-loader).

### vue 生命周期
```
beforeCreate：加载动画等
created：请求数据，关闭加载动画
beforeMount：挂载虚拟dom
mounted：模板已经编译完了，页面显示出来之后操作在这里面写
beforeUpdate：组件更新之前调用函数
updated：组件更新之后调用的函数
beforeDestroy：组件销毁之前调用的函数
destroyed：组件销毁之后调用的函数
```

