<img width="870" height="671" alt="image" src="https://github.com/user-attachments/assets/57599ca8-f616-4bd8-8538-e293fdf4f4e1" />


## Lộ trình tổng thể: 5–6 tháng

**Python → NumPy → Pandas → Data Visualization → Statistics → SQL → Machine Learning → Projects**

### Giai đoạn 1 — Python nền tảng cho Data Science

**2–3 tuần**

Học đúng những phần cần dùng:

* Biến, kiểu dữ liệu
* `if/elif/else`
* `for`, `while`
* `list`, `tuple`, `dict`, `set`
* Function
* `lambda`, `map`, `filter`
* List/Dictionary Comprehension
* Exception handling
* Đọc/ghi file
* Module/package
* `pip`, virtual environment
* Jupyter Notebook
* Git cơ bản

**Bài tập:** xử lý file CSV đơn giản, thống kê dữ liệu bán hàng, viết các hàm tính toán.

> Không cần dành quá nhiều thời gian vào OOP, Design Pattern hay thuật toán nâng cao ở giai đoạn này.

---

### Giai đoạn 2 — NumPy

**1 tuần**

Mục tiêu: hiểu cách Python xử lý dữ liệu dạng mảng.

* `ndarray`
* `shape`, `dtype`
* Indexing / slicing
* Boolean masking
* Broadcasting
* Vectorization
* Aggregation
* Random
* Linear algebra cơ bản

Bạn cần hiểu **tại sao NumPy nhanh hơn việc dùng vòng `for` thuần Python**.

---

### Giai đoạn 3 — Pandas ⭐

**2–3 tuần**

Đây là một trong những phần **quan trọng nhất**.

Học:

* `Series`, `DataFrame`
* Import/export CSV, Excel
* `loc`, `iloc`
* Filtering
* Sorting
* `groupby`
* `agg`
* `merge`, `join`, `concat`
* `pivot_table`
* Missing values
* Duplicate
* Data type
* Datetime
* String operations
* Apply/map
* Data cleaning

Ví dụ bạn phải làm được:

```python
df.groupby("category")["sales"].sum()
```

và hiểu chính xác câu lệnh đó đang làm gì.

**Project:**

> Phân tích dataset bán hàng: doanh thu theo tháng, sản phẩm, khu vực, khách hàng.

---

### Giai đoạn 4 — Data Visualization

**1–2 tuần**

Học:

* Matplotlib
* Seaborn
* Plotly cơ bản

Biểu đồ quan trọng:

* Histogram
* Boxplot
* Bar chart
* Line chart
* Scatter plot
* Heatmap

Quan trọng hơn syntax là:

> **Dữ liệu → câu hỏi → biểu đồ phù hợp → insight**

Ví dụ không chỉ vẽ:

```python
sns.barplot(...)
```

mà phải trả lời được:

**"Khu vực nào tạo ra nhiều doanh thu nhất và tại sao?"**

---

### Giai đoạn 5 — Statistics cho Data Science

**2–3 tuần**

Không cần học thống kê theo kiểu toán thuần túy.

Tập trung:

* Mean / Median / Mode
* Variance / Standard deviation
* Percentile
* Distribution
* Normal distribution
* Probability
* Correlation / covariance
* Sampling
* Confidence interval
* Hypothesis testing
* p-value
* A/B testing

Sau phần này bạn phải hiểu được những câu như:

> "Correlation = 0.8 có nghĩa gì?"

và

> "p-value nhỏ có thực sự chứng minh A gây ra B không?"

---

### Giai đoạn 6 — SQL

**2 tuần**

Đừng bỏ qua SQL.

Học:

```sql
SELECT
FROM
WHERE
GROUP BY
HAVING
ORDER BY
LIMIT
```

sau đó:

* JOIN
* Subquery
* CTE
* Window functions
* `CASE WHEN`
* Date functions
* Aggregation

Mục tiêu cuối:

**SQL lấy dữ liệu → Pandas xử lý → Visualization → Insight**

Đây mới là workflow Data Analyst/Data Scientist thực tế.

---

# Giai đoạn 7 — Machine Learning

**4–6 tuần**

Bắt đầu với `scikit-learn`.

