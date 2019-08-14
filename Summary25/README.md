#  表行组件
> * 制作表行组件
为自己的页面表格编写表行组件。
需要采用 <tr is=""></tr>
```
<div id="myApp">
        <table border="1">
            <tr><td>序号</td>名称<td></td></tr>
            <tr is="my-item1"></tr>
            <tr is="my-item2"></tr>
            <!-- 
                <my-item1></my-item1>
                <my-item2></my-item2> 
            -->
        </table>
    </div>
    <script>
        Vue.component("my-item1",{
            template: "<tr><td>1</td><td>西瓜</td></tr>"
        });
        Vue.component("my-item2",{
            template: "<tr><td>2</td><td>橙子</td></tr>"
        })
        var myApp = new Vue({
            el: "#myApp"
        })
    </script>

```