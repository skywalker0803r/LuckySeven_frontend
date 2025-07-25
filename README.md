# LuckySeven 前端應用

此目錄包含 LuckySeven 專案的前端應用程式。它提供了一個直觀的用戶界面，用於與後端服務進行交互，實現加密貨幣交易策略的回測、管理和實時監控。

## 主要功能

*   **K 線圖顯示**：在主頁面 (index.html) 上，用戶可以查看實時或歷史的加密貨幣 K 線圖。支持選擇不同的交易對、時間間隔和日期範圍。
*   **策略編輯與回測**：用戶可以在主頁面編輯和運行交易策略的回測。回測結果會以詳細的指標和圖表形式展示，包括策略資產曲線、買入持有資產曲線、價格序列和實際交易買賣點。
*   **策略保存**：用戶可以將編輯好的策略保存到後端數據庫中，以便後續管理和運行。
*   **策略儀表板**：在儀表板頁面 (dashboard.html) 上，用戶可以查看所有已保存的策略列表，並對策略進行啟動、停止和刪除操作。
*   **策略實時監控**：在策略監控頁面 (strategy_monitor.html) 上，用戶可以實時查看正在運行策略的詳細信息，包括其 K 線圖上的交易信號、權益曲線和詳細的交易日誌。

## 技術棧

*   **HTML5**：頁面結構。
*   **Tailwind CSS**：用於快速構建響應式和美觀的用戶界面。
*   **jQuery**：簡化 DOM 操作和事件處理。
*   **D3.js**：強大的數據可視化庫，用於繪製圖表。
*   **TechanJS**：基於 D3.js 的金融圖表庫，專門用於繪製 K 線圖。
*   **JavaScript (ES6+)**：前端邏輯和與後端 API 的交互。

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
