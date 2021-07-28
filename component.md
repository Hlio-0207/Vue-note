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
//例如 定义一个名为 button-rounter 的组件 定义数据count 值为0 定义点击自增方法clickAdd  
Vue.component('button-rounter',{  
  data:function(){  
    return{  
      count:0  
    }  
   },  
  methods:{  
     clickAdd:function(){  
      this.count++
     }  
    },  
  template:'<button @click="clickAdd">You clicked me {{ count }} times</button>'  
})  

//注意 一个组件的data选项必须是一个函数 因此每个实例可以维护一份被返回的对象的独立copy  
data:function(){  
  return{  
    count:0  
  }  
  }  
 //而不是像定义Vue实例一样
 data:{  
  count:0  
  }  
  
