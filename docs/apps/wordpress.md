---
sidebar_position: 5

---

# وردپرس


## نحوه استفاده

### ورود به سرور

با اطلاعات ssh که در اطلاعات سرور ابری در پنل هایو قابل مشاهده است یا از طریق ایمیلی که برای شما ارسال شده است ‌‌می‌توانید به سرور وارد شوید.

** پورت پیش فرض ssh در سرورهای هایو ۲۲۸۰ است

### دریافت اطاعات ورود به وردپرس

اطلاعات ورود به وردپرس از ۲ طریق زیر قابل دسترسی است:

- [x] بعد از ssh به سرور در مسیر <span dir="ltr">/home/bitnami/bitnami_credentials</span>
 


- [x] از طریق کنسول هایو اطلاعات ورود در کنسول چاپ شده است

### اطلاعات ورود به دیتابیس

اطلاعات ورود به دیتابیس به شرح زیر است:

- نام کاربری: root
- رمز عبور: همان رمزی که در بخش دریافت اطلاعات ورود به وردپرس بدست آورده‌اید

### نحوه ست کردن دامین

در یک دی ان اس منیجر مثل کلودفلر یا ارائه‌‌دهندگان مشابه دامنه خود را اضافه کنید. سپس اقدام زیر را انجام دهید:

- یک A Record با مقادیر @ و www برای دامنه خود اضافه کنید

حالا براحتی با دامنه می‌توانید سایت خود را مشاهده کنید

### نحوه فعال‌سازی گواهی رایگان Let's Encrypt certificate SSL

برای این کار از طریق ssh یا کنسول هایو به سرور خود وارد شوید و سپس دستور زیر را وارد نمایید:

‍‍``` sudo /opt/bitnami/bncert-tool ```

سپس به سوالات آن اینگونه پاسخ دهید:

- Domains => دامنه سایت مورد نظر را به شکل www.mydomain.com mydomain.com وارد نمایید.

Enable/disable redirections:

- Enable HTTP to HTTPS redirection [Y/n]: Y
- nable non-www to www redirection [Y/n]: Y
- Enable www to non-www redirection [y/N]: N
- Do you agree to these changes? [Y/n]: Y
- E-mail address []: یک آدرس ایمیل اضافه کنید
- Do you agree to the Let's Encrypt Subscriber Agreement? [Y/n]: Y
- Enter

 در نهایت با پیام زیر مواجه می‌شوید:
 
<p dir="ltr">

Success

The Bitnami HTTPS Configuration Tool succeeded in modifying your installation.
</p>

