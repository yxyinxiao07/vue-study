# vue-cli 2.0 3.0 区别

3.0 新加入了 TypeScript 以及 PWA 的支持
部分命令发生了变化：
下载安装  npm install -g vue@cli
删除了vue list
创建项目   vue create
启动项目   npm run serve
默认项目目录结构也发生了变化：
移除了配置文件目录，config 和 build 文件夹
移除了 static 文件夹，新增 public 文件夹，并且 index.html 移动到 public 中
在 src 文件夹中新增了 views 文件夹，用于分类 视图组件 和 公共组件  


## 安装 （npm新版本 包命名更严格, vue-cli3.0相应跟着变化）
2.0安装  $ npm install -g vue-cli    
3.0安装  npm install -g @vue/cli(需要先卸载2.0，npm uninstall -g vue-cli)

## 目录结构
2.0生成目录结构</br>
![image](https://github.com/yxyinxiao07/vue-study/blob/master/img/1.jpg)</br>
3.0目录结构</br>
![image](https://github.com/yxyinxiao07/vue-study/blob/master/img/2.jpg)</br>
从CLI 3的整个项目结构我们可以发现，这个结构很简单，没有相关的配置文件或复杂的目录结构。CLI 3仅生成构建应用程序所需的文件，让使用者不用关心这些工具的具体配置，从而降低了工具的使用难度。

CLI 3启动方式是内置服务 vue-cli-service serve  
CLI 2启动方式是webpack-dev-server --inline --progress --config build/webpack.dev.conf.js 这里用webpack-dev-server搭一个服务

3.0版本下，你想看看默认的webpack配置，可执行vue inspect查看，默认情况下，会将配置输出到控制台，你也可以将结果指向一个文件，例如：vue inspect > webpack.config.js

## 图形化界面
安装好了CLI 3的前提下，执行vue ui命令 ，会自动在浏览器打开图形界面</br>
![image](https://github.com/yxyinxiao07/vue-study/blob/master/img/3.jpg)</br>
