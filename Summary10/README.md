
# 设定计算属性  
## 计算属性中set/get用法  
设置计算属性，同步更新元数据的值   
```
<div id="myApp">
        <p>HM 的一件羽绒服售价为{{price}}元, 那它的含税价格为{{priceInTax}}元, 那么它大概价值{{priceToDollar}}美元</p>
        <button type="button" @click="btnClick(3000)">这次是给含税价格设定为3000元</button>
        <!-- 上次是给price加上1000元 -->
    </div>
    <script>
        var myApp = new Vue({
            el: "#myApp",
            data: {
                price: 2000,
            },
            computed: {
                priceInTax: {
                    get: function(){
                        return Math.round(this.price * 1.08);
                    },
                    set: function(value){
                        this.price = Math.round(value/1.08);
                    }
                },
                priceToDollar: function(){
                    return Math.round(this.priceInTax / 7.0);
                }
            },
            methods: {
                btnClick: function(value){
                    this.priceInTax = Math.round(value);
                }

            }
        })
    </script>

```