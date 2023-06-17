# SMOTE-studynote

SMOTE（Synthetic Minority Over-sampling Technique）是一種用於處理類別不平衡問題的過採樣方法。
它通過合成少數類樣本的新樣本來增加數據集中少數類的數量，從而改善模型的訓練效果。

### Paper1:[DeepSMOTE Fusing Deep Learning and SMOTE.pdf](https://github.com/Anderson991288/SMOTE-studynote/files/11779355/DeepSMOTE.Fusing.Deep.Learning.and.SMOTE.pdf)



### SMOTE的基本步驟：

1.選擇一個少數類的樣本作為基礎樣本。

2.找到與基礎樣本最近的k個鄰居。這些鄰居可以是來自相同類別的樣本，也可以是來自其他類別的樣本。

3.隨機選擇一個鄰居，並計算基礎樣本和鄰居之間的差異。

4.根據差異和一個隨機數生成新的合成樣本。合成樣本的特徵值介於基礎樣本和鄰居之間。

5.重複執行步驟2到步驟4，直到生成足夠數量的合成樣本。

這樣，我們就可以使用SMOTE來增加數據集中少數類的數量，從而改善模型在少數類上的預測效果。

### SMOTE模擬: 

* calculateDistance函數:用於計算兩個樣本之間的歐氏距離
* 將結果儲存在distances中
* 使用printf將計算的距離輸出
  
```
double calculateDistance(Sample* sample1, Sample* sample2) {
    double distance = 0.0;
    for (int i = 0; i < FEATURE_DIM; i++) {
        double diff = sample1->features[i] - sample2->features[i];
        distance += diff * diff;
    }
    return sqrt(distance);
}

int main() {
    // 假設我們有一些樣本
    Sample samples[] = {
        {{1.0, 2.0, 3.0, 4.0, 5.0, 6.0, 2.0, 2.0, 9.0, 9.0}, 0},
        {{2.0, 3.0, 4.0, 5.0, 6.0, 7.0, 3.0, 1.0, 6.0, 8.0}, 0},
        {{4.0, 5.0, 6.0, 7.0, 8.0, 2.0, 5.0, 5.0, 1.0, 2.0}, 1},
        {{5.0, 6.0, 7.0, 8.0, 9.0, 1.0, 6.0, 7.0, 3.0, 1.0}, 1}
    };
    int numSamples = 4;

//    int k = 3;  // 鄰居數
//    int numSyntheticSamples = 5;  // 每個少數類的合成樣本數

    double distances[MAX_SAMPLES];
    
    for (int i = 0; i < numSamples-1; i++) {
        distances[i] = calculateDistance(&samples[i], &samples[i+1]);
        printf("Distance: %f\n", distances[i]);
    }
```
