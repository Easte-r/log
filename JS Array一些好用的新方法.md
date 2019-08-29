```
- reduce 计算数组之和（reduceRight） https://www.runoob.com/jsref/jsref-reduce.html es3
var total = arr.reduce((total, curr, index, arr) => {})
- some 计算数组是否符合某种规则并返回boolean https://developer.mozilla.org/zh-CN/docs/Web/JavaScript/Reference/Global_Objects/Array/some 1.6 
var isExist = arr.some(age => age > 18)
- every 与some相反 需要数组内全部符合规则才true，否则false
- find 计算数组中是否符合某种规则并返回符合规则的第一个数 不符合返回undefined es6
- findIndex 计算数组中是否符合某种规则并返回符合规则的第一个数的索引 不符合返回-1
- fill 使用指定值填充数组 [0,0,0].fill(1) es6
Array(5).fill(0)
- includes 判断一个数组知否包含指定的值返回boolean es6
[1, 2, 3].includes(3, 3) // (search, fromindex?)
- filter 根据指定方法的条件，选出数组中符合条件的元素组成新数组 https://developer.mozilla.org/zh-CN/docs/Web/JavaScript/Reference/Global_Objects/Array/filter 1.6
- flat 按照一个指定深度进行数组合并 https://developer.mozilla.org/zh-CN/docs/Web/JavaScript/Reference/Global_Objects/Array/flat#%E6%89%81%E5%B9%B3%E5%8C%96%E5%B5%8C%E5%A5%97%E6%95%B0%E7%BB%84
var arr1 = [1, 2, [3, 4]];
arr1.flat();
- flatMap https://developer.mozilla.org/zh-CN/docs/Web/JavaScript/Reference/Global_Objects/Array/flatMap#Map_%E4%B8%8E_flatMap
- copyWithin 方法浅复制数组的一部分到同一数组中的另一个位置，并返回它 https://developer.mozilla.org/zh-CN/docs/Web/JavaScript/Reference/Global_Objects/Array/copyWithin
- 静态方法 Array.of(7) // [7] Array.of(1, 2, 3) // [1, 2, 3]
- 静态方法 Array.from('AA') // ['A', 'A'] Array.from()
- 静态方法 Array.isArray(arr) https://developer.mozilla.org/zh-CN/docs/Web/JavaScript/Reference/Global_Objects/Array/isArray#Polyfill

- reverse 将数组倒序 1.1
- forEach((curr, index, arr) => {}) es3
- map 通过指定函数处理原数组每个元素 1.6
- indexOf 数组中查找指定元素 未找到返回-1（类似于字符串查找）1.6

备注js1.6 对应es3 https://developer.mozilla.org/zh-CN/docs/Web/JavaScript/New_in_JavaScript/1.6

## 应用场景：
- 全选或者不全选
- 一个数组中判断是否有指定值 some find findIndex includes indexOf 推荐用indexOf
- 是否所有元素都满足某条件 every
- 服务器配置了多条分享，但通过一个数组进行下发：首页（home），详情（detail），我的（me） name（key） filter
- var home = allArray.filter(v => v.key=='home') 首页分享的时候从home数组中随机提取一个当做分享内容
- 多层嵌套数组进行平铺展开 arr.flat(Infinity) ["你好啊我叫", ["赛","利","亚"]].flat(1)
- ["你好啊我叫", ["赛","利","亚"]].flat(1).flatMap(s => s.split(''))
- 购物车页面初始化假设有10个商品。初始化为全不选 fill 
-var arr = Array(10).fill(false)
- 数据量较大的数组计算总价 reduce
- [1,2,3].reduce((t, c) => t+c)

```


数组操作是编程中经常遇到的一个问题，es6及其以上提供的一些新方法。增强了数组操作，即使不使用打包转义，也可以引入“垫片”来使用以上这些方法
