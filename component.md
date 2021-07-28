//vue 组件

示例
//先注册组件
Vue.component('button-demo',{
  template:'<button>hello world</button>'
})
//注册名为'button-demo'组件之后 <button-demo></button-demo>就等价于<button>hello world</button>
//然后通过Vue注册的组件只能在Vue的注册范围内使用 例如
New Vue({
  el:'#app',
  data:{
  },
  methods:{
  
  }
})
//'#app'的div 为Vue实例的挂载目标 组件button-demo只能写在此div里才能使用
<div id='app'>
  <button-demo></button-demo>
</div>

//Vue组件不仅能组合html标签 每一个Vue组件对相当于一个Vue实例 在组件内可定义 方法 数据 以及 引用其他组件
