# Imbalance Reduction Techniques Applied to ECG Classification Problem


* 使用了高度不平衡的ECG數據集MIT-BIH進行實驗
* 多類UMCE的組合模型，目的在處理不平衡的數據集

* 一種方法是使用SMOTE
* 另一種方法是在生成的學習樣本中引入雜訊的SMOTE

* 基準模型是一個在訓練集進行欠採樣的單一ResNet網絡
* 多類UMCE模型在實驗中表現優於基準模型，但未能超越將SMOTE應用於訓練集的單一模型的結果
* 引入雜訊的SMOTE生成的數據並未帶來顯著改善
* 未來的研究可以考慮將多類UMCE與SMOTE結合使用，以提升深度學習模型在不平衡數據集上的性能
