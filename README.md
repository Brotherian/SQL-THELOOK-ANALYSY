# SQL Basic JOIN Mini Project
## 📖 Project Overview
Mini Project ini bertujuan untuk mengimplementasikan konsep **SQL JOIN** dalam proses pengolahan dan analisis data. Melalui project ini, data yang berasal dari beberapa tabel akan digabungkan menggunakan berbagai jenis JOIN untuk menghasilkan informasi yang lebih komprehensif dan mendukung proses pengambilan keputusan berbasis data.

Project ini dikembangkan sebagai bagian dari pembelajaran Data Analytics dengan fokus pada pemahaman relasi antar tabel, optimasi query, dan eksplorasi data menggunakan SQL.

---

## 🎯 Objectives

Tujuan utama dari project ini adalah:

- Memahami konsep relasi antar tabel dalam database relasional.
- Mengimplementasikan `INNER JOIN`, `LEFT JOIN`, `RIGHT JOIN`, dan `FULL OUTER JOIN` (jika didukung DBMS).
- Menghasilkan dataset terintegrasi dari beberapa sumber data.
- Menjawab kebutuhan bisnis melalui analisis data menggunakan SQL.
- Mengembangkan kemampuan problem solving dan data exploration.

 

---

## 🗂 Project Structure

```text

sql-basic-join-project/
│
├── README.md
├── datasets/
│ ├── customers.csv
│ ├── orders.csv
│ ├── products.csv
│ └── order_details.csv
│
├── sql/
│ ├── 01_data_exploration.sql
│ ├── 02_inner_join.sql
│ ├── 03_left_join.sql
│ ├── 04_right_join.sql
│ └── 05_final_analysis.sql
│
├── outputs/
│ ├── result_tables.xlsx
│ ├── screenshots/
│ └── dashboard.png
│
└── documentation/
└── project_report.pdf

```

---

## 🛠 Technology Stack
| Component                   | Tools                               |
|-----------------------------|-------------------------------------|
| Database                    | MySQL / PostgreSQL / SQL Server     |
| Query Tool                  | DBeaver / MySQL Workbench / pgAdmin |
| Data Processing             | SQL                                 |
| Documentation               | Markdown                            |
| Visualization (Optional)    | Excel / Power BI / Tableau          |

---

## 📊 Dataset Description

Dataset yang digunakan terdiri dari beberapa tabel yang saling berhubungan.
| Table Name   | Description                     |
|--------------|---------------------------------|
| Customers    | Informasi pelanggan             |
| Orders       | Data transaksi pelanggan        |
| Order Details| Detail produk yang dibeli       |
| Products     | Informasi produk                |
| Categories   | Kategori produk (jika tersedia) |
> Sesuaikan daftar tabel dengan dataset yang diberikan pada assignment.

---
## 🔗 Database Relationship
Contoh relasi antar tabel:

```text

Customers
│
│ customer_id
▼
Orders
│
│ order_id
▼
Order_Details
│
│ product_id
▼
Products

```

Relasi ini memungkinkan data transaksi dan data pelanggan dianalisis secara terintegrasi melalui operasi JOIN.

---

## 🚀 Project Workflow

### 1. Data Understanding
- Memahami struktur setiap tabel.
- Mengidentifikasi Primary Key dan Foreign Key.
- Memvalidasi kualitas data sebelum analisis.

### 2. Data Exploration
- Meninjau isi data.
- Mengidentifikasi missing value atau inkonsistensi data.
- Memastikan relasi tabel berjalan dengan baik.

### 3. Data Joining
Melakukan kombinasi data menggunakan:
- INNER JOIN
- LEFT JOIN
- RIGHT JOIN
- FULL OUTER JOIN (apabila didukung)

### 4. Data Analysis

Mengekstrak informasi yang diperlukan untuk menjawab pertanyaan bisnis atau assignment.

### 5. Reporting

Menyusun hasil query, insight, dan kesimpulan dalam format yang mudah dipahami.

---

## 📝 SQL Implementation

### Example 1 - INNER JOIN

```sql
SELECT
c.customer_name,
o.order_id,
o.order_date
FROM customers c
INNER JOIN orders o
ON c.customer_id = o.customer_id;

```
**Purpose**
Menampilkan pelanggan yang memiliki transaksi pesanan.
---
### Example 2 - LEFT JOIN

```sql
SELECT
c.customer_name,
o.order_id
FROM customers c
LEFT JOIN orders o
ON c.customer_id = o.customer_id;

```

**Purpose**
Menampilkan seluruh pelanggan, termasuk yang belum pernah melakukan transaksi.
---

### Example 3 - Multi Table JOIN
```sql

SELECT
c.customer_name,
p.product_name,
od.quantity
FROM customers c
INNER JOIN orders o
ON c.customer_id = o.customer_id
INNER JOIN order_details od
ON o.order_id = od.order_id
INNER JOIN products p
ON od.product_id = p.product_id;

```

**Purpose**

Menampilkan produk yang dibeli oleh masing-masing pelanggan.
---

## 📈 Key Findings
Beberapa insight yang dapat diperoleh dari hasil analisis:
1. Produk dengan jumlah penjualan tertinggi.
2. Pelanggan dengan transaksi terbesar.
3. Kategori produk paling populer.
4. Distribusi transaksi pelanggan.
5. Pola pembelian berdasarkan periode waktu tertentu.

> Bagian ini diisi berdasarkan hasil analisis yang diperoleh.
---

## ✅ Conclusion

Berdasarkan implementasi SQL JOIN pada beberapa tabel yang saling berelasi, data dari berbagai sumber dapat digabungkan menjadi informasi yang lebih lengkap dan bernilai. Penggunaan JOIN memungkinkan analisis yang lebih mendalam terkait pelanggan, transaksi, dan produk sehingga dapat mendukung pengambilan keputusan berbasis data.

---
## 📚 Learning Outcomes

Setelah menyelesaikan project ini, peserta diharapkan mampu:
- Memahami konsep database relasional.
- Mengidentifikasi hubungan antar tabel.
- Menggunakan berbagai jenis JOIN secara tepat.
- Menulis query SQL yang lebih terstruktur dan efisien.
- Menghasilkan insight bisnis dari hasil pengolahan data.
---

## 👤 Author
**Nama:** [Ian]
**Program:** Data Analytics Bootcamp
**Module:** SQL Basic JOIN
**Project:** Mini Project Sesi 5
**Date:** [11-11-2026]

---

## 📄 License
Project ini dibuat untuk tujuan pembelajaran dan pengembangan kemampuan Data Analytics.
