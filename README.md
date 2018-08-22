React脚手架
========

# Feature:

* 支持eslint，预置一些规则

* 配置了babel，加入antd和lodash的按需加载及其他配置

* 预置webpack配置（包括开发和生产环境配置），包括了几个
常用的loader，uglify，no-console

* 支持HotModule

* 使用2空格缩进

* git commit 使用 [AngularJS commit conventions](https://github.com/angular/angular.js/blob/master/DEVELOPERS.md#commits)

* 使用githook保证提交都必须通过eslint和commit检查

* 支持一键生成Changelog

# 使用方法

## 预览本示例项目

```bash
  yarn
  yarn start
```

## 开始项目

你可以自行选择yarn还是npm

```bash
git clone https://github.com/D-e-e-m-o/React-boilerplate
git chechout clean
rm -rf .git
git init
npm i
```

记得修改`package.json`内的初始化信息

## 提交代码

```bash
  git add $yourfile
  npm run commit
```

## 生成changelog

```bash
  npm run changelog
```

## 使用git hook

husky已经预先设置了常用的hook。原理：安装husky后，它在`.git`目录下生成一些`hook script`，当满足条件（比如precommit），它会查找`package.json`内是否包含对应的script，如果有就执行。本脚手架的强制eslint和
commit message检查就是这样实现的。因此，想自定义hook，可以自己在
`package.json`内添加script就可以了。

# 注意

1. 如果运行build的时候，uglify插件报错了，尝试将`uglifyES`改为`uglifyJS`
