# نام دیتاست
### Persian Snappfood & Digikala Comments Sentiment Analysis (DKSF)

<div align="right">

دیتاست نظرات کاربران **دیجی‌کالا** و **اسنپ‌فود** به زبان فارسی برای **تحلیل احساسات**.

</div>

## درباره دیتاست
- **زبان :** فارسی
- **تعداد نمونه‌ها :**
  - Train: 28,602 نمونه
  - Test: 2,315 نمونه
- **لیبل کلاس ها :**
  - 0 → negative (منفی)
  - 1 → positive (مثبت)
  - 2 → neutral (خنثی)

## ساختار دیتاست
هر نمونه شامل دو ستون است :

| ستون   | نوع داده | توضیحات                                 |
|--------|-----------|------------------------------------------|
| `text` | string    | متن نظر کاربر (کامنت)                  |
| `label`| int       | لیبل احساسات (۰=منفی، ۱=مثبت، ۲=خنثی) |

## لینک دیتاست
https://huggingface.co/datasets/hezarai/sentiment-dksf

## فایل پروژم

<div align="center">

<a href="https://github.com/amir-v-z/Project-NLP/blob/main/project.ipynb"><img src="https://media.giphy.com/media/v1.Y2lkPTc5MGI3NjExNmRkOXUxbXo3ejhsbWRleTdxc2h2Y29jZ2x2OG1rNDRhbnV0NGNzciZlcD12MV9zdGlja2Vyc19zZWFyY2gmY3Q9cw/zTLHQqoO61y8xgdyus/giphy.gif" width="150"></a>

</div>

## کار هایی که روی دیتاست انجام دادم

* بررسی های اولیه دیتاست (Initial Dataset Reviews)
  - بارگزاری دیتاست (آموزشی)
  - بررسی تعداد ستون ها
  - توزیع کلاس های ستون ها
  - آمارگیری اولیه قبل پیش پردازش
* پیش پردازش متن (Preprocessing Text)
  - نرمالسازی، توکنایز، حذف کلمات اضافه
  - آمارگیری بعد از پیش پردازش
  - رفع مشکل داده های NaN
* نمایش متن (Text Embedding)
  - از روش های کلاسیک (TF-IDF)
    * انتخاب بهترین مقدار برای max_features
    * ذخیره Vectorizer
  - از روش های شبکه های عصبی (FastText, Word2Vec)
  - از روش های زبانی زمینه ای (ParsBERT)
  - مقایسه روش ها
* طراحی و پیاده سازی مدل کاربردی
  - بارگزاری دیتاست (تستی)
  - انجام مراحل پیش پردازش و نمایش متن روی داده های تست
  - مقایسه عملکرد روی داده تست