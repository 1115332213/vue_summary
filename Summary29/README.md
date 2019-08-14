#  组件：参数验证
> * props:组件参数验证语法
为组件中接受到的变量进行逻辑验证
```
 <div id="myApp">
        <h3>个人信息</h3>
        <show-info pname="Peter" :age="50" :deteail="{language:'English', Country: 'U.S.A'}"></show-info>
        <!-- pname接收字符串常亮  :pname接收变量 -->
    </div>
    <script>
        Vue.component("show-info", {
            props:{
                pname: {
                    type:String,
                    required: true,
                },
                age: {
                    type: Number,
                    validator: function(value){
                        return value > 0 && value < 130;
                    }
                },
                detail: {
                    type:Object,
                    default: function(){
                        return {
                            language: "English",
                            country: "England"
                        }
                    }
                }

            },
            template: "<div>"
            + "<div> {{this.pname}} </div>" 
            + "<div> {{this.age}} </div>" 
            + "<div> {{this.detail.country}} </div>" 
            + "<div> {{this.detail.language}} </div>" 
            + "</div>"
        })
        var myApp = new Vue({
            el: "#myApp"
        })
    </script>

```