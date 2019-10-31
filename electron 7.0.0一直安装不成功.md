## 克隆了electron-quick-start项目。跑不起来，安装都是失败，简直不能忍。详细找了原因。

 - electron无法下载下来electron-v7.0.0-win32-x64.zip


## 解决办法
升级Electron到7.0.0，提示Electron failed to install correctly, please delete node_modules/electron and try installing again。

 - 解决方法1
 
   - 前往淘宝镜像 https://npm.taobao.org/mirrors/electron/7.0.0/ 手动下载对应的包，windows下载electron-v7.0.0-win32-x64.zip

   - 然后在node_modules\electron\下创建dist文件夹。将下载的压缩包解压进刚刚创建的dist。

   - 在node_modules\electron\中创建path.txt，内容为electron.exe（对应自己的平台，不同平台不一样）。

   - 可以npm start 正常启动了。

 - 解决方法2
 
   - 找到node_modules\@electron\get\dist\cjs\index.js 第93行 url = artifact_utils_1.getArtifactRemoteURL(artifactDetails);

   - 改成 url ="https://npm.taobao.org/mirrors/electron/7.0.0/electron-v7.0.0-win32-x64.zip";

   - 然后再运行node node_modules\electron\install.js
   
   - 可以npm start 正常启动了。
