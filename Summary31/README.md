# slot的插槽的基础使用
## slot
slot是父组件与子组件的通讯方式，可以将父组件的内容显示在子组件当中
```
   <div id="myApp">
        <my-item pname="Tom"> <span style="color:red;"> 你爱吃什么？</span></my-item>
        <my-item pname="Peter"> 你最喜欢的运动？</my-item>
        <my-item pname="Sue"> 喜不喜欢吃西瓜？</my-item>
    </div>
    <script>
        Vue.component("my-item", {
            props: ["pname"],
            template: "<div>"
            + "<p>Hello {{pname}}</p>"
            + "<slot></slot>" 
            + "</div>"
        })
        var myApp = new Vue({
            el: "#myApp"
        })
    </script>

```