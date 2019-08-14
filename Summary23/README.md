#  组件基础中的基础
> * component
组件就是页面上的一小块区域内容，完成一个小的页面功能，请参照视频第六课。
```
<div id="myApp">
        <ol>        
            <my-item1></my-item1>
            <my-item2></my-item2>
        </ol>
    </div>
    <script>
    Vue.component("my-item1", {
        template: "<li>让我们一起摇摆</li>"
    })
    Vue.component("my-item2", {
        template: "<li>让我们一起看电视吧</li>"
    })
    var myApp = new Vue({
        el: "#myApp"
    })
    </script>

```