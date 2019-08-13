
# 观察属性的使用
## watch
与computed属性类似，用于观察变量的变化，然后进行相应的处理。
```
 <div id="myApp">
            <p>HM 的一件羽绒服售价为{{price}}元, 那它的含税价格为{{priceInTax}}元, 那么它大概价值{{priceToDollar}}美元</p>
            <button type="button" @click="btnClick(1000)">加价1000元</button>
    </div>
    <script>
        var myApp = new Vue({
            el: "#myApp",
            data: {
                price: 2000,
                priceInTax: 0,
                priceToDollar: 0
            },
            watch: {
                price: function(newVal, oldVal){
                    console.log(newVal, oldVal);
                    this.priceInTax = this.price * 1.05;
                    this.priceToDollar = this.priceInTax / 7.0;
                }
            },
            methods: {
                btnClick: function(){
                    this.price = this.price + 1000;
                }
            }
        })
        //如果想要开始显示出priceInTax和prictToDollar的值, 执行下面语句即可，生成Vue对象后对price赋值，即可出发监听事件
        //myApp.price=2100
    </script>

```