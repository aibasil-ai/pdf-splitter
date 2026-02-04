## Purpose

定義多檔 PDF 依上傳順序合併為單一 PDF 的行為與輸出要求。

## Requirements

### Requirement: 接受多個 PDF 檔案合併
系統 SHALL 允許使用者在「多檔合併」模式一次選取多個 PDF 檔案作為合併來源。

#### Scenario: 允許多檔選取
- **WHEN** 使用者在多檔合併模式選取兩個以上 PDF 檔案
- **THEN** 系統接受所有被選取的 PDF 檔案作為合併來源

### Requirement: 合併時保留上傳順序
系統 SHALL 依使用者選取檔案的順序進行合併，後選取的檔案內容 MUST 接在先選取的檔案內容之後。

#### Scenario: 合併順序被保留
- **WHEN** 使用者依序選取 A、B、C 三個 PDF 檔案
- **THEN** 合併輸出 PDF 的頁面順序為 A 的所有頁面、接著 B 的所有頁面、最後 C 的所有頁面

### Requirement: 產出單一合併 PDF
系統 SHALL 在合併完成後產生單一合併 PDF 並觸發下載。

#### Scenario: 下載合併 PDF
- **WHEN** 合併流程成功完成
- **THEN** 系統下載一個包含所有來源檔案頁面的單一 PDF 檔案

### Requirement: 拒絕非 PDF 檔案
系統 MUST 拒絕任何非 PDF 的檔案，並 MUST 提示錯誤訊息以告知使用者。

#### Scenario: 選取非 PDF 檔案
- **WHEN** 使用者在多檔合併模式選取包含非 PDF 的檔案
- **THEN** 系統拒絕該檔案並顯示錯誤提示

### Requirement: 驗證合併輸入非空
系統 MUST 在未選取任何檔案時阻止合併流程，並 MUST 顯示提示訊息。

#### Scenario: 未選取任何檔案
- **WHEN** 使用者未選取任何檔案即嘗試合併
- **THEN** 系統不執行合併並顯示提示訊息
