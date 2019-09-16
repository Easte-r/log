## ant-design 按需加载
 - 改 babel.config.js 文件 依赖插件“babel-plugin-import” 
 - 使用方式 import {Button} from 'ant-design-vue'
 - 开启enablejavascript



## 详细步骤
```
vue.config.js文件  需要安装使用的相关库 less less-loader
css: {
    loaderOptions: {
        less: {
            javascriptEnabled: true
        }
    }
}

babel.config.js文件  增加plugins配置
module.exports = {
	presets: [
		'@vue/app'
	],
	plugins: [
		[
			"import",
			{ libraryName: "ant-design-vue", libraryDirectory: "es", style: true }
		]
	]
}

全量引入的使用
- Vue
 - import Antd from 'ant-design-vue'
 - import 'ant-design-vue/dist/antd.css'
 - Vue.use(Antd);
 
 - <a-button type="primary>按钮<a-button>
 - 打包大小 app.js 11.6Mb

按需引入
- Vue
 - import { Button } from 'ant-design-vue';
 - Vue.use(Button);

 - <a-button type="primary>按钮<a-button>
 - 打包大小 app.js 5.3Mb
