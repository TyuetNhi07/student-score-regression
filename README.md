# Student Score Regression

Ứng dụng demo hồi quy tuyến tính dự đoán điểm thi (dữ liệu tổng hợp, chỉ phục vụ giảng dạy).
Công nghệ: scikit-learn, ipywidgets, Voilà, Render.

## Chạy cục bộ

```bash
python -m venv .venv
# Windows: .venv\Scripts\Activate.ps1   |   Linux/macOS: source .venv/bin/activate
python -m pip install --upgrade pip
pip install -r requirements.txt
python -m training.generate_data
python -m training.train_model
voila app.ipynb --no-browser --port=8866
```

Mở http://localhost:8866.

## Triển khai

Commit cả `artifacts/linear_regression.joblib`, rồi tạo Blueprint trên Render từ `render.yaml`.
Không huấn luyện lại khi dịch vụ khởi động; không commit `.venv`, `.env` hay bí mật.
