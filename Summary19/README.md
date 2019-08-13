# 表单复选框
## v-model input[type="checkbox"]

```
<div id="myApp">
        <input type="checkbox" id="item1" value="game1" v-model="selectedItems"> <label for="item1">game1</label>
        <input type="checkbox" id="item2" value="game2" v-model="selectedItems"> <label for="item2">game2</label>
        <input type="checkbox" id="item3" value="game3" v-model="selectedItems"> <label for="item3">game3</label>
        <input type="checkbox" id="item4" value="game4" v-model="selectedItems"> <label for="item4">game4</label>
        <p>Selected Items: {{selectedItems}}</p>
    </div>
    <script>
        var myApp = new Vue({
            el: "#myApp",
            data: {
                selectedItems: ["game1"]
            }
        })
    </script>
```