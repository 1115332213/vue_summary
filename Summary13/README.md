# 条件渲染
## v-if   
## v-else-if
## v-else
为html标记绑定样式单class对象。
```
<div id="myApp">
        <p>考试成绩</p>
        <p v-if="score == 0">成绩未公布</p>
        <p v-else-if="score < 60">{{score}}不及格</p>
        <p v-else-if="score < 80">{{score}}中等</p>
        <p v-else>{{score}}优秀</p>
        <button type="button" @click="btnClick">公布成绩</button>
    </div>
    <script>
        var myApp = new Vue({
            el: "#myApp",
            data: {
                score: 0
            },
            methods: {
                btnClick: function(){
                    this.score = Math.round(Math.random() * 100);
                }
            }
        })
    </script>
```