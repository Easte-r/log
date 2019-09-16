
 - 安装库 babel-plugin-component
 - 与ant类似，修改babel.config.js
 
 
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

development环境 app.js包2.3Mb
