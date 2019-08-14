#  为vue组件添加数据
> * 组件的数据函数
为Vue.js组件添加数据，使组件可以动态显示各种数据，注意是数据函数，不是数据属性。
```
<div id="myApp">
        今天的天气是: <today-weather/>
    </div>
    <script>
    Vue.component("today-weather",{
        template: "<span> {{weather}} </span>",
        data: function(){
            return {
                weather: "雨夹雪"
            }
        }
    })    
    
    var myApp = new Vue({
        el: "#myApp"
    })
    </script>

```