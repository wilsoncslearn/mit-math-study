# MIT 数学学习与进度同步

面向中文学习者的 MIT OpenCourseWare 数学课程导航：找到课程、分清教材与讲义、安排学习顺序，再通过练习检验理解。

这是个人使用的私有学习仓库，用于跨主机共享学习进度、教学约定与课程导航；不是 MIT 官方项目，也不是完整课程资料镜像。

## 从哪里开始

- **第一次学习微积分**：先从 18.01 单变量微积分开始，再学习 18.02 多变量微积分。
- **想学习线性代数**：可将 18.06SC 作为独立学习主线，也可与微积分并行；按自己的基础调整节奏。
- **想学习概率与统计**：查看 18.05；该版本课程大纲列出的先修课程为 18.02。
- **已经有自己的教材主线**：把对应课程作为补充，不必为了“学完 MIT”同时开启所有课程。

具体的资料使用方法见 [学习说明](README_学习说明.md)。

## 课程导航

| 方向 | 官方课程 | 版本 | 教师 |
| --- | --- | --- | --- |
| 单变量微积分 | [18.01 Single Variable Calculus](https://ocw.mit.edu/courses/18-01-single-variable-calculus-fall-2006/) | 2006 秋季 | David Jerison |
| 多变量微积分 | [18.02 Multivariable Calculus](https://ocw.mit.edu/courses/18-02-multivariable-calculus-fall-2007/) | 2007 秋季 | Denis Auroux |
| 线性代数 | [18.06SC Linear Algebra](https://ocw.mit.edu/courses/18-06sc-linear-algebra-fall-2011/) | 2011 秋季 | Gilbert Strang |
| 概率与统计 | [18.05 Introduction to Probability and Statistics](https://ocw.mit.edu/courses/18-05-introduction-to-probability-and-statistics-spring-2022/) | 2022 春季 | Jeremy Orloff、Jennifer French Kamrin |

补充阅读：[Gilbert Strang《Calculus》官方开放教材入口](https://ocw.mit.edu/courses/res-18-001-calculus-fall-2023/)。它不是上述微积分课程指定教材，也不是 Strang 的线性代数教材。

## 如何获取资料

### 官方来源

从上表进入课程主页，查看讲义、作业、考试和课程下载入口。仅阅读本指南不需要下载整个离线包。

### 百度网盘

完整离线资料已另行备份到百度网盘，**公开分享链接与提取码待补充**。目前请使用官方来源。

离线资料不等于所有内容都能离线使用：视频、在线答题检查器和部分外部交互演示仍可能需要联网；整理的资料中不包含商业配套教材全文或完整课程视频档案。

## 跨主机同步

本仓库保持私有，课程大文件另放网盘。同步的是实际学习记录，而不只是空白模板：

- [微积分学习进度](微积分学习进度.md)：18.01 与 18.02 分别维护。
- [线性代数学习进度](线性代数学习进度.md)：18.06SC。
- [学习约定](agent.md)：教学方式、掌握判断、记录规则。
- [AI 助教入口](AGENTS.md)：提醒支持该入口的工具先读取约定和进度。

概率论的既有进度仍在独立工作区，尚未迁入本仓库；这里只提供 18.05 的课程导航，不代表概率论进度已经同步。

### 新电脑首次使用

登录有权访问此私有仓库的 GitHub 账号后，执行：

```sh
git clone https://github.com/HP-Patience/mit-math-study.git
cd mit-math-study
```

仓库可以放在任意目录。需要离线材料时，从网盘另行获取，把课程文件夹放在仓库根目录，保持原有名称；不需要把整个离线包再上传 GitHub。没有离线资料也可以从官网阅读。

### 每次换电脑学习

开始前，在仓库目录执行：

```sh
git status --short
git pull --ff-only
```

如果有未提交修改，先检查并保存它们；如果拉取报错或分支已经分叉，先处理差异，不要强制覆盖。尽量不要在两台电脑同时修改同一份进度。

学习结束需要记录时，告诉 AI：“记录本次学习进度，并提交、推送到 GitHub。”也可以手动更新文件后执行：

```sh
git diff
git add -- 微积分学习进度.md 线性代数学习进度.md
git diff --cached
git commit -m "Update study progress"
git push
```

没有文件变化时不需要提交。修改学习约定或其他文件时，检查内容后单独加入提交。若推送被拒绝，先比较并合并两台电脑的改动，再推送；不要使用强制推送或覆盖另一台电脑的记录。

Git 同步的是文件，不会自动同步不同 AI 平台的聊天历史。进度中应保留“本次学到哪里、理解依据、卡点、下次起点”，新会话先读取这些文件再继续。只有推送成功后，另一台电脑才能拉取到本次更新。

### 同步范围与隐私

`.gitignore` 使用白名单，只允许本仓库列出的文本文件进入版本控制，默认排除课程包、PDF、网页镜像及本机配置。新增笔记要同步时需显式加入白名单。

白名单不会自动移除已跟踪文件或清除历史。若将来想公开分享，建议另建仅包含整理后指南与笔记的公开仓库；不要直接把包含个人进度历史的私有仓库改成公开。

## 来源与使用边界

课程及原始教学资料来自 [MIT OpenCourseWare](https://ocw.mit.edu/)，版权与使用条件以各资料自身声明及 [MIT OCW 使用条款](https://ocw.mit.edu/pages/privacy-and-terms-of-use/) 为准。

本项目的名称不代表 MIT 背书。不要把 MIT 提供的课程资料误认为采用软件领域的 MIT License；转载或改编前应核对相应许可、保留署名与原始声明。未单独授权的第三方内容不因出现在本指南或网盘中而获得新的授权。
