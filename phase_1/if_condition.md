## `if / elif / else` trong Python

Đây là **cấu trúc điều kiện**, dùng để cho chương trình đưa ra quyết định dựa trên một điều kiện `True` hoặc `False`.

### 1. Cú pháp cơ bản

```python
if điều_kiện:
    # code chạy khi điều kiện đúng
elif điều_kiện_khác:
    # code chạy khi điều kiện trên sai,
    # nhưng điều kiện này đúng
else:
    # code chạy khi tất cả điều kiện đều sai
```

**Lưu ý quan trọng:** Python dùng **thụt lề (indentation)** để xác định khối lệnh.

---

### 2. `if`

Dùng khi chỉ có **một điều kiện**:

```python
age = 20

if age >= 18:
    print("Đủ tuổi")
```

Kết quả:

```text
Đủ tuổi
```

Nếu `age = 15` thì không có gì được in ra.

---

### 3. `if ... else`

Dùng khi có **2 trường hợp**:

```python
age = 15

if age >= 18:
    print("Người lớn")
else:
    print("Chưa đủ 18 tuổi")
```

Kết quả:

```text
Chưa đủ 18 tuổi
```

Có thể hiểu:

```text
Nếu đúng  → if
Nếu sai   → else
```

---

### 4. `if ... elif ... else`

Dùng khi có **nhiều trường hợp**:

```python
score = 8

if score >= 9:
    print("Xuất sắc")
elif score >= 7:
    print("Khá")
elif score >= 5:
    print("Trung bình")
else:
    print("Yếu")
```

Kết quả:

```text
Khá
```

Python kiểm tra **từ trên xuống dưới** và khi gặp điều kiện đúng đầu tiên, nó thực hiện khối đó rồi bỏ qua các `elif/else` còn lại.

---

## 5. Kết hợp với toán tử so sánh

Các toán tử thường dùng:

| Toán tử | Ý nghĩa           |
| ------- | ----------------- |
| `==`    | bằng              |
| `!=`    | khác              |
| `>`     | lớn hơn           |
| `<`     | nhỏ hơn           |
| `>=`    | lớn hơn hoặc bằng |
| `<=`    | nhỏ hơn hoặc bằng |

Ví dụ:

```python
x = 10

if x == 10:
    print("x bằng 10")
```

⚠️ Phân biệt:

```python
x = 10    # gán giá trị
x == 10   # kiểm tra bằng
```

---

## 6. Kết hợp `and`, `or`, `not`

### `and`

**Tất cả điều kiện phải đúng:**

```python
age = 20
has_ticket = True

if age >= 18 and has_ticket:
    print("Được vào")
```

### `or`

**Chỉ cần một điều kiện đúng:**

```python
is_student = True
is_teacher = False

if is_student or is_teacher:
    print("Được giảm giá")
```

### `not`

Đảo ngược `True ↔ False`:

```python
is_raining = False

if not is_raining:
    print("Có thể đi chơi")
```

---

# 7. Ví dụ rất quan trọng cho Data Science

Trong Data Science, bạn sẽ thường xuyên dùng điều kiện để **phân loại dữ liệu**.

Ví dụ phân loại tuổi:

```python
age = 25

if age < 18:
    group = "Trẻ em"
elif age < 60:
    group = "Người trưởng thành"
else:
    group = "Người cao tuổi"

print(group)
```

Kết quả:

```text
Người trưởng thành
```

Hoặc phân loại điểm:

```python
score = 7.5

if score >= 8:
    label = "Good"
elif score >= 6.5:
    label = "Average"
else:
    label = "Bad"

print(label)
```

Đây chính là tư duy **rule-based classification** — rất hữu ích trước khi bạn học các thuật toán Machine Learning.

---

## 8. `if` lồng nhau — nested `if`

Bạn có thể đặt `if` bên trong `if`:

```python
age = 20
has_ticket = True

if age >= 18:
    if has_ticket:
        print("Được vào")
    else:
        print("Không có vé")
else:
    print("Chưa đủ tuổi")
```

Tuy nhiên, khi logic phức tạp, thường có thể viết gọn bằng `and`:

```python
if age >= 18 and has_ticket:
    print("Được vào")
```

---

## 9. Một lỗi rất hay gặp

❌ Sai:

```python
age = 20

if age = 18:
    print("18 tuổi")
```

`=` là **gán**, không phải so sánh.

✅ Đúng:

```python
if age == 18:
    print("18 tuổi")
```

---

# 10. Bài tập nhỏ

Hãy tự viết chương trình:

> Cho `temperature = 32`.
>
> * Nếu nhiệt độ `>= 35`: in `"Rất nóng"`
> * Nếu `>= 30`: in `"Nóng"`
> * Nếu `>= 20`: in `"Dễ chịu"`
> * Còn lại: in `"Lạnh"`

Đáp án:

```python
temperature = 32

if temperature >= 35:
    print("Rất nóng")
elif temperature >= 30:
    print("Nóng")
elif temperature >= 20:
    print("Dễ chịu")
else:
    print("Lạnh")
```

### Cần nắm chắc

```text
if      → kiểm tra điều kiện đầu tiên
elif    → kiểm tra điều kiện tiếp theo
else    → trường hợp còn lại

==      → so sánh
=       → gán
and     → và
or      → hoặc
not     → phủ định
```

**Trong lộ trình Python Data Science**, phần tiếp theo nên học là **vòng lặp `for` và `while`**, sau đó kết hợp `if` + loop để xử lý dữ liệu.
