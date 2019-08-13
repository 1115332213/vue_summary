# slot的组合
## slot
在子组件中通过为多个slot进行命名,来接受父组件的不同内容的数据
```
<div id="myApp">
        <all-items item1="apple" item2="onion">
            <span slot="item3">graps</span>
            <span slot="item4">pear</span>
            <span slot="item5">plantegg</span>
        </all-items>
    </div>
    <script>
        Vue.component("all-items",{
            props: ["item1", "item2"],
            template: "<div> <p>{{item1}}</p> <p>{{item2}}</p> <p><slot name='item3'></slot></p> <p><slot name='item4'></slot></p> <p><slot name='item5'></slot></p></div>"
        })
        var myApp = new Vue({
            el: "#myApp",
        })
    </script>
```
