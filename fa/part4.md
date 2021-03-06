# ۴. آپدیت‌کردن HTTP

بهتر نیست که یک پرتکول بهتر بسازیم؟ پرتکولی که...

1. به تأخیرها کمتر حساس باشه
2. مشکل HTTP Pipelining رو و Head-of-line blocking رو حل کنه
3. نیازی به افزایش تعداد Host name نداشته باشه
4. از همین تعامل‌ها، محتوا و ساختارهای URI پشتیبانی کنه
5. و توسط کارگروه HTTPbis در IETF ساخته شده باشه!

## ۴.۱. IETF و کارگروه HTTPbis

IETF یک سازمان برای توسعه و ترویج استانداردهای اینترنت در سطح پرتکول است. این سازمان بیشتر به خاطر سری استانداردهای RFC شامل TCP، DNS، FTP و از همه بهتر HTTP و یک‌سری پرتکول‌های دیگر که هیچ‌جا شناخته نشده‌اند، مشهور است.

در IETF، کارگروه‌های اختصاصی با اختیارات محدود برای رسیدن به یک هدف مشخص کار می‌کنند. آن‌ها یک منشور مشخص می‌کنند تا خط‌مشی‌ها و محدودیت‌ها برای چیزی که تولید می‌کنند را مشخص کنند. همه‌ی افراد اجازه‌ی مشارکت در بحث و توسعه را دارند. هر کسی که شرکت می‌کند و چیزی می‌گوید، گفته‌ی او، اهمیت یکسانی نسبت به گفته‌های دیگران دارد و هر کسی به عنوان یک فرد مستقل شناخته می‌شود، بدون درنظرگرفتن شرکتی که او در آن‌جا کار می‌کند.

کارگروه HTTPbis در تابستان ۲۰۰۷ شکل گرفت و وظیفه دارد تا استانداردهای HTTP را آپدیت کند. در این گروه، بحث درمورد نسخه‌ی بعدی HTTP در اواخر سال ۲۰۱۲ شکل گرفت. کار آپدیت HTTP 1.1 در اوایل ۲۰۱۴ تمام شد که نتیجه‌ی آن را در سری [RFC 7230](https://tools.ietf.org/html/rfc7230) می‌بینید.

آخرین نشست فنی کارگروه HTTPbis در ژوئن ۲۰۱۴ در شهر نیویورک برگزار شد. بحث‌های باقی‌مانده و روند رسمی IETF انجام شدند تا این استاندارد RFC به طور رسمی سال بعد عرضه شود.

بازیگران بزرگ‌تر در عرصه‌ی HTTP در جلسات و گفتگوهای این کارگروه غایب بودند. نمی‌خواهم نام هیچ شرکت یا محصول خاصی را ببرم، اما واضح است که بعضی از بازیگران اصلی اینترنت امروز، مطمئن هستند که IETF بدون آن‌ها هم عملکرد خوبی خواهد داشت...

### ۴.۱.۱. پسوند bis

نام گروه HTTPbis است که پسوند bis از [در لاتین به معنای دو](https://en.wiktionary.org/wiki/bis#Latin) است. پسوند Bis معمولا در IETF برای هر آپدیت یا نسخه‌ی دوم هر چیزی استفاده می‌شود؛ مثلا همین به‌روز‌رسانی HTTP 1.1.

## ۴.۲. http2 از SPDY شروع شد

[SPDY](https://en.wikipedia.org/wiki/SPDY) یک پرتکول است که توسط گوگل توسعه‌ داده و توزیع شد. آن‌ها، این پرتکول را در یک محیط باز توسعه دادند و از همگان دعوت کردند که شرکت کنند ولی روشن است که آن‌ها با کنترل‌کردن پیاده‌سازی یک مرورگر پرطرفدار و هم‌چنین سرورهای پرجمعیتی که از سرویس‌ها استفاده می‌کردند، سود می‌بردند.

هنگامی که گروه HTTPbis تمصمیم گرفت که روی http2 کار کند، SPDY قبلا ثابت کرده بود که یک طرح عملی است. SPDY نشان داده بود که استفاده از آن در اینترنت ممکن است و آماری هم وجود دارد که تا چه حد خوب کار می‌کند. کار http2 با پیش‌نویس SPDY/3 شروع شد که به سادگی، تبدیل به پیش‌نویس صفر (draft-00) HTTP2 با کمی تغییر شد.
  
