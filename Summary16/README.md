# JS 对象迭代
## v-for
循环渲染js对象，打印其所有的属性和属性值
```
<div id="myApp">
        <h3>我的个人信息</h3>
        <div v-for="(value, key) in items">
            {{key}} : {{value}}
        </div>
    </div>
    <script>
        var myApp = new Vue({
            el: "#myApp",
            data: {
                items:{
                    name: "Peter",
                    age: "22",
                    set: "Female",
                    language: "English"
                }
            }
        })
    </script>
```
