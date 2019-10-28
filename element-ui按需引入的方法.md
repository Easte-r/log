
 - 安装库 babel-plugin-component
 - 与ant类似，修改babel.config.js
 
 ```
 babel.config.js文件配置 
 module.exports = {
	presets: [
		'@vue/app'
	],
	plugins: [
		[
			"component",
			{ "libraryName": "element-ui", "styleLibraryName": "theme-chalk" }
		]
	]
}
```
development环境 app.js包2.3Mb


## 定义主题色

```
// custom.scss
/* 改变主题色变量 */
$--color-primary: #5cbb7a !default;
// $--color-primary: #409EFF !default;
$--font-path: '~element-ui/lib/theme-chalk/fonts';
// @import "~element-ui/packages/theme-chalk/src/index";

// 按需加载或者全量加载 
// main.ts
import Element from 'element-ui'; // 全量加载。（按需加载类似）
// 在use Element之前引入scss
import './custom.scss'; 
// 使用Element
Vue.use(Element);




// 其他地方使用主题色
// aaa.vue
@import '@custom.scss';
color: $--color-primary;
```
