Đây là **bài nền tảng đầu tiên** trong lộ trình Python Data Science. Bạn nên nắm thật chắc phần này trước khi sang NumPy/Pandas.

# 1. Biến (Variables)

Trong Python, **biến là tên dùng để tham chiếu đến một giá trị/object**.

```python
name = "An"
age = 25
height = 1.72
is_student = True
```

Có thể hiểu:

```text
name ─────► "An"
age  ─────► 25
height ───► 1.72
```

Python **không cần khai báo kiểu biến trước**:

```python
age = 25
age = "twenty five"
```

Biến `age` có thể được gán sang object có kiểu khác.

---

# 2. Các kiểu dữ liệu quan trọng

Trong Data Science, trước tiên cần nắm các kiểu sau:

| Kiểu    | Ví dụ           | Ý nghĩa          |
| ------- | --------------- | ---------------- |
| `int`   | `10`            | Số nguyên        |
| `float` | `3.14`          | Số thực          |
| `str`   | `"Python"`      | Chuỗi            |
| `bool`  | `True`, `False` | Đúng/Sai         |
| `None`  | `None`          | Không có giá trị |
| `list`  | `[1, 2, 3]`     | Danh sách        |
| `tuple` | `(1, 2, 3)`     | Tuple            |
| `dict`  | `{"age": 25}`   | Key-value        |
| `set`   | `{1, 2, 3}`     | Tập hợp          |

Trong giai đoạn đầu, **ưu tiên cực chắc `int`, `float`, `str`, `bool`, `list`, `dict`**.

---

# 3. Kiểm tra kiểu dữ liệu với `type()`

```python
age = 25
print(type(age))
```

Kết quả:

```python
<class 'int'>
```

Ví dụ:

```python
x = 10
y = 3.14
name = "Python"
active = True

print(type(x))
print(type(y))
print(type(name))
print(type(active))
```

---

# 4. `int` — số nguyên

```python
age = 25
quantity = 100
year = 2026
```

Các phép toán:

```python
a = 10
b = 3

print(a + b)   # 13
print(a - b)   # 7
print(a * b)   # 30
print(a / b)   # 3.333...
print(a // b)  # 3
print(a % b)   # 1
print(a ** b)  # 1000
```

Đặc biệt cần nhớ:

```python
/   # chia thông thường → float
//  # chia lấy phần nguyên
%   # chia lấy dư
**  # lũy thừa
```

---

# 5. `float` — số thực

```python
price = 19.99
temperature = 36.5
mean = 7.25
```

Ví dụ Data Science:

```python
scores = [7.5, 8.0, 9.25, 6.75]
```

Các giá trị đo lường, thống kê thường xuất hiện dưới dạng `float`.

---

# 6. `str` — chuỗi

```python
name = "Nguyen Van A"
country = "Vietnam"
```

Có thể dùng:

```python
name = "Python"
```

hoặc:

```python
name = 'Python'
```

Nối chuỗi:

```python
first_name = "Nguyen"
last_name = "An"

full_name = first_name + " " + last_name

print(full_name)
```

Kết quả:

```text
Nguyen An
```

### f-string — cực kỳ quan trọng

```python
name = "An"
age = 25

print(f"Tôi tên là {name}, tôi {age} tuổi.")
```

Đây là cách rất phổ biến để đưa biến vào chuỗi.

---

# 7. `bool` — True / False

```python
is_student = True
is_logged_in = False
```

Kiểu này đặc biệt quan trọng khi xử lý điều kiện và lọc dữ liệu.

```python
age = 25

print(age > 18)
print(age == 25)
print(age < 18)
```

Kết quả:

```text
True
True
False
```

Các toán tử thường dùng:

```python
==   # bằng
!=   # khác
>    # lớn hơn
<    # nhỏ hơn
>=   # lớn hơn hoặc bằng
<=   # nhỏ hơn hoặc bằng
```

**Lưu ý:**

```python
x = 10
```

