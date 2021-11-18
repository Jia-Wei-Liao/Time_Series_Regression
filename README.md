# Data Mining Research & Practice HW3 - Time Series Regression
## 資料集敘述
使用新竹地區 2020 年 10-12 月之空氣品質資料，進行時間序列分析 & 迴歸預測 PM2.5 值。
本資料集(如附檔)包含 AMB_TEMP、CH4、CO、NMHC、NO、NO2、NOx、O3、PM10、PM2.5、RAINFALL、RH、SO2、THC、WD_HR、WIND_DIREC、WIND_SPEED、WS_HR 共 18 種屬性(汙染物)之逐時資料。其中第一行之 0-23 代表小時。

- \# 表示儀器檢核為無效值
- \* 表示程式檢核為無效值
- x 表示人工檢核為無效值
- A 是指因儀器疑似故障警報所產生的無效值
- 空白 表示缺失值

(資料來源: https://airtw.epa.gov.tw/CHT/Query/His_Data.aspx)

## 目標
- 使用 10 和 11 月資料當作訓練集，12 月之資料當作測試集
- 將前六小時的汙染物數據做為特徵，未來第一個小時/未來第六個小時的 PM2.5 數據為預測目標
- 使用兩種模型 Linear Regression 和 XGBoost 建模並計算 MAE
