---
title: เพิ่มฟอร์มเอนทิตีแบบกำหนดเองใหม่ (Project Service Automation 2.x)
description: หัวข้อนี้แสดงข้อมูลเกี่ยวกับวิธีการเพิ่มฟอร์มเอนทิตีแบบกำหนดเอง สำหรับโอกาสทางการขาย ใบเสนอราคา หรือใบแจ้งหนี้ ใน Dynamics 365 Project Service Automation 2.x
author: makk
manager: kfend
ms.custom:
- dyn365-projectservice
ms.date: 3/14/2019
ms.topic: article
ms.service: business-applications
ms.author: makk
audience: admin
search.audienceType:
- admin
- customizer
search.app:
- D365PS
- ProjectOperations
ms.openlocfilehash: 9c9e31dc6d4d5a8ad5cc568f2d7d673c8703936d
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 02/15/2021
ms.locfileid: "5284876"
---
# <a name="add-new-custom-entity-forms-project-service-automation-2x"></a><span data-ttu-id="07523-103">เพิ่มฟอร์มเอนทิตีแบบกำหนดเองใหม่ (Project Service Automation 2.x)</span><span class="sxs-lookup"><span data-stu-id="07523-103">Add new custom entity forms (Project Service Automation 2.x)</span></span>

[!include [banner](../../includes/psa-now-project-operations.md)]

## <a name="type-field"></a><span data-ttu-id="07523-104">ฟิลด์ชนิด</span><span class="sxs-lookup"><span data-stu-id="07523-104">Type field</span></span> 

<span data-ttu-id="07523-105">Dynamics 365 Project Service Automation อาศัยฟิลด์ **ชนิด** (**msdyn\_ordertype**) ของเอนทิตีโอกาสทางการขาย ใบเสนอราคา ใบสั่ง และใบแจ้งหนี้ เพื่อแยกเวอร์ชัน **ตามงาน** ของเอนทิตีเหล่านี้ จากเวอร์ชัน **ตามรายการ** และ **ตามการให้บริการ**</span><span class="sxs-lookup"><span data-stu-id="07523-105">Dynamics 365 Project Service Automation relies on the **Type** (**msdyn\_ordertype**) field of the Opportunity, Quote, Order, and Invoice entities to distinguish **work-based** versions of these entities from **item-based** and **service-based** versions.</span></span> <span data-ttu-id="07523-106">เวอร์ชัน ตามงาน ของเอนทิตีเหล่านี้ จะถูกจัดการโดย PSA</span><span class="sxs-lookup"><span data-stu-id="07523-106">Work-based versions of these entities are handled by PSA.</span></span> <span data-ttu-id="07523-107">ตรรกะทางธุรกิจจำนวนมากบนฝั่งไคลเอ็นต์และฝั่งเซิร์ฟเวอร์ของโซลูชัน ขึ้นอยู่กับฟิลด์ **ชนิด**</span><span class="sxs-lookup"><span data-stu-id="07523-107">Lots of business logic on the client side and server side of the solution depends on the **Type** field.</span></span> <span data-ttu-id="07523-108">ดังนั้น จึงเป็นสิ่งสำคัญที่จะเตรียมใช้งานฟิลด์ด้วยค่าที่ถูกต้อง เมื่อเอนทิตีถูกสร้างขึ้น</span><span class="sxs-lookup"><span data-stu-id="07523-108">Therefore, it's important that the field be initialized with a correct value when the entities are created.</span></span> <span data-ttu-id="07523-109">ค่าที่ไม่ถูกต้อง อาจทำให้เกิดพฤติกรรมที่ไม่ถูกต้อง และตรรกะทางธุรกิจบางอย่างอาจทำงานไม่ถูกต้อง</span><span class="sxs-lookup"><span data-stu-id="07523-109">An incorrect value can cause incorrect behaviors, and some business logic might not run correctly.</span></span>

## <a name="automatic-form-switching"></a><span data-ttu-id="07523-110">การสลับฟอร์มอัตโนมัติ</span><span class="sxs-lookup"><span data-stu-id="07523-110">Automatic form switching</span></span>

