## vue.js引入  
```
<!-- 开发环境版本，包含了有帮助的命令行警告 -->  
<script src="https://cdn.jsdelivr.net/npm/vue/dist/vue.js"></script>  
<!-- 生产环境版本，优化了尺寸和速度 -->  
<script src="https://cdn.jsdelivr.net/npm/vue"></script>  
```
## html代码块  
```
<div id="myApp">
    {{message}}
</div>
```
## js脚本部分 
```
var myApp = new Vue({
    el: "#myApp",
    data: {
        message: "Hello world"
    }
})
```