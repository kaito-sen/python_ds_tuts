## `for` và `while` trong Python

Trong Data Science, vòng lặp giúp bạn **lặp qua dữ liệu, thực hiện phép tính, xử lý từng phần tử**. Tuy nhiên, khi làm việc với `NumPy`/`Pandas`, sau này bạn sẽ thường ưu tiên **vectorization** thay vì loop để tăng hiệu năng.

---

### 1. `for` — lặp qua một tập hợp

Cú pháp:

```python
for biến in iterable:
    # code
```

Ví dụ:

```python
numbers = [10, 20, 30, 40]

for x in numbers:
    print(x)
```

Kết quả:

```text
10
20
30
40
```

`for` thường dùng để duyệt:

```python
# List
for x in [1, 2, 3]:
    print(x)

# String
for char in "Python":
    print(char)

# range
for i in range(5):
    print(i)
```

`range(5)` tạo các giá trị:

```text
0 1 2 3 4
```

---

### 2. `range()` — cực kỳ quan trọng

```python
range(start, stop, step)
```

Ví dụ:

```python
for i in range(1, 6):
    print(i)
```

```text
1
2
3
4
5
```

Lưu ý: **`stop` không được tính**.

Có thể thêm bước nhảy:

```python
for i in range(0, 10, 2):
    print(i)
```

```text
0
2
4
6
8
```

Đi ngược:

```python
for i in range(5, 0, -1):
    print(i)
```

```text
5
4
3
2
1
```

---

### 3. `for` + `if`

Đây là pattern bạn sẽ dùng rất nhiều:

```python
numbers = [1, 2, 3, 4, 5, 6]

for x in numbers:
    if x % 2 == 0:
        print(x)
```

Kết quả:

```text
2
4
6
```

Ví dụ gần với Data Science:

```python
scores = [65, 82, 91, 55, 78]

for score in scores:
    if score >= 80:
        print("Pass:", score)
```

---

### 4. `enumerate()` — rất nên biết

Thay vì:

```python
names = ["An", "Bình", "Chi"]

for i in range(len(names)):
    print(i, names[i])
```

Nên viết:

```python
for i, name in enumerate(names):
    print(i, name)
```

Kết quả:

```text
0 An
1 Bình
2 Chi
```

Trong Data Science, `enumerate()` khá hữu ích khi cần **index + value**.

---

### 5. `while` — lặp khi điều kiện còn đúng

Cú pháp:

```python
while condition:
    # code
```

Ví dụ:

```python
i = 1

while i <= 5:
    print(i)
    i += 1
```

Kết quả:

```text
1
2
3
4
5
```

Điểm quan trọng là phải có thứ gì đó làm thay đổi điều kiện:

```python
i += 1
```

Nếu không:

```python
i = 1

while i <= 5:
    print(i)
```

→ **vòng lặp vô hạn**.

---

## 6. `break` — dừng vòng lặp

```python
for i in range(10):
    if i == 5:
        break
    print(i)
```

Kết quả:

```text
0
1
2
3
4
```

Khi `i == 5`, `break` lập tức thoát khỏi vòng lặp.

---

## 7. `continue` — bỏ qua một vòng

```python
for i in range(5):
    if i == 2:
        continue
    print(i)
```

Kết quả:

```text
0
1
3
4
```

`continue` **không dừng loop**, chỉ bỏ qua lần lặp hiện tại.

---

## 8. `for` hay `while`?

| Tình huống                     | Nên dùng          |
| ------------------------------ | ----------------- |
| Biết rõ cần lặp qua list       | `for`             |
| Duyệt từng phần tử             | `for`             |
| Lặp `n` lần                    | `for` + `range()` |
| Không biết trước số lần lặp    | `while`           |
| Lặp đến khi điều kiện thay đổi | `while`           |
| Tìm một phần tử rồi dừng       | `for` + `break`   |

Ví dụ:

```python
# for: biết cần duyệt toàn bộ list
for number in numbers:
    print(number)
```

Trong khi:

```python
# while: chạy cho đến khi đạt điều kiện
balance = 100

while balance > 0:
    balance -= 20
    print(balance)
```

---

# 9. Nested loop — vòng lặp lồng nhau

Ví dụ:

```python
for i in range(3):
    for j in range(2):
        print(i, j)
```

Kết quả:

```text
0 0
0 1
1 0
1 1
2 0
2 1
```

Bạn sẽ gặp nested loop khi xử lý dữ liệu nhiều chiều, nhưng **đừng lạm dụng** vì có thể rất chậm khi dữ liệu lớn.

---

# 10. Một pattern rất quan trọng: tính tổng

```python
numbers = [10, 20, 30, 40]

total = 0

for x in numbers:
    total += x

print(total)
```

Kết quả:

```text
100
```

Nhưng trong Python thực tế có thể dùng:

```python
total = sum(numbers)
```

Đây là tư duy quan trọng khi học Data Science:

> **Biết loop → nhưng cũng phải biết khi nào không nên dùng loop.**

Sau này với NumPy, thay vì:

```python
total = 0

for x in numbers:
    total += x
```

ta sẽ có:

```python
import numpy as np

numbers = np.array([10, 20, 30, 40])

total = np.sum(numbers)
```

---

## 11. Bài tập nên làm

### Bài 1

In các số từ `1` đến `100`.

### Bài 2

In các số chẵn từ `1` đến `100`.

### Bài 3

Cho:

```python
numbers = [12, 5, 8, 20, 3, 15, 7]
```

Tính tổng các số **lớn hơn 10** bằng `for`.

### Bài 4

Cho:

```python
scores = [45, 78, 92, 56, 88, 35, 96]
```

Đếm có bao nhiêu điểm `>= 80`.

### Bài 5

Dùng `while` để in:

```text
10
9
8
...
1
```

### Bài 6 — Data Science mindset

Cho:

```python
temperatures = [28, 31, 35, 29, 40, 26, 33]
```

Tìm nhiệt độ lớn nhất **bằng loop**, không dùng `max()`.

---

### Thứ tự học Python Data Science ở phần này

Bạn nên nắm chắc:

**`for` → `range()` → `enumerate()` → `while` → `break` → `continue` → nested loop**

Sau đó chuyển sang **List / Dictionary nâng cao + List Comprehension**, rồi mới đi vào **NumPy**.
