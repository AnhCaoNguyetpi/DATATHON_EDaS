# 📊 Time Series Forecasting Project

## 1. Tổng quan

Dự án này xây dựng một pipeline hoàn chỉnh cho bài toán **dự báo chuỗi thời gian (Time Series Forecasting)**, bao gồm:
- Phân tích dữ liệu (EDA)
- Xây dựng đặc trưng (feature engineering)
- Huấn luyện mô hình
- Tạo kết quả dự đoán

Mục tiêu chính:
- Hiểu hành vi dữ liệu theo thời gian (trend, seasonality)
- Xây dựng feature giúp mô hình học được động lực dữ liệu
- Đảm bảo **tính tái lập (reproducibility)**

---

## 2. Cấu trúc repository

```
.
├── Code giải câu hỏi trắc nghiệm.ipynb
├── Exploratory Data Analysis.ipynb
├── final_model.ipynb
├── submission.csv
└── README.md
```

### Mô tả chi tiết:

- **Exploratory Data Analysis.ipynb**
  - Phân tích dữ liệu
  - Kiểm tra missing values
  - Phát hiện trend và seasonality

- **final_model.ipynb**
  - Tiền xử lý dữ liệu
  - Feature engineering:
    - Lag features
    - Rolling statistics
    - Time-based features
  - Huấn luyện mô hình
  - Dự báo và xuất file

- **submission.csv**
  - File kết quả cuối cùng

---

## 3. Yêu cầu môi trường

### Python
- Python >= 3.9

### Cài đặt thư viện

```bash
pip install pandas numpy scikit-learn matplotlib seaborn
```

Nếu sử dụng model nâng cao:
```bash
pip install xgboost lightgbm
```

---

## 4. Hướng dẫn chạy (Reproducibility)

### Bước 1: Clone repository

```bash
git clone <repo-link>
cd <repo-name>
```

---

### Bước 2: Chuẩn bị dữ liệu

- Đặt dữ liệu đầu vào đúng đường dẫn trong notebook
- Đảm bảo định dạng dữ liệu không thay đổi

---

### Bước 3: Chạy EDA (khuyến nghị)

```bash
Exploratory Data Analysis.ipynb
```

Giúp:
- Hiểu dữ liệu
- Xác định pattern quan trọng

---

### Bước 4: Train model + Forecast

```bash
final_model.ipynb
```

Pipeline bao gồm:
1. Data preprocessing  
2. Feature engineering  
3. Model training  
4. Prediction  

---

### Bước 5: Xuất kết quả

Sau khi chạy xong sẽ tạo:

```bash
submission.csv
```

---

## 5. Pipeline tổng thể

```
Raw Data
   ↓
EDA
   ↓
Feature Engineering
   ↓
Model Training
   ↓
Prediction
   ↓
submission.csv
```

---

## 6. Insight chính

- Lag features rất quan trọng → dữ liệu quá khứ ảnh hưởng mạnh
- Seasonality rõ ràng → cần feature theo thời gian
- Không phải mọi biến đầu vào đều quyết định output → cần chọn lọc feature
- Một số biến có thể gây nhiễu → cần xử lý

---

## 7. Lưu ý tái lập kết quả

- Không thay đổi thứ tự chạy notebook
- Giữ nguyên pipeline
- Đảm bảo version thư viện giống nhau
- Cố định random seed (nếu có)

---

## 8. Hướng phát triển

- Hyperparameter tuning
- Sử dụng model nâng cao (LightGBM, XGBoost)
- Time Series Cross Validation
- Feature selection nâng cao


