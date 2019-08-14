#  组件：事件传递
> * v-on
> * $emit


v-on  
侦听组件事件，当组件触发事件后进行事件处理。
$emit
触发事件，并将数据提交给事件侦听者。
```
 <div id="myApp">
        <add-method :a="6" :b="12" @event_add="addListener"></add-method>
        <p>
        the result is {{result}}
        </p>
    </div>
    <script>
        Vue.component("add-method", {
            props: ["a", "b"],
            template: "<div><button @click=btnEventGenerate>click</button></div>",
            methods: {
                btnEventGenerate: function(){
                    this.$emit("event_add", {
                        result: this.a + this.b
                    })
                }
            }
        })

        var myApp = new Vue({
            el: "#myApp",
            data: {
                result: 0
            },
            methods:{
                addListener: function(val){
                    this.result = val.result;
                }
            }
        })
    </script>

```