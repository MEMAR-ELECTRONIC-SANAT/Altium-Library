# کتابخانه سمبل‌های شماتیک در Altium Designer
**Altium Schematic Symbol Library**

این پوشه برای نگهداری کتابخانه‌های **Schematic Library** با پسوند **.SchLib** در نرم‌افزار Altium Designer در نظر گرفته شده است. هر Symbol نمایش گرافیکی و منطقی یک قطعه در شماتیک است و اطلاعات پایه‌های آن برای ارتباط با مدار و تخصیص Footprint به کار می‌رود.

[مشاهده پوشه AltiumSCHLIB](https://github.com/MEMAR-ELECTRONIC-SANAT/Altium-Library/tree/main/AltiumSCHLIB)

## معرفی و کاربرد

یک سمبل شماتیک، بسته به نوع قطعه و نحوه پیاده‌سازی آن، می‌تواند شامل موارد زیر باشد:

- **Symbol Graphics:** شکل گرافیکی قطعه در صفحه شماتیک.
- **Pins:** پایه‌ها، شماره پایه، نام پایه و نوع الکتریکی آن‌ها.
- **Designator و Comment:** شناسه مرجع قطعه و توضیحات نمایشی.
- **Parameters:** پارامترهایی مانند شماره قطعه، سازنده یا توضیحات، در صورت تعریف.
- **Footprint Model:** ارجاع به الگوی PCB متناظر، در صورت اختصاص‌دادن مدل به سمبل.

ساختار و میزان اطلاعات ممکن است بین سمبل‌ها متفاوت باشد؛ بنابراین مشخصات هر قطعه باید پیش از استفاده بررسی شود.

## نحوه استفاده در Altium Designer

1. فایل کتابخانه با پسوند **.SchLib** را دریافت کنید.
2. آن را در Altium Designer از طریق پنل **SCH Library** باز کنید یا از مسیر **Preferences → Data Management → File-based Libraries** به کتابخانه‌های قابل دسترس اضافه کنید.
3. سمبل موردنظر را از پنل کتابخانه انتخاب کرده و در شماتیک قرار دهید.
4. شماره و نام پایه‌ها، نوع الکتریکی پایه‌ها و پارامترهای قطعه را با دیتاشیت سازنده تطبیق دهید.
5. در صورت وجود Footprint Model، نام و مسیر Footprint را بررسی کنید و پس از انتقال قطعه به PCB، تطبیق پایه‌ها را کنترل کنید.

## نکات فنی و کنترل کیفیت

- شماره پایه‌ها (Pin Designator) باید دقیقاً با شماره پایه‌های قطعه در دیتاشیت مطابقت داشته باشد.
- نوع الکتریکی پایه‌ها مانند Input، Output، Passive و Power باید متناسب با عملکرد واقعی قطعه تنظیم شود تا بررسی‌های ERC نتیجه قابل اتکایی داشته باشند.
- پایه‌های تغذیه، زمین، پایه‌های بدون اتصال (NC) و پایه‌های چندگانه را با دقت بررسی کنید.
- وجود مدل PCB در سمبل را مفروض ندانید؛ اتصال به Footprint باید جداگانه کنترل شود.
- پس از قرار دادن سمبل در شماتیک، اتصالات و خروجی ERC را بازبینی کنید.

## ارتباط با کتابخانه PCB

برای طراحی کامل، سمبل این پوشه را با Footprint متناظر در [AltiumPCBLIB](https://github.com/MEMAR-ELECTRONIC-SANAT/Altium-Library/tree/main/AltiumPCBLIB) تطبیق دهید. تطابق شماره پایه‌های Symbol با شماره Padهای Footprint از الزامات مهم انتقال صحیح طراحی از شماتیک به PCB است.

## تصاویر و دیاگرام‌های راهنما

در صورت اضافه‌شدن تصاویر، نمای سمبل، شماره‌گذاری پایه‌ها، ویژگی‌های الکتریکی و نمونه اتصال آن به Footprint در این بخش معرفی خواهند شد.

## تهیه و تدوین

**معمار الکترونیک صنعت / MEMAR ELECTRONIC SANAT (MES)**

همراه شما در مسیر طراحی و ساخت مدارهای مطمئن

- [GitHub](https://github.com/MEMAR-ELECTRONIC-SANAT)
- [Telegram](https://t.me/Memar_Electronic)
- [Instagram](https://www.instagram.com/Memar.Electronic)

[مشاهده سایر آموزش‌ها](https://github.com/MEMAR-ELECTRONIC-SANAT)

---

# Altium Schematic Symbol Library

This directory is intended for **Altium Schematic Library** files (.SchLib). A schematic symbol represents a component in the circuit diagram and defines its pins and associated component information.

## Overview

Depending on the component, a symbol may contain graphical primitives, pins, pin names and numbers, electrical pin types, designator/comment fields, parameters, and an optional PCB footprint model reference. The exact content varies between components.

## How to use

1. Download the required .SchLib file.
2. Open it in Altium Designer using the **SCH Library** panel, or add it through **Preferences → Data Management → File-based Libraries**.
3. Select the symbol and place it in your schematic.
4. Verify pin names, pin numbers, electrical types, and component parameters against the manufacturer's datasheet.
5. If a PCB footprint model is assigned, verify its name and mapping before transferring the design to the PCB editor.

## Design checks

- Pin designators must match the manufacturer's datasheet.
- Set electrical pin types appropriately (Input, Output, Passive, Power, etc.) to support meaningful ERC checks.
- Carefully review power, ground, NC, and multi-part component pins.
- Do not assume that every symbol has an associated PCB footprint.
- Review schematic connectivity and Electrical Rules Check (ERC) results.

For a complete design, match each symbol with its corresponding footprint in [AltiumPCBLIB](https://github.com/MEMAR-ELECTRONIC-SANAT/Altium-Library/tree/main/AltiumPCBLIB). Symbol pin numbers must correspond to the footprint pad numbers.

## Images and Reference Diagrams

Symbol views, pin numbering, electrical properties, and symbol-to-footprint examples can be documented here as they are added.

## Prepared by

**MEMAR ELECTRONIC SANAT (MES)**

*Your partner in designing and building reliable circuits.*

- [GitHub](https://github.com/MEMAR-ELECTRONIC-SANAT)
- [Telegram](https://t.me/Memar_Electronic)
- [Instagram](https://www.instagram.com/Memar.Electronic)

[Explore more tutorials](https://github.com/MEMAR-ELECTRONIC-SANAT)
