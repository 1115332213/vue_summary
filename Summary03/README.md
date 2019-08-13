## if判断式 通过参数值判断该标签是否被渲染
```
<p v-if="seen"> Good Boy </p>
```
## for 循环  循环渲染标签
```
<ol>
	<li v-for="item in items">{{item.name}} </li>
</ol>
```