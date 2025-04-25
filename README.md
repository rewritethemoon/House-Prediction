# House Price Prediction

Dự án dự đoán giá nhà tại TP.HCM dựa trên dữ liệu crawl từ batdongsan.vn. Sử dụng Large Language Model (LLM) để trích xuất đặc trưng từ mô tả. Repository chứa mã nguồn, notebook phân tích và dữ liệu.

![Website Source](website.png)

## Cấu trúc thư mục

```
├── Báo_cáo_Đồ_án_NMKHDL.pdf           # Báo cáo dự án
├── Crawling.ipynb                      # Notebook crawl dữ liệu
├── Data.zip                           # Dữ liệu crawl và xử lý
├── Ghep_data.ipynb                    # Gộp dữ liệu từ nhiều nguồn
├── LLM.ipynb                          # Trích xuất đặc trưng bằng LLM
├── Methodology.ipynb                  # Phương pháp mô hình hóa và đánh giá
├── Preprocessing_and_FeatureEngineering.ipynb # Xử lý và tạo đặc trưng
├── data_crawl.csv                     # Dữ liệu thô
├── data_final.csv                     # Dữ liệu đã xử lý
├── data_hcm_llm.csv                   # Dữ liệu từ LLM
└── website.png                        # Ảnh minh họa website
```

## Bắt đầu

### Yêu cầu
- Python >= 3.8
- Jupyter Notebook

### Cài đặt
1. Clone repository:
   ```
   git clone https://github.com/rewritethemoon/House-Prediction.git
   cd House-Prediction
   ```

2. (Tùy chọn) Tạo môi trường ảo:
   ```
   python -m venv venv
   source venv/bin/activate  # Windows: venv\Scripts\activate
   ```

3. Cài đặt thư viện:
   ```
   pip install -r requirements.txt
   ```

## Quy trình dự án

1. Thu thập dữ liệu
   - Crawl từ batdongsan.vn bằng Crawling.ipynb.
   - Dữ liệu: giá, số phòng, địa chỉ, mô tả, ...

2. Trích xuất đặc trưng
   - Sử dụng LLM.ipynb để trích xuất chiều rộng, chiều dài, số tầng từ mô tả.
   - Gộp dữ liệu trong Ghep_data.ipynb.

3. Xử lý và tạo đặc trưng
   - Xử lý giá bất thường (ví dụ: 500 triệu tỷ).
   - Làm sạch, chuyển đổi và xử lý giá trị thiếu.
   - Tạo đặc trưng mới: tổng diện tích, có mặt tiền, ...
   - Notebook chính: Preprocessing_and_FeatureEngineering.ipynb.

4. Huấn luyện mô hình
   - Thử nghiệm Linear Regression và Gradient Boosting.
   - Đánh giá bằng R², RMSE, ...
   - Chi tiết trong Methodology.ipynb.

## Lưu ý
- Đảm bảo cài đặt đầy đủ các thư viện trong requirements.txt.
- File Data.zip chứa dữ liệu cần thiết để chạy các notebook.

## Liên hệ
Nếu có thắc mắc, vui lòng mở issue trên GitHub hoặc liên hệ qua email@example.com.
