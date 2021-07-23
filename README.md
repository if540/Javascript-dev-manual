# Javascript-dev-manual
Javascript 開發手冊

## GIT 版控

- git remote update -p [同步遠端分支](https://zlargon.gitbooks.io/git-tutorial/content/remote/delete_branch.html)，並且移除過時的遠端分支
- git pull origin master 把 master 的內容更新到所在分支上

```shell
# gitlab 載回分支

git clone --single-branch --branch <branchname> <remote-repo>
# EX: git clone --single-branch -b XxxxGame https://git.xxx.com/xxx-xxx/xxxxx.git

# 更動加入暫存
git add .

# 暫存 commit
git commit -m "標題" 
 
# git push 推送
git push origin <分支名稱>

# git pull 取回
git pull origin master
```

GIT 學習文章

- [遠端數據庫託管與操作](https://awdr74100.github.io/2020-04-18-git-remote/)
