# Javascript-dev-manual
Javascript 開發手冊

> 不要問我標準答案是什麼，過程中有問題會跟你互動。 - 川升 總經理

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

# cherry-pick 撿回某 commit 放到暫存不直接 commit
git cherry-pick 6a498ec --no-commit
```

GIT 學習文章

- [遠端數據庫託管與操作](https://awdr74100.github.io/2020-04-18-git-remote/)
- [cherry-pick 撿回某 commit 放到暫存不直接 commit](https://gitbook.tw/chapters/faq/cherry-pick.html)
- [Git衝突：commit your changes or stash them before you can merge.](https://blog.csdn.net/liuchunming033/article/details/45368237)
