# ETL Pipeline: Daily Net Sales Analysis

## هدف پروژه
این پروژه یک ETL Pipeline عملی است که داده‌های فروش و مرجوعی فروشگاه‌ها را پردازش می‌کند، شاخص‌های کلیدی مالی مثل Net Sales و NetSalesDividedBy10 را محاسبه می‌کند و خروجی CSV و نمودارهای تحلیلی برای بررسی روند فروش تولید می‌کند.

---

## ویژگی‌های کلیدی
- ETL کامل: Extract → Transform → Load
- محاسبه Net Sales و NetSalesDividedBy10
- خروجی CSV برای استفاده در داشبوردهای BI
- نمودار خطی Net Sales روزانه برای هر فروشگاه با matplotlib
- نمونه داده CSV همراه پروژه

---

## ساختار پروژه
etl-net-sales/
├── data/invoices_sample.csv
├── etl_net_sales_pipeline.ipynb # فایل Notebook اصلی
├── output/net_sales_report_YYYYMMDD.csv
├── requirements.txt
└── README.md

---

## نصب و اجرا
1. کلون کردن پروژه:
```bash
git clone <URL-of-your-repo>
cd etl-net-sales
نصب وابستگی‌ها:

pip install -r requirements.txt
اجرا:

Colab: فایل etl_net_sales_pipeline.ipynb را باز کنید و تمام سلول‌ها را Run کنید.

محلی (Local Python): اگر خواستی Notebook را روی سیستم خودت اجرا کنی می‌توانی با jupyter notebook یا jupyter lab بازش کنی و اجرا کنی.

خروجی CSV در مسیر output/net_sales_report_YYYYMMDD.csv ذخیره می‌شود.
| storeid | documentdate | sale_amount | return_amount | net_sales | net_sales_div_10 |
| ------- | ------------ | ----------- | ------------- | --------- | ---------------- |
| 101     | 2026-02-20   | 1000        | 200           | 800       | 80.0             |
| 101     | 2026-02-21   | 800         | 0             | 800       | 80.0             |
| 102     | 2026-02-20   | 1500        | 0             | 1500      | 150.0            |

توضیح

داده‌ها از CSV خوانده می‌شوند.

داده‌های فروش و مرجوعی جدا و گروه‌بندی می‌شوند.

فروش کلی و شاخص های مرتبط محاسبه میشوند.

خروجی CSV و نمودار روزانه برای هر فروشگاه تولید می‌شود.





