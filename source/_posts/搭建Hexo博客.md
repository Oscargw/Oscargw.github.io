---
title: 搭建Hexo博客
---

- [x] **hexo搭建** 
参考：https://eliyar.biz/how_to_build_hexo_blog/
```shell
npm i hexo-cli -g
hexo init
npm i
hexo g
hexo s
```
- [x] **hexo编译报错**
解决方法：node10升级到node14.
- [x] **hexo init 卡主**
解决方法：
D:\nodejs\node_global\node_modules\hexo-cli\lib\console\init.js文件中，
const GIT_REPO_URL = 'https://github.com/hexojs/hexo-starter.git' 修改为：
const GIT_REPO_URL = 'https://github.com **.cnpmjs.org** /hexojs/hexo-starter.git';

- [ ] **github部署**
参考：https://cloud.tencent.com/developer/article/1662782
- [x] **hexo d提交报警告：warning: CRLF will be replaced by LF in public/assets/css/style.css** 
解决方法，参考：https://www.codegrepper.com/code-examples/whatever/warning%3A+CRLF+will+be+replaced+by+LF+in+public%2Fassets%2Fcss%2Fstyle.css.
```
git config --global core.autocrlf input
```
