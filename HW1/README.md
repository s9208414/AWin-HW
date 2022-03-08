## 索引
* <a href='#1'>目的</a>
* <a href='#2'>匯入相關函式庫</a>
* <a href='#3'>讀取資料，並整理資料以查看資料大致狀況</a>
* <a href='#4'>資料前處理</a>
* <a href='#5'>訓練模型</a>
* <a href='#6'>模型評估</a>
## 目的#1
#### 本專案期望使用機器學習中的各種分類器透過輸入欲預測之手機各方面特徵，以對未知的手機之價格做預測。
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
###### 針對價格0的precison為42/42+3+0+0= 42/45, recall為42/42+0+0+0= 1, F1-score為2/(45/42+(1))= 84/87, accuracy為42+28+34+60/42+28+34+60+3+0+0+0+0+0= 164/167
![image](https://user-images.githubusercontent.com/68068287/156771982-58aecbe7-a878-43cf-b31a-5deacd9d25dc.png)
###### 2. 線性核的SVC
###### 針對價格0的precison為41/41+1+0+0= 41/42, recall為41/41+1+0+0= 41/42, F1-score為2/(42/41+42/41)= 82/84, accuracy為41+48+44+60/41+48+44+60+1+0+0+1+0+0= 193/195
![image](https://user-images.githubusercontent.com/68068287/156772076-3c55df27-7c38-44b2-9297-4909ce8de7e8.png)
###### 3. 多項的非線性SVC
###### 針對價格0的precison為37/37+6+0+0= 37/43, recall為37/37+5+0+0= 37/42, F1-score為2/(43/37+42/37)= 74/85, accuracy為37+31+36+48/37+31+36+48+6+0+0+5+0+0= 152/163
![image](https://user-images.githubusercontent.com/68068287/156772115-d80e1b9a-b614-4110-acb4-59ddb5a66c13.png)
###### 4. 高斯核的非線性分類器
###### 針對價格0的precison為34/34+7+0+0= 34/41, recall為34/34+8+0+0= 34/42, F1-score為2/(41/34+42/34)= 68/83, accuracy為34+27+34+46/34+27+34+46+7+0+0+8+0+0= 141/156
![image](https://user-images.githubusercontent.com/68068287/156772151-7fab2ade-740c-418c-890f-a9ee6466979f.png)
###### 5. KNN
###### 針對價格0的precison為29/29+29+5+2= 29/65, recall為29/29+12+0+1= 29/42, F1-score為2/(65/29+42/29)= 58/107, accuracy為29+16+15+29/29+16+15+29+29+5+2+12+0+1= 89/109
![image](https://user-images.githubusercontent.com/68068287/156772271-b0e3d49d-dce9-4a65-bffe-32a9bc21e280.png)
###### 6. Decision Tree
###### 7. Random Forest
