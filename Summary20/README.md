# 表单单选按钮
## v-model input[type="radio"]

```
<div id="myApp">
        <div>
            <p>性别:</p>
            <label for="male">男:</label> <input type="radio" id="male" value="男" v-model="selectedSex">
            <label for="female">女:</label> <input type="radio"  id="female" value="女" v-model="selectedSex">
        </div>

        <div>
            <p>爱好:</p>
            <label for="movie">电影:</label> <input type="radio" id="movie" value="电影" v-model="selectedHobby">
            <label for="swim">游泳:</label> <input type="radio"  id="swim" value="游泳" v-model="selectedHobby">
        </div>
        <p>性别:{{selectedSex}}</p>
        <p>爱好:{{selectedHobby}}</p>
    </div>
    <script>
        var myApp = new Vue({
            el: "#myApp",
            data: {
                selectedSex: "男",
                selectedHobby: ""
            }
        })
    </script>
```