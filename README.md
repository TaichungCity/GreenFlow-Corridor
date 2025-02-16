# 綠行幹道(GreenFlow-Corridor)
主幹道交通號誌時空圖模擬器 (Traffic Signal Time-Space Diagram Simulator)

本模擬器是一個互動式交通號誌時空圖模擬系統，旨在以時制計畫呈現主幹道路各路口的號誌配時狀態，以及車輛在路口間的行駛與等待情形。  
This simulator is an interactive system that displays the timing plan status of traffic signals along a main road and simulates vehicle movements and waiting behaviors between intersections based on a timing plan.

---

## 功能介紹 (Features)

### 時空圖繪製 (Time-Space Diagram Drawing)
利用 HTML5 Canvas 繪製以時間為 X 軸、距離為 Y 軸的時空圖，直觀展示各交叉口的號誌狀態與車輛運行軌跡。  
The simulator uses HTML5 Canvas to draw a time-space diagram (time on the X-axis and distance on the Y-axis) that visually presents the signal status at intersections and the trajectories of vehicles.

### 車輛模擬與時制計畫 (Vehicle Simulation & Timing Plan)
根據各交叉口所設定的綠燈／紅燈秒數與時差，系統模擬車輛在路口間的行駛、等待與排隊情形，並以「時制計畫」方式呈現號誌配時。  
Based on the timing plan for each intersection (with defined green/red durations and offsets), the simulator models the movement, waiting, and queuing of vehicles between intersections using a timing plan approach.

### 出城與進城方向 (Outbound and Inbound Directions)
- **出城方向 (Outbound):** 時空圖中車輛軌跡與綠燈帶呈現向上延伸。  
- **進城方向 (Inbound):** 時空圖中車輛軌跡與綠燈帶則呈現向下延伸。  
For the simulation, the outbound direction displays trajectories extending upward, while the inbound direction shows trajectories extending downward.

### 自動更新 (Auto Update)
當使用者修改左側面板的參數時，時空圖會自動更新，無需額外按下任何按鈕。  
The diagram automatically updates whenever parameters on the left panel are changed, with no need to click an update button.

### 動畫播放 (Animation Playback)
播放動畫後，您可以觀察車輛依照時制計畫在各交叉口間的動態行駛、等待與排隊情形。  
Once the animation is started, you can observe the dynamic movement and waiting behavior of vehicles between intersections according to the timing plan.

### JSON 匯入／匯出 (JSON Import/Export)
您可以將全域參數（例如車速、發車間隔、出／進城帶寬比值）及各交叉口資料以 JSON 格式匯出，或從 JSON 檔案中匯入設定。  
Global settings and intersection data (including the outbound/inbound bandwidth ratio) can be exported to or imported from a JSON file for easy backup and sharing.

### 遺傳演算法優化 (Genetic Algorithm Optimization)
系統內建遺傳演算法，自動優化各交叉口間的時差參數，達成最佳綠燈連續通行效果。  
A built-in Genetic Algorithm automatically optimizes the offsets between intersections to achieve optimal continuous green signal operation.

---

## 操作流程 (Usage Workflow)

### 1. 開啟網頁 / Open the Webpage  
以瀏覽器開啟 `index.html`，系統自動載入左側參數設定區與右側的時空圖及動畫區。  
Open `index.html` in your browser; the interface loads with the configuration panel on the left and the diagram and animation area on the right.

### 2. 參數設定 / Configure Parameters  
在左側面板中依序設定：  
- **車速 (Speed, km/h)**  
- **發車間隔 (Departure Interval)**  
- **出／進城帶寬比值 (Outbound/Inbound Bandwidth Ratio)**  
- **交叉口時制計畫參數 (Intersection Timing Plan Parameters)**  
  (包括路口名稱、累積距離、綠燈／紅燈秒數與時差)  
Enter the vehicle speed, departure interval, bandwidth ratio, and intersection timing plan parameters on the left panel.

### 3. 自動更新時空圖 / Auto Update Diagram  
當參數設定變動時，右側的時空圖會自動更新，立即呈現最新模擬結果。  
The time-space diagram automatically updates to reflect the latest simulation results whenever parameters change.

### 4. 播放動畫 / Play Animation  
播放動畫後，您可以觀察車輛依照時制計畫在各交叉口間的動態行駛與等待情形。  
After starting the animation, observe the dynamic movement and waiting behavior of vehicles between intersections as specified by the timing plan.

### 5. JSON 匯入／匯出 / JSON Import/Export  
利用 JSON 匯入／匯出功能，您可以儲存或讀取包含全域參數與交叉口資料的設定檔。  
Use the JSON import/export feature to save or load configuration files that include all global settings and intersection data.

### 6. 優化時差 / Optimize Timing Offsets  
系統透過遺傳演算法自動優化各交叉口間的時差參數，達成最佳綠燈連續通行效果。  
The Genetic Algorithm automatically optimizes the offsets between intersections to achieve optimal continuous green signal operation.

---

## License

This project is licensed under the MIT License.  
(本專案採用 MIT 授權，詳細內容請參閱 LICENSE 檔案。)
