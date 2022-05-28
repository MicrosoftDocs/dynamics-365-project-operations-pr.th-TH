---
title: เพิ่มฟอร์มเอนทิตีแบบกำหนดเองใหม่ (Project Service Automation 2.x)
description: หัวข้อนี้แสดงข้อมูลเกี่ยวกับวิธีการเพิ่มฟอร์มเอนทิตีแบบกำหนดเอง สำหรับโอกาสทางการขาย ใบเสนอราคา หรือใบแจ้งหนี้ ใน Dynamics 365 Project Service Automation 2.x
author: makk
ms.custom:
- dyn365-projectservice
ms.date: 3/14/2019
ms.topic: article
ms.author: makk
audience: admin
search.audienceType:
- admin
- customizer
search.app:
- D365PS
- ProjectOperations
ms.reviewer: johnmichalak
ms.openlocfilehash: ffc702bbe9cedb2a0cc8da8d8f58e48005950127
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 04/14/2022
ms.locfileid: "8584343"
---
# <a name="add-new-custom-entity-forms-project-service-automation-2x"></a>เพิ่มฟอร์มเอนทิตีแบบกำหนดเองใหม่ (Project Service Automation 2.x)

[!include [banner](../../includes/psa-now-project-operations.md)]

## <a name="type-field"></a>ฟิลด์ชนิด 

Dynamics 365 Project Service Automation อาศัยฟิลด์ **ชนิด** (**msdyn\_ordertype**) ของเอนทิตีโอกาสทางการขาย ใบเสนอราคา ใบสั่ง และใบแจ้งหนี้ เพื่อแยกเวอร์ชัน **ตามงาน** ของเอนทิตีเหล่านี้ จากเวอร์ชัน **ตามรายการ** และ **ตามการให้บริการ** เวอร์ชัน ตามงาน ของเอนทิตีเหล่านี้ จะถูกจัดการโดย PSA ตรรกะทางธุรกิจจำนวนมากบนฝั่งไคลเอ็นต์และฝั่งเซิร์ฟเวอร์ของโซลูชัน ขึ้นอยู่กับฟิลด์ **ชนิด** ดังนั้น จึงเป็นสิ่งสำคัญที่จะเตรียมใช้งานฟิลด์ด้วยค่าที่ถูกต้อง เมื่อเอนทิตีถูกสร้างขึ้น ค่าที่ไม่ถูกต้อง อาจทำให้เกิดพฤติกรรมที่ไม่ถูกต้อง และตรรกะทางธุรกิจบางอย่างอาจทำงานไม่ถูกต้อง

## <a name="automatic-form-switching"></a>การสลับฟอร์มอัตโนมัติ

เพื่อหลีกเลี่ยงความเสียหายของข้อมูลที่อาจเกิดขึ้นและพฤติกรรมที่ไม่คาดคิดที่เกิดจากการเริ่มต้นที่ไม่ถูกต้อง และการแก้ไขเรกคอร์ดของเอนทิตีการขาย PSA จะมีตรรกะสำหรับการสลับแบบฟอร์มอัตโนมัติในฟอร์มสำเร็จรูป ตรรกะนี้จะนำผู้ใช้ไปยังแบบฟอร์มที่ถูกต้อง สำหรับการทำงานกับเวอร์ชันตามงาน หรือชนิดอื่นๆ ของเอนทิตีโอกาสทางการขาย ใบเสนอราคา ใบสั่ง หรือใบแจ้งหนี้ เมื่อผู้ใช้เปิดเวอร์ชันตามงานของเอนทิตีโอกาสทางการขาย ใบเสนอราคา ใบสั่ง หรือใบแจ้งหนี้ ฟอร์มจะถูกสลับไปยัง **ข้อมูลโครงการ**

ตรรกะการสลับแบบฟอร์มอัตโนมัติจะอาศัยการแม็ประหว่างค่า **formid** และฟิลด์ **msdyn\_ordertype** ฟอร์มสำเร็จรูปทั้งหมดได้ถูกเพิ่มลงในการแมปนั้นแล้ว อย่างไรก็ตาม ฟอร์มที่กำหนดเองต้องถูกเพิ่มด้วยตนเอง เพื่อบ่งชี้ว่าเอนทิตีเวอร์ชันใดที่มีวัตถุประสงค์เพื่อจัดการ ซึ่งจะขึ้นอยู่กับฟิลดต์ **msdyn\_ordertype** หากการสลับฟอร์มหายไปจากการแมป ตรรกะจะสลับไปยังฟอร์มสำเร็จรูป โดยขึ้นอยู่กับค่าที่ถูกบันทึกไว้ในฟิลด์ **msdyn\_ordertype** ของเอนทิตี

