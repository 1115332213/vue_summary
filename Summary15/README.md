# 列表渲染
## v-for
循环数组元素，整理内容显示到页面上。
```
<div id="myApp">
        <p>Tom杂货店中的东西有</p>
        <hr>
        <ul>
            <li v-for="(item, index) in items">{{index+1}}. {{item.name}} {{item.price}}元</li>
        </ul>
    </div>
    <script>
        var myApp = new Vue({
            el: "#myApp",
            data: {
                items: [
                    {name:"Apple", price:1.08},
                    {name:"Onion", price:99.99},
                    {name:"Melon", price:4.18}
                ]
            }
        })
    </script>
```