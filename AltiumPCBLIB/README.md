# کتابخانه فوت‌پرینت‌های PCB در Altium Designer
**Altium PCB Footprint Library**

این پوشه برای نگهداری کتابخانه‌های **PCB Library** با پسوند **.PcbLib** در نرم‌افزار Altium Designer در نظر گرفته شده است. هر Footprint، الگوی فیزیکی یک قطعه روی برد مدار چاپی را تعریف می‌کند و مبنای جانمایی و اتصال پایه‌های قطعه در محیط PCB است.

[مشاهده پوشه AltiumPCBLIB](https://github.com/MEMAR-ELECTRONIC-SANAT/Altium-Library/tree/main/AltiumPCBLIB)

## معرفی و کاربرد

کتابخانه‌های این بخش می‌توانند شامل اطلاعاتی مانند موارد زیر باشند:

- **Pads:** محل و ابعاد پدهای قطعه و مشخصات سوراخ‌کاری در قطعات پایه‌دار.
- **Silkscreen:** ترسیمات و نوشته‌های راهنمای روی لایه چاپ.
- **Solder Mask و Paste Mask:** محدوده ماسک لحیم و خمیر قلع.
- **Assembly و Courtyard:** اطلاعات مورد استفاده در مونتاژ و کنترل فاصله قطعات.
- **3D Body:** مدل سه‌بعدی قطعه، در صورت وجود و تعبیه‌شدن در Footprint.

وجود همه این موارد برای تمام قطعات تضمین‌شده نیست و باید فایل هر قطعه جداگانه بررسی شود.

## نحوه استفاده در Altium Designer

1. فایل کتابخانه با پسوند **.PcbLib** را از این پوشه دریافت کنید.
2. در Altium Designer از پنل **PCB Library** فایل را باز کنید؛ در صورت نیاز از مسیر **Preferences → Data Management → File-based Libraries** آن را به کتابخانه‌های قابل دسترس اضافه کنید.
3. Footprint موردنظر را انتخاب و در طراحی PCB استفاده کنید.
4. پیش از ساخت برد، ابعاد پدها، فاصله پایه‌ها، ابعاد بدنه، الگوی سوراخ‌کاری و شماره‌گذاری پایه‌ها را با دیتاشیت قطعه تطبیق دهید.

## نکات فنی و کنترل کیفیت

- نام و شماره‌گذاری Padها باید با Pinها و Footprint مربوط به قطعه در شماتیک مطابقت داشته باشد.
- ابعاد و فواصل باید بر اساس دیتاشیت سازنده و الزامات مونتاژ بررسی شوند.
- وجود مدل سه‌بعدی را از داخل محیط PCB بررسی کنید؛ همه Footprintها الزاماً مدل 3D ندارند.
- قبل از سفارش ساخت PCB، نمای دوبعدی و سه‌بعدی، فاصله قطعات و قوانین طراحی (DRC) را کنترل کنید.
- در صورت مشاهده مغایرت، دیتاشیت سازنده مرجع نهایی بررسی است.

## ارتباط با کتابخانه شماتیک

برای طراحی کامل، Footprint این پوشه را در کنار Symbol متناظر از پوشه [AltiumSCHLIB](https://github.com/MEMAR-ELECTRONIC-SANAT/Altium-Library/tree/main/AltiumSCHLIB) بررسی کنید. تطبیق شماره پایه‌های شماتیک با شماره Padهای PCB ضروری است.

## تصاویر و دیاگرام‌های راهنما

در صورت اضافه‌شدن تصاویر، نمای Footprint، ابعاد مکانیکی، لایه‌های مختلف و مدل سه‌بعدی قطعات در این بخش معرفی خواهند شد.

## تهیه و تدوین

**معمار الکترونیک صنعت / MEMAR ELECTRONIC SANAT (MES)**

همراه شما در مسیر طراحی و ساخت مدارهای مطمئن

- [GitHub](https://github.com/MEMAR-ELECTRONIC-SANAT)
- [Telegram](https://t.me/Memar_Electronic)
- [Instagram](https://www.instagram.com/Memar.Electronic)

[مشاهده سایر آموزش‌ها](https://github.com/MEMAR-ELECTRONIC-SANAT)

---

# Altium PCB Footprint Library

This directory is intended for **Altium PCB Library** files (.PcbLib). A footprint defines a component's physical land pattern on a printed circuit board and is used during PCB placement and routing.

## Overview

Depending on the component, a footprint may contain pads, silkscreen graphics, solder-mask and paste-mask definitions, assembly/courtyard outlines, and an optional 3D body. Not every footprint necessarily includes all these elements.

## How to use

1. Download the required .PcbLib file.
2. Open it in Altium Designer using the **PCB Library** panel, or add it through **Preferences → Data Management → File-based Libraries**.
3. Select the required footprint and use it in your PCB design.
4. Verify pad dimensions, pitch, drill sizes, body outline, and pad numbering against the manufacturer's datasheet before fabrication.

## Design checks

- Confirm that pad numbering matches the corresponding schematic symbol pins.
- Verify land-pattern dimensions against the component datasheet and assembly requirements.
- Check whether a 3D model is actually included.
- Run the PCB design-rule check (DRC) and inspect both 2D and 3D views before ordering the board.
- The manufacturer's datasheet is the final reference when resolving discrepancies.

For a complete design, also review the matching schematic symbol in [AltiumSCHLIB](https://github.com/MEMAR-ELECTRONIC-SANAT/Altium-Library/tree/main/AltiumSCHLIB).

## Images and Reference Diagrams

Footprint views, mechanical dimensions, layer details, and 3D model images can be documented here as they are added.

## Prepared by

**MEMAR ELECTRONIC SANAT (MES)**

*Your partner in designing and building reliable circuits.*

- [GitHub](https://github.com/MEMAR-ELECTRONIC-SANAT)
- [Telegram](https://t.me/Memar_Electronic)
- [Instagram](https://www.instagram.com/Memar.Electronic)

[Explore more tutorials](https://github.com/MEMAR-ELECTRONIC-SANAT)
