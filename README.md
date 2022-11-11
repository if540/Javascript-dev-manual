# Javascript-dev-manual
Javascript 開發手冊

> 不要問我標準答案是什麼，過程中有問題會跟你互動。 - 川升 總經理

[Vue3 源碼深入](https://www.bilibili.com/video/BV1NB4y157w3?p=5)

[線上簡歷開源項目](https://github.com/huajian-pro/resume-design)

[[Javascript] 初探Regex 正規表達式](https://moojing.medium.com/javascript-%E5%88%9D%E6%8E%A2regex-%E6%AD%A3%E8%A6%8F%E8%A1%A8%E9%81%94%E5%BC%8F-1da2f4d94795)

[如何設計一個屬性面板](https://zhuanlan.zhihu.com/p/481756755)

[基於設計稿識別的可視化低程式碼系統實踐](https://segmentfault.com/a/1190000042292787)

[前端工程師面試問題集](https://h5bp.org/Front-end-Developer-Interview-Questions/translations/chinese-traditional/)

[the SOLID](https://medium.com/backticks-tildes/the-s-o-l-i-d-principles-in-pictures-b34ce2f1e898)

[30secondsofcode](https://www.30secondsofcode.org/)

[Flexbox佈局中不為人知的細節](https://juejin.cn/post/6938292463605907492)

[JAMstack 到底是什麼巫術？](https://ithelp.ithome.com.tw/articles/10235208)

[Flex/Grid Layout Modules](https://blog.hinablue.me/viewport-the-css-device-adaptation/)

[Codepen trending](https://codepen.io/tag/trending)

[Flexbox Playground](https://flexbox.netlify.app/)

[CSS Grid Cheat Sheet](https://alialaa.github.io/css-grid-cheat-sheet/)

[盆栽瀏覽器](https://bonsaibrowser.com/)

[javascript-make-iterable](https://www.30secondsofcode.org/articles/s/javascript-make-iterable)

[採用 TypeScript 前你該考慮的十件事 | Jeremy Lu](https://youtu.be/EEdd8zov4-w?t=861) - xstate.js

[XState Fundamentals with David Khourshid, Founder of Stately](https://www.youtube.com/watch?v=BJfeWEPBZXQ)

[Awesome-WebAssembly-Applications](https://github.com/mcuking/Awesome-WebAssembly-Applications)

[Learn Responsive Sizing with these 4 Simple Concepts](https://www.youtube.com/watch?v=j-tiO0gadeg)

[Github Repo Using Semantics](https://github.com/JuanitoFatas/git-style-guide)

[netlify cms](https://app.netlify.com/)

[i18next](https://www.i18next.com/)

[candlestick-charts ](https://apexcharts.com/vue-chart-demos/candlestick-charts/basic/)

[deck-of-cards](https://github.com/deck-of-cards)

[前端收藏，常用在線圖片網站](https://juejin.cn/post/7041382036145176583#heading-9)

## GIT 版控

- git merge [分支名] --no-ff [Day 13 - 你的就是我的 再談 git merge](https://ithelp.ithome.com.tw/articles/10222637)
- git checkout -b [分支名] [HASH Code] [Day 26 - GIT 狀況題 03 不小心把還沒合併到主分支的分支刪除了，該怎麼辦？](https://ithelp.ithome.com.tw/articles/10227305)
- git remote update -p [同步遠端分支](https://zlargon.gitbooks.io/git-tutorial/content/remote/delete_branch.html)，並且移除過時的遠端分支
- git pull origin master 把遠端的 master 內容更新到所在分支上
- git pull . master 把本機的 master 內容更新到所在分支上
- [合併多個 commit](https://dev.to/pb/git-squash-simplified-3ba1)

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

# 合併多個 commit 為一個
git rebase -i HEAD~N
```

```shell
# 比較不同分支間的檔案差異
# git diff <branch1> <branch2> -- <file>
git diff master dev -- file/path

# 查找完整路徑
git ls-files

# 比較不同 merge commit
git diff fc17405...ee2de56

# 檢示紀錄 (今天早上 9 點到 12 點之間所有的 Commit)
git log --oneline --since="9am" --until="12am"
```

```shell
# 救回誤刪的 stash
git fsck --unreachable
git show <sha>
```

GIT 學習文章

- [遠端數據庫託管與操作](https://awdr74100.github.io/2020-04-18-git-remote/)
- [cherry-pick 撿回某 commit 放到暫存不直接 commit](https://gitbook.tw/chapters/faq/cherry-pick.html)
- [Git衝突：commit your changes or stash them before you can merge.](https://blog.csdn.net/liuchunming033/article/details/45368237)
- [cherry-pick 假設我們在branch cr1 上開發了好幾個功能，要先上前面部分功能，某些不需要](https://ithelp.ithome.com.tw/articles/10187976)
- [Git 比較不同分支間的檔案差異 diff files in two branches](https://matthung0807.blogspot.com/2019/11/git-diff-files-in-two-branches.html)
- [分支 比對](https://git-scm.com/docs/git-diff#Documentation/git-diff.txt-Comparingbranches)
- [使用 git rebase 避免無謂的 merge](https://ihower.tw/blog/archives/3843)
- [檢視紀錄](https://gitbook.tw/chapters/using-git/log.html)
- [救回誤刪的 stash1](https://www.jianshu.com/p/ae1987efec61)、[救回誤刪的 stash2](https://zhuanlan.zhihu.com/p/28948567)

### 正規表達式

```js
// 排除關鍵字 json
/\.js(?!on)|\.css$/
```

### test

```shell
yarn add --dev jest @types/jest
```

```shell
yarn add -D babel-jest @babel/core @babel/preset-env
```

```js
// babel.config.js
module.exports = {
  presets: [
    [
      '@babel/preset-env',
      {
        targets: {
          node: 'current',
        },
      },
    ],
  ],
};
```

環境設定參考:

- [jest build test env](https://titangene.github.io/article/jest-build-test-env.html)

### Server 參考：

- [litespeedtech](https://litespeedtech.com/)
- [nss](https://www.nss.com.tw/wordpresshosting/)
- [網易資訊](https://wanteasy.com.tw/litespeed-web-server.html)
- [LiteSpeed 主機架站，最簡單有效的速度優化方式](https://kamadiam.com/litespeed-web-server-hosting/)
