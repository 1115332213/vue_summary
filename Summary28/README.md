#  组件：传递变量
> * 制作组件可接收变量数据
制作可接受变量参数的组件
```
<div id="myApp">
        <label for="input_name">名字：</label><input id="input_name" type="text" v-model="name">
        <hr>
        <say-hello :pname="name"></say-hello>
    </div>
    <script>
        Vue.component("say-hello", {
            props:["pname"],
            template: "<div> Hello, <strong>{{pname}}</strong></div>"
        })
        var myApp = new Vue({
            el: "#myApp",
            data: {
                name: "12342"
            }
        })
    
    </script>

```