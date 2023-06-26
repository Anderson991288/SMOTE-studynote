# Undersampled Majority Class Ensemble for highly imbalanced
### 論文概要
為了解決高度不平衡資料分類問題，提出了一種稱為umce的multiple classifier system的方法，該系統基於多數類別的k-fold division，將一個不平衡問題分為多個平衡問題，同時確保在訓練過程中存在所有可用樣本。

該方法使用了五種提出的融合方法和基於分類器在測試集上的統計依賴性的修剪方法。

使用基準資料集和兩種不同的基礎分類器。研究結果表明，這種方法在處理高度不平衡資料時具有良好的效果。


### 本研究的主要貢獻包括：

* 使用多數類別的k-fold undersampling建立一個 homogenous ensemble
  
* 提出了五種合併方法生成ensemble decision
  
* 使用基於分類器在測試集上的反應的統計依賴性的修剪方法，調整決策規則
  
* 對於所提出的方法實作進行評估
