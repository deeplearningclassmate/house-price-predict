#2023 SINOPAC AI GO Competition <br>
<br>
【比賽介紹】<br>
官方提供external, public, private資料集，共21個欄位特徵與1欄位預測目標（房價），部分欄位資料已使用z-score做去識別化，每筆不動產之橫、縱坐標有做小幅度移動做去識別化，透過使用Machine Learning進行預測，競賽以MAPE (Mean Absolute Percentage Error)作為評估模型優劣的方法。
<br>
【步驟】<br>
資料預處理<br>
空值刪除<br>
特徵轉換：二度分帶轉經緯度、文字轉數值代碼<br>
增加特徵：與車站最短距離、最短距離之站點級別、周圍0.5m以內之超商數量、人口密度、平均收入等等..<br>
資料標準化：StandardScaler()<br>
篩選特徵：刪除類別特徵、文字特徵、人數特徵、標準差>10<br>
訓練模型：使用BaggingRegressor模型，為集成學習的一種，採用Bootstrap Aggregating技術，建立多個獨立基礎回歸模型，隨機抽取樣本訓練每個基礎模型，結果由平均計算或投票決定，可提升模型穩定性、性能、泛化能力，降低整體模型的方差<br>
評估模型：MAPE、R2 score<br>
<br>
【結果】總排名127<br>
<br>
