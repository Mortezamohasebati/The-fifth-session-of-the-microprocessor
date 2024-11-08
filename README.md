## گزارش کار 
درس: ریزپردازنده
نام دانشجو: مرتضی زینل محاسبتی / سینا عربشاهی
استاد : دکتر عباسی




---

# مقدمه

در این آزمایش، چهار بخش کد مختلف با هدف‌های متفاوت اجرا شده‌اند. هر بخش از کد شامل نمایش اطلاعات به شکل‌های گوناگون بر روی LCD کاراکتری 16x2 با استفاده از آردوینو است. هدف اصلی این آزمایش، آموزش نحوه استفاده از LCD برای نمایش پیام، پیمایش متنی، ایجاد انیمیشن ساده و خواندن اطلاعات از یک سنسور خارجی (فاصله‌سنج التراسونیک) و نمایش آن‌ها به‌صورت عددی بر روی LCD است.


---

قطعات و تجهیزات مورد استفاده

1. آردوینو Uno یا مدل‌های مشابه


2. LCD کاراکتری 16x2 با کنترلر HD44780


3. پتانسیومتر 10 کیلو اهم برای تنظیم کنتراست نمایشگر


4. سنسور فاصله‌سنج التراسونیک HC-SR04


5. بردبرد و سیم‌های جامپر برای برقراری اتصالات




---

بخش اول: نمایش پیام ثابت "Hello, World!"

توضیح عملکرد

در این بخش، هدف نمایش پیام ساده و ثابت "Hello, World!" بر روی LCD کاراکتری است. ابتدا با استفاده از کتابخانه LiquidCrystal، یک شیء برای LCD ایجاد می‌شود و پین‌های مرتبط با RS، EN و پین‌های داده D4 تا D7 مشخص می‌شوند. سپس در تابع setup()، تنظیمات اولیه LCD انجام شده و با استفاده از دستور lcd.print، پیام موردنظر در سطر اول نمایش داده می‌شود.

هدف و نتیجه

این بخش به‌منظور آشنایی با روش ساده نمایش پیام ثابت روی LCD طراحی شده است. پیام به‌درستی نمایش داده شد و امکان مشاهده پیام به‌طور ثابت بر روی صفحه‌نمایش فراهم گردید.


---

بخش دوم: پیمایش پیام

توضیح عملکرد

در این بخش، یک پیام متنی ("Hello, Arduino!") به‌صورت پیمایشی از سمت چپ به راست بر روی LCD نمایش داده می‌شود. برای ایجاد این افکت، از تابع substring در زبان برنامه‌نویسی آردوینو استفاده شده تا هر بار یک بخش از متن روی LCD چاپ شود. با یک تاخیر کوتاه بین هر نمایش، متن به‌صورت متحرک و پیمایشی دیده می‌شود.

هدف و نتیجه

هدف این بخش، پیاده‌سازی افکت پیمایش برای نمایش بهتر و جذاب‌تر پیام است. پیام "Hello, Arduino!" به‌صورت متحرک از سمت چپ به راست نمایش داده شد و قابلیت تنظیم سرعت پیمایش نیز از طریق تغییر زمان تأخیر وجود دارد.


---

بخش سوم: نمایش انیمیشن ساده

توضیح عملکرد

در این قسمت، دو کاراکتر سفارشی ایجاد شده که نشان‌دهنده یک شخص با دست‌های بالا و پایین است. این دو کاراکتر به کمک الگوی باینری برای هر پیکسل تعریف شده‌اند. سپس با استفاده از تابع lcd.createChar() این کاراکترها در LCD ذخیره می‌شوند. با تعریف یک آرایه از مختصات، این کاراکترها در موقعیت‌های مختلف روی LCD به نمایش در می‌آیند و به‌گونه‌ای دیده می‌شود که کاراکتر از سمت چپ سطر اول به سمت راست حرکت می‌کند و سپس به سطر دوم منتقل می‌شود.

هدف و نتیجه

هدف از این بخش، آشنایی با ایجاد و نمایش کاراکترهای سفارشی و نمایش انیمیشن ساده روی LCD بود. کاراکتر به‌صورت متحرک و انیمیشن بر روی LCD نمایش داده شد که نشان‌دهنده حرکتی ساده است. این بخش، امکان نمایش گرافیکی و ایجاد انیمیشن‌های سفارشی بر روی LCD را فراهم می‌کند.


---

بخش چهارم: نمایش فاصله با سنسور التراسونیک

توضیح عملکرد

در این بخش، فاصله توسط سنسور التراسونیک HC-SR04 اندازه‌گیری و سپس بر روی LCD نمایش داده می‌شود. ابتدا پین‌های trig و echo سنسور به آردوینو متصل می‌شوند. در هر بار اجرای loop(), پالس صوتی از طریق پین trig ارسال و زمان دریافت برگشت آن از طریق echo اندازه‌گیری می‌شود. با توجه به سرعت صوت، فاصله با فرمول مناسب محاسبه و روی LCD نمایش داده می‌شود.

هدف و نتیجه

هدف این بخش، نمایش اطلاعات سنسور خارجی (فاصله‌سنج التراسونیک) بر روی LCD بود. این روش برای نمایش اطلاعات عددی و لحظه‌ای بر روی نمایشگرهای LCD بسیار کاربردی است و در بسیاری از پروژه‌های مرتبط با فاصله‌سنجی و تشخیص اجسام قابل استفاده است. فاصله به‌درستی محاسبه و روی LCD نمایش داده شد.


---

نتیجه‌گیری کلی

در این آزمایش، به موفقیت نحوه استفاده از LCD کاراکتری 16x2 با آردوینو جهت نمایش پیام‌ها، پیمایش متن، انیمیشن ساده و داده‌های سنسور بررسی شد. هر بخش از کد به طور مؤثری عملکرد مطلوب خود را ارائه داد. این نتایج نشان داد که نمایشگرهای کاراکتری می‌توانند به سادگی و با استفاده از کتابخانه‌های مناسب، اطلاعات متنوعی را نمایش دهند و کاربرد بسیاری در پروژه‌های تعاملی و سیستم‌های تعبیه‌شده دارند.


---

پیشنهادات برای کارهای بعدی

برای ادامه و بهبود این پروژه، پیشنهادات زیر مطرح می‌گردد:

1. افزایش پیچیدگی انیمیشن‌ها: ایجاد انیمیشن‌های پیشرفته‌تر با استفاده از ترکیب چند کاراکتر سفارشی.
2. اضافه کردن داده‌های دیگر سنسورها: مانند دما، رطوبت و ... جهت نمایش در LCD.


3. بهینه‌سازی کدها: استفاده از روش‌های بهینه‌تر برای بهبود خوانایی و عملکرد کدها.


4. استفاده از نمایشگرهای دیگر: به عنوان مثال، نمایشگرهای OLED برای نمایش گرافیک‌های پیشرفته‌تر.




---

