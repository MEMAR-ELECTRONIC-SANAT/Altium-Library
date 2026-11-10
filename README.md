![Altium Library — MES](Images/altium-library-banner.svg)

# کتابخانه قطعات Altium Designer | MES Altium Library

مخزن **MES Altium Library** مجموعه‌ای از کتابخانه‌های قطعات الکترونیکی برای استفاده در نرم‌افزار **Altium Designer** است. این مجموعه، فایل‌های کتابخانه شماتیک و PCB را همراه با یک کاتالوگ وب برای جست‌وجو و دریافت فایل‌های قطعات ارائه می‌کند.

**معمار الکترونیک صنعت (MES)** با هدف فراهم‌کردن منابع کاربردی برای طراحی مدارهای الکترونیکی، این مخزن را سازمان‌دهی و ارائه می‌کند.

<div dir="rtl">

## دسترسی سریع

- **[ورود به کاتالوگ آنلاین قطعات (GitHub Pages)](https://memar-electronic-sanat.github.io/Altium-Library/)**
- [مشاهده فایل‌های کتابخانه PCB](./AltiumPCBLIB/)
- [مشاهده فایل‌های کتابخانه شماتیک](./AltiumSCHLIB/)
- [دریافت پایگاه داده قطعات (CSV)](./DB_Chilaboard_Altium-Library.csv)
- [مشاهده تصاویر و منابع گرافیکی](./Images/)

</div>

---

## معرفی کاتالوگ آنلاین

فایل [index.html](./index.html) رابط وب این مخزن است. این صفحه اطلاعات قطعات را از فایل CSV موجود در ریشه مخزن می‌خواند و امکان مرور و جست‌وجوی کاتالوگ را فراهم می‌کند.

قابلیت‌های رابط وب:

- جست‌وجوی قطعات بر اساس اطلاعات ثبت‌شده در پایگاه داده
- فیلتر قطعات بر اساس نوع کتابخانه؛ شامل **Footprint** و **Schematic Symbol**
- فیلتر و انتخاب کتابخانه موردنظر
- نمایش گروه‌بندی‌شده قطعات و صفحه‌بندی نتایج
- دسترسی به پیوند دریافت فایل کتابخانه متناظر
- رابط دوزبانه فارسی و انگلیسی
- طراحی واکنش‌گرا با هویت بصری آبی و کهربایی MES

برای عملکرد صحیح کاتالوگ، فایل HTML باید از طریق وب‌سرور یا GitHub Pages اجرا شود؛ بازکردن مستقیم آن با پروتکل `file://` ممکن است به دلیل محدودیت دسترسی مرورگر به فایل CSV با خطا مواجه شود.

## ساختار مخزن

| مسیر | محتوا |
|---|---|
| [AltiumPCBLIB](./AltiumPCBLIB/) | کتابخانه‌های PCB با فرمت `.PcbLib` |
| [AltiumSCHLIB](./AltiumSCHLIB/) | کتابخانه‌های شماتیک با فرمت `.SchLib` |
| [DB_Chilaboard_Altium-Library.csv](./DB_Chilaboard_Altium-Library.csv) | پایگاه داده مورد استفاده کاتالوگ آنلاین |
| [Images](./Images/) | تصاویر و فایل‌های گرافیکی راهنما |
| [index.html](./index.html) | رابط وب کاتالوگ قطعات |
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

فایل [DB_Chilaboard_Altium-Library.csv](./DB_Chilaboard_Altium-Library.csv) داده‌های موردنیاز کاتالوگ آنلاین را نگهداری می‌کند. رابط وب این فایل را بارگذاری کرده و اطلاعات آن را برای جست‌وجو، فیلتر و نمایش قطعات به‌کار می‌گیرد.

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

- **[Open the online component catalog (GitHub Pages)](https://memar-electronic-sanat.github.io/Altium-Library/)**
- [PCB libraries](./AltiumPCBLIB/)
- [Schematic libraries](./AltiumSCHLIB/)
- [Component database (CSV)](./DB_Chilaboard_Altium-Library.csv)
- [Images and graphics](./Images/)

## Online catalog

[index.html](./index.html) provides the web interface. It loads component information from the CSV database stored in the repository root.

The interface provides:

- Component search across the available database fields
- Type filters for **PCB Footprints** and **Schematic Symbols**
- Library selection and filtering
- Grouped results and pagination
- Links to the corresponding library files
- Persian and English user interfaces
- Responsive layout with MES blue-and-amber branding

For reliable operation, serve the page through a web server or GitHub Pages. Opening the HTML file directly with the `file://` protocol may prevent the browser from loading the CSV database.

## Repository structure

| Path | Contents |
|---|---|
| [AltiumPCBLIB](./AltiumPCBLIB/) | PCB libraries in `.PcbLib` format |
| [AltiumSCHLIB](./AltiumSCHLIB/) | Schematic libraries in `.SchLib` format |
| [DB_Chilaboard_Altium-Library.csv](./DB_Chilaboard_Altium-Library.csv) | Component database used by the web catalog |
| [Images](./Images/) | Repository images and graphics |
| [index.html](./index.html) | Web-based component catalog |
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

[DB_Chilaboard_Altium-Library.csv](./DB_Chilaboard_Altium-Library.csv) stores the data used by the online catalog. The web interface loads this file to search, filter, and display component records.

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
