# Homepage

## Quick Start
1. Fork本仓库到`USERNAME/USERNAME.github.io`，其中`USERNAME`是你的github用户名。
1. 配置谷歌学术引用爬虫：
    1. 在你的谷歌学术引用页面的url里找到你的谷歌学术ID：例如，在url https://scholar.google.com/citations?user=SCHOLAR_ID 中，`SCHOLAR_ID`部分即为你的谷歌学术ID。
    1. 在github本仓库页面的`Settings -> Secrets -> Actions -> New repository secret`中，添加`GOOGLE_SCHOLAR_ID`变量：`name=GOOGLE_SCHOLAR_ID`、`value=SCHOLAR_ID`。
    1. 在github本仓库页面的`Action`中，点击*"I understand my workflows, go ahead and enable them"*启用workflows by clicking *"。本action将会谷歌学术引用的统计量数据`gs_data.json`到本仓库的`google-scholar-stats`分支中。每次修改main分支的内容会触发该action。本action也会在每天08:00 UTC定时触发。
1. 使用 [favicon-generator](https://redketchup.io/favicon-generator)生成favicon（网页icon文件），并下载所有文件到`REPO/images`。
1. 修改主页配置文件[_config.yml](_config.yml):
    1. `title`: 主页标题
    1. `description`: 主页的描述
    1. `repository`: USER_NAME/REPO_NAME  
    1. `google_analytics_id` (可选的): 谷歌Analytics ID
    1. SEO相关的键值 (可选的): 从搜索引擎的控制台里获得对应的ID (例如：Google, Bing and Baidu)，然后粘贴到这里。
    1. `author`: 主页作者信息，包括其他网页、Email、所在城市、大学等。
1. 将你的主页内容添加到 [_pages/about.md](_pages/about.md)以及includes下.
1. 将代码推送到github/main分支下；
1. 在github项目下，点击settings tab, 在左侧Code and automation部分，点击Build and deployment菜单
1. 在Branch选项下，选择main分支，另外一个选项保持默认即可，点击保存；
1. 你的主页将会被部署到`https://USERNAME.github.io`.

## Debug Locally

1. 使用`git clone`将本项目克隆到本地。
1. 安装Jekyll的构建环境，包括`Ruby`、`RubyGems`、`GCC`和`Make`。参考[该教程](https://jekyllrb.com/docs/installation/#requirements)。
1. 运行 `bash run_server.sh` 来启动Jekyll实时重载服务器。
1. 在浏览器里打开 [http://127.0.0.1:4000](http://127.0.0.1:4000)。如果你修改了网页的源码，服务器会自动重新编译并刷新页面。
1. 当你修改完毕你的页面以后, 使用`git`命令，`commit`你的改动并`push`到你的github仓库中。

## 页面修改
```
├── _config.yml                # 配置文件
├── _data/
│   └── navigation.yml         # 导航菜单
├── _pages/
│   ├── about.md               # 主页
│   └── includes/              # 主页各部分内容
│       ├── intro.md           # About Me 个人简介
│       ├── education.md       # 教育背景与培训
│       ├── pub.md             # Publications 发表论文
│       ├── presentations.md   # Presentations 学术报告/会议
│       ├── patents.md         # Patents 专利
│       ├── teaching.md        # Teaching 教学经历
│       ├── service.md         # Service 学术服务
│       ├── honers.md          # Honors & Awards 荣誉奖项
```
- 修改时主要关注几个页面：
    - 页面左侧内容在_config.yml中修改；
    - 头部菜单在navigation.yml修改；
    - 各个菜单的详情页在includes/下的页面；

## 生成 GitHub Star 徽章
Shields.io 的 GitHub Star 徽章 URL 格式如下：

```text
https://img.shields.io/github/stars/<GITHUB_USER>/<REPO>?
```
- <GITHUB_USER>：GitHub 用户名或组织名（如:yuewei-ling）

- <REPO>：仓库名（如:yueweiling.github.io

- <STYLE_OPTIONS>（可选）：

    - style=social（默认样式，带 GitHub 图标）

    - style=flat（扁平化设计）

    - style=flat-square（方形扁平设计）

    - logo=github（自定义 GitHub 图标）