## 匯入相關函式庫 
###### 1. pandas:用來匯入相關表格資料
###### 2. matplotlib.pyplot、seaborn:用來視覺化輸入資料以方便進行資料整理
###### 3. sklearn:內涵機器學習模型相關函式
## 讀取資料，並整理資料以查看資料大致狀況
###### 1. 以head()、describe()函式來查看大致狀況
###### 2. 查看資料是否含有空值，以及透過seaborn的heatmap()查看各欄位間的關聯性，以及目標特徵(price_range)與其他特徵的關聯性，是很重要的步驟
## 資料前處理
###### 1. 將訓練資料透過train_test_split()拆分成要訓練的資料以及測試的資料
###### 2. 將資料標準化以加快模型收斂速度
## 訓練模型
#### 參數是憑經驗去調整
###### 1. SVM: 4種分類器，包含線性SVC、線性核的SVC、多項的非線性SVC、高斯核的非線性分類器
###### 2. KNN
###### 3. Decision Tree
###### 4. Random Forest
## 模型評估
#### 以此次任務來說，recall會比precision還重要一些，因為預測手機價格範圍應是求正確，而recall這個評估標準是如果在該預測為正樣本中卻預測其為負樣本，也就是說如果本該預測其為範圍1，卻預測其為4，因此應該要較重視recall的值，希望該值能愈大愈好，代表其預測錯誤的機率愈低。(Decision Tree、Random Forest無法用confusion matrix來評估，查網路並自己試了很久，都會報錯，不好意思TT)
###### 1. 線性SVC
![image](https://user-images.githubusercontent.com/68068287/156771982-58aecbe7-a878-43cf-b31a-5deacd9d25dc.png)
###### 2. 線性核的SVC
![image](https://user-images.githubusercontent.com/68068287/156772076-3c55df27-7c38-44b2-9297-4909ce8de7e8.png)
###### 3. 多項的非線性SVC
![image](https://user-images.githubusercontent.com/68068287/156772115-d80e1b9a-b614-4110-acb4-59ddb5a66c13.png)
###### 4. 高斯核的非線性分類器
![image](https://user-images.githubusercontent.com/68068287/156772151-7fab2ade-740c-418c-890f-a9ee6466979f.png)
###### 5. KNN
![image](https://user-images.githubusercontent.com/68068287/156772271-b0e3d49d-dce9-4a65-bffe-32a9bc21e280.png)
###### 6. Decision Tree
###### 7. Random Forest
