# vue-demo

> A Vue.js project

## Build Setup

``` bash
# install dependencies
npm install

# serve with hot reload at localhost:8080
npm run dev

# build for production with minification
npm run build

# build for production and view the bundle analyzer report
npm run build --report

# run unit tests
npm run unit

# run e2e tests
npm run e2e

# run all tests
npm test
```

For a detailed explanation on how things work, check out the [guide](http://vuejs-templates.github.io/webpack/) and [docs for vue-loader](http://vuejs.github.io/vue-loader).

# 教程

# 基于VSCode 和 Vue 前端开发环境搭建 
## vscode 安装 
 官网下载 [VSCodeUserSetup-x64-1.27.2.exe] 到本地，直接安装
 启动vscode 安装前端开发便利性的插件 便利开发。
 ![](http://one17356s.bkt.clouddn.com/18-9-29/83627385.jpg)
# VSCode 安装完成
 
 --- 
 
# vue开发环境搭建:
- Node.js: javascript运行环境(runtime),不同系统直接运行各种编程语言
- npm: Nodejs下的包管理器。由于国内使用npm会很慢,这里推荐使用淘宝NPM镜像（http://npm.taobao.org/） 
`$ npm install -g cnpm –registry=https://registry.npm.taobao.org`
- webpack: 它主要的用途是通过 CommonJS 的语法把所有浏览器端需要发布的静态资源做相应的准备，比如资源的合并和打包。
- vue-cli: 用户生成Vue工程模板
 
### 安装node.js 
从官网下载node-v8.12.0-x64.msi node 安装文件进行傻瓜式一步步安装，将node 安装路径添加到path路径(`D:\Dev\NodeJS\nodejs`)下即可。
![](http://one17356s.bkt.clouddn.com/18-9-29/73062297.jpg)
然后cmd下执行`node -v` 出现如下提示说明nodejs 安装成功。
![](http://one17356s.bkt.clouddn.com/18-9-29/70179801.jpg)

npm包管理器，是集成在node中的，所以，直接输入 npm -v就会如下图所示，显示出npm的版本信息。

配置npm的全局模块的存放路径以及cache的路径，例如我希望将以上两个文件夹放在NodeJS的主目录下，便在NodeJs下建立"node_global"及"node_cache"两个文件夹
需要设置npm命令的prefix和cache参数，prefix设置npm下载的第三方包存储的位置，cache则是设置npm使用的缓存位置。可以通过npm config get [参数名] 来查看某个参数的值
### 配置module 存放的目录地址
```
npm config set cache "D:\Dev\NodeJS\repo\node_cache"
npm config set prefix "D:\Dev\NodeJS\repo\node_global"
```

### 设置环境变量

根据自己情况是否需要将 prefix 参数对应目录添加到path环境变量，因为有些插件有提供命令行命令，设置到path将便利在cmd下使用插件提供的命令。这里设置这个路径。

新增 ： NODE_PATH 环境变量 `NODE_PATH = D:\Dev\NodeJS\repo\node_global\node_modules` ; 路径即是 prefix参数/node_modules

修改 path 环境变量新增 prefix 参数设置的值 `D:\Dev\NodeJS\node_global\`。

### 安装module 
```
npm install -g XXX 安装module 到本地 prefix/node_modules
npm install express -g //“-g”这个参数意思是装到global目录下 ,也即prefix 参数设置的目录下。
npm install -g vue-cli 
npm install -gd express --registry=https://registry.npm.taobao.org   //安装时手动指定从哪个镜像服务器获取资源

//为了避免每次安装都需要--registry参数，可以使用如下命令进行永久设置远程仓库：
npm config set registry https://registry.npm.taobao.org
// 删除设置的全局 仓库配置
npm config delete registry

```



使用 cnpm 加速 npm ,安装 cnpm module ，感觉不用安装 cnpm 也可以
`npm install -g cnpm --registry=https://registry.npm.taobao.org`
执行完后就可以使用cnpm安装module 

# 安装Vue 脚手架开发环境
```
// 第一步 安装Vue
npm install -g vue --verbose
// 第二步 安装 vue-cli
npm install -g vue-cli  --verbose
// 第三步 安装Webpack,webpack是构建工具
npm install webpack -g  --verbose // 显示所有安装信息 


npm uninstall -g vue-cli //卸载模块
```

# 创建基于 webpack模板  的 vue 项目
```
// 创建一个基于 webpack 模板的新项目, vue-demo 是项目名字
vue init webpack vue-demo

```
![](http://one17356s.bkt.clouddn.com/18-9-29/60329429.jpg)
---

## 这里需要进行一些配置，默认回车即可或者输入 Y 即可。

![](http://one17356s.bkt.clouddn.com/18-9-29/41363087.jpg)

## 创建成功后的目录层级
![](http://one17356s.bkt.clouddn.com/18-9-29/59530387.jpg)
## 运行刚刚创建的空项目
```
cd vue-demo   //进入到刚创建的项目中
//安装项目依赖，工程根目录下有 node_modules文件夹 文件夹里面存放了我们需要的依赖包
npm install     //如果不能成功install，可先尝试将npm升级到最新版本【npm install npm -g】，然后install
npm run dev     //运行项目
```

![](http://one17356s.bkt.clouddn.com/18-9-29/79280779.jpg)

# 参考：
## node + npm 配置  vue 开发环境
 [Node.js安装及环境配置之Windows篇](https://blog.csdn.net/qq_26562641/article/details/72235585)
 
 [NodeJS、npm安装配置，指定npm安装目录，可移植的node以及模块](https://blog.csdn.net/suiyuehuimou/article/details/74143436)
 
 [Vue环境搭建（Windows下搭建Vue.js）](https://blog.csdn.net/Mr_ChenXu/article/details/79054775)
 
 [(一)nodejs开发环境搭建: 安装nodejs以及配置npm](https://blog.csdn.net/aitangyong/article/details/49095827)
 
 [NodeJS、NPM安装配置步骤(windows版本) 以及环境变量](https://blog.csdn.net/haluoluo211/article/details/51782121)

 [node环境变量配置，npm环境变量配置](https://blog.csdn.net/jianleking/article/details/79130667)
 
 [Vue学习【一】环境搭建，demo运行](https://blog.csdn.net/u011439689/article/details/72470037)
 
 [快速搭建 Node.js 开发环境以及加速 npm](https://blog.csdn.net/Violent_clown/article/details/78188294)
## Vscode 
 [前端开发必备的15个 Visual Studio Code 插件](http://f2ex.cn/15-essential-plugins-for-visual-studio-code/)
 
 
