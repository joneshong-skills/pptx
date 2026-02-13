[English](README.md) | [繁體中文](README.zh.md)

# PPTX 技能

一個用於建立、讀取和編輯 PowerPoint 簡報 (.pptx 檔案) 的 Claude Code 技能。

## 功能特色

- **讀取與分析**: 使用 markitdown 擷取文字，產生視覺化縮圖概覽
- **從範本編輯**: 解包/重新打包 XML 工作流程，精確進行範本編輯
- **從頭建立**: 使用 PptxGenJS 產生簡報，完整設計控制
- **視覺 QA**: 轉換為圖片進行自動化投影片檢查與驗證
- **XML 驗證**: 基於 Schema 的 Office Open XML 結構驗證

## 安裝

```bash
# 複製到你的技能目錄
cp -r pptx/ ~/.claude/skills/pptx/
```

### Python 相依套件

```bash
pip install "markitdown[pptx]" Pillow
```

### Node.js 相依套件

```bash
npm install -g pptxgenjs
```

### 系統相依套件 (macOS)

```bash
brew install libreoffice poppler
```

## 使用方式

直接請 Claude 處理 PowerPoint 檔案：

- 「建立一份關於 AI 趨勢的簡報」
- 「讀取 presentation.pptx 的內容」
- 「編輯我範本裡的投影片」
- 「從這份大綱產生 10 頁簡報」
- 「從這份簡報擷取文字」

## 檔案結構

```
pptx/
  SKILL.md              -- 主要技能指引
  references/
    editing.md          -- 範本編輯指南
    pptxgenjs.md        -- PptxGenJS 建立指南
  scripts/              -- Python 輔助腳本
    add_slide.py        -- 新增投影片
    clean.py            -- 清理 XML 產物
    thumbnail.py        -- 產生投影片縮圖
    office/             -- Office XML 工具
      pack.py           -- 將 XML 打包回 .pptx
      unpack.py         -- 將 .pptx 解包為 XML
      validate.py       -- XML Schema 驗證
      soffice.py        -- LibreOffice 包裝器
      helpers/          -- XML 處理輔助模組
      schemas/          -- Office Open XML Schema
      validators/       -- 格式專屬驗證器
  assets/               -- (保留供未來資源使用)
```

## 授權

專有授權。完整條款請見 LICENSE.txt。

## 來源

改編自 [anthropics/skills](https://github.com/anthropics/skills/tree/main/skills/pptx)。
