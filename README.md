# Hand-Tracking-Machine-Hand
這個專案使用 MediaPipe 進行手部追蹤，根據手勢控制 Arduino 上的伺服馬達。程式透過攝影機檢測手部姿勢，將手勢轉換為 6 位二進位編號（5 根手指 + 額外角度），並透過序列埠傳送給 Arduino 驅動機械手。
# 功能介紹
- **手部追蹤**：使用 MediaPipe 檢測手部關鍵點，計算手指關節角度。
- **手勢識別**：將手勢轉換為 64 種可能的編號（0-63）。
- **Arduino 通訊**：透過序列埠將手勢編號傳送給 Arduino。
- **機械手控制**：Arduino 根據收到的編號控制 6 個伺服馬達。
- **螢幕顯示**：即時顯示手部關鍵點、角度與手勢編號。
# 內容分類
將完整程式碼依不同功能進行分離。
- **Main**：完整的動作捕捉、手勢邏輯與訊息傳輸程式
- **手部動作追蹤與螢幕顯示**：用於追蹤與影像處理之部分
- **通訊與傳輸**：透過pySerial，使Python與Arduino進行通訊之部分。
- **手掌馬達控制**：用於控制手掌的.ino程式碼，處理接收到的手勢資訊並執行。
# 使用函式庫
使用 pip 進行安裝。
- **mediapipe**
- **opencv-python**
- **numpy**
- **pyserial**
