# Class绑定
## v-bind:class
为html tag 绑定class样式
```
<div id="myApp">
        <p v-bind:class="{active: isActive}">红色字体1</p>
        <p :class="{active: isActive}">红色字体2</p>
        <button @click="changeColor">改变颜色</button>
    </div>
    <script>
        var myApp = new Vue({
            el: "#myApp",
            data: {
                isActive: true
            },
            methods: {
                changeColor: function(){
                    this.isActive = !this.isActive;
                }
            }
        })
    </script>
```