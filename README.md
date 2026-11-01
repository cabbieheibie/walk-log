# 走路日記（PWA）

走路機每日紀錄：日期、體重、中午／晚上走路分鐘（自動加總）、每月成績單＋勵志小語、JSON 備份。
純前端、零套件，資料只存在手機瀏覽器（localStorage）。

## 放到網路上（才能「加到主畫面」並離線使用）
PWA 需要 HTTPS，最簡單是 GitHub Pages：
1. 建一個 repo，把這個資料夾的所有檔案放在根目錄（index.html、manifest.json、sw.js、icons/）
2. Settings → Pages → Branch: main / root → Save
3. 用 iPhone Safari 開 `https://<帳號>.github.io/<repo>/` → 分享 → 加入主畫面

本機測試：`python3 -m http.server 8000`，開 http://localhost:8000

## 更新程式後
把 `sw.js` 第 3 行的 `CACHE` 版本號 +1，手機才會換成新版。

## 備份
設定頁 → 備份（分享／存到「檔案」）。匯入採「合併」：同一天以備份檔為準。
