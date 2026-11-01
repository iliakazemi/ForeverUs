# اپلیکیشن اندروید foreverus.ir

اپ یک پوسته‌ی WebView است که مستقیم به https://foreverus.ir/ وصل می‌شود.
هر تغییری روی سایت بدهید، بدون ساخت دوباره‌ی APK، همان لحظه در اپ دیده می‌شود.

امکانات: کشیدن به پایین برای رفرش، نوار پیشرفت، دکمه‌ی برگشت، صفحه‌ی «بدون اینترنت»،
آپلود فایل از داخل سایت، باز شدن لینک‌های بیرونی و tel:/mailto: در برنامه‌های خودشان.

## روش ۱: ساخت APK بدون نصب چیزی (GitHub)
1. یک مخزن (repository) جدید در GitHub بسازید و همه‌ی فایل‌های این پوشه را در آن آپلود کنید.
2. به تب **Actions** بروید، workflow با نام **Build APK** را اجرا کنید (Run workflow).
3. بعد از چند دقیقه، در پایین صفحه‌ی اجرا، بخش **Artifacts** فایل `ForeverUs-APK` را دانلود کنید.
4. داخلش `app-debug.apk` است. روی گوشی نصب کنید (اجازه‌ی نصب از منبع ناشناس لازم است).

## روش ۲: Android Studio
پوشه را با Android Studio باز کنید، صبر کنید Sync تمام شود،
سپس **Build > Build APK(s)** را بزنید.

## شخصی‌سازی
- نام اپ: `app/src/main/res/values/strings.xml`
- رنگ آیکن: `app/src/main/res/values/colors.xml`
- آیکن (فعلاً یک قلب ساده است): `app/src/main/res/drawable/ic_launcher_foreground.xml`
  یا در Android Studio: روی `res` راست‌کلیک > New > Image Asset
- آدرس سایت: ثابت‌های `HOME_URL` و `HOST` در `MainActivity.java`

## نکته
این APK با کلید debug امضا شده و برای نصب مستقیم روی گوشی مناسب است.
برای انتشار در Google Play یا کافه‌بازار باید نسخه‌ی release با کلید امضای خودتان ساخته شود.
