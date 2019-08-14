#  组件 参数传递
> * 为组件传递数据
制作可接受参数的组件
```
<div id="myApp">
        <h3>成绩列表</h3>
        <test-score :score="50"></test-score>
        <test-score :score="70"></test-score>
        <test-score :score="90"></test-score>
    </div>
    <script>
        Vue.component("test-score", {
            props:["score"],
            template: "<div><span>{{score}}: {{testResult}}</span></div>",
            computed: {
                testResult: function(){
                    var strResult = "";
                    if(this.score < 60) {
                        strResult = "不及格";
                    }else if(this.score < 80) {
                        strResult = "中等成绩";
                    }else{
                        strResult = "优秀";
                    }
                    return strResult;
                }
            }
        });
        var myApp = new Vue({
            el: "#myApp"
        })
    </script>

```