## 請解釋後端與前端的差異。

### 前端
* 點開瀏覽器後，所有「看的到」的部分，都屬於前端的範疇。
* 前端三本柱：
  * HTML：骨架，沒有它什麼都沒有，三個組成當中最重要的。
  * CSS：外衣，沒有依然能夠讀介面的內容，只不過沒有排版會變非常醜。
  * JavaScript：與使用者互動，讓使用者有更好的體驗。
### 後端
* 「看不到」的部分
* Server 和 Database 的天下，負責資料的儲存和資料傳遞的中轉站。

## 假設我今天去 Google 首頁搜尋框打上：JavaScri[t 並且按下 Enter，請說出從這一刻開始到我看到搜尋結果為止發生在背後的事情。
1. Client 端（客戶端）送出 關鍵字"JavaScript" 的 request 給 Server。
2. Server 拿著關鍵字到 database 裡找，把含有 "JavaScript" 這個關鍵字的資料找出來。
3. Server 收到來自 database 裡含有 "JavaScript" 關鍵字的資料，並 response 回 client 端。
4. client 端收到來自 server 的資料，並呈現給使用者。

## 請列舉出 5 個 command line 指令並且說明功用
1. `color`：設定預設主控台的前景和背景色彩。
2. `comp`：比較兩個或兩組檔案的內容。
3. `exit`：離開 cmd.exe 程式 （命令直譯器）。
4. `help`：為 Windows 命令提供說明資訊。
5. `print`：列印檔案。
