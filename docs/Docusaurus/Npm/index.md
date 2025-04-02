# Npm

npm（Node Package Manager)

`package.json`
package.json設定所使用到的library到底有什麼，並記錄所有的dependency(依賴)關係。

`package-lock.json`
讓不同環境中的專案在每次部屬時，保持一樣的版本。

1. 每次 npm install / uninstall /update 都會更新
2. 紀錄每個套件的詳細版本
3. 紀錄套件的 tarball(套件壓縮檔)，是從哪個 url 下載來的
4. 使用 hash(雜湊)，確認檔案是否損壞
5. 以一個 require 欄位，說明這個 dependency　是被哪個函式庫所要求的

`node_modules`
套件的實際儲存位置
