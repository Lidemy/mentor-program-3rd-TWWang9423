## 跟你朋友介紹 Git

### 什麼是 Git？
OK，好我們現在知道 Git 是一種「版本控制系統」，那什麼叫做「版本控制系統」？或者說什麼叫做「版本」？

> 我知道，就是 version control sysytem 嘛。

那這個 version 指的到底是什麼？

其實每次新增、修改、刪除笑話內容，在你「另存新檔」的時候，這個動作所造成的結果都可以看成是一種版本。這時候問題來了，我除了想知道什麼時候新增了笑話內容以外，我還想知道那些笑話內容在什麼時候做過修改的，如果每次不管是新增、修改還是刪除，我都要不停開新資料夾或另存新檔，那真的會瘋掉。

這時候有 Git 的幫忙，可以幫你省下很多時間精力，只要你的檔案內容有任何改動，是的你沒聽錯，是「任何改動」，Git 都會幫記錄下來，而且他只記錄改動的部分，沒改動的部分他會直接從最後一次更新的時間節點，把這個沒改動的部分拉出來讓你知道，而不用自己在檔案海裡面翻騰。

Git 就是一個擅長拉葡萄的園丁（儲存庫管理者），當你想知道一串葡萄上每個葡萄的細節，他都可以很完整的、不讓任何一顆葡萄脫落的呈現在你面前，讓你知道每顆葡萄上的一切，諸如什麼時候長出來的（時間）、誰種下這顆葡萄的（作者）、誰在葡萄上面偷灑農藥(何人修改)等等，萬一對這顆葡萄不滿意，還可以砍掉再種一顆出來。

此外，你可以自己種葡萄玩（local 端），另一方面也可以透過 GitHub 遠端（remote）跟別的葡萄園園主合作，從遠端拉別人的葡萄藤嫁接在自己的葡萄身上（共同開發）。

### Git 安裝
想體驗 Git 的強大功能，首先要把它下載下來，這裡推薦[cmder](https://cmder.net/)。
安裝完成之後，就可以來大概跑個流程。

#### 進入視野
* `cd ~/desktop`
  * 把路徑切換到桌面，也就是將注意力轉移到桌面。
* `mkdir git-practice`
  * 建立 git-practice 資料夾（資料夾名稱可自訂）。
* `cd git-practice`
  * 切換至 git-practice。
* `git init`
  * Initialise，初始化，進入 Git 的版控。
> git init 指令會在目錄裡建立一個 .git 的目錄，在一些作業系統中預設為隱藏，可能需要開啟檢視隱藏檔之類的設定才看的到。   此外，.git 是 Git 版控的精華所在，一旦刪除，神仙也救不回檔案 ～。

#### 開始監控
* `touch test.txt`
  * 新增檔案：test.txt。
* `vim test.txt`
  * 輸入訊息（想寫什麼就寫什麼，有人情使喚人就是任性。）
* `git add test.txt`
  * 將檔案加入索引（index），或者說從 Working Directory 加到 Staging Area。
  * `git add .`如果有很多檔案想一次性丟到暫存區，這個指令是你的好朋友。
> **注意：Git 只在乎「檔案內容」，空資料夾的情況下輸入 git add, Git 不會理你。**

#### 進入地方再教育營
* `git commit -m "Leave some messages"`
  * 將 Staging Area 裡的檔案存進 Repository。
  * 如果檔案已存在於 Staging Area，可合併`git add` 和 `git commit`兩步驟，直接使用`git commit -am "Leave some messages"`，如果是新建立的檔案 (untracked file) ，則不能省略步驟。
> 到了這裡，等於是「完成一次備份」，commit 的同時等同宣告一個版本的建立。

#### 轉入國家集中營
* 在 GitHub 上開新專案：點選網站右上角 "+" 的 "New"。
* 在 "Repository name" 處輸入 "git_test"，後點選 "Create repository"。
* 在 local 端輸入`git remote add origin https://github.com/TWWang9423/git_test.git`
* `git push -u origin master`，將 local 端 commit 過的專案 push 至 Github 上遠端的專案裡。
  * 這裡可以看成是在遠端做備份。
  * 之後如果還有 commit 要丟遠端備份，只需要輸入 `git push origin master`。

#### 國家集中營與地方再教育營的資訊共通 
* `git pull origin master`
  * 如果遠端有新的資訊，可以直接從上面拉下來。
  
### branch 分支
* 詳情請參考我 hw1.md 中的交作業流程。
* 不同的 branch 可以進行 merge，這是多人協作時最常使用的功能。
* merge 時偶爾會發生 conflict 的情況，這通常發生在不同 branch 上，相同檔案的某個部位同時被改動，在 merge 的過程中， Git 並不知道該保留誰的那個部分，這時候就要手動解決了。

### 還有許多 Git 的功能......
諸如：
* 我不想再被 Git 版控了......
* 靠邀，不小心刪到不該刪的目錄和檔案了，該去哪救......
* 哇，剛剛的 commit 後悔了，可以拆掉不要嗎......
* 有些東西我不想被版控欸，可以抽出來嗎......

**總之 Git 還有非常多功能，有興趣的話可以自己慢慢研究，另外推薦一本我覺得還不錯的 Git 入門書籍：[為你自己學 Git](https://gitbook.tw/)**
