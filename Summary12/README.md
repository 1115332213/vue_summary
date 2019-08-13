# Class对象绑定
## v-bind:class  (缩写可以省略v-bind)
为html标记绑定样式单class对象。
```
<div id="myApp">
        <p v-bind:class="pclass">class要改变得对象</p>
        <p :class="pclass">class要改变得对象</p>
        <button type="button" @click="btnClick">change</button>
    </div>
    <script>
        var myApp = new Vue({
            el:"#myApp",
            data: {
                pclass: {
                    active: true,
                    big: true
                }
            },
            methods: {
                btnClick:function(){
                    this.pclass.active = !this.pclass.active;
                    this.pclass.big = !this.pclass.big;
                }
            }
        })
    </script>
```