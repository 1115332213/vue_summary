# 事件处理器
## v-on:(event)/@(event)
页面元素的事件绑定。（click,keyup,load等等）
```
<div id="myApp">
        <input type="text" v-on:keyup="inputKeyup($event)" id="input">
        <button type="button" @click="btnClick($event)" id="btn">click</button>
    </div>
    <script>
        var myApp = new Vue({
            el: "#myApp",
            methods: {
                inputKeyup: function(event){
                    this.debugLog(event);
                },
                btnClick: function(event){
                    this.debugLog(event);
                },
                debugLog: function(event){
                    console.log(
                        event.srcElement.tagName, 
                        event.srcElement.innerHTML,
                        event.srcElement.id,
                        event.key ? event.key : ""
                    )
                }
            }
        })
    </script>
```