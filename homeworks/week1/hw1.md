## 交作業流程
1. 切換到 \mentor-program-3rd-TWWang9423\homeworks\week1 的目錄底下。
   `cd \mentor-program-3rd-TWWang9423\homeworks\week1`
2. 建立一個名為 "week1" 的 new branch。
   `git branch week1`
   > 這一步至關重要，寫作業前永遠記得先建立一個 new branch。
3. 從當前的 "master" 切換到 "week1" 這個新分支。
   `git checkout week1`
4. 開始做作業，叫出 vim 編輯作業內容。
   `vim hw1.md`
   * 輸入以上內容後按下 enter 鍵進入 vim 的普通模式，再按 I 鍵進入「插入模式」開始輸入內容。
   * 待輸入完畢後按 Esc 鍵回到普通模式，回普通模式後鍵入 ":wq" 以存檔並離開 vim 編輯器。
   * 其他作業的流程與此相同。
5. 將完成作答或修改的作業內容進行 commit。
     ```
     git commit -am "*leave your own message here*"。
     ```
     > 注意，兩步驟可以合併的前提是檔案「已經存在」 Staging Area，也就是已存在的檔案經過修改後，可逕行移至 Repository。
6. 都完成 commit 後，上傳到 GitHub 上：
   `git push origin week1`
7. 請求跟 master 合併，點右上方綠色按鈕 "Compare & pull request"，鍵入標題和內容後點 "Create pull request"。
> 完成後記得複製網址。
8. 到[作業區] (https://github.com/Lidemy/homeworks-3rd/issues) creat an issue，內容貼上剛剛複製的網址。
> issue 的標題必須按照格式。
9. 確認作業已通過，自己的 issue 是 closed 的狀態，將分支切回原本的 master。
   `git checkout master`
10. 回到 master 後，將 GitHub 上已經經過 merge 的東西，拉下來與 local 端進行同步。
   `git pull origin master`
11. 將原本做作業用的分支刪除。
   `git branch -d week1`

* 作業若需要修改從 step 1 開始
