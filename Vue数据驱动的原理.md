## 主要基于 Object.defineProperty 采用数据劫持结合发布者-订阅者模式的方式

示例

 1. 定义了obj下的一个属性txt
 2. 在set中做处理，当txt被赋值的时候，拿到value 更新视图。
 3. 当键盘按下的时候，把input中的数据赋值给txt 

```
<body>
    <div id="app">
    <input type="text" id="txt">
    <p id="show"></p>
</div>
</body>
<script type="text/javascript">
    var obj = {}
    Object.defineProperty(obj, 'txt', {
        get: function () {
            return obj
        },
        set: function (newValue) {
            document.getElementById('txt').value = newValue
            document.getElementById('show').innerHTML = newValue
        }
    })
    document.addEventListener('keyup', function (e) {
        obj.txt = e.target.value
    })
</script>
```
