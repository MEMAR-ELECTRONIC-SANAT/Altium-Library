![Altium Library — MES](Images/altium-library-banner.svg)

# کتابخانه قطعات Altium Designer | MES Altium Library

مخزن **MES Altium Library** مجموعه‌ای از کتابخانه‌های قطعات الکترونیکی برای استفاده در نرم‌افزار **Altium Designer** است. این مجموعه، فایل‌های کتابخانه شماتیک و PCB را همراه با یک کاتالوگ وب برای جست‌وجو و دریافت فایل‌های قطعات ارائه می‌کند.

**معمار الکترونیک صنعت (MES)** با هدف فراهم‌کردن منابع کاربردی برای طراحی مدارهای الکترونیکی، این مخزن را سازمان‌دهی و ارائه می‌کند.

<div dir="rtl">

## دسترسی سریع

- **<a href="https://memar-electronic-sanat.github.io/Altium-Library/" target="_blank" rel="noopener noreferrer">ورود به کاتالوگ آنلاین قطعات (GitHub Pages)</a>**
- [مشاهده فایل‌های کتابخانه PCB](./AltiumPCBLIB/)
- [مشاهده فایل‌های کتابخانه شماتیک](./AltiumSCHLIB/)
- [دریافت پایگاه داده قطعات (CSV)](./DB_MEMAR_Altium-Library.csv)
- [مشاهده تصاویر و منابع گرافیکی](./Images/)

</div>

---

## معرفی کاتالوگ آنلاین

