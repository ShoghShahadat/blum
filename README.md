# بلومتود

CLAIM خودکار برای BLUM / @blum

[برای خواندن راهنمای اندونزیایی اینجا کلیک کنید](README_ID.md)

## فهرست مطالب
- [بلومتود](#blumtod)
- [فهرست مطالب](#table-of-contents)
- [هشدار](#warning)
- [ویژگی‌ها](#feature)
- [ثبت نام؟](#register-)
- [نحوه استفاده](#how-to-use)
  - [ویژگی پارامترهای Bot.py](#botpy-parameter-feature)
  - [درباره Config.json](#about-configjson)
  - [درباره پروکسی](#about-proxy)
  - [ویندوز](#windows)
  - [لینوکس](#linux)
  - [ترموکس](#termux)
- [راهنمای ویدئویی برای دریافت داده‌ها](#video-guide-to-get-data)
- [دستور جاوا اسکریپت برای دریافت داده‌های تلگرام برای دسکتاپ](#javascript-command-to-get-telegram-data-for-desktop)
- [اجرای 24/7](#run-for-247)
- [بحث](#discussion)
- [حمایت از کار من](#support-my-work)
- [سوالات متداول (QnA)](#qna)
- [تشکر](#thank-you--3)

## هشدار

تمامی ریسک‌ها بر عهده کاربر است.

## ویژگی‌ها

- [x] Claim خودکار
- [x] Claim روزانه خودکار
- [x] پشتیبانی از پروکسی، به [درباره پروکسی](#about-proxy) مراجعه کنید
- [x] پشتیبانی از چندین حساب کاربری
- [x] Claim خودکار پاداش ارجاع
- [x] تکمیل خودکار وظایف، به [درباره Config.json](#about-configjson) مراجعه کنید
- [x] بازی خودکار (ورودی تصادفی از کاربر)، به [درباره Config.json](#about-configjson) مراجعه کنید

## ثبت نام؟

برای ثبت نام روی لینک زیر کلیک کنید: [https://t.me/BlumCryptoBot/app?startapp=ref_aPYIYj1oKc](https://t.me/BlumCryptoBot/app?startapp=ref_aPYIYj1oKc)

## نحوه استفاده

### ویژگی پارامترهای Bot.py

در اینجا برخی از پارامترها برای فعال کردن ویژگی‌ها آمده است:

| پارامتر    | توضیحات                                            |
| ---------- | -------------------------------------------------- |
| --data     | تعیین فایل داده ورودی سفارشی (پیش‌فرض: data.txt)  |

### درباره Config.json

توضیحات Config.json:

| کلید               | توضیحات                                                                                                     |
| ------------------ | ----------------------------------------------------------------------------------------------------------- |
| interval           | نوع مقدار: عدد صحیح یا اعشاری <br> فاصله زمانی بین حساب‌ها                                                  |
| auto_complete_task | نوع مقدار: بولین (true/false)، فعال (true) برای فعال کردن تکمیل خودکار وظایف                               |
| auto_play_game     | نوع مقدار: بولین (true/false)، فعال (true) برای فعال کردن بازی خودکار                                       |
| game_point         | نوع مقدار: عدد صحیح یا اعشاری <br> کمترین امتیاز به دست آمده هنگام بازی <br> بالاترین امتیاز به دست آمده  |

### درباره پروکسی

در این سایت برای دریافت پروکسی رایگان ثبت‌نام کنید: [اینجا](https://www.webshare.io/?referral_code=dwj0m9cdi4mp)

می‌توانید لیست پروکسی خود را در `proxies.txt` اضافه کنید و قالب پروکسی مانند مثال زیر است:

قالب:

```
http://host:port
http://user:pass@host:port
```

مثال:

```
http://127.0.0.1:6969
http://user:pass@127.0.0.1:6969
socks5://127.0.0.1:6969
socks5://user:pass@127.0.0.1:6969
```

### ویندوز

1. مطمئن شوید که روی کامپیوتر شما python و git نصب شده است.
   
   پیشنهاد: از نسخه 3.8+ (یا بالاتر) پایتون استفاده کنید.

   سایت پایتون: [https://python.org](https://python.org)
   
   سایت گیت: [https://git-scm.com/](https://git-scm.com/)

2. این مخزن را کلون کنید:
   ```shell
   git clone https://github.com/akasakaid/blumtod.git
   ```

3. به دایرکتوری blumtod بروید:
   ```
   cd blumtod
   ```

4. کتابخانه‌های مورد نیاز را نصب کنید:
   ```
   python -m pip install -r requirements.txt
   ```

5. فایل `data.txt` را ویرایش کنید و توکن‌های خود را وارد کنید. توکن خود را در [نحوه یافتن توکن حساب](#how-to-find-account-token) بیابید. هر خط برای یک حساب است، اگر حساب دومی دارید، آن را در خط جدید اضافه کنید.

6. برنامه اصلی را اجرا کنید:
   ```
   python bot.py
   ```

### لینوکس

1. مطمئن شوید که python و git روی کامپیوتر شما نصب شده‌اند.

   پیشنهاد: از نسخه 3.8+ (یا بالاتر) پایتون استفاده کنید.

   python:
   ```shell
   sudo apt install python3 python3-pip
   ```

   git:
   ```shell
   sudo apt install git
   ```

2. این مخزن را کلون کنید:
   
   ```shell
   git clone https://github.com/akasakaid/blumtod.git
   ```

3. به دایرکتوری blumtod بروید:

   ```shell
   cd blumtod
   ```

4. کتابخانه‌های مورد نیاز را نصب کنید:

   ```
   python3 -m pip install -r requirements.txt
   ```

5. فایل `data.txt` را ویرایش کنید و توکن‌های خود را وارد کنید. توکن خود را در [نحوه یافتن توکن حساب](#how-to-find-account-token) بیابید. هر خط برای یک حساب است، اگر حساب دومی دارید، آن را در خط جدید اضافه کنید.

6. برنامه اصلی را اجرا کنید:
   ```
   python bot.py
   ```

### ترموکس

1. مطمئن شوید که در ترموکس شما python و git نصب شده‌اند.

   python:
   ```
   pkg install python
   ```

   git:
   ```
   pkg install git
   ```

2. این مخزن را کلون کنید:
   ```shell
   git clone https://github.com/akasakaid/blumtod.git
   ```

3. به دایرکتوری blumtod بروید:
   ```
   cd blumtod
   ```

4. کتابخانه‌های مورد نیاز را نصب کنید:
   ```
   python -m pip install -r requirements.txt
   ```

5. فایل `data.txt` را ویرایش کنید و توکن‌های خود را وارد کنید. توکن خود را در [نحوه یافتن توکن حساب](#how-to-find-account-token) بیابید. هر خط برای یک حساب است، اگر حساب دومی دارید، آن را در خط جدید اضافه کنید.

6. برنامه اصلی را اجرا کنید:
   ```
   python bot.py
   ```

## راهنمای ویدئویی برای دریافت داده‌ها

داده‌های مورد نیاز مانند [پیکسلورس‌بات](https://github.com/akasakaid/pixelversebot) است، بنابراین می‌توانید همان آموزش/راهنمای ویدئویی برای دریافت داده‌ها را مشاهده کنید:

اینجا: [https://youtu.be/KTZW9A75guI](https://youtu.be/KTZW9A75guI)

## دستور جاوا اسکریپت برای دریافت داده‌های تلگرام برای دسکتاپ

```javascript
copy(Telegram.WebApp.initData)
```

## اجرای 24/7

شما می‌توانید اسکریپت بات را به صورت 24/7 با استفاده از VPS یا RDP اجرا کنید. می‌توانید از برنامه `screen` در VPS لینوکس برای اجرای اسکریپت بات در پس‌زمینه استفاده کنید.

## بحث

اگر سوالی دارید یا نیاز به راهنمایی دارید، می‌توانید در اینجا بپرسید: [@sdsproject_chat](https://t.me/sdsproject_chat)

## حمایت از کار من

برای حمایت از من می‌توانید از طریق لینک‌های زیر به من قهوه بخرید:

- [اندونزی] https://s.id/nusanqr (QRIS)
- [اندونزی] https://trakteer.id/fawwazthoerif/tip
- [جهانی] https://sociabuzz.com/fawwazthoerif/tribe

## سوالات متداول (QnA)

س: آیا این بات/اسکریپت برنامه نیاز به استفاده از پروکسی دارد؟

ج: خیر، این بات/اسکریپت برنامه نیازی به استفاده از پروکسی ندارد.

س: چگونه می‌توانم از پروکسی استفاده کنم؟

ج: کافی است فایل `proxies.txt` را طبق قالبی
