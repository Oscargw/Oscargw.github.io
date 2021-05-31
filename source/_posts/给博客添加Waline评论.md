---
title: 给博客添加Waline评论
tags: 
- Hexo
- 博客
- waline
---

- 参考文档：
  [Waline-快速上手](https://waline.js.org/get-started.html#vercel-%E9%83%A8%E7%BD%B2)
- 需要使用LeanCloud，参考：
  [LeanCloud - https://console.leancloud.app/apps](https://console.leancloud.app/apps)
- Vercel部署：
  直接点击：[Vercel](https://vercel.com/new/git/external?repository-url=https%3A%2F%2Fgithub.com%2Fwalinejs%2Fwaline%2Ftree%2Fmain%2Fexample)
  一定要从leancloud拿到 **LEAN_ID**，**LEAN_KEY**，**LEAN_MASTER_KEY**
- 获取serverURL
  部署后，点击visit，拿到serverURL， https://xxxxxx.vercel.app，配置到主题.xml
- 注册管理员。
  点击<serverURL>/ui/register注册。

