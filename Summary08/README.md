# 计算属性的使用
## computed
处理元数据，便于进行二次利用。（比如：消费税自动计算功能）
```
<div id="myApp">
        <p>HM的一件羽绒服售价为{{price}}元, 那它的含税价格为{{priceInTax}}元, 那么它大概价值{{priceToDollar}}美元</p>
    </div>
    <script>
        var myApp =new Vue({
            el: "#myApp",
            data: {
                price: 1200
            },
            computed: {
                priceInTax: function(){
                    return this.price * 1.05;
                },
                priceToDollar: function(){
                    return Math.round(this.priceInTax / 7.0);
                }
            }
        })
    </script>
```
