##GitHub同步开发流程
项目A用**[A]**表示，项目A的仓库路径用**{A}**表示
1. 首先fork项目[A]
2. 把fork过去的项目也就是你的项目clone到你的本地
3. 在命令行运行 git branch develop 来创建一个新分支
4. 运行 git checkout develop 来切换到新分支
5. 运行 git remote add upstream {A} 把项目A的仓库添加为远端库
6. 运行 git remote update更新
7. 运行 git fetch upstream gh-pages 拉取项目A的库的更新到本地
8. 运行 git rebase upstream/gh-pages 将项目A的更新合并到你的分支

这是一个初始化流程，只需要做一遍就行，之后请一直在develop分支进行修改。

如果修改过程中项目A的库有了更新，请重复6、7、8步。

修改之后，首先push到你的库，然后登录GitHub，在你的库的首页可以看到一个 pull request 按钮，点击它，填写一些说明信息，然后提交即可