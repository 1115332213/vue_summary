#  局部组件的使用
> * 组件的局部注册
Vue.js的组件不仅可以单独声明注册使用，还可以在Vue实例中进行局部注册使用。
```
<div id="myApp">
        <ol>
            <my-item1></my-item1>
            <my-item2></my-item2>
        </ol>
    </div>
    <script>   
        var component1 = {
            template: "<li>我要去吃饭<li>"
        }
        var component2 = {
            template: "<li>我要去喝水<li>"
        }
        var myApp = new Vue({
            el: "#myApp",
            data: {
                
            },
            components: {
                "my-item1": component1,
                "my-item2": component2
            }
        })
    </script>

```