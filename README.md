# IP 防護測試實驗室｜IEC 60529 IP Test Lab

IEC 60529 IP 防護等級（Ingress Protection）測試手法的中英雙語動畫教學網頁。每一個 IP 數字背後都有一套測試設備，這個網頁用動畫把它們演示出來，並附上標準原文的參數。

An animated, bilingual (繁體中文 / English) guide to how IEC 60529 IP ratings are actually tested.

**網站 Live site：** https://iec60529-ip-test-lab.vercel.app/

---

## 功能

| 區塊 | 內容 |
|---|---|
| IP 銘牌解碼器 | 點選第一、第二位數，顯示意義，並切換到對應的測試動畫 |
| 第一位數測試台 | IP1X–IP4X 探棒動畫：拖動「開口尺寸」「危險部位深度」滑桿，即時判定通過與否（含 40–50 V 信號燈）<br>IP5X／IP6X 粉塵艙動畫：切換 Category 1／2、調整抽氣速率，自動算出 2 h～8 h 測試時間 |
| 第二位數測試台 | IPX1–IPX9 九種動畫：滴水箱＋轉盤、傾斜 15°、擺動管（可切換手持噴嘴）、6.3／12.5 mm 噴水嘴、浸水深度規則（<850 mm／≥850 mm）、IPX9 80 °C 高壓扇形噴嘴 |
| 雙重標示產生器 | 勾選通過的測試，產生正確標示（例如 IPX6/IPX7），並判斷 Versatile／Restricted 用途 |
| 參數速查表 | Table 6–9 全部參數，含 IPX3／IPX4 擺動管孔數與總水量、IPX9 與車用 IPX9K 比較 |
| 中英術語對照 | 29 個標準與實驗室常用詞 |
| 小測驗 | 6 題，涵蓋最常見的誤解（例如 IP67 能不能沖水） |

右上角可切換 **中文／EN／雙語** 三種模式，選擇會記在瀏覽器中。

## 常見誤解（網頁中都有說明）

- **IP67 不代表能抗水柱**：IPX7／IPX8 不往下涵蓋 IPX5／IPX6，要兩者都宣告必須雙重標示，例如 IP66/IP67。
- **IPX3／IPX4 不一定是 10 L/min**：10 L/min 只適用手持噴嘴；擺動管法依管半徑查 Table 9，最多 7 L/min。
- **IP2X 試驗指是 10 N**：30 N 是 Ø12.5 mm 物體探棒球的力。
- **IP6X 一律抽負壓**：不論外殼是否真的有壓差，都當 Category 1，負壓上限 2 kPa。
- **IPX7 深度看外殼高度**：高度 <850 mm 最低點在水下 1 m；≥850 mm 最高點在水下 0.15 m。

## 檔案結構

```
index.html                       單檔網頁（HTML + CSS + Canvas 動畫，無建置步驟）
IEC 60529 測試手法研究筆記.md     參數整理、條文出處、實務踩坑
工作筆記.md                       開發紀錄
.vercelignore                    排除 *.md，網站只公開 index.html
```

## 部署與更新

- 平台：Vercel（已連結本 repo），push 到 `main` 會自動部署。
- 更新流程：修改 `index.html` → commit → push。
- 本機預覽：直接用瀏覽器開啟 `index.html` 即可，不需要伺服器。
- 外部資源只有 Google Fonts，其餘 CSS／JS 全部內嵌。

## 資料來源

- **IEC 60529:1989 + A1:1999 + A2:2013**（合併版 Ed. 2.2）原文，美國聯邦法規 IBR 公開版：
  https://law.resource.org/pub/us/cfr/ibr/inc/iec/iec.60529.2013.pdf
- IPX9 與 ISO 20653 IPX9K 比較為外部整理資料（Video Experts Group、ITS GmbH、DLS EMC），**未對照 ISO 20653 原文**。

## 注意事項

- 動畫為示意，未按比例繪製。
- IPX9 動畫的 4 個噴射位置只示意角度分布，0° 的基準方向以標準 Figure 12 為準。
- 標準多處允許產品標準（product standard）另行規定樣品數、安裝、是否通電與允許進水量；正式送測請以最新版標準與產品標準為準。
