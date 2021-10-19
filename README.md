# Javascript-dev-manual
Javascript 開發手冊

> 不要問我標準答案是什麼，過程中有問題會跟你互動。 - 川升 總經理

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

[Awesome-WebAssembly-Applications](https://github.com/mcuking/Awesome-WebAssembly-Applications)

## GIT 版控

- git merge [分支名] --no-ff [Day 13 - 你的就是我的 再談 git merge](https://ithelp.ithome.com.tw/articles/10222637)
- git checkout -b [分支名] [HASH Code] [Day 26 - GIT 狀況題 03 不小心把還沒合併到主分支的分支刪除了，該怎麼辦？](https://ithelp.ithome.com.tw/articles/10227305)
- git remote update -p [同步遠端分支](https://zlargon.gitbooks.io/git-tutorial/content/remote/delete_branch.html)，並且移除過時的遠端分支
- git pull origin master 把遠端的 master 內容更新到所在分支上
- git pull . master 把本機的 master 內容更新到所在分支上

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
- [cherry-pick 假設我們在branch cr1 上開發了好幾個功能，要先上前面部分功能，某些不需要](https://ithelp.ithome.com.tw/articles/10187976)

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
