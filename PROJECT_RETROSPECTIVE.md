# 技術回顧｜Vue 3 計算機練習

## 專案定位

本 Repository 以兩份單頁 HTML 練習 Vue 3 的基本互動模式。功能範圍是四則運算與簡單歷史紀錄，適合作為前端框架入門實作，不應包裝成完整產品。

## 可確認的實作

### 資料綁定
- 使用 `Vue.createApp()` 建立 Vue 應用。
- 透過 `data()` 提供數字、運算子、結果及歷史紀錄等狀態。
- 使用 `v-model.number` 將輸入欄位與數值狀態綁定。

### 事件與條件邏輯
- 使用 `@click` 綁定運算子選擇與計算事件。
- 透過 `switch` 依運算子執行加減乘除。
- 使用 `:class` 根據目前選取的運算子切換按鈕樣式。

### 列表渲染與介面
- 使用 `v-for` 顯示計算歷史。
- 計算完成後將運算式與結果組成字串，加入 history array。
- 使用 Bootstrap 5 grid、form 與 button 樣式建立版面。

## 技術能力紀錄

- HTML / JavaScript
- Vue 3 Options API
- Reactive data binding
- Event handling
- Dynamic class binding
- List rendering
- Bootstrap 5

## 靜態檢視發現

1. 初始 `operator` 值為 `add`，但計算邏輯只處理 `+`、`-`、`*`、`÷`。首次操作若未先選擇運算子，switch 不會執行四則運算分支。
2. 除法沒有處理除數為零的情況。
3. 輸入欄位在計算後被設為空字串，沒有額外驗證空值或無效數值。
4. `calculator.html` 的 `clearHistory()` 使用 `pop()`，只移除最後一筆紀錄，並非清空整個陣列。
5. 兩份 HTML 是相近的練習版本，不能當成兩個獨立作品計算。

## 驗證範圍

本回顧依目前 HTML / JavaScript 原始碼靜態整理，沒有重新執行瀏覽器測試，也沒有宣稱所有輸入情境均已處理。