<span data-ttu-id="07523-111">เพื่อหลีกเลี่ยงความเสียหายของข้อมูลที่อาจเกิดขึ้นและพฤติกรรมที่ไม่คาดคิดที่เกิดจากการเริ่มต้นที่ไม่ถูกต้อง และการแก้ไขเรกคอร์ดของเอนทิตีการขาย PSA จะมีตรรกะสำหรับการสลับแบบฟอร์มอัตโนมัติในฟอร์มสำเร็จรูป</span><span class="sxs-lookup"><span data-stu-id="07523-111">To avoid potential data corruption and unexpected behaviors that are caused by incorrect initialization and editing of the sales entity records, PSA now includes logic for automatic form switching in out-of-box forms.</span></span> <span data-ttu-id="07523-112">ตรรกะนี้จะนำผู้ใช้ไปยังแบบฟอร์มที่ถูกต้อง สำหรับการทำงานกับเวอร์ชันตามงาน หรือชนิดอื่นๆ ของเอนทิตีโอกาสทางการขาย ใบเสนอราคา ใบสั่ง หรือใบแจ้งหนี้</span><span class="sxs-lookup"><span data-stu-id="07523-112">This logic takes users to the correct form for working with the work-based version or any other type of Opportunity, Quote, Order, or Invoice entity.</span></span> <span data-ttu-id="07523-113">เมื่อผู้ใช้เปิดเวอร์ชันตามงานของเอนทิตีโอกาสทางการขาย ใบเสนอราคา ใบสั่ง หรือใบแจ้งหนี้ ฟอร์มจะถูกสลับไปยัง **ข้อมูลโครงการ**</span><span class="sxs-lookup"><span data-stu-id="07523-113">When a user opens the work-based version of an Opportunity, Quote, Order, or Invoice entity, the form is switched to **Project Information**.</span></span>

<span data-ttu-id="07523-114">ตรรกะการสลับแบบฟอร์มอัตโนมัติจะอาศัยการแม็ประหว่างค่า **formid** และฟิลด์ **msdyn\_ordertype**</span><span class="sxs-lookup"><span data-stu-id="07523-114">The automatic form switching logic relies on the mapping between the **formId** value and the **msdyn\_ordertype** field.</span></span> <span data-ttu-id="07523-115">ฟอร์มสำเร็จรูปทั้งหมดได้ถูกเพิ่มลงในการแมปนั้นแล้ว</span><span class="sxs-lookup"><span data-stu-id="07523-115">All out-of-box forms have been added to that mapping.</span></span> <span data-ttu-id="07523-116">อย่างไรก็ตาม ฟอร์มที่กำหนดเองต้องถูกเพิ่มด้วยตนเอง เพื่อบ่งชี้ว่าเอนทิตีเวอร์ชันใดที่มีวัตถุประสงค์เพื่อจัดการ</span><span class="sxs-lookup"><span data-stu-id="07523-116">However, custom forms must be manually added to indicate which version of the entity they are intended to handle.</span></span> <span data-ttu-id="07523-117">ซึ่งจะขึ้นอยู่กับฟิลดต์ **msdyn\_ordertype**</span><span class="sxs-lookup"><span data-stu-id="07523-117">This is based on the **msdyn\_ordertype** field.</span></span> <span data-ttu-id="07523-118">หากการสลับฟอร์มหายไปจากการแมป ตรรกะจะสลับไปยังฟอร์มสำเร็จรูป โดยขึ้นอยู่กับค่าที่ถูกบันทึกไว้ในฟิลด์ **msdyn\_ordertype** ของเอนทิตี</span><span class="sxs-lookup"><span data-stu-id="07523-118">If the form switching is missing from the mapping, logic will switch to the out-of-box form, based on the value that is saved in the **msdyn\_ordertype** field of the entity.</span></span>

## <a name="add-custom-forms-and-turn-on-the-form-switching-logic"></a><span data-ttu-id="07523-119">เพิ่มฟอร์มแบบกำหนดเองและเปิดตรรกะการสลับฟอร์ม</span><span class="sxs-lookup"><span data-stu-id="07523-119">Add custom forms and turn on the form switching logic</span></span>

<span data-ttu-id="07523-120">ตัวอย่างต่อไปนี้แสดงวิธีการเพิ่มฟอร์มแบบกำหนดเอง **โครงการของฉัน** เพื่อให้สามารถทำงานร่วมกับโอกาสทางการขายตามงาน</span><span class="sxs-lookup"><span data-stu-id="07523-120">The following example shows how to add a custom form, **My Project Information**, so that it works with work-based opportunities.</span></span> <span data-ttu-id="07523-121">กระบวนการเดียวกันจะถูกใช้ในการเพิ่มฟอร์มแบบกำหนดเอง เพื่อให้ทำงานกับใบเสนอราคา ใบสั่ง และใบแจ้งหนี้</span><span class="sxs-lookup"><span data-stu-id="07523-121">The same process is used to add custom forms so that they work with quotes, orders, and invoices.</span></span>

<span data-ttu-id="07523-122">ทำตามขั้นตอนเหล่านี้ เพื่อสร้างฟอร์มเวอร์ชันกำหนดเอง **ข้อมูลโครงการ**</span><span class="sxs-lookup"><span data-stu-id="07523-122">Follow these steps to create a custom version of the **Project Information** form.</span></span>

