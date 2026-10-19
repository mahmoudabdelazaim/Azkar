# حِصْن — Azkar

<div dir="rtl">

تطبيق إسلامي عربي في **ملف HTML واحد** (`index.html`)، يجمع الأذكار ومواقيت الصلاة والقرآن والأدوات اليومية للمسلم، ويعمل مباشرة من المتصفح بدون تثبيت أو خادم أو حساب.

> «حِصْنٌ» — اسم التطبيق (كان سابقًا «حصن المسلم»).

</div>

A single-file, Arabic (RTL) Islamic companion web app: adhkar, prayer times, Quran listening, and daily worship trackers. No build step, no backend, no account. Open `index.html` and it runs.

---

## المميزات | Features

<div dir="rtl">

### الأذكار والصوتيات
- **أذكار الصباح والمساء**، أذكار النوم والاستيقاظ، أذكار بعد الصلاة، أذكار دخول المنزل والخروج، وأذكار المناسبات.
- **أدعية مأثورة**، دعاء الاستخارة، الصلاة على النبي ﷺ، وأسماء الله الحسنى.
- **مكتبة صوتية** بأربعة أقسام: **قرآن، أذكار، ابتهالات، أناشيد**، مع مشغّل يكمل من حيث توقفت، وتشغيل عشوائي، ومؤقت إيقاف.
- **مفضلة الأذكار** (نجمة بجانب كل قسم).
- **المسبحة** الإلكترونية مع إعدادات (اهتزاز، نقر، …).
- **الرقية الشرعية**: الآيات، الأدعية، الاستماع، والآداب.

### الصلاة والمواقيت
- **مواقيت الصلاة** والعدّ التنازلي للصلاة التالية، ومواقيت الغد، مع **ضبط المواقيت**.
- **اتجاه القبلة**.
- **متتبع الصلوات اليوم**، قضاء الصلوات الفائتة، نوافل اليوم، السنن الرواتب، سنن الجمعة، دليل صلاة المسافر.
- **التنبيهات والأذان**: إعدادات التنبيهات والتذكيرات (بما فيها الأذان) مجمّعة داخل الإعدادات.

### القرآن
- **ورد القرآن اليوم**، خطة ختمة القرآن، حاسبة ورد الختمة، سجل الختمات.
- متابعة الحفظ وجدول المراجعة، حاسبة الحفظ، دفتر تدبر الآيات، ومؤقت التدبر والورد.
- فهرس السور، الأنبياء في القرآن، وتجويد مبسّط.

### الصيام والتقويم
- صيام اليوم، رمضان وإمساكية رمضان، ست من شوال، الصيام المستحب القادم، قضاء الصيام، وأحكام الصيام.
- **التقويم الهجري** ومحوّل التاريخ، الأشهر الهجرية، والعدّ التنازلي للمناسبات.

### أدوات وحاسبات
- حاسبة الزكاة، زكاة الفطر، وحاسبة الكفارات والفدية.
- خطوات الوضوء، ركعات الصلوات، أركان الإسلام والإيمان، أعمال الحج والعمرة.
- الأربعون النووية، حديث اليوم، ذكر اليوم، واختبر معلوماتك.

### المتابعة الشخصية
- محاسبة النفس اليومية، عادات الخير، تحدي ٣٠ يومًا، عداد التوبة والاستغفار.
- سجل الصدقات والصدقة الجارية، دفتر الدعوات، دفتر الامتنان، دفتر الفوائد.
- **التقرير الأسبوعي** وسجل إنجازات العبادة.

### مكتبة الأحكام
- مئات المواضيع الفقهية والتربوية المختصرة في العبادات والمعاملات والأخلاق والأسرة والتقنية والميراث وغيرها.

### الإعدادات
- **المظهر**: اللون المميز وحجم الخط.
- **النسخة الاحتياطية**: تصدير بياناتك كملف نصي `hisn-backup-YYYY-MM-DD.txt`، واستعادتها برفع الملف نفسه.

</div>

---

## التشغيل | Getting Started

```bash
git clone https://github.com/mahmoudabdelazaim/Azkar.git
cd Azkar
```

Then either:

- **Open `index.html`** directly in a modern browser, or
- Serve the folder with any static server (needed for some browser features such as geolocation and notifications, which require a secure context):

```bash
python3 -m http.server 8000
# open http://localhost:8000
```

It can also be hosted on **GitHub Pages**: *Settings → Pages → Deploy from branch → `main` / root*.

---

## الصوتيات | Audio

The app looks for local audio in subfolders of `audio/`:

```
audio/
├── quran/
├── adhkar/
├── ibtihalat/
├── anasheed/
└── adhan/
```

Some tracks (e.g. Quran recitations, sample adhkar and adhan) are streamed from external hosts, so those need an internet connection.

---

## البيانات والخصوصية | Data & Privacy

- All your progress, settings, and trackers are stored **locally in your browser** (`localStorage`). Nothing is sent to a server owned by this project.
- **Location** (optional): used only to compute prayer times and the qibla direction, and to fetch the current weather from [Open-Meteo](https://open-meteo.com/).
- Clearing browser data erases your records, so use **Settings → Backup** regularly.

---

## التقنيات | Tech

- Plain **HTML + CSS + vanilla JavaScript** in one file, RTL layout (`dir="rtl"`, `lang="ar"`).
- Browser APIs: `localStorage`, Geolocation, Notifications, Media Session, Web Share, Vibration.
- Fonts: Amiri, Aref Ruqaa, IBM Plex Sans Arabic (Google Fonts).

---

## الإسهام | Contributing

Issues and pull requests are welcome. Since the whole app lives in `index.html`, please keep changes small and focused, and test on a mobile screen size since the UI is mobile-first.

## ملاحظة | Disclaimer

The Hukm (rulings) and educational content are brief summaries meant as a reminder. For detailed fatwas, please refer to qualified scholars.

## الترخيص | License

No license has been specified yet. Add a `LICENSE` file to state how others may use this project.

---

<div dir="rtl" align="center">

**جعله الله خالصًا لوجهه الكريم، ونفع به.**

</div>
