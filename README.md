**快速设置— 如果你知道该怎么操作，直接使用下面的地址**


我们强烈建议所有的git仓库都有一个`README`, `LICENSE`, `.gitignore`文件

初始化 readme 文件

Git入门？查看 [帮助](https://gitee.com/oschina/git-osc/wikis/%E5%B8%AE%E5%8A%A9) , [Visual Studio](https://gitee.com/help/articles/4118) / [TortoiseGit](http://my.oschina.net/longxuu/blog/141699) / [Eclipse](https://gitee.com/help/articles/4119) / [Xcode](http://my.oschina.net/zxs/blog/142544) 下如何连接本站, [如何导入仓库](http://www.oschina.net/question/82993_133520)

# 简易的命令行入门教程:

## Git 全局设置:

git config --global user.name "space704034204"
git config --global user.email "704034204@qq.com"

## 创建 git 仓库:

mkdir obsidian_repo_lx
cd obsidian_repo_lx
git init 
touch README.md
git add README.md
git commit -m "first commit"
git remote add origin https://gitee.com/space704034204/obsidian_repo_lx.git
git push -u origin "master"

## 已有仓库?

cd existing_git_repo
git remote add origin https://gitee.com/space704034204/obsidian_repo_lx.git
git push -u origin "master"