là **gán giá trị**.

```python
x == 10
```

là **so sánh**.

Đây là lỗi người mới học rất hay gặp.

---

# 8. Chuyển đổi kiểu dữ liệu

Đây là phần **rất quan trọng trong Data Science** vì dữ liệu thực tế thường bị sai kiểu.

```python
age = "25"

print(type(age))
```

`age` đang là `str`.

Chuyển thành `int`:

```python
age = int(age)

print(type(age))
```

### Một số hàm chuyển kiểu

```python
int()
float()
str()
bool()
```

Ví dụ:

```python
x = "10"

a = int(x)
b = float(x)
c = str(a)

print(a)       # 10
print(b)       # 10.0
print(c)       # "10"
```

---

# 9. `list` — cực kỳ quan trọng với Data Science

List chứa nhiều giá trị:

```python
scores = [7, 8, 9, 10]
```

Truy cập phần tử:

```python
print(scores[0])
print(scores[1])
```

Kết quả:

```text
7
8
```

Python bắt đầu đếm từ **0**.

```text
[7, 8, 9, 10]
 ↑  ↑  ↑   ↑
 0  1  2   3
```

Thêm phần tử:

```python
scores.append(6)
```

Kết quả:

```python
[7, 8, 9, 10, 6]
```

Sau này khi học NumPy/Pandas, tư duy về collection như `list` sẽ được sử dụng liên tục.

---

# 10. `dict` — cực kỳ quan trọng

Dictionary lưu dữ liệu dạng **key → value**:

```python
student = {
    "name": "An",
    "age": 25,
    "score": 8.5
}
```

Lấy dữ liệu:

```python
print(student["name"])
print(student["age"])
print(student["score"])
```

Kết quả:

```text
An
25
8.5
```

Đây là cấu trúc rất gần với dữ liệu JSON/API mà bạn sẽ gặp trong Data Science.

---

# 11. `None`

`None` biểu thị **không có giá trị**:

```python
result = None
```

Ví dụ:

```python
age = None
```

Trong dữ liệu thực tế, bạn sẽ thường gặp khái niệm **missing value**. Khi học Pandas, `None` và các dạng missing data sẽ trở nên rất quan trọng.

---

# 12. Quy tắc đặt tên biến

Nên:

```python
student_name = "An"
age = 25
average_score = 8.5
```

Không nên:

```python
a = "An"
x = 25
abc = 8.5
```

trừ khi biến có phạm vi rất nhỏ.

Python sử dụng quy ước **snake_case**:

```python
total_sales = 1000
average_price = 25.5
customer_count = 100
```

Không được:

```python
2name = "An"      # Sai
student-name = "" # Sai
```

---

# 13. Bài tập thực hành

Hãy tự viết code cho 5 bài này:

### Bài 1

Tạo các biến:

```text
name
age
height
is_student
```

với kiểu dữ liệu phù hợp.

### Bài 2

Cho:

```python
a = 15
b = 4
```

Tính:

* tổng
* hiệu
* tích
* thương
* thương nguyên
* số dư
* lũy thừa

### Bài 3

```python
age = "25"
```

Chuyển `age` thành `int` và kiểm tra `type()`.

### Bài 4

Tạo:

```python
scores = [7.5, 8, 9, 6.5, 10]
```

Sau đó:

* lấy điểm đầu tiên
* lấy điểm cuối cùng
* thêm điểm `8.5`
* kiểm tra độ dài danh sách

### Bài 5 — liên quan Data Science

Tạo dictionary:

```python
student = {
    "name": "An",
    "age": 25,
    "math": 8.5,
    "python": 9.0
}
```

Sau đó in ra:

```text
Tên: An
Tuổi: 25
Điểm Python: 9.0
```

**Mục tiêu của bài này:** bạn phải thật sự hiểu `variable → data type → operation → collection`, vì đây là nền móng để chuyển sang **NumPy → Pandas → Matplotlib → Machine Learning**.
