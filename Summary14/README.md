# 元素显示
## v-show
v-show为false时，该标签不会再dom中消失(只是将display设置为none而已)， 而v-if为false时，该标签会在dom中消失
```
 <div id="myApp">
        <p v-show="seen">这里是该篇文章的题目</p>
        <button type="button" @click="btnClick">click</button>
    </div>
    <script>
        var myApp = new Vue({
            el: "#myApp",
            data: {
                seen: true
            },
            methods: {
                btnClick: function(){
                    this.seen = !this.seen;
                }
            }
        })
    </script>
```