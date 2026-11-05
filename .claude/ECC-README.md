# 從 ECC 挑選安裝的 Claude Code 工具

來源：[affaan-m/ECC](https://github.com/affaan-m/ECC)（舊名 everything-claude-code）v2.2.3，
commit `b38be6a7f6350964d59328b52f0624e1d1d552d1`（2026-10-29）。
檔案內容與原作者版完全相同，未做修改。授權為 MIT，見 `ECC-LICENSE`。

只挑了 9 個跟 Python／機器學習相關的元件，沒有安裝 hooks、規則（rules）和 MCP 設定。

| 類型 | 名稱 | 用途 |
|---|---|---|
| 指令 | `/plan` | 先整理需求、列出風險和步驟，等你確認後才開始改程式 |
| 指令 | `/build-fix` | 程式跑不起來或編譯錯誤時，一次修一個錯誤 |
| 指令 | `/python-review` | 檢查 Python 程式的寫法、型別、安全問題 |
| 代理 | `planner` | 規劃複雜功能的子代理 |
| 代理 | `python-reviewer` | `/python-review` 會呼叫的審查子代理 |
| 代理 | `build-error-resolver` | 修建置錯誤的子代理（偏向 TypeScript／JavaScript 專案） |
| 技能 | `python-patterns` | Python 慣用寫法、型別提示、PEP 8 |
| 技能 | `python-testing` | 用 pytest 寫測試 |
| 技能 | `pytorch-patterns` | PyTorch 模型、訓練迴圈、資料載入的寫法 |

技能不用手動呼叫，Claude 寫到相關程式時會自動參考。

## 更新或移除

- 更新：從原作者 repo 重新複製同名檔案覆蓋即可。
- 移除：刪掉對應的檔案或資料夾即可，沒有其他地方需要清理。
