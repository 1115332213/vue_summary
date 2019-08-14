# 表单下拉框
> * v-model
> * select
## 表单下拉框的绑定
```
<div id="myApp">
        <p>我最喜欢的食物</p>
        <select v-model="food" id="select1" style="width:200px;">
            <option>苹果</option>
            <option>橘子</option>
            <option>橙子</option>
        </select>

        <p>我喜欢的食物</p>
        <select v-model="foods" id="select2" style="width:200px; height:200px;" multiple>
            <option>桃子</option>
            <option>苹果</option>
            <option>番茄</option>
            <option>橘子</option>
            <option>橙子</option>
            <!-- 使用ctrl键进行多选 -->
        </select>
        <p>我最喜欢的食物:{{food}}</p>
        <p>我喜欢的食物:{{foods}}</p>
    </div>
    <script>
        var myApp = new Vue({
            el: "#myApp",
            data: {
                food: "橘子",
                foods: []
            }
        })
    </script>
```