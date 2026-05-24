# nhom9_KHDL

# Phân tích biến động giá xăng dầu tại Việt Nam giai đoạn 2020–2025

## Giới thiệu đề tài

 Phân tích biến động **giá xăng dầu tại Việt Nam trong giai đoạn 2020–2025** dựa trên dữ liệu thực tế từ **Petrolimex**.

Mục tiêu của bài là sử dụng các thư viện xử lý dữ liệu phổ biến như **PySpark, Pandas, NumPy và Matplotlib** để:

- Đọc và xử lý dữ liệu giá xăng dầu
- Làm sạch dữ liệu thiếu
- Phân tích biến động giá theo thời gian
- Tìm giá cao nhất, thấp nhất và giá trung bình
- Trực quan hóa dữ liệu bằng biểu đồ
- Đưa ra nhận xét và đánh giá xu hướng biến động giá xăng

---

## Bộ câu hỏi nghiên cứu

Trong bài phân tích, các câu hỏi được đặt ra gồm:

1. Giá xăng RON95 tại Việt Nam biến động như thế nào trong giai đoạn 2020–2025?

2. Tại sao giá xăng RON95 lại có biến động mạnh trong giai đoạn 2020–2025?

3. Thời điểm nào giá xăng RON95 đạt mức cao nhất?

4. Thời điểm nào giá xăng RON95 đạt mức thấp nhất?

5. Năm nào có giá xăng trung bình cao nhất?

6. Mức chênh lệch giữa giá cao nhất và thấp nhất là bao nhiêu?

7. Sau giai đoạn tăng mạnh, giá xăng có xu hướng giảm hay tiếp tục tăng?

---

## Công nghệ và thư viện sử dụng

Bài phân tích sử dụng các công nghệ và thư viện sau:

- **PySpark** → Đọc và xử lý dữ liệu lớn
- **Pandas** → Xử lý dữ liệu dạng bảng
- **NumPy** → Tính toán thống kê
- **Matplotlib** → Trực quan hóa dữ liệu bằng biểu đồ
- **Jupyter Notebook** → Thực hiện phân tích dữ liệu

---

## Cấu trúc thư mục

```text
baithuchanh5/
│── data/
│   └── Petrolimex_oilprice.csv
│
│── phan_tich_xang_dau_vn.ipynb
│── main.py
│── README.md
```

---

## Dataset sử dụng

Nguồn dữ liệu:

**Petrolimex Fuel Price Dataset (Kaggle)**

Dữ liệu bao gồm:

- Xăng RON95
- Xăng E5 RON92
- Dầu Diesel
- Dầu hỏa

Trong bài phân tích tập trung vào:

**Xăng RON95 vùng 1 (RON95 zone1)**

---

# Hướng dẫn chạy notebook và script

## Mục đích

Thư mục này chứa:

- **phan_tich_xang_dau_vn.ipynb**  
Notebook dùng để phân tích biến động giá xăng dầu tại Việt Nam giai đoạn **2020–2025**.

- **data/Petrolimex_oilprice.csv**  
Dữ liệu đầu vào chứa thông tin giá xăng dầu Việt Nam.

- **main.py**  
File Python dùng để thử nghiệm (không bắt buộc để chạy notebook).

---

## Cấu trúc thư mục

```text
baithuchanh5/
│── .idea/
│
│── data/
│   └── Petrolimex_oilprice.csv
│
│── phan_tich_xang_dau_vn.ipynb
│── main.py
│── README.md
```

---

## Yêu cầu

Để chạy được notebook cần:

- **Python 3.8+** hoặc tương đương
- Đã cài đặt **PyCharm**
- Đã cấu hình **Python Interpreter**
- Đã cài đặt **Jupyter Notebook**

Các thư viện cần thiết:

```bash
pandas
numpy
matplotlib
pyspark
jupyter
```

---

## Cách chạy trong PyCharm

### Bước 1: Mở project

Mở thư mục project trong PyCharm:

```text
D:\baithuchanh5
```

---

### Bước 2: Mở notebook

Mở file:

```text
phan_tich_xang_dau_vn.ipynb
```

---

