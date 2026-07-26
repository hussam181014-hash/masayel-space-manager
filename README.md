# 🏪 Space OS — استخبارات الموردين

نظام إدارة مساحات الأرفف (رف عادي / طبلية / ثلاجة) وتوزيعها على الموردين، مع مسح باركود وتقارير تحليلية.

![Aurora Daylight Theme](preview.html)

## ✨ المميزات

- 🎯 **إنشاء أرفف ذكي**: رف عادي، طبلية، ثلاجة (نوع A أو B) — مع توليد أكواد القواطع تلقائيًا
- 📱 **PWA قابل للتثبيت**: يتثبت على الشاشة الرئيسية زي أي تطبيق (أندرويد وآيفون)، ويشتغل أوفلاين بعد أول فتحة
- 📷 **Barcode Scanner**: يمسح كود القاطع بكاميرا الجوال
- 🖨️ **طباعة باركود (QR)**: قاطع واحد، أو رف كامل، أو مجموعة أرفف مع بعض دفعة واحدة — من خريطة الموقع
- 📊 **تقارير شاملة**: خريطة الموقع (Treemap)، توزيع الموردين، معدل الدوران، توزيع التصنيفات
- 🔐 **نظام صلاحيات**: مالك / مستخدم بصلاحيات محدودة
- 🎨 **ثيم Aurora Daylight**: تصميم عصري مريح للعين
- 🌐 **RTL Arabic**: واجهة عربية كاملة من اليمين للشمال

## 🚀 التشغيل

التطبيق Single-Page HTML — مفيش build step:

```bash
# الطريقة 1: افتح index.html في المتصفح مباشرة
open index.html

# الطريقة 2: شغّل سيرفر محلي (مستحسن عشان الـ Service Worker)
python3 -m http.server 8000
# افتح http://localhost:8000
```

## 🔧 الإعداد

1. أنشئ مشروع على [Supabase](https://supabase.com)
2. شغّل الـ migrations المرفقة (هتحتاج تعملها أو تنشئها)
3. حدّث الـ credentials في `index.html`:
   ```js
   const SUPABASE_URL = "your-project-url";
   const SUPABASE_ANON_KEY = "your-anon-key";
   ```

## 🛠️ Tech Stack

- **Frontend**: Vanilla HTML/CSS/JS (zero dependencies)
- **Backend**: Supabase (PostgreSQL + Auth + RLS)
- **Charts**: Chart.js
- **QR Scanner**: html5-qrcode
- **QR Label Printing**: qrcode.js
- **Icons**: Tabler Icons
- **Font**: IBM Plex Sans Arabic

## 📂 هيكل المشروع

```
.
├── index.html              # التطبيق الرئيسي
├── preview.html            # Aurora Daylight Theme Preview
├── icons/                  # أيقونات الـ PWA (192/512 + maskable + apple-touch-icon + favicon)
├── README.md
└── LICENSE
```

## 🎨 الألوان (Aurora Daylight)

| Token | Color | Usage |
|---|---|---|
| `--accent` | `#0d9488` | Primary actions, links |
| `--accent-2` | `#7c3aed` | Secondary highlights |
| `--amber` | `#d97706` | Premium tier, warnings |
| `--danger` | `#e11d48` | Errors, destructive actions |

## 📜 License

MIT License — see [LICENSE](LICENSE)

## 👤 المؤلف

**اسمك** — [@github-username](https://github.com/اسم-المستخدم-بتاعك)