1. <span data-ttu-id="07523-123">ในเอนทิตีโอกาสทางการชสสบ เปิดฟอร์ม **ข้อมูลโครงการ** และบันทึกสำเนาภายใต้ชื่อ **ข้อมูลโครงการของฉัน**</span><span class="sxs-lookup"><span data-stu-id="07523-123">In the Opportunity entity, open the **Project Information** form, and save a copy under the name **My Project Information**.</span></span>
2. <span data-ttu-id="07523-124">เปิดฟอร์มใหม่ จากนั้นในคุณสมบัติโปรดตรวจสอบให้แน่ใจว่าสคริปต์การเริ่มต้นฟอร์ม จากฟอร์ม **ข้อมูลโครงการ** มีอยู่</span><span class="sxs-lookup"><span data-stu-id="07523-124">Open the new form, and then, in the properties, make sure that the form initialization scripts from the **Project Information** form are present.</span></span> 

    > [!IMPORTANT]
    > <span data-ttu-id="07523-125">อย่าเอาสคริปต์ออก</span><span class="sxs-lookup"><span data-stu-id="07523-125">Don't remove the scripts.</span></span> <span data-ttu-id="07523-126">มิฉะนั้น ข้อมูลบางอย่างอาจถูกเริ่มต้นอย่างไม่ถูกต้อง</span><span class="sxs-lookup"><span data-stu-id="07523-126">Otherwise, some data might be initialized incorrectly.</span></span>

3. <span data-ttu-id="07523-127">ตรวจสอบว่าฟิลด์ **ชนิด** (**msdyn\_ordertype**) มีอยู่ในฟอร์ม</span><span class="sxs-lookup"><span data-stu-id="07523-127">Verify that the **Type** (**msdyn\_ordertype**) field is present in the form.</span></span> 

    > [!IMPORTANT]
    > <span data-ttu-id="07523-128">อย่าเอาฟิลด์นี้ออก</span><span class="sxs-lookup"><span data-stu-id="07523-128">Don't remove this field.</span></span> <span data-ttu-id="07523-129">มิฉะนั้น สคริปต์การเริ่มต้นจะล้มเหลว</span><span class="sxs-lookup"><span data-stu-id="07523-129">Otherwise, the initialization scripts will fail.</span></span>

4. <span data-ttu-id="07523-130">ค้นหาค่า **formId** ของฟอร์มใหม่</span><span class="sxs-lookup"><span data-stu-id="07523-130">Find the **formId** value of the new form.</span></span> <span data-ttu-id="07523-131">คุณสามารถทำการนี้ให้สำเร็จได้ในสองวิธี:</span><span class="sxs-lookup"><span data-stu-id="07523-131">You can complete this step in two ways:</span></span>

    - <span data-ttu-id="07523-132">ส่งออกฟอร์ม **โครงการของฉัน** เป็นส่วนหนึ่งของโซลูชันที่ไม่มีการจัดการ จากนั้นค้นหาค่า **formId** ในไฟล์ customization.xml .xml ของโซลูชันที่ส่งออก</span><span class="sxs-lookup"><span data-stu-id="07523-132">Export the **My Project Information** form as part of an unmanaged solution, and then look up the **formId** value in the customization.xml file of the exported solution.</span></span>
    - <span data-ttu-id="07523-133">เปิดฟอร์ม **โครงการของฉัน** ในตัวแก้ไขฟอร์ม แล้วค้นหาตัวระบุที่ไม่ซ้ำกัน (GUID) ถัดจากพารามิเตอร์ **fromId** ใน URL ดังที่แสดงในภาพประกอบต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="07523-133">Open the **My Project Information** form in the form editor, and then look for the globally unique identifier (GUID) next to the **fromId** parameter in the URL, as shown in the following illustration.</span></span>

    ![ค่า formId ของฟอร์มใหม่ ใน URL](media/how-to-add-custom-forms-in-v2.0.png)

5. <span data-ttu-id="07523-135">สร้างการแม็ป **msdyn\_ordertype** สำหรับค่า **formId** โดยการแก้ไขทรัพยากรบนเว็บ msdyn\_/SalesDocument/PSSalesDocumentCustomFormIds.js</span><span class="sxs-lookup"><span data-stu-id="07523-135">Create an **msdyn\_ordertype** mapping for the **formId** value by editing the msdyn\_/SalesDocument/PSSalesDocumentCustomFormIds.js web resource.</span></span> <span data-ttu-id="07523-136">ลบรหัสออกจากทรัพยากร และแทนที่ด้วยรหัสต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="07523-136">Remove the code from the resource, and replace it with the following code.</span></span>

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

6. <span data-ttu-id="07523-137">บันทึก และจากนั้นเผยแพร่การแก้ไข/ปรับปรุงตามคำสั่ง</span><span class="sxs-lookup"><span data-stu-id="07523-137">Save and then publish the customizations.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]