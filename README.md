# Car Motors — Microsoft Access Database

> مشروع أكاديمي عربي لإدارة معرض سيارات باستخدام Microsoft Access.

## About the project

**Car Motors** is an Arabic Microsoft Access database project for managing a car showroom. It demonstrates relational database design through tables, relationships, data-entry forms, queries with calculated fields, and printable reports.

هذا مشروع أكاديمي يطبق مفاهيم قواعد البيانات العلائقية في نظام لإدارة معرض سيارات. يسهّل تنظيم بيانات السيارات والعملاء والموظفين والمبيعات والصيانة وطرق الدفع، ويقلل تكرار البيانات من خلال العلاقات بين الجداول.

## Features

- إدارة السيارات: الاسم، الموديل، السعر، اللون، حالة التوفر، والشركة المصنعة.
- إدارة الشركات المصنعة.
- إدارة العملاء وبيانات التواصل.
- إدارة الموظفين: الاسم، المسمى الوظيفي، الهاتف، والراتب الشهري.
- تسجيل المبيعات وربطها بالسيارة والعميل والموظف وطريقة الدفع.
- تسجيل عمليات صيانة السيارات وتكلفتها وملاحظاتها.
- استعلامات بحث وحسابات تلقائية للخصم والضريبة والسعر النهائي.
- تقارير منسقة لسيارات المعرض قابلة للطباعة أو التصدير إلى PDF.
- واجهة عربية رئيسية للانتقال السريع بين أجزاء النظام.

## Database tables

| Table | Purpose | Key examples |
|---|---|---|
| السيارات | بيانات سيارات المعرض | رقم السيارة، الاسم، الموديل، السعر، اللون، متوفر |
| الشركات المصنعة | بيانات الشركات | رقم الشركة المصنعة، اسم الشركة، الدولة |
| العملاء | بيانات العملاء | رقم العميل، الاسم، الهاتف، البريد الإلكتروني، العنوان |
| الموظفين | بيانات العاملين | رقم الموظف، الاسم الكامل، المسمى الوظيفي، الهاتف، الراتب الشهري |
| المبيعات | عمليات البيع | رقم العملية، رقم السيارة، رقم العميل، رقم الموظف، تاريخ البيع، السعر النهائي، طريقة الدفع |
| طرق الدفع | وسائل السداد | رقم طريقة الدفع، اسم طريقة الدفع |
| الصيانة | سجلات صيانة السيارات | رقم الصيانة، رقم السيارة، تاريخ الصيانة، نوع الصيانة، التكلفة، ملاحظات |

## Relationships

The database uses one-to-many relationships to preserve referential integrity and avoid duplicate data:

- الشركة المصنعة → السيارات.
- السيارات → المبيعات.
- السيارات → الصيانة.
- العملاء → المبيعات.
- الموظفين → المبيعات.
- طرق الدفع → المبيعات.

See the relationship diagram in [`screenshots/relationships.jpg`](screenshots/relationships.jpg).

## Queries and reports

- **البحث عن سيارة**: استعلام تفاعلي يطلب رقم السيارة ويعرض تفاصيلها.
- **تفاصيل المبيعات**: يجمع معلومات السيارات والعملاء والموظفين وطرق الدفع في نتيجة واحدة.
- **حساب أسعار السيارات**: يحسب الخصم والضريبة والسعر النهائي باستخدام حقول محسوبة.
- **تقرير سيارات المعرض**: يعرض رقم السيارة والاسم والموديل واللون والسعر في تقرير قابل للطباعة.

## Screenshots

| View | Screenshot |
|---|---|
| Main interface | [Open](screenshots/main-interface.jpg) |
| Cars form | [Open](screenshots/cars-form.jpg) |
| Employees form | [Open](screenshots/employees-form.jpg) |
| Sales form | [Open](screenshots/sales-form.jpg) |
| Relationships | [Open](screenshots/relationships.jpg) |
| Calculated price query | [Open](screenshots/car-price-query.jpg) |
| Available cars report | [Open](screenshots/available-cars-report.jpg) |

## How to run

1. Install Microsoft Access.
2. Download the `.accdb` file from the `database/` folder after it is added.
3. Open the database with Microsoft Access.
4. Start from the Arabic main interface (الواجهة الرئيسية).

> The database file will be added later to `database/Car-Motors.accdb`.

## Technologies

- Microsoft Access
- Relational database design
- Arabic user-interface design

## Notes

The records shown in the screenshots are used for academic demonstration. Please avoid publishing real personal data in a public repository.
