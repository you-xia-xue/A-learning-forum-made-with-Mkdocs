# 如何在 VS Code 中贡献 Markdown 页面到仓库（AI生成）
这是AI生成的界面，我推荐各位不懂/麻烦的也能通过自己用各种方法解决

前提准备  
安装 VS Code      
安装 Git 并配置用户信息（用户名和邮箱）  
拥有 GitHub 账号   

**步骤 1**：Fork 原仓库  
打开浏览器，访问仓库地址：https://github.com/you-xia-xue/A-learning-forum-made-with-Mkdocs  
点击右上角的 Fork 按钮，将仓库复制到自己的 GitHub 账号下（生成个人仓库副本）  

**步骤 2**：在 VS Code 中克隆 Fork 后的仓库（preview 分支）  
打开 VS Code，点击左侧菜单栏的 源代码管理（图标类似分支）  
点击 克隆仓库，在弹出的输入框中粘贴自己 Fork 后的仓库地址（格式：https://github.com/你的GitHub用户名/A-learning-forum-made-with-Mkdocs）  
选择本地存放仓库的文件夹，等待克隆完成  
克隆完成后，点击 打开文件夹 进入仓库目录  
切换到 preview 分支（关键步骤）：  
打开 VS Code 终端（快捷键：Ctrl+`` 或 菜单栏 - 终端 - 新建终端）  
输入命令并回车：  
```bash
运行
git checkout preview
```
若提示分支不存在，先拉取远程 preview 分支：  
```bash  
运行
git fetch origin preview
git checkout preview
```

**步骤 3**：创建并编辑自己的 Markdown 页面  
在 VS Code 的资源管理器中，进入 docs 目录（仓库的文档都存放在此目录）  
右键 docs 目录，选择 新建文件，命名为 你的页面名称.md（例如：python学习笔记.md）  
编辑 Markdown 内容，示例：  
``` markdown
# Python学习笔记

## 基础语法
- 变量定义：`name = "张三"`
- 条件语句：`if a > b: print(a)`

## 学习资源
- [Python官方文档](https://docs.python.org/) 
```
编辑完成后，按 Ctrl+S 保存文件  

**步骤 4**：提交修改到自己的仓库  
回到 VS Code 的 源代码管理 面板  
在 更改 区域可以看到你创建的 Markdown 文件，勾选该文件  
在 消息 输入框中填写提交说明（例如：添加Python学习笔记页面）  
点击 提交 按钮（对勾图标）  
提交完成后，点击 同步更改 按钮（箭头循环图标），将本地修改推送到自己 Fork 的 GitHub 仓库  
步骤 5：创建 Pull Request（PR）到原仓库的 preview 分支
打开自己 Fork 的仓库 GitHub 页面（https://github.com/你的GitHub用户名/A-learning-forum-made-with-Mkdocs）  
点击页面上的 Compare & pull request 按钮  
在 PR 页面中：   
确保 base repository 选择原仓库 you-xia-xue/A-learning-forum-made-with-Mkdocs  
确保 base 分支选择 preview  
确保 head repository 选择你的仓库，compare 分支选择 preview  
在描述框中填写 PR 的详细说明（例如：新增了Python学习笔记页面，包含基础语法和资源链接）  
点击 Create pull request 按钮提交  
后续  
提交后，原仓库管理员会审核你的 PR，审核通过后将合并到原仓库的 preview 分支，你的 Markdown 页面将显示在网站中。  

## 题外话：如果你想在本地预览或者是比创建页面更大的操作  
请参阅 https://squidfunk.github.io/mkdocs-material/