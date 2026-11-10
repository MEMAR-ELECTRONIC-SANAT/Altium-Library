# Altium Library | کتابخانه قطعات Altium Designer

مخزن **Altium-Library** مجموعه‌ای از کتابخانه‌های قطعات الکترونیکی برای استفاده در نرم‌افزار **Altium Designer** است. ساختار مخزن شامل کتابخانه‌های شماتیک و PCB است تا بتوانید نماد قطعه را در طراحی شماتیک و الگوی فیزیکی آن را در طراحی برد به‌کار ببرید.

این مخزن بر پایه پروژه **Chilaboard Altium Library** معرفی شده است و نسخه اولیه README به مجموعه‌ای با بیش از ۵۰۰۰ قطعه اشاره می‌کند. برای جست‌وجوی آنلاین قطعات نیز می‌توانید از پیوند زیر استفاده کنید.

- **جست‌وجوی آنلاین قطعات:** [Altium Library Online Search](https://chilaboard.github.io/Altium-Library/)

---

## ساختار کتابخانه‌ها

### ۱. کتابخانه PCB — Footprint

مسیر: [AltiumPCBLIB](./AltiumPCBLIB/)

این پوشه برای نگهداری کتابخانه‌های PCB با فرمت **.PcbLib** در نظر گرفته شده است. هر Footprint نمایانگر الگوی فیزیکی یک قطعه روی برد است و معمولاً شامل پدها (Pads)، شماره‌گذاری، لایه‌های مکانیکی و چاپ سیلک (Silkscreen)، محدوده بدنه و در صورت وجود مدل سه‌بعدی (3D Body) می‌شود.

### ۲. کتابخانه شماتیک — Symbol

مسیر: [AltiumSCHLIB](./AltiumSCHLIB/)

این پوشه برای نگهداری کتابخانه‌های شماتیک با فرمت **.SchLib** است. هر Symbol نمایش منطقی قطعه در نقشه شماتیک را فراهم می‌کند و می‌تواند شامل پایه‌ها (Pins) با نام، شماره و نوع الکتریکی، شکل گرافیکی، مشخصات قطعه و ارتباط با Footprint متناظر باشد.

---

## ارتباط کتابخانه شماتیک و PCB

در جریان معمول طراحی، ابتدا Symbol قطعه از کتابخانه شماتیک در سند **Schematic** قرار می‌گیرد و سپس Footprint متناظر آن برای انتقال به محیط **PCB** اختصاص داده می‌شود.

| بخش | فرمت فایل | کاربرد |
|---|---|---|
| کتابخانه شماتیک | .SchLib | نمایش منطقی قطعه در نقشه مدار |
| کتابخانه PCB | .PcbLib | تعریف پدها و الگوی فیزیکی قطعه روی برد |

وجود Symbol و Footprint متناظر، به‌تنهایی تضمین‌کننده صحت قطعه نیست؛ تطبیق دقیق آن‌ها با دیتاشیت سازنده ضروری است.

## روش استفاده در Altium Designer

1. مخزن را دانلود یا Clone کنید.
2. در Altium Designer از پنل **Libraries** یا بخش **Components**، کتابخانه موردنیاز را اضافه کنید.
3. برای قطعات شماتیک، فایل‌های **.SchLib** و برای الگوهای PCB، فایل‌های **.PcbLib** را انتخاب کنید.
4. در صورت نیاز، مسیر کتابخانه‌ها را در تنظیمات جست‌وجوی کتابخانه یا Workspace خود ثبت کنید.
5. پس از قرار دادن قطعه در شماتیک، تخصیص Footprint و ارتباط آن با قطعه را بررسی کنید.

## نکات فنی و کنترل کیفیت

پیش از استفاده از هر قطعه در طراحی نهایی، موارد زیر را بررسی کنید:

- شماره‌گذاری و ترتیب پایه‌های Symbol با دیتاشیت قطعه مطابقت داشته باشد.
- شماره، تعداد، ابعاد و فاصله پدهای Footprint با پکیج واقعی قطعه یکسان باشد.
- ابعاد بدنه و محدوده‌های مونتاژ با نقشه مکانیکی دیتاشیت کنترل شوند.
- نوع پایه‌ها و اتصالات تغذیه، زمین و سیگنال در Symbol به‌درستی تعریف شده باشند.
- در صورت وجود مدل سه‌بعدی، جهت‌گیری و ابعاد آن با قطعه واقعی تطبیق داده شود.
- پس از افزودن قطعات به پروژه، بررسی‌های **ERC** و **DRC** انجام شوند.

**توجه:** کتابخانه‌ها ابزار کمکی طراحی هستند. مسئولیت بررسی نهایی Symbol، Footprint، شماره پایه‌ها و انطباق با دیتاشیت بر عهده طراح است.

## به‌روزرسانی فهرست قطعات

در نسخه اولیه این پروژه، برای به‌روزرسانی فهرست قطعات از اسکریپت زیر نام برده شده است:

```bash
python scanlib.py
```

این دستور را در محیط و مسیر مناسب پروژه اجرا کنید؛ پیش از اجرا، وجود فایل **scanlib.py** و پیش‌نیازهای آن را در نسخه دریافت‌شده بررسی کنید.

## مشارکت و توسعه

برای توسعه این مجموعه می‌توانید کتابخانه‌های جدید یا اصلاحات مربوط به قطعات موجود را در مخزن مشارکت دهید. هنگام افزودن یا اصلاح قطعه، لطفاً نام‌گذاری منظم، تطبیق با دیتاشیت و هماهنگی بین Symbol و Footprint متناظر را رعایت کنید.

## تصاویر و دیاگرام‌های راهنما

در حال حاضر تصویر یا دیاگرام مستقلی در این بخش از README معرفی نشده است. در صورت افزودن تصاویر راهنما به مخزن، پیوند آن‌ها در همین بخش قرار خواهد گرفت.

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

**Altium-Library** is a collection of electronic component libraries for **Altium Designer**. It provides schematic symbols and PCB footprints used during circuit design and printed circuit board layout.

The repository is introduced as being based on **Chilaboard Altium Library**. The original README refers to a collection of more than 5,000 components. Online component search is available here:

- **Online component search:** [Altium Library Online Search](https://chilaboard.github.io/Altium-Library/)

## Library directories

### 1. PCB Footprints

Directory: [AltiumPCBLIB](./AltiumPCBLIB/)

This directory contains PCB libraries in **.PcbLib** format. A footprint defines the physical land pattern of a component, including pads, pad numbering, silkscreen, mechanical outlines and, where available, 3D bodies.

### 2. Schematic Symbols

Directory: [AltiumSCHLIB](./AltiumSCHLIB/)

This directory contains schematic libraries in **.SchLib** format. A schematic symbol represents the logical function and pins of a component. It may also include component parameters and an associated PCB footprint.

## Using the libraries

1. Clone or download this repository.
2. In Altium Designer, open the **Libraries** or **Components** panel.
3. Add the required **.SchLib** or **.PcbLib** files.
4. Place schematic symbols in your schematic and assign the corresponding PCB footprints.
5. Verify component mappings before transferring the design to the PCB document.

## Design verification

Always verify pin numbers, pin types, pad dimensions, pad pitch, package outline and footprint orientation against the manufacturer's datasheet. Run **ERC** and **DRC** checks as part of the design review.

Library content is provided as a design aid. The designer remains responsible for validating every symbol and footprint before manufacturing.

## Updating the component list

The original project README mentions the following command for scanning the library:

```bash
python scanlib.py
```

Before running it, verify that **scanlib.py** and its required dependencies are present in your local copy.

## Contributing

Contributions of new or corrected component libraries are welcome. Please keep naming consistent, use manufacturer datasheets as the reference, and verify schematic-to-footprint mapping.

## Guide Images and Diagrams

No standalone guide images or diagrams are currently referenced in this README. Links to relevant visual documentation can be added here when such files are available.

---

## Prepared by

**MEMAR ELECTRONIC SANAT (MES)**  
*Your partner in designing and building reliable circuits.*

- **GitHub:** [MEMAR-ELECTRONIC-SANAT](https://github.com/MEMAR-ELECTRONIC-SANAT)
- **Telegram:** [Memar Electronic](https://t.me/Memar_Electronic)
- **Instagram:** [Memar Electronic](https://www.instagram.com/Memar.Electronic)
- **More tutorials:** [MES GitHub](https://github.com/MEMAR-ELECTRONIC-SANAT)
