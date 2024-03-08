# Software Engineering Lab
## آزمایش اول - مدیریت نسخ پروژه و یک‌پارچه‌سازی و استقرار مستمر

<br><br>
___

### روال انجام آزمایش
در این پروژه یک نرم‌افزار static frontend را به‌صورت pure پیاده‌سازی و سپس با کمک Github Actions  این نرم‌افزار static خود را به‌صورت خودکار، روی Github Pages مستقر (deploy) کرده‌ایم. تصویر زیر خروجی کار را نشان می‌دهد.
<br><br>
![alt text](/readme_resouce/readme1.png)
<br><br>
___

### پیش‌برد روند پروژه

ابتدا مخزن گیت‌هاب توسط PO ساخته شد و سپس دو عضو دیگر که developer هستند به مخزن اضافه شدند.همچنین مطابق تصویر زیر در تنظیمات مخزن، شاخه‌ی main را روی حالت protected تنظیم کرده تا بدون pull request تغییری صورت نگیرد.
<br><br>
![alt text](/readme_resouce/readme2.png)
<br><br>
در ادامه PO یک پروژه‌ی Kanban ساخته و task های پروژه را تعریف کرد که در تصویر زیر قابل مشاهده است.
![alt text](/readme_resouce/readme3.png)
<br><br>

مطابق user-story های تعریف شده دو شاخه‌ی اصلی برای محتوا و استایل ساخته شد که چون در صورت گزارش اشاره‌ای به issue کردن تسک ها در kanban نشده بود علاوه بر 7 تسک تعریف شده این دو شاخه را نیز به kanban اضافه کردیم که در نهایت به وضعیت done در آمد که در شکل زیر قابل مشاهده است. 
<br><br>
![alt text](/readme_resouce/readme4.png)
<br><br>

بعد از تمام شدن کار هر شاخه نیاز به pull request بود که دو تصویر زیر حالت آن در قبل و پس از review نشان می‌دهد. همانطور که مشخص است شخص مرور کننده کامیت هارا بررسی  و آن‌هارا approve تا با شاخه‌ی اصلی ادغام شود.
<br><br>
![alt text](/readme_resouce/readme5.png)
![alt text](/readme_resouce/readme6.png)
![alt text](/readme_resouce/readme7.png)
<br><br>

### حل کانفلیکت‌ها

<br><br>
___

### پرسش‌ها

1. پوشه‌ی .git چیست؟ چه اطلاعاتی در آن ذخیره می‌شود؟ با چه دستوری ساخته می‌شود؟ <br><br>
پوشه‌ی .git یک پوشه‌ی مخفی است که فراداده (metadata) و object database مربوط به پروژه را در خود ذخیره می‌کند. این بخش مهم‌ترین عضو Git بوده و همان بخشی است که وقتی یک repository را clone می‌کنیم به کامپیوتر دیگری کپی می‌شود. اطلاعات مهمی اعم از شاخه‌ها (branches)، کامیت‌ها، پیکربندی و ... در آن ذخیره می‌شود که در ادامه به توضیح آن‌ها خواهیم پرداخت: <br>
   objects:  شامل تمام اشیاء Git مانند کامیت‌ها، درختان (trees) و بلاب‌ها (blobs) است. <br>
   refs:  شامل اشاره‌گرها به کامیت‌ها، از جمله اشاره‌گرها به شاخه‌ها و تگ‌ها. <br>
   HEAD:  فایلی که شاخه فعال فعلی را نشان می‌دهد. <br>
   config:  فایلی که تنظیمات مخزن را نگهداری می‌کند. <br>
   index:  فایلی که حالت فعلی فضای کاری (working directory) را ثبت می‌کند. <br>
 پوشه‌ی hooks: این پوشه حاوی فایل‌های اسکریپت است. Git hookها اسکریپت‌هایی هستند که قبل یا بعد از رویدادهایی مانند commit، push و غیره اجرا می‌شوند. <br>
این پوشه با دستور git init در root ایجاد می‌شود. زمانی که این دستور را اجرا می‌کنیم، پوشه‌ی جدیدی در دایرکتوری فعلی ساخته شده و پروژه آماده‌ی مدیریت با Git می‌شود.
<br><br>
***