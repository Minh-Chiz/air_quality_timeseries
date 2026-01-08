# Lab 4: Dự đoán Chất lượng Không khí Beijing (PM2.5)
## Học phần: Data Mining - FIT DNU

Chào mừng đến với repository của nhóm chúng mình. Dự án này thực hiện phân tích và dự báo nồng độ bụi mịn PM2.5 tại Bắc Kinh sử dụng pipeline chuẩn: **EDA -> Regression -> ARIMA**, được tự động hóa bằng Papermill.

📍 **Repository:** [https://github.com/Minh-Chiz/air_quality_timeseries](https://github.com/Minh-Chiz/air_quality_timeseries)

---

## 👥 Thành viên Nhóm [...]

| STT | Họ và Tên | Mã Sinh Viên | Vai trò |
|---|---|---|---|
| 1 | Vũ Ngọc Bảo | 1771020079 | Trưởng nhóm, Code chính |
| 2 | Nguyễn Đức Mạnh | 1771020456 | Phân tích EDA, Viết báo cáo |
| 3 | Hoàng Minh Chí | 1771020096 | Chạy mô hình |
| 4 | Trần Tiến Quang | 1771020569 | Viết báo cáo |

---

## 🚀 Giới thiệu Dự án

Dự án đóng vai trò Data Scientist thực thụ để giải quyết bài toán dự báo ô nhiễm không khí:
1.  **Làm sạch & EDA:** Xử lý dữ liệu thiếu, phân tích ngoại lai (outliers), kiểm định tính dừng (ADF/KPSS) và tính chu kỳ (ACF/PACF).
2.  **Regression Baseline:** Xây dựng mô hình hồi quy dự báo PM2.5 dựa trên các biến trễ (Lag features) và yếu tố thời gian.
3.  **ARIMA Forecasting:** Phân tích chuỗi thời gian chuyên sâu và chọn tham số $(p,d,q)$ tối ưu để dự báo.

**Chủ đề nâng cao (FIT-DNU CONQUER):**
*Nhóm chọn chủ đề:* **[Điền tên chủ đề: VD: Chủ đề 1 - So sánh Regression vs ARIMA]**

---

## 📂 Cấu trúc Dự án

```text
air_quality_timeseries/
├── data/
│   ├── raw/                  # Chứa file zip dữ liệu gốc (PRSA2017_Data...)
│   └── processed/            # Chứa dữ liệu đã làm sạch và file kết quả (model, metrics)
├── notebooks/
│   ├── preprocessing_and_eda.ipynb    # Bước 1: Tiền xử lý & EDA
│   ├── regression_modelling.ipynb     # Bước 2: Hồi quy Baseline
│   ├── arima_forecasting.ipynb        # Bước 3: Dự báo ARIMA
│   └── runs/                          # Kết quả chạy tự động (Output)
├── src/                      # Mã nguồn (thư viện hàm xử lý)
├── run_papermill.py          # Script chạy tự động toàn bộ pipeline
├── requirements.txt          # Danh sách thư viện cần thiết
└── README.md                 # Thông tin dự án

