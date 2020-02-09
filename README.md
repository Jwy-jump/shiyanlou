# shiyanlou
利用命令行提交代码步骤
进入你的项目目录
1：拉取服务器代码，避免覆盖他人代码
git pull
2：查看当前项目中有哪些文件被修改过
git status
具体状态如下：
1：Untracked: 未跟踪,一般为新增文件，此文件在文件夹中, 但并没有加入到git库, 不参与版本控制. 通过git add 状态变为Staged.
2：Modified: 文件已修改, 仅仅是修改, 并没有进行其他的操作.
3：deleted： 文件已删除，本地删除，服务器上还没有删除.
4：renamed：

3：将状态改变的代码提交至缓存
git add + 文件
git add -u + 路径：将修改过的被跟踪代码提交缓存
git add -A + 路径: 将修改过的未被跟踪的代码提交至缓存
例如：
git add -u vpaas-frontend/src/components
将 vpaas-frontend/src/components 目录下被跟踪的已修改过的代码提交到缓存中

git add -A vpaas-frontend/src/components
将 vpaas-frontend/src/components 目录下未被跟踪的已修改过的代码提交到缓存中

git add .
使用上面的命令将所有的修改的文件提交到缓存区

4：将代码提交到本地仓库中
git commit -m “修改项目代码”

5：将缓存区代码推送到Git服务器
git push

常见问题
1：误将代码提交到缓存中（利用 git add 命令误将代码提交的缓存中）
解决办法：利用 git reset 命令将撤回缓存中的代码。

2：误将代码提交到本地仓库（利用 git commit 命令误将代码提交到本地仓库）
解决办法：
git reset —hard + 版本号
彻底回退到某个版本，本地的代码也会改变上一个版本内容。
