<!--
 * @Author: Weidows
 * @Date: 2020-11-28 17:36:36
 * @LastEditors: Weidows
 * @LastEditTime: 2021-02-14 20:15:41
 * @FilePath: \Keeper\README.md
 * @Description:
-->

<h1 align="center">

⭐️ Weidow's 🌈 の Keeper ⭐️

</h1>

# Intro

- ## 基于 `GitHub-Action` 的定时任务.
- ## 每日`push`一次刷绿`GitHub + Gitee`
- ## 一个每日溜圈的`爬虫`.
  - ### 每日访问唤醒休眠的 `LeanCloud` 评论后台.
  - ### 每日获取`必应壁纸`.

---

# Feature

- 在指定时间对 `GitHub + Gitee` 进行 `push` 以保持 Profile 格子绿油油(但是操作原理不同).
  - [GitHub profile预览](https://github.com/Weidows)
  - [Gitee profile预览](https://gitee.com/Weidows)
- 每次执行任务会把 Log 记录在 `Tasks.log` 中.
- 必应壁纸存储在[Bing](./Bing/)里面.
- 任务都在`daily.yml`里面,可自定义修改.
- LeanCloud 后台休眠时无法自行唤醒,这时让 GitHub-Action 每天早上访问后台一次就可以唤醒休眠了.

---

# How-To-Use

- ## 首先声明 : Fork 本项目不会产生 GitHub 刷绿效果!
  - 那就给个 `Star` 呗!
- ### [`下载/clone`](https://github.com/Weidows/Keeper/releases)本项目,自己新建一个仓库或者把本仓库文件复制到目标仓库`根目录`.
- ## 进入你的 `GitHub-keeper` 仓库里`enable Action`.

---

# Config

- ## GitHub 刷绿+爬取必应壁纸进行到此步骤已经可以正常使用了.
  - 不需要 Gitee 刷绿的话注释掉或删掉 daily.yml 里所有带 Gitee 的行就好了.
  - 不需要唤醒 LeanCloud 功能可以不用管.
- ## Gitee 刷绿配置需要 ssh 连接.,配置如下:
  - 如何生成秘钥可以查看[这篇文章](https://weidows.github.io/post/experience/SSH)或者寻求百度.
  - `公钥`复制到`Gitee用户设置`里(注意不是仓库设置)
  - 在你的`GitHub-keeper`仓库设置里新建一个`secret`,如下:
    - 名字: `RSA` :
    - 内容: `私钥文件内容复制进来`
- ## 唤醒 LeanCloud 后台:
  - 新建`secret`
  - 名字: URL
  - 内容: 需要唤醒的后台地址,如`https://weidows.avosapps.us/comments`

---

# [反馈](https://weidows.github.io/tags/about)

    后续会更新,同时欢迎有兴趣的提出修改意见或共同整改!

> 借鉴@justjavac 迷渡[https://github.com/justjavac/auto-green](https://github.com/justjavac/auto-green)

> @墨涩[https://gitee.com/mstf/bingdownload](https://gitee.com/mstf/bingdownload)

> @AimTao[https://github.com/AimTao/leancloud-self-wake](https://github.com/AimTao/leancloud-self-wake)
