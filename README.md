# github-forks-delete
:fork_and_knife:该项目使用Node和Shell来批量删除github的项目

:computer:刚开始玩Github随手fork了很多项目，毕竟那时年轻，生怕作者删库啊，前几日整理发现已经fork了几百项目，想着删除一批，然而手动删了十来个就抓狂了，Github删除项目的步骤也太多了，抱着试试看的心态找了几个项目,测试下来只有[Peripona/bulk-clean-repos](https://github.com/Peripona/bulk-clean-repos)成功了，再次感谢下作者！

### 步骤：
1. 打开`fetchSaveRepo.js`，修改`repoUrl`为自己的url
2. 执行`node fetchSaveRepo.js`来生成自己的项目列表到`repos.txt`
3. 生成一个拥有删除项目权限的[Authorization Token](https://github.com/settings/tokens/new)
4. 修改`deleteRepos.sh`文件中对应`*******************`为生新成的token
5. 执行`./deleteRepos.sh`

>注：

* 如果运行中报错请按照提示安装相应模块
* 如果想保留部分项目，可以将不想删除的项目从生成的`repos.txt`文件列表中移除即可，如果项目过多，后续每次执行生成项目目录前记得清空`repos.txt`
* 测试环境：macos+node
