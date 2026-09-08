# 🎬 Netflix Movies & TV Shows Analytics Dashboard

![Netflix Dashboard Banner](https://img.shields.io/badge/Power%20BI-Netflix%20Analytics-E50914?style=for-the-badge&logo=powerbi&logoColor=white)
![Theme](https://img.shields.io/badge/Theme-Netflix%20Soft%20Dark-141414?style=for-the-badge)
![Status](https://img.shields.io/badge/Status-Completed-success?style=for-the-badge)

لوحة تحكم وتطبيق تحليلي تفاعلي مصمم باستخدام **Power BI** لتحليل وتصور بيانات منصة **Netflix** الشاملة. يتميز المشروع بتصميم فاخر بلغة **Dark Luxury** مستوحى من الهوية البصرية الرسمية لمنصة Netflix، مع تقديم تحليلات دقيقة ومتعمقة للمحتوى، التوزيع الجغرافي، التصنيفات العمرية، والاتجاهات الزمنية.

---

## 📸 معاينة التقرير (Dashboard Preview)

<div align="center">
  <img src="Netflix Dashboard.png" alt="Netflix Power BI Dashboard Preview" width="900" style="border-radius: 10px; box-shadow: 0px 4px 20px rgba(0,0,0,0.5);">
</div>

---

## 🌟 المميزات الرئيسية (Key Features)

- 🎨 **تصميم مخصص (Custom Dark Luxury Theme):**
  - اعتماد هويّة بصريّة احترافية مخصصة (`Netflix_Soft_Dark.json`) بالألوان الأيقونية للمنصة (`#E50914` الأحمر الشهير، والخلفيات الداكنة التفاعلية).
  - واجهات سلسة توفر تجربة مستخدم (UX/UI) مريحة ومبسطة مع تباين عالي في القراءة.

- 📊 **تحليلات شاملة للمحتوى (Content Distribution):**
  - مقارنة شاملة بين **الأفلام (Movies)** و**المسلسلات (TV Shows)**.
  - تحليل توزيع المحتوى حسب **التصنيفات والأنواع (Genres & Categories)**.

- 🌍 **التحليل الجغرافي (Geographic Insights):**
  - خريطة تفاعلية ومخططات توضح أعلى الدول إنتاجاً للمحتوى المتاح على المنصة.

- ⏱️ **الاتجاهات الزمنية (Time-Series Trends):**
  - تتبع نمو وإضافة المحتوى عبر السنوات (Release Year vs Added Year).
  - تحليل أوقات الذروة والمحتوى حسب مدة العرض (Duration/Seasons).

- 🔞 **التصنيف العمري وتقييم الجمهور (Ratings Breakdown):**
  - عرض توزيع الفئات العمرية (`TV-MA`, `TV-14`, `PG-13`, `R`, إلخ) ونسبة كل فئة.

---

## 🛠️ التقنيات والأدوات المستخدمة (Tech Stack & Tools)

- **Power BI Desktop:** لبناء وإعداد التقرير والمخططات التفاعلية.
- **DAX (Data Analysis Expressions):** لكتابة المقاييس المخصصة (Custom Measures)، والحسابات التجميعية (Calculations).
- **Power Query (M Code):** لتنظيف البيانات، معالجتها، وإعادة هيكلتها (Data Cleaning & Transformation).
- **JSON Custom Theme:** ملف سمة داكنة مخصص لتعديل لوحة الألوان (`Netflix_Soft_Dark.json`).

---

## 📐 قياسات DAX الأساسية (Sample DAX Measures)

```dax
// إجمالي المحتوى
Total Titles = COUNTROWS('Netflix_Titles')

// إجمالي الأفلام
Total Movies = CALCULATE([Total Titles], 'Netflix_Titles'[type] = "Movie")

// إجمالي المسلسلات
Total TV Shows = CALCULATE([Total Titles], 'Netflix_Titles'[type] = "TV Show")

// نسبة الأفلام
% Movies = DIVIDE([Total Movies], [Total Titles], 0)
```

---

## 📂 هيكل المشروع (Repository Structure)

```text
├── Report/
│   ├── Layout                    # تصميم الصفحات والواجهات Tiled Layout
│   └── StaticResources/
│       └── RegisteredResources/
│           └── Netflix_Soft_Dark.json  # السمة البصرية المخصصة
├── DataModel                     # نموذج البيانات والمشاركات
├── README.md                      # توثيق المشروع
```

---

## 🚀 كيفية التشغيل (How to Run)

1. قم بتحميل مشروع Power BI ملف `.pbix` أو افتحه من خلال **Power BI Desktop**.
2. تأكد من ربط مصدر البيانات (Data Source Settings) في حال احتجت إلى تحديث البيانات.
3. لتطبيق السمة الداكنة المخصصة:
   - اذهب إلى تبويب **View** > **Themes** > **Browse for themes**.
   - اختر الملف `Netflix_Soft_Dark.json` المتواجد داخل المجلد.

---

## 👤 إعداد وتطوير (Author)

- **حسين زهران (Hussein Zahran)**
- 🎓 طالب ذكاء اصطناعي - جامعة الزيتونة الأردنية
- 💼 مهتم بذكاء الأعمال (Business Intelligence)، تحليل البيانات، والذكاء الاصطناعي.

---
<div align="center">
  <sub>تم إنشاء هذا الملف وتوثيقه باحترافية لتناسب مشاريع Portfolio و GitHub.</sub>
</div>