## <a name="add-custom-forms-and-turn-on-the-form-switching-logic"></a>เพิ่มฟอร์มแบบกำหนดเองและเปิดตรรกะการสลับฟอร์ม

ตัวอย่างต่อไปนี้แสดงวิธีการเพิ่มฟอร์มแบบกำหนดเอง **โครงการของฉัน** เพื่อให้สามารถทำงานร่วมกับโอกาสทางการขายตามงาน กระบวนการเดียวกันจะถูกใช้ในการเพิ่มฟอร์มแบบกำหนดเอง เพื่อให้ทำงานกับใบเสนอราคา ใบสั่ง และใบแจ้งหนี้

ทำตามขั้นตอนเหล่านี้ เพื่อสร้างฟอร์มเวอร์ชันกำหนดเอง **ข้อมูลโครงการ**

1. ในเอนทิตีโอกาสทางการชสสบ เปิดฟอร์ม **ข้อมูลโครงการ** และบันทึกสำเนาภายใต้ชื่อ **ข้อมูลโครงการของฉัน**
2. เปิดฟอร์มใหม่ จากนั้นในคุณสมบัติโปรดตรวจสอบให้แน่ใจว่าสคริปต์การเริ่มต้นฟอร์ม จากฟอร์ม **ข้อมูลโครงการ** มีอยู่ 

    > [!IMPORTANT]
    > อย่าเอาสคริปต์ออก มิฉะนั้น ข้อมูลบางอย่างอาจถูกเริ่มต้นอย่างไม่ถูกต้อง

3. ตรวจสอบว่าฟิลด์ **ชนิด** (**msdyn\_ordertype**) มีอยู่ในฟอร์ม 

    > [!IMPORTANT]
    > อย่าเอาฟิลด์นี้ออก มิฉะนั้น สคริปต์การเริ่มต้นจะล้มเหลว

4. ค้นหาค่า **formId** ของฟอร์มใหม่ คุณสามารถทำการนี้ให้สำเร็จได้ในสองวิธี:

    - ส่งออกฟอร์ม **โครงการของฉัน** เป็นส่วนหนึ่งของโซลูชันที่ไม่มีการจัดการ จากนั้นค้นหาค่า **formId** ในไฟล์ customization.xml .xml ของโซลูชันที่ส่งออก
    - เปิดฟอร์ม **โครงการของฉัน** ในตัวแก้ไขฟอร์ม แล้วค้นหาตัวระบุที่ไม่ซ้ำกัน (GUID) ถัดจากพารามิเตอร์ **fromId** ใน URL ดังที่แสดงในภาพประกอบต่อไปนี้

    ![ค่า formId ของฟอร์มใหม่ใน URL](media/how-to-add-custom-forms-in-v2.0.png)

5. สร้างการแม็ป **msdyn\_ordertype** สำหรับค่า **formId** โดยการแก้ไขทรัพยากรบนเว็บ msdyn\_/SalesDocument/PSSalesDocumentCustomFormIds.js ลบรหัสออกจากทรัพยากร และแทนที่ด้วยรหัสต่อไปนี้

    ```javascript
    define(["require", "exports"], function (require, exports) {
        "use strict";
        var SalesDocumentCustomFormIds = (function () {
            function SalesDocumentCustomFormIds() {
            }
            SalesDocumentCustomFormIds.overwriteFormIds = function (mappedFormIds) {
                /*
                ---- Notes ----
                mappedFormIds[SalesEntity][OrderType] => The array of forms IDs that support particular entity and order type
                Add or overwrite customized formId for the particular entity and order type by calling:
                    mappedFormIds[<EntityType>][<msdyn_ordertype>].push("<formId>");
                Allowed msdyn_ordertype values for reference:
                    ServiceBased: 690970002 (Field Service version of the entity)
                    WorkBased: 192350001 (PSA version of the entity)
                    ItemBased: 192350000 (Regular out of the box entity)
                Uncomment and update one of the following lines to register custom PSA form for required entity:
                */      
                //mappedFormIds[1][192350001].push("<formId>"); //Quote
                //mappedFormIds[5][192350001].push("<formId>"); //Quote Line
                //mappedFormIds[2][192350001].push("<formId>"); //Sales Order
                //mappedFormIds[6][192350001].push("<formId>"); //Sales Order Line
                // In this example we have added new form for Opportunity
                mappedFormIds[0][192350001].push("192EE537-DCC4-45D3-B7AF-EA694B9113D2"); //Opportunity
                //mappedFormIds[4][192350001].push("<formId>"); //Opportunity Line
            };
            return SalesDocumentCustomFormIds;
        }());
        exports.default = SalesDocumentCustomFormIds;
    });
    ```

6. บันทึก และจากนั้นเผยแพร่การแก้ไข/ปรับปรุงตามคำสั่ง


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
