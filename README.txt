韓文初級單字卡（自架版）
======================

收錄兩份單字：
- TOPIK I 1671（TOPIK-I-1671.pdf）
- 初級必備單字（第二本書，書本 pp.198–292：主題單字、代名詞與副詞、格式體、打招呼用語、慣用語、數字時間、必背單字表）
兩本都有的字合併成同一張卡，卡片上會標出 TOPIK 編號和書中頁碼（★ 為書中標示的重要程度）。

檔案
- index.html               網頁本體
- words.js                 單字資料（一行一個單字，可直接用文字編輯器修改）
- words.csv                同一份資料的表格版，方便用 Excel／Google 試算表檢查（網頁不會讀它）
- manifest.webmanifest、icon-*.png、apple-touch-icon.png   加入主畫面用的設定與圖示
- sw.js                    離線快取

最簡單的上架方式（免費）
1. 打開 https://app.netlify.com/drop ，把整個 topik1-cards 資料夾拖進去，會得到一個 https 網址。
   或：建立 GitHub 儲存庫，上傳這些檔案，開啟 Settings › Pages。
2. 用手機打開那個網址。
   - iPhone（Safari）：分享按鈕 › 加入主畫面
   - Android（Chrome）：右上角 ⋮ › 加到主畫面／安裝應用程式

注意
- 直接在電腦雙擊 index.html 也能用，但離線快取與加入主畫面需要 https 網址。
- 進度存在各自瀏覽器裡；自架版和 Claude 上的版本進度不互通。

修改單字資料（words.js）
每個單字長這樣：
{"id": 2, "no": 2, "ko": "가격", "en": "price", "cat": "shop", "senses": [{"zh": "價格、價錢", "origin": "漢字詞", "hanja": "價格"}], "b": [["list", 252, 2]]}
- id：卡片編號（1–1671 與 TOPIK 編號相同；2001 起是第二本書新增的字）。進度和標記依這個編號保存，請不要改動。
- no：TOPIK 編號（只在 TOPIK 裡的字才有）    ko：韓文    en：TOPIK PDF 的英文
- cat：分類代號（檔案上方 categories 有對照表）
- senses：意思清單；origin 可填 漢字詞／固有詞／外來語／混種詞／片語／待確認；hanja 是漢字（沒有就省略）
- note：附註（可省略）
- b：第二本書的出處 [章節, 頁碼, 序號, 星等]；章節代號見檔案上方 meta.sections
改完存檔，重新整理網頁即可。
