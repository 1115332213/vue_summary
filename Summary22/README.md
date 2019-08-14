# 表单修饰符
> * v-model.lazy
> * v-model.nubmer
> * v-model.trim

```
.lazy
用户输入内容时不做绑定数据的更新处理，在控件的onchange事件中更新绑定的变量。
用户名：<input v-model.lazy="username">


.number
将用户输入的内容转换为数值类型，如果用户输入非数值的时候，则返回NaN。
年龄：<input v-model.number="age" type="number">


.trim
自动去掉用户输入内容两端的空格。
意见：<input v-model.trim="content">

```
```
<div id="myApp">
        <div>
            <label for="name">姓名:</label>
            <input type="text" id="name" v-model.lazy="name" @change="focusChange">
            <p v-if="seen">可注册</p>
        </div>
        <div>
            <label for="age">年龄:</label>
            <input type="number" id="age" v-model.nubmer="age">
        </div>
        <div>
            <label for="info">信息:</label>
            <textarea v-model.trim="info" id="info" cols="30" rows="10"></textarea>
        </div>

        <p>
            姓名:{{name}}
        </p>
        <p>
            年龄:{{age}}
        </p>
        <p>
            信息:{{info}}
        </p>
    </div>
    <script>
        var myApp = new Vue({
            el: "#myApp",
            data: {
                name: "",
                age: "",
                info: "",
                seen: false
            },
            methods: {
                focusChange: function(){
                    if (this.name.length > 0) this.seen=true;
                    else this.seen=false;
                }
            }
        })
    </script>
```