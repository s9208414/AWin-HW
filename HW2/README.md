## 匯入相關函式庫 
###### 1. numpy: 用來轉換一般串列成ndarray，因其提供很多串列運算，方便後續操作
###### 2. os: 資料路徑操作
###### 3. cv2: 讀入圖片檔案所需
###### 4. random: 用來打散原資料，方便後續分割隨機資料成訓練集、驗證集、測試集
###### 5. sklearn.model_selection: 分割資料所需
###### 6. keras.utils: 用來對目標特徵資料做one-hot-encoding，讓類別轉成0跟1以方便程式計算
###### 7. keras.models: 用以產生模型的初始序列物件、模型儲存及載入
###### 8. keras.layers: 建立模型的各類網路層所需
###### 9. matplotlib.pyplot: 繪製訓練過程的狀況
###### 10. sklearn.metrics: 提供confusion matrix以評估模型
