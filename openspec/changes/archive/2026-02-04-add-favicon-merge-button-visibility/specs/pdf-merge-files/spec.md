## MODIFIED Requirements

### Requirement: 產出單一合併 PDF
系統 SHALL 在合併完成後產生單一合併 PDF 並觸發下載。

#### Scenario: 下載合併 PDF
- **WHEN** 使用者在多檔合併模式上傳至少一個 PDF 檔案
- **THEN** 「下載合併後的 PDF」按鈕顯示

#### Scenario: 下載合併 PDF
- **WHEN** 使用者尚未上傳任何 PDF 檔案
- **THEN** 「下載合併後的 PDF」按鈕不顯示

#### Scenario: 下載合併 PDF
- **WHEN** 合併流程成功完成
- **THEN** 系統下載一個包含所有來源檔案頁面的單一 PDF 檔案
