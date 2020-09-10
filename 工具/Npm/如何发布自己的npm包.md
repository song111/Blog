## 如何发布自己的 npm 包
[TOC]

作为一名前端开发人员安装使用 npm 包是日常工作的一部分，优秀的 npm 包为我们提供了很多便利，也为我们的开发节省了很多的时间。很多公司都会拥有自己的私有 npm 仓库用于管理私有的 npm 包，所以学习开发发布一个好用 **No Bug npm** 包是一项很重要的技能，下面我会结合自己的实战心得总结下发布一个 npm 包的流程。


#### 1.初始化项目

#### 2.package.json 配置

- **name:** 项目名称
- **version:** 项目版本号
- **description:** 项目简介
- **main:** 项目暴露的入口文件
- **scripts:** npm 执行命令
- **keywords:** 关键字利于搜索
- **author:** 作者
- **license:** 许可证书类型(ISC | MIT ...)
- **files:** 会发布到到仓库的文件白名单 也可以用.npmignore 设置白名单
- **repository:** 仓库地址和类型

#### 3.项目命名和版本管理规范

**命名:** 注册 npm 用户帐户或创建组织时，系统会授予与您的用户或组织名称匹配的范围。您可以将此作用域用作相关程序包的命名空间。

**版本管理：**

#### 4.开发功能以及打包编译


#### 5.README文档编写

为了帮助其他人在 npm 上找到你发布的软件包，你需要提供一个文档包括安装，配置和使用程序包中的代码的说明。README文档将会自动作为 npm 包的主页显示。

#### 6.发布到npm仓库
- 搜索项目名查看是否有重名项目
```bash
npm search package-name 
```
- 注册登录
```bash
npm login 
```
- 发布
```bash
cd project-dir
npm publish --access public 
```
- 安装测试
```bash
npm install package-name 
```

**常用 npm 命令表**
| Action | Commond |
| ---------------- | ------------------------------ |
| 创建软连接 | npm link [package-name] |
| 删除链接 | npm unlink |
| 登录 | npm login |
| 查找 npm 包 | npm search [package-name] |
| 发布 | npm publish [package-name] |
| 撤销发布 | npm unpublish [package-name] |
| 查看包信息 | npm info [package-name] |
| 查看包的当前版本 | npm view [package-name] version |
| 查看包的所有版本 | npm view [package-name] versions |
|查看包安装依赖|npm ls |
