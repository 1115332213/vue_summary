# 表单控件绑定
## v-model input textarea
为表单控件元素创建双向数据绑定。（将JS变量的值“快速”设定到控件上，然后将用户输入的内容“快速”设置回JS变量）
```
 <div id="myApp">
        <input type="text" v-model="message">
        <p>Message is: {message}}</p>
        <textarea v-model="message" id="textarea1" cols="30" rows="10"></textarea>

    </div>
    <script>
        var myApp = new Vue({
            el: "#myApp",
            data: {
                message: ""
            }
        })
    </script>
```