[کاتالوگ آنلاین قطعات](https://memar-electronic-sanat.github.io/Altium-Library/) رابط وب این مخزن است. برای مشاهده کد منبع، فایل [index.html](https://github.com/MEMAR-ELECTRONIC-SANAT/Altium-Library/blob/main/index.html) را باز کنید. این صفحه اطلاعات قطعات را از فایل CSV موجود در ریشه مخزن می‌خواند و امکان مرور و جست‌وجوی کاتالوگ را فراهم می‌کند.

قابلیت‌های رابط وب (نسخه دوزبانه FA/EN، نسخه رابط 1.8):

- رابط کاربری دوزبانه فارسی و انگلیسی با امکان تغییر زبان از نوار بالای صفحه
- پشتیبانی از چیدمان راست‌به‌چپ (RTL) در حالت فارسی و چپ‌به‌راست (LTR) در حالت انگلیسی
- ذخیره انتخاب زبان در مرورگر و بازیابی آن در مراجعه بعدی
- تم آبی کبالتی با جزئیات کهربایی و فیروزه‌ای، هماهنگ با هویت بصری MES
- پنجره **About (درباره ما)** برای معرفی مجموعه و راه‌های ارتباطی
- پنجره **Help (راهنما)** شامل معرفی قابلیت‌ها، روش جست‌وجو و فیلتر، نحوه دریافت کتابخانه‌ها و نکات فنی
- صفحه آغازین (Splash Screen) با نشان تجاری MES
- جست‌وجوی قطعات بر اساس فیلدهای پایگاه داده؛ پشتیبانی از عبارت‌های منظم (Regular Expressions)
- فیلتر قطعات بر اساس نوع کتابخانه؛ شامل **Footprint** و **Schematic Symbol**
- فیلتر و انتخاب کتابخانه موردنظر از نوار کناری
- نمایش گروه‌بندی‌شده قطعات، شمارنده‌ها و صفحه‌بندی نتایج
- دسترسی مستقیم به پیوند دریافت فایل کتابخانه متناظر از مخزن GitHub
- طراحی واکنش‌گرا برای نمایشگرهای دسکتاپ و تلفن همراه

کاتالوگ داده‌ها را از فایل [DB_MEMAR_Altium-Library.csv](./DB_MEMAR_Altium-Library.csv) در ریشه مخزن دریافت می‌کند. برای عملکرد صحیح، صفحه باید از طریق GitHub Pages یا یک وب‌سرور HTTP اجرا شود؛ بازکردن مستقیم فایل با پروتکل `file://` ممکن است به دلیل محدودیت امنیتی مرورگر در دسترسی به CSV با خطا مواجه شود.

## ساختار مخزن

| مسیر | محتوا |
|---|---|
| [AltiumPCBLIB](./AltiumPCBLIB/) | کتابخانه‌های PCB با فرمت `.PcbLib` |
| [AltiumSCHLIB](./AltiumSCHLIB/) | کتابخانه‌های شماتیک با فرمت `.SchLib` |
| [DB_MEMAR_Altium-Library.csv](./DB_MEMAR_Altium-Library.csv) | پایگاه داده مورد استفاده کاتالوگ آنلاین |
| [Images](./Images/) | تصاویر و فایل‌های گرافیکی راهنما |
| [کاتالوگ آنلاین](https://memar-electronic-sanat.github.io/Altium-Library/) (فایل اجرایی)؛ [index.html](https://github.com/MEMAR-ELECTRONIC-SANAT/Altium-Library/blob/main/index.html) (کد منبع) |
| [.nojekyll](./.nojekyll) | فایل کمکی برای انتشار مستقیم محتوا در GitHub Pages |

## انواع کتابخانه

### ۱. کتابخانه PCB — Footprint

مسیر: [AltiumPCBLIB](./AltiumPCBLIB/)

فایل‌های `.PcbLib` الگوی فیزیکی قطعات را در محیط PCB تعریف می‌کنند. این الگوها می‌توانند شامل موارد زیر باشند:

- پدها (Pads) و شماره‌گذاری پایه‌ها
- خطوط و محدوده‌های مکانیکی بدنه
- علائم چاپ سیلک (Silkscreen)
- لایه‌های کمکی و اطلاعات مونتاژ
- مدل سه‌بعدی قطعه (3D Body)، در صورت وجود

### ۲. کتابخانه شماتیک — Schematic Symbol

مسیر: [AltiumSCHLIB](./AltiumSCHLIB/)

فایل‌های `.SchLib` نمایش منطقی قطعات را در نقشه شماتیک فراهم می‌کنند و ممکن است شامل پایه‌ها (Pins)، نام و شماره پایه، نوع الکتریکی پایه‌ها، مشخصات قطعه و ارتباط با Footprint متناظر باشند.

## روش استفاده در Altium Designer

1. مخزن را با گزینه **Download ZIP** دریافت یا با Git کلون کنید.
2. در Altium Designer پنل **Libraries** یا **Components** را باز کنید.
3. فایل کتابخانه موردنیاز را اضافه کنید:
   - برای نماد شماتیک: فایل `.SchLib`
   - برای الگوی PCB: فایل `.PcbLib`
4. نماد قطعه را در شماتیک قرار دهید و Footprint متناظر را به آن اختصاص دهید.
5. پیش از انتقال طراحی به محیط PCB، ارتباط Symbol و Footprint را بررسی کنید.

## کنترل فنی پیش از استفاده

اطلاعات کتابخانه باید با دیتاشیت و نقشه مکانیکی قطعه واقعی تطبیق داده شود. به‌ویژه موارد زیر را کنترل کنید:

- شماره پایه‌ها و ترتیب آن‌ها در Symbol
- تعداد، شماره‌گذاری، ابعاد و فاصله پدها در Footprint
- ابعاد بدنه و محدوده‌های مکانیکی پکیج
- نوع الکتریکی پایه‌ها و اتصالات تغذیه و زمین
- جهت‌گیری و ابعاد مدل سه‌بعدی، در صورت وجود
- تطبیق ارتباط بین Symbol و Footprint

پس از افزودن قطعات به پروژه، بررسی‌های **ERC** و **DRC** را اجرا کنید. وجود یک قطعه در کتابخانه به معنی تأیید صحت آن برای تولید نیست؛ بررسی نهایی بر اساس دیتاشیت سازنده بر عهده طراح است.

## پایگاه داده قطعات

فایل CSV فعلی شامل **10,972 رکورد** و **12 ستون** است: 4,284 رکورد از نوع `PCBLIB` و 6,688 رکورد از نوع `SCHLIB`. کاتالوگ نسخه 1.8 این فایل را از ریشه مخزن و با نام `DB_MEMAR_Altium-Library.csv` بارگذاری می‌کند.

**اصلاحات ساختاری:** 7 رکورد مربوط به قطعات `LTC2955`، `LTC2954`، `LTC2951` و `MAX16054` با 7 ردیف اطلاعاتی جابه‌جا‌شده ادغام شدند؛ مسیر کتابخانه به `AltiumSCHLIB/pwr_onoff_toggle.SchLib` اصلاح شد. نام ستون دوازدهم نیز از URL نامرتبط به `LAST_MODIFIED` تغییر یافت. پس از اصلاح، تمام 10,972 رکورد دقیقاً 12 ستون دارند و هیچ رکوردی فاقد `PATH` نیست.

**نکته اعتبارسنجی باقی‌مانده:** یک مسیر دیگر در داده‌ها با فایل موجود در مخزن تطبیق ندارد: `AltiumSCHLIB/adc_power_monitor.SchLib`. این مورد خارج از 14 ردیف اصلاح‌شده است و برای سالم بودن لینک مربوط به آن باید جداگانه بررسی شود.

فایل [DB_MEMAR_Altium-Library.csv](./DB_MEMAR_Altium-Library.csv) داده‌های موردنیاز کاتالوگ آنلاین را نگهداری می‌کند. رابط وب این فایل را بارگذاری کرده و اطلاعات آن را برای جست‌وجو، فیلتر و نمایش قطعات به‌کار می‌گیرد.

در صورت ویرایش ساختار یا نام ستون‌های CSV، منطق پردازش داده در `index.html` نیز باید متناسب با آن بررسی و به‌روزرسانی شود.

## مشارکت و گزارش خطا

برای پیشنهاد اصلاح یا افزودن کتابخانه جدید، از بخش [Issues](https://github.com/MEMAR-ELECTRONIC-SANAT/Altium-Library/issues) استفاده کنید. هنگام گزارش خطا، در صورت امکان شماره قطعه، سازنده، لینک دیتاشیت و توضیح دقیق مغایرت را ارائه دهید.

در مشارکت‌ها لطفاً این موارد را رعایت کنید:

- نام‌گذاری فایل‌ها و قطعات روشن و یکپارچه باشد.
- شماره پایه‌ها و ابعاد Footprint با دیتاشیت کنترل شوند.
- ارتباط Symbol و Footprint بررسی شود.
- تغییرات پیشنهادی همراه با مرجع فنی معتبر ارائه شوند.

## مجوز استفاده

شرایط استفاده، بازتوزیع و تغییر محتوای مخزن تابع فایل [LICENSE](./LICENSE) است. پیش از استفاده در پروژه‌های تجاری یا بازنشر محتوا، متن مجوز را مطالعه کنید.

## تصاویر و دیاگرام‌های راهنما

- [مشاهده پوشه تصاویر مخزن](./Images/)
- [تصویر سربرگ کتابخانه Altium](./Images/altium-library-banner.svg)

---

## تهیه و تدوین

**معمار الکترونیک صنعت**  
**MEMAR ELECTRONIC SANAT (MES)**

*همراه شما در مسیر طراحی و ساخت مدارهای مطمئن*

- **GitHub:** [MEMAR-ELECTRONIC-SANAT](https://github.com/MEMAR-ELECTRONIC-SANAT)
- **Telegram:** [Memar Electronic](https://t.me/Memar_Electronic)
- **Instagram:** [Memar Electronic](https://www.instagram.com/Memar.Electronic)
- **مشاهده سایر آموزش‌ها:** [MES GitHub](https://github.com/MEMAR-ELECTRONIC-SANAT)

---

# English

## Overview

**MES Altium Library** is a collection of electronic component libraries for **Altium Designer**. The repository provides schematic symbols, PCB footprints, a CSV component database, and a web-based catalog for browsing and locating library files.

The repository is organized and presented by **MEMAR ELECTRONIC SANAT (MES)** to provide practical resources for electronic design.

## Quick access

- **<a href="https://memar-electronic-sanat.github.io/Altium-Library/" target="_blank" rel="noopener noreferrer">Open the online component catalog (GitHub Pages)</a>**
- [PCB libraries](./AltiumPCBLIB/)
- [Schematic libraries](./AltiumSCHLIB/)
- [Component database (CSV)](./DB_MEMAR_Altium-Library.csv)
- [Images and graphics](./Images/)

## Online catalog

[The online component catalog](https://memar-electronic-sanat.github.io/Altium-Library/) provides the web interface. To inspect its source code, open [index.html](https://github.com/MEMAR-ELECTRONIC-SANAT/Altium-Library/blob/main/index.html). It loads component information from the CSV database stored in the repository root.

The bilingual FA/EN interface (UI version 1.8) includes:

- Persian and English language switching from the top toolbar
- Right-to-left (RTL) layout for Persian and left-to-right (LTR) layout for English
- Browser-based language preference persistence across visits
- Cobalt-blue theme with amber and teal accents, aligned with MES visual identity
- **About** dialog introducing the organization and contact channels
- **Help** dialog covering catalog features, search and filters, library downloads, and technical notes
- MES-branded splash screen
- Component search across database fields, including regular-expression (Regex) queries
- Type filters for **PCB Footprints** and **Schematic Symbols**
- Sidebar library selection and filtering
- Grouped results, live counters, and pagination
- Direct links to the corresponding library files in the GitHub repository
- Responsive layout for desktop and mobile screens

The catalog loads its component data from [DB_MEMAR_Altium-Library.csv](./DB_MEMAR_Altium-Library.csv) in the repository root. For reliable operation, serve the page through GitHub Pages or an HTTP web server. Opening the HTML file directly with the `file://` protocol may prevent the browser from loading the CSV database.

## Repository structure

| Path | Contents |
|---|---|
| [AltiumPCBLIB](./AltiumPCBLIB/) | PCB libraries in `.PcbLib` format |
| [AltiumSCHLIB](./AltiumSCHLIB/) | Schematic libraries in `.SchLib` format |
| [DB_MEMAR_Altium-Library.csv](./DB_MEMAR_Altium-Library.csv) | Component database used by the web catalog |
| [Images](./Images/) | Repository images and graphics |
| [Online catalog](https://memar-electronic-sanat.github.io/Altium-Library/) (live page); [index.html](https://github.com/MEMAR-ELECTRONIC-SANAT/Altium-Library/blob/main/index.html) (source code) |
| [.nojekyll](./.nojekyll) | Helper file for direct content publishing with GitHub Pages |

## Library types

### 1. PCB Footprints

Directory: [AltiumPCBLIB](./AltiumPCBLIB/)

The `.PcbLib` files define the physical land patterns used in PCB layout. A footprint may contain pads and pad numbering, mechanical outlines, silkscreen markings, assembly information, and a 3D body where available.

### 2. Schematic Symbols

Directory: [AltiumSCHLIB](./AltiumSCHLIB/)

The `.SchLib` files define the logical representation of components in schematics. A symbol may include pins, pin names and numbers, electrical pin types, component parameters, and a link to its corresponding PCB footprint.

## Using the libraries in Altium Designer

1. Download the repository using **Download ZIP** or clone it with Git.
2. Open the **Libraries** or **Components** panel in Altium Designer.
3. Add the required library file:
   - Schematic symbol: `.SchLib`
   - PCB footprint: `.PcbLib`
4. Place the symbol in the schematic and assign its corresponding footprint.
5. Verify the symbol-to-footprint mapping before transferring the design to PCB.

## Design verification

Always validate library data against the manufacturer's datasheet and package drawing. Check pin numbering, pad count and dimensions, pad pitch, package outline, electrical pin types, and 3D model orientation where applicable.

Run **ERC** and **DRC** checks as part of the design review. Library availability does not imply that a component has been approved for manufacturing; final verification remains the designer's responsibility.

## Component database

The current CSV contains **10,972 records** and **12 columns**: 4,284 `PCBLIB` records and 6,688 `SCHLIB` records. The v1.8 web catalog loads this root-level file as `DB_MEMAR_Altium-Library.csv`.

**Structural repairs:** The 7 records for `LTC2955`, `LTC2954`, `LTC2951`, and `MAX16054` were reconstructed by merging them with their 7 displaced continuation rows. Their library path now points to `AltiumSCHLIB/pwr_onoff_toggle.SchLib`. The twelfth column header was changed from an unrelated URL to `LAST_MODIFIED`. After repair, all 10,972 records have exactly 12 columns and none has an empty `PATH`.

**Remaining validation note:** One other CSV path does not match a file in the repository: `AltiumSCHLIB/adc_power_monitor.SchLib`. This is outside the 14 repaired rows and should be checked separately before relying on that entry's download link.

[DB_MEMAR_Altium-Library.csv](./DB_MEMAR_Altium-Library.csv) stores the data used by the online catalog. The web interface loads this file to search, filter, and display component records.

If the CSV structure or column names are changed, review the data-processing logic in `index.html` accordingly.

## Contributions and issue reports

Use the repository [Issues](https://github.com/MEMAR-ELECTRONIC-SANAT/Altium-Library/issues) page to report problems or suggest new libraries. When possible, include the part number, manufacturer, datasheet link, and a clear description of the issue.

Please keep file naming consistent, verify symbols and footprints against datasheets, check symbol-to-footprint mappings, and provide technical references for proposed changes.

## License

Use, redistribution, and modification of repository content are governed by the [LICENSE](./LICENSE) file. Review its terms before using or redistributing the content, especially in commercial projects.

## Guide Images and Diagrams

- [Browse repository images](./Images/)
- [Altium Library banner](./Images/altium-library-banner.svg)

---

## Prepared by

**MEMAR ELECTRONIC SANAT (MES)**

*Your partner in designing and building reliable circuits.*

- **GitHub:** [MEMAR-ELECTRONIC-SANAT](https://github.com/MEMAR-ELECTRONIC-SANAT)
- **Telegram:** [Memar Electronic](https://t.me/Memar_Electronic)
- **Instagram:** [Memar Electronic](https://www.instagram.com/Memar.Electronic)
- **More tutorials:** [MES GitHub](https://github.com/MEMAR-ELECTRONIC-SANAT)
