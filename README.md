# LuckySeven 前端應用

此目錄包含 LuckySeven 專案的前端應用程式。它提供了一個直觀的用戶界面，用於與後端服務進行交互，實現加密貨幣交易策略的回測、管理和實時監控。

## 主要功能

*   **加密貨幣 K 線圖**：在 `index.html` 主頁面，用戶可以選擇不同的交易對、時間間隔和日期範圍，從後端獲取並顯示加密貨幣的歷史 K 線數據。圖表使用 D3.js 和 TechanJS 繪製。
*   **策略編輯器與回測**：用戶可以在 `index.html` 中選擇現有策略或直接編輯策略代碼。通過指定交易對、時間間隔和日期範圍，運行策略回測。回測結果會展示詳細的績效指標，並以圖表形式呈現策略資產曲線、買入持有資產曲線、價格序列以及買賣點信號。
*   **策略保存**：用戶可以將自定義或修改後的策略代碼保存到後端數據庫中，以便後續使用和管理。
*   **策略儀表板**：`dashboard.html` 頁面提供已保存策略的管理界面，用戶可以查看、啟動、停止和刪除策略。
*   **策略實時監控**：`strategy_monitor.html` 頁面用於實時監控正在運行的策略，顯示其交易日誌、權益曲線和 K 線圖上的交易信號。

## 技術棧

*   **HTML5**：構建頁面結構。
*   **Tailwind CSS**：用於快速構建響應式和美觀的用戶界面。
*   **jQuery**：簡化 DOM 操作和事件處理，用於處理頁面交互和 AJAX 請求。
*   **D3.js**：強大的數據可視化庫，特別用於處理和綁定數據到 DOM 元素，是 TechanJS 的基礎。
*   **TechanJS**：基於 D3.js 的金融圖表庫，專門用於繪製 K 線圖和相關技術指標。
*   **JavaScript (ES6+)**：實現前端邏輯，包括數據獲取、圖表繪製、事件處理和與後端 API 的交互。

## 目錄結構

*   `index.html`：前端應用程式的主入口點，包含 K 線圖、策略編輯器和回測功能。
*   `dashboard.html`：策略儀表板頁面，用於管理已保存的策略。
*   `strategy_monitor.html`：策略實時監控頁面，顯示運行中策略的詳細數據和圖表。
*   `config.js`：包含前端應用程式的配置，例如後端 API 的 URL。
*   `.git/`：Git 版本控制相關文件。
*   `README.md`：此文件。

## 如何運行前端

1.  **確保後端服務正在運行**：
    前端應用程式需要後端服務提供數據和 API 支持。請確保您已按照 `LuckySeven_backend/README.md` 中的說明啟動了後端服務。
2.  **打開 `index.html` 或 `dashboard.html`**：
    由於這是一個純前端應用，您無需啟動任何服務器。只需在您的網絡瀏覽器中直接打開 `LuckySeven_frontend/index.html` 或 `LuckySeven_frontend/dashboard.html` 文件即可。

    例如，如果您在本地文件系統中，可以直接雙擊 `index.html` 文件，或者在瀏覽器中輸入類似 `file:///C:/Users/YourUser/Desktop/LuckySeven/LuckySeven_frontend/index.html` 的路徑。

    **注意**：由於瀏覽器的安全限制 (CORS)，直接通過 `file://` 協議訪問時可能會遇到一些問題，尤其是在與後端 API 交互時。建議使用一個簡單的本地 Web 服務器來提供這些文件，例如 Python 的 `http.server`：

    ```bash
    # 在 LuckySeven_frontend/ 目錄下運行
    python -m http.server 8000
    ```
    然後在瀏覽器中訪問 `http://localhost:8000/index.html`。

現在，前端應用程式已準備就緒，可以與後端服務進行交互。
