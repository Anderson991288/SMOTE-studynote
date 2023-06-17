# SMOTE-studynote

SMOTE（Synthetic Minority Over-sampling Technique）是一種用於處理類別不平衡問題的過採樣方法。
它通過合成少數類樣本的新樣本來增加數據集中少數類的數量，從而改善模型的訓練效果。

### 以下是SMOTE的基本步驟：

1.選擇一個少數類的樣本作為基礎樣本。

2.找到與基礎樣本最近的k個鄰居。這些鄰居可以是來自相同類別的樣本，也可以是來自其他類別的樣本。

3.隨機選擇一個鄰居，並計算基礎樣本和鄰居之間的差異。

4.根據差異和一個隨機數生成新的合成樣本。合成樣本的特徵值介於基礎樣本和鄰居之間。

5.重複執行步驟2到步驟4，直到生成足夠數量的合成樣本。

這樣，我們就可以使用SMOTE來增加數據集中少數類的數量，從而改善模型在少數類上的預測效果。

