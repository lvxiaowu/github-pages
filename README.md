# 为什么使用 Github Actions ？

众所周知，前端部署无非就是把打包之后的代码丢到 nginx html 目录下就完事了，但是每逢产品频繁改需求，你总要重复一遍遍以下动作：修改，打包，登录服务器，上传代码，重启服务器。繁琐，Github Actions 可以帮你解决这一切。

# Github Actions 是什么？

大家知道，持续[集成](https://www.ruanyifeng.com/blog/2015/09/continuous-integration.html?fileGuid=1PWJAvQBtLA5IGh3)由很多操作组成，比如拉取最新代码、运行测试、登录服务器、部署服务器等，GitHub 把这些操作统一称为 Actions 。

![流程](https://static-venus.shandiantech.com/skio/20210527/1622099530432_process.png)

> Github 集成了 Actions 市场，允许开发者把操作写成独立的脚本，发布到 Actions 市场

[官方市场](https://github.com/marketplace?type=actions)
[awesome actions](https://github.com/sdras/awesome-actions)

# GitHub Actions 的一些自己的术语。

1. workflow （工作流程）：持续集成一次运行的过程，就是一个 workflow。
2. job （任务）：一个 workflow 由一个或多个 jobs 构成，含义是一次持续集成的运行，可以完成多个任务。
3. step（步骤）：每个 job 由多个 step 构成，一步步完成。
4. action （动作）：每个 step 可以依次执行一个或多个命令（action）。

> [action 官网配置](https://docs.github.com/cn/actions/reference/context-and-expression-syntax-for-github-actions)

# 创建 Github Pages 站点

> 这里使用 Actions 市场中的[GitHub Pages v3](https://github.com/marketplace/actions/github-pages-v3) 插件

1. 账户全局创建权限 ACCESS_TOKEN，账号 /settings/profile

[https://github.com/lvxiaowu/github-pages](https://github.com/lvxiaowu/github-pages)
