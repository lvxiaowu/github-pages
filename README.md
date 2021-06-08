# 自动化部署介绍，以 github 为例

1. 基于 github 的 Actions
1.1 Github Pages 站点
1.2 Github Actions + Docker 

2. 基于 jenkins + nginx

---

## Github Actions 是什么？

比如拉取最新代码、运行测试、登录服务器、部署服务器等，GitHub 把这些操作统一称为 Actions 。

## 为什么使用 Github Actions ？

众所周知，前端部署无非就是把打包之后的代码丢到 nginx html 目录下就完事了，但是每逢产品频繁改需求，你总要重复一遍遍以下动作：修改，打包，登录服务器，上传代码，重启服务器。繁琐，Github Actions 可以帮你解决这一切。

![流程](https://static-venus.shandiantech.com/skio/20210527/1622099530432_process.png)

## GitHub Actions 有一些自己的术语。

1. workflow （工作流程）：持续集成一次运行的过程，就是一个 workflow。
2. job （任务）：一个 workflow 由一个或多个 jobs 构成，含义是一次持续集成的运行，可以完成多个任务。
3. step（步骤）：每个 job 由多个 step 构成，一步步完成。
4. action （动作）：每个 step 可以依次执行一个或多个命令（action）。

## GitHub Actions 开发市场。

Github 集成了 Actions 市场，允许开发者把操作写成独立的脚本，发布到 Actions 市场

[官方市场](https://github.com/marketplace?type=actions)
[awesome actions](https://github.com/sdras/awesome-actions)

---

# 创建 Github Pages 站点

> 这里使用 Actions 市场中的[GitHub Pages v3](https://github.com/marketplace/actions/github-pages-v3) 插件

1. 账户全局创建权限 GITHUB_TOKEN（配置路径 /settings/Developer settings）

[https://lvxiaowu.github.io/github-pages](https://lvxiaowu.github.io/github-pages)

# github Actions 搭配 docker

1.  项目根目录新建 nginx 配置
2.  项目根目录新建 Dockerfile 文件
3.  配置容器镜像服务，选择[阿里云的容器镜像服务](https://cr.console.aliyun.com/cn-hangzhou/instance/dashboard)
4.  配置 action 所需要的账号信息，如服务器、docker，项目 /settings/secrets/actions

[http://www.lvxiaowu.top/docker](http://www.lvxiaowu.top/docker)


# jenkins + nginx

1. linux主机安装 docker 、nginx、jenkins
2. 配置jenkins, 拉取代码->安装依赖->上传服务器->nginx 匹配

[http://10.16.19.88/jenkins](http://10.16.19.88/jenkins)