### Supervised Learning

Regression:

* Linear Regression
* Ridge/Lasso
* Decision Tree
* Random Forest
* Gradient Boosting

Classification:

* Logistic Regression
* KNN
* Decision Tree
* Random Forest
* Gradient Boosting

### Unsupervised Learning

* K-Means
* PCA
* Clustering

### Quan trọng hơn việc học nhiều model

Bạn phải hiểu:

**Dataset → EDA → Feature Engineering → Train/Test Split → Model → Evaluation → Tuning**

Học thêm:

* Overfitting / Underfitting
* Bias / Variance
* Cross-validation
* Feature scaling
* Encoding
* Pipelines
* Hyperparameter tuning

Metrics:

* MAE
* MSE / RMSE
* R²
* Accuracy
* Precision
* Recall
* F1
* ROC-AUC

---

# Giai đoạn 8 — Portfolio Projects ⭐⭐⭐

Đây là phần quyết định bạn **thực sự biết Data Science hay chỉ học syntax**.

Mình đề xuất làm **4 project tăng dần độ khó**:

### Project 1 — EDA

**Sales Analysis**

Python + Pandas + Matplotlib/Seaborn

→ Cleaning
→ EDA
→ Visualization
→ Business insights

### Project 2 — SQL + Python

**Customer Analytics**

SQL lấy dữ liệu → Pandas phân tích → Visualization.

### Project 3 — Machine Learning

**Customer Churn Prediction**

→ EDA
→ Feature engineering
→ Classification
→ Evaluation
→ Explain model

### Project 4 — End-to-End ⭐

**Một project hoàn chỉnh**

```text
Raw Data
   ↓
SQL
   ↓
Python/Pandas
   ↓
EDA
   ↓
Feature Engineering
   ↓
Machine Learning
   ↓
Evaluation
   ↓
Dashboard / Report
```

Project cuối nên được trình bày như một **case study thực tế**, chứ không phải chỉ là một notebook dài.

---

# Thứ tự học mình khuyên bạn

```text
                    DATA SCIENCE
                         │
          ┌──────────────┴──────────────┐
          ↓                             ↓
       Python                          SQL
          │
          ↓
        NumPy
          │
          ↓
       Pandas
          │
          ↓
   Data Visualization
          │
          ↓
     Statistics
          │
          ↓
   Machine Learning
          │
          ↓
      Projects
          │
          ↓
       Portfolio
```

## Lịch học mỗi ngày

Nếu bạn có **2 giờ/ngày**:

**30 phút** — học theory/concept
**60 phút** — code
**30 phút** — bài tập/project

Đừng học theo kiểu:

> xem video → chép code → "hiểu rồi"

Hãy dùng tỷ lệ:

> **20% học — 80% thực hành**

---

## Stack cuối cùng bạn nên đạt được

```text
Python
├── NumPy
├── Pandas
├── Matplotlib
├── Seaborn
└── Scikit-learn

SQL
│
├── PostgreSQL / MySQL
└── Advanced SQL

Statistics
│
└── Hypothesis Testing / A-B Testing

Tools
├── Jupyter
├── VS Code
└── Git/GitHub
```

**Chưa cần học TensorFlow/PyTorch ngay.** Deep Learning nên để sau khi bạn đã vững Python + Pandas + Statistics + ML.

### Nếu học từ con số 0, mình sẽ chia thành 24 tuần:

| Tuần  | Trọng tâm                |
| ----- | ------------------------ |
| 1–3   | Python                   |
| 4     | NumPy                    |
| 5–7   | Pandas                   |
| 8–9   | Visualization            |
| 10–12 | Statistics               |
| 13–14 | SQL                      |
| 15–18 | Machine Learning         |
| 19–24 | 3–4 Projects + Portfolio |

**Quan trọng:** đừng cố "học hết Python". Hãy học Python **đủ để giải quyết bài toán dữ liệu**, rồi tăng độ khó thông qua project.

Nếu bạn muốn, mình có thể xây tiếp cho bạn **lộ trình 24 tuần cực chi tiết theo từng ngày**, gồm **bài học → bài tập → dataset → project → tiêu chí kiểm tra**, bắt đầu từ **Day 1 Python**.