### Bước 3: Kiểm tra Python Interpreter

Nếu PyCharm chưa tự chọn môi trường Python:

Vào:

```text
File → Settings → Project → Python Interpreter
```

Chọn Python Interpreter đã được cài đặt trên máy.

---

### Bước 4: Chạy notebook

Có thể chạy theo 2 cách:

### Chạy từng cell

Nhấn nút **Run (▶)** ở từng cell trong notebook.

Notebook sẽ chạy lần lượt các bước:

- Import thư viện
- Đọc dữ liệu bằng PySpark
- Chuyển đổi kiểu dữ liệu ngày tháng
- Lọc dữ liệu từ năm 2020–2025
- Xử lý dữ liệu thiếu
- Tính toán thống kê bằng NumPy
- Trực quan hóa dữ liệu bằng Matplotlib
- Phân tích và đánh giá kết quả

---

### Hoặc chạy toàn bộ notebook

Chọn:

```text
Run All Cells
```

để chạy toàn bộ notebook cùng lúc.

---

## Chạy trực tiếp bằng Terminal

Mở terminal trong thư mục project:

```text
D:\baithuchanh5
```

---

### Cài đặt thư viện cần thiết (nếu chưa có)

```bash
pip install jupyter pandas numpy matplotlib pyspark
```

---

### Chạy notebook bằng nbconvert

```bash
python -m nbconvert --to notebook --execute phan_tich_xang_dau_vn.ipynb --inplace
```

Lệnh trên sẽ:

- Tự động chạy toàn bộ notebook
- Lưu trực tiếp kết quả vào file `.ipynb`

---

### Hoặc mở Jupyter Notebook trực tiếp

Chạy lệnh:

```bash
python -m notebook
```

Sau đó mở file:

```text
phan_tich_xang_dau_vn.ipynb
```

trong trình duyệt.

---

## Các bước phân tích dữ liệu

### Bước 1: Đọc dữ liệu bằng PySpark

- Tạo Spark Session
- Đọc file CSV
- Kiểm tra dữ liệu đầu vào

### Bước 2: Làm sạch dữ liệu

- Chuyển cột Date sang kiểu ngày tháng
- Tạo cột Year
- Lọc dữ liệu từ năm 2020–2025
- Xử lý dữ liệu thiếu bằng `dropna()`

### Bước 3: Phân tích thống kê

Sử dụng **NumPy** để tính:

- Giá cao nhất
- Giá thấp nhất
- Giá trung bình
- Mức chênh lệch giá

### Bước 4: Trực quan hóa dữ liệu

Sử dụng **Matplotlib** để:

- Vẽ biểu đồ biến động giá xăng theo thời gian
- Vẽ biểu đồ giá trung bình theo năm

### Bước 5: Phân tích kết quả

- Xác định thời điểm giá cao nhất
- Xác định thời điểm giá thấp nhất
- Phân tích xu hướng tăng giảm giá xăng
- Đưa ra nhận xét về biến động giá

---

## Kết quả chính

Kết quả phân tích cho thấy:

- Giá cao nhất: **26.270 VNĐ/lít**
- Giá thấp nhất: **19.410 VNĐ/lít**
- Giá trung bình: **22.297 VNĐ/lít**
- Mức chênh lệch: **6.860 VNĐ/lít**

### Top 3 giá cao nhất

| Ngày | Giá xăng |
|------|----------|
| 21/09/2023 | 26.270 |
| 17/04/2024 | 25.760 |
| 02/05/2024 | 25.480 |

### Top 3 giá thấp nhất

| Ngày | Giá xăng |
|------|----------|
| 17/04/2025 | 19.410 |
| 10/04/2025 | 19.580 |
| 25/12/2025 | 19.540 |

---

## Nhận xét

- Giai đoạn **2023–đầu 2024** là thời kỳ giá xăng tăng mạnh nhất.
- Năm **2023** có giá xăng trung bình cao nhất.
- Từ cuối **2024 đến 2025**, giá xăng có xu hướng giảm và ổn định hơn.
- Giá xăng chịu ảnh hưởng bởi thị trường năng lượng thế giới và chính sách điều chỉnh trong nước.

---
