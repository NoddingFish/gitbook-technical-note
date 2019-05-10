# Layui 使用过程中注意点

##### 1、如果 layui 数据表格列宽自适应出现横向滚动条的解决方案：

正常情况下，自适应的列宽不会导致 table 容器出现滚动条。如果你的出现了，请按照下述方案解决：

1. 如果 table 是在 layui 的后台布局容器中（注意：不是在 iframe 中），在你的页面加上这段 CSS：

   ```css
   .layui-body{overflow-y: scroll;}
   ```

2. 如果 table 是在独立的页面，在你的页面加上这段 CSS：

   ```css
   body{overflow-y: scroll;}
   ```

总体而言，table 列宽自适应出现横向滚动条的几率一般是比较小的，主要原因是 table 的渲染有时会在浏览器纵向滚动条出现之前渲染完毕，这时 table 容器会被强制减少滚动条宽度的差（一般是 17px），导致 table 的横向滚动条出现。建议强制给你的页面显示出纵向滚动条。

若还不能解决：

```css
.layui-table-body{overflow-x: hidden;}
```

> [如果 layui 数据表格列宽自适应出现横向滚动条的解决方案](<https://fly.layui.com/jie/18737/>)



##### 2、Layui 第三方组件：formSelects 4.x

引入后需要渲染：

```js
formSelects.render();
```

> [formSelects-v4.js 基于Layui的多选解决方案](https://hnzzmsf.github.io/example/example_v4.html)