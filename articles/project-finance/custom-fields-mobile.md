---
title: ใช้ฟิลด์ที่กำหนดเองสำหรับแอปบนมือถือ Microsoft Dynamics 365 Project Timesheet บน iOS และ Android
description: หัวข้อนี้มีรูปแบบทั่วไปสำหรับการใช้ส่วนขยายเพื่อใช้ฟิลด์ที่กำหนดเอง
author: KimANelson
manager: AnnBe
ms.date: 05/29/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: 4564bbda-34ea-4647-a9bc-f6ef17b1038b
ms.search.region: Global
ms.search.industry: Service industries
ms.author: knelson
ms.dyn365.ops.version: 10.0.3
ms.search.validFrom: 2019-05-29
ms.openlocfilehash: 16c3b79dcaaf8c5c491587618256694f82f44753
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 03/24/2020
ms.locfileid: "3756386"
---
# <a name="implement-custom-fields-for-the-microsoft-dynamics-365-project-timesheet-mobile-app-on-ios-and-android"></a><span data-ttu-id="7e738-103">ใช้ฟิลด์ที่กำหนดเองสำหรับแอปบนมือถือ Microsoft Dynamics 365 Project Timesheet บน iOS และ Android</span><span class="sxs-lookup"><span data-stu-id="7e738-103">Implement custom fields for the Microsoft Dynamics 365 Project Timesheet mobile app on iOS and Android</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="7e738-104">หัวข้อนี้มีรูปแบบทั่วไปสำหรับการใช้ส่วนขยายเพื่อใช้ฟิลด์ที่กำหนดเอง</span><span class="sxs-lookup"><span data-stu-id="7e738-104">This topic provides common patterns for using extensions to implement custom fields.</span></span> <span data-ttu-id="7e738-105">หัวข้อต่อไปนี้ครอบคลุม:</span><span class="sxs-lookup"><span data-stu-id="7e738-105">The following topics are covered:</span></span>

- <span data-ttu-id="7e738-106">ชนิดข้อมูลต่างๆ ที่กรอบฟิลด์ข้อมูลที่กำหนดเองสนับสนุน</span><span class="sxs-lookup"><span data-stu-id="7e738-106">The various data types that the custom field framework supports</span></span>
- <span data-ttu-id="7e738-107">วิธีแสดงฟิลด์แบบอ่านอย่างเดียวหรือแก้ไขได้ในรายการแผ่นเวลาและบันทึกค่าที่ผู้ใช้ระบุกลับไปยังฐานข้อมูล</span><span class="sxs-lookup"><span data-stu-id="7e738-107">How to show read-only or editable fields on timesheet entries, and save user-provided values back to the database</span></span>
- <span data-ttu-id="7e738-108">วิธีแสดงฟิลด์แบบอ่านอย่างเดียวบนส่วนหัวของแผ่นเวลา</span><span class="sxs-lookup"><span data-stu-id="7e738-108">How to show read-only fields on the timesheet header</span></span>
- <span data-ttu-id="7e738-109">วิธีการรวมตรรกะทางธุรกิจที่กำหนดเองอื่นๆ เพื่อป้อนค่าเริ่มต้นในฟิลด์และทำการตรวจสอบความถูกต้องเพิ่มเติม</span><span class="sxs-lookup"><span data-stu-id="7e738-109">How to integrate other custom business logic to enter default values in fields and do additional validation</span></span>

## <a name="audience"></a><span data-ttu-id="7e738-110">ผู้ชม</span><span class="sxs-lookup"><span data-stu-id="7e738-110">Audience</span></span>

<span data-ttu-id="7e738-111">หัวข้อนี้มีไว้สำหรับนักพัฒนาที่กำลังรวมฟิลด์ที่กำหนดเองไว้ในแอปพลิเคชันมือถือ Microsoft Dynamics 365 Project Timesheet ที่พร้อมใช้งานสำหรับ Apple iOS และ Google Android</span><span class="sxs-lookup"><span data-stu-id="7e738-111">This topic is intended for developers who are integrating their custom fields into the Microsoft Dynamics 365 Project Timesheet mobile application that is available for Apple iOS and Google Android.</span></span> <span data-ttu-id="7e738-112">สมมติฐานคือผู้อ่านคุ้นเคยกับการพัฒนา X++ และฟังก์ชันการทำงานของแผ่นเวลาโครงการ</span><span class="sxs-lookup"><span data-stu-id="7e738-112">The assumption is that readers are familiar with X++ development and project timesheet functionality.</span></span>

## <a name="data-contract--tstimesheetcustomfield-x-class"></a><span data-ttu-id="7e738-113">สัญญาข้อมูล - คลาส TSTimesheetCustomField X++</span><span class="sxs-lookup"><span data-stu-id="7e738-113">Data contract – TSTimesheetCustomField X++ class</span></span>

<span data-ttu-id="7e738-114">คลาส **TSTimesheetCustomField** คือคลาสสัญญาข้อมูล X++ ที่แสดงข้อมูลเกี่ยวกับฟิลด์ที่กำหนดเองสำหรับฟังก์ชันการทำงานของแผ่นเวลา</span><span class="sxs-lookup"><span data-stu-id="7e738-114">The **TSTimesheetCustomField** class is the X++ data contract class that represents information about a custom field for timesheet functionality.</span></span> <span data-ttu-id="7e738-115">รายการของออบเจ็กต์ฟิลด์ที่กำหนดเองจะถูกส่งผ่านทั้งสัญญาข้อมูล TSTimesheetDetails และสัญญาข้อมูล TSTimesheetEntry เพื่อแสดงฟิลด์ที่กำหนดเองในแอปมือถือ</span><span class="sxs-lookup"><span data-stu-id="7e738-115">Lists of the custom field objects are passed on both the TSTimesheetDetails data contract and the TSTimesheetEntry data contract to show custom fields in the mobile app.</span></span>

- <span data-ttu-id="7e738-116">**TSTimesheetDetails** - สัญญาส่วนหัวของแผ่นเวลา</span><span class="sxs-lookup"><span data-stu-id="7e738-116">**TSTimesheetDetails** - The timesheet header contract.</span></span>
- <span data-ttu-id="7e738-117">**TSTimesheetEntry** - สัญญาการทำธุรกรรมแผ่นเวลา</span><span class="sxs-lookup"><span data-stu-id="7e738-117">**TSTimesheetEntry** - The timesheet transaction contract.</span></span> <span data-ttu-id="7e738-118">กลุ่มของวัตถุเหล่านี้ที่มีข้อมูลโครงการเดียวกันและค่า **timesheetLineRecId** เป็นเส้น</span><span class="sxs-lookup"><span data-stu-id="7e738-118">Groups of these objects that have the same project information and **timesheetLineRecId** value constitute a line.</span></span>

### <a name="fieldbasetype-types"></a><span data-ttu-id="7e738-119">fieldBaseType (ประเภท)</span><span class="sxs-lookup"><span data-stu-id="7e738-119">fieldBaseType (Types)</span></span>

<span data-ttu-id="7e738-120">คุณสมบัติ **FieldBaseType** บนออบเจ็กต์ **TsTimesheetCustom** กำหนดประเภทของฟิลด์ที่ปรากฏในแอป</span><span class="sxs-lookup"><span data-stu-id="7e738-120">The **FieldBaseType** property on the **TsTimesheetCustom** object determines the type of the field that appears in the app.</span></span> <span data-ttu-id="7e738-121">ค่า **ประเภท** ดังต่อไปนี้ได้รับการรองรับ</span><span class="sxs-lookup"><span data-stu-id="7e738-121">The following **Types** values that are supported.</span></span>

| <span data-ttu-id="7e738-122">ค่าของประเภท</span><span class="sxs-lookup"><span data-stu-id="7e738-122">Types value</span></span> | <span data-ttu-id="7e738-123">ประเภท</span><span class="sxs-lookup"><span data-stu-id="7e738-123">Type</span></span>              | <span data-ttu-id="7e738-124">หมายเหตุ</span><span class="sxs-lookup"><span data-stu-id="7e738-124">Notes</span></span> |
|-------------|-------------------|-------|
| <span data-ttu-id="7e738-125">12</span><span class="sxs-lookup"><span data-stu-id="7e738-125">0</span></span>           | <span data-ttu-id="7e738-126">String (และ Enum)</span><span class="sxs-lookup"><span data-stu-id="7e738-126">String (and Enum)</span></span> | <span data-ttu-id="7e738-127">ฟิลด์จะปรากฏเป็นฟิลด์ข้อความ</span><span class="sxs-lookup"><span data-stu-id="7e738-127">The field appears as a text field.</span></span> |
| <span data-ttu-id="7e738-128">1</span><span class="sxs-lookup"><span data-stu-id="7e738-128">1</span></span>           | <span data-ttu-id="7e738-129">Integer</span><span class="sxs-lookup"><span data-stu-id="7e738-129">Integer</span></span>           | <span data-ttu-id="7e738-130">ค่าจะแสดงเป็นตัวเลขโดยไม่มีตำแหน่งทศนิยม</span><span class="sxs-lookup"><span data-stu-id="7e738-130">The value is shown as a number without decimal places.</span></span> |
| <span data-ttu-id="7e738-131">2</span><span class="sxs-lookup"><span data-stu-id="7e738-131">2</span></span>           | <span data-ttu-id="7e738-132">จริง</span><span class="sxs-lookup"><span data-stu-id="7e738-132">Real</span></span>              | <span data-ttu-id="7e738-133">ค่าจะแสดงเป็นตัวเลขที่มีตำแหน่งทศนิยม</span><span class="sxs-lookup"><span data-stu-id="7e738-133">The value is shown as a number that has decimal places.</span></span><p><span data-ttu-id="7e738-134">หากต้องการแสดงมูลค่าที่แท้จริงเป็นสกุลเงินในแอป ให้ใช้คุณสมบัติ **fieldExtenededType**</span><span class="sxs-lookup"><span data-stu-id="7e738-134">To show the real value as a currency in the app, use the **fieldExtenededType** property.</span></span> <span data-ttu-id="7e738-135">คุณสามารถใช้คุณสมบัติ **numberOfDecimals** เพื่อกำหนดจำนวนตำแหน่งทศนิยมที่จะแสดง</span><span class="sxs-lookup"><span data-stu-id="7e738-135">You can use the **numberOfDecimals** property to set the number of decimal places that are shown.</span></span></p> |
| <span data-ttu-id="7e738-136">3</span><span class="sxs-lookup"><span data-stu-id="7e738-136">3</span></span>           | <span data-ttu-id="7e738-137">Date</span><span class="sxs-lookup"><span data-stu-id="7e738-137">Date</span></span>              | <span data-ttu-id="7e738-138">รูปแบบวันที่กำหนดโดยการตั้งค่า **รูปแบบวันที่ เวลา และตัวเลข** ของผู้ใช้ที่ระบุไว้ภายใต้ **การกำหนดภาษาและประเทศ/ภูมิภาค** ใน **ตัวเลือกผู้ใช้**</span><span class="sxs-lookup"><span data-stu-id="7e738-138">Date formats are determined by the user's **Date, times, and number format** setting that is specified under **Language and country/region preference** in **User options**.</span></span> |
| <span data-ttu-id="7e738-139">4</span><span class="sxs-lookup"><span data-stu-id="7e738-139">4</span></span>           | <span data-ttu-id="7e738-140">Boolean</span><span class="sxs-lookup"><span data-stu-id="7e738-140">Boolean</span></span>           | |
| <span data-ttu-id="7e738-141">15</span><span class="sxs-lookup"><span data-stu-id="7e738-141">15</span></span>          | <span data-ttu-id="7e738-142">GUID</span><span class="sxs-lookup"><span data-stu-id="7e738-142">GUID</span></span>              | |
| <span data-ttu-id="7e738-143">16</span><span class="sxs-lookup"><span data-stu-id="7e738-143">16</span></span>          | <span data-ttu-id="7e738-144">Int64</span><span class="sxs-lookup"><span data-stu-id="7e738-144">Int64</span></span>             | |

- <span data-ttu-id="7e738-145">ถ้าคุณสมบัติ **stringOptions** ไม่ได้ระบุบนออบเจ็กต์ **TSTimesheetCustomField** ฟิลด์ข้อความอิสระจะถูกจัดเตรียมไว้ให้กับผู้ใช้</span><span class="sxs-lookup"><span data-stu-id="7e738-145">If the **stringOptions** property isn't provided on the **TSTimesheetCustomField** object, a free-text field is provided to the user.</span></span>

    <span data-ttu-id="7e738-146">คุณสมบัติ **stringLength** สามารถใช้เพื่อตั้งค่าความยาวสตริงสูงสุดที่ผู้ใช้ป้อนได้</span><span class="sxs-lookup"><span data-stu-id="7e738-146">The **stringLength** property can be used to set the maximum string length that users can enter.</span></span>

- <span data-ttu-id="7e738-147">ถ้าคุณสมบัติ **stringOptions** มีให้ในออบเจ็กต์ **TSTimesheetCustomField** องค์ประกอบรายการเหล่านั้นเป็นค่าเดียวที่ผู้ใช้สามารถเลือกได้โดยใช้ปุ่มตัวเลือก (ปุ่มตัวเลือก)</span><span class="sxs-lookup"><span data-stu-id="7e738-147">If the **stringOptions** property is provided on the **TSTimesheetCustomField** object, those list elements are the only values that users can select by using option buttons (radio buttons).</span></span>

    <span data-ttu-id="7e738-148">ในกรณีนี้ฟิลด์สตริงสามารถทำหน้าที่เป็นค่า enum สำหรับวัตถุประสงค์ในการป้อนข้อมูลของผู้ใช้</span><span class="sxs-lookup"><span data-stu-id="7e738-148">In this case, the string field can act as an enum value for the purpose of user entry.</span></span> <span data-ttu-id="7e738-149">ในการบันทึกค่าลงในฐานข้อมูลเป็น enum ให้แม็ปค่าสตริงกลับไปเป็นค่า enum ด้วยตนเองก่อนที่คุณจะบันทึกลงในฐานข้อมูลโดยใช้ชุดของคำสั่ง (ดูที่ส่วน "ใช้ชุดของคำสั่งบนคลาส TSTimesheetEntryService เพื่อบันทึกรายการแผ่นเวลาจากแอปกลับไปที่ฐานข้อมูล" ต่อไปในหัวข้อนี้เป็นตัวอย่าง)</span><span class="sxs-lookup"><span data-stu-id="7e738-149">To save the value to the database as an enum, manually map the string value back to the enum value before you save to the database by using chain of command (see the “Use chain of command on the TSTimesheetEntryService class to save a timesheet entry from the app back to the database” section later in this topic for an example).</span></span>

### <a name="fieldextendedtype-tscustomfieldextendedtype"></a><span data-ttu-id="7e738-150">fieldExtendedType (TSCustomFieldExtendedType)</span><span class="sxs-lookup"><span data-stu-id="7e738-150">fieldExtendedType (TSCustomFieldExtendedType)</span></span>

<span data-ttu-id="7e738-151">คุณสามารถใช้คุณสมบัตินี้เพื่อจัดรูปแบบค่าจริงเป็นสกุลเงิน</span><span class="sxs-lookup"><span data-stu-id="7e738-151">You can use this property to format real values as currency.</span></span> <span data-ttu-id="7e738-152">แนวทางนี้ใช้ได้เฉพาะเมื่อค่า **fieldBaseType** คือ **จริง**</span><span class="sxs-lookup"><span data-stu-id="7e738-152">This approach is applicable only when the **fieldBaseType** value is **Real**.</span></span>

- <span data-ttu-id="7e738-153">**TSCustomFieldExtendedType:ไม่มี** - ไม่มีการใช้การจัดรูปแบบ</span><span class="sxs-lookup"><span data-stu-id="7e738-153">**TSCustomFieldExtendedType:None** – No formatting is applied.</span></span>
- <span data-ttu-id="7e738-154">**TSCustomFieldExtendedType::สกุลเงิน** - จัดรูปแบบค่าเป็นสกุลเงิน</span><span class="sxs-lookup"><span data-stu-id="7e738-154">**TSCustomFieldExtendedType::Currency** – Format the value as currency.</span></span>

    <span data-ttu-id="7e738-155">เมื่อการจัดรูปแบบสกุลเงินใช้งานอยู่ ฟิลด์ **stringValue** อาจถูกใช้ส่งรหัสสกุลเงินที่ควรจะแสดงในแอป</span><span class="sxs-lookup"><span data-stu-id="7e738-155">When currency formatting is active, the **stringValue** field can be used pass the currency code that should be shown in the app.</span></span> <span data-ttu-id="7e738-156">ค่านี้เป็นค่าอ่านอย่างเดียว</span><span class="sxs-lookup"><span data-stu-id="7e738-156">The value is a read-only value.</span></span>

    <span data-ttu-id="7e738-157">ฟิลด์ **realValue** มีจำนวนเงินที่ควรบันทึกลงในฐานข้อมูล</span><span class="sxs-lookup"><span data-stu-id="7e738-157">The **realValue** field contains the money amount that should be saved to the database.</span></span>

### <a name="fieldsection-tscustomfieldsection"></a><span data-ttu-id="7e738-158">fieldSection (TSCustomFieldSection)</span><span class="sxs-lookup"><span data-stu-id="7e738-158">fieldSection (TSCustomFieldSection)</span></span>

<span data-ttu-id="7e738-159">คุณสามารถใช้คุณสมบัตินี้ระบุตำแหน่งที่ฟิลด์ที่กำหนดเองควรปรากฏในแอป</span><span class="sxs-lookup"><span data-stu-id="7e738-159">You can use this property specify where the custom field should appear in the app.</span></span>

- <span data-ttu-id="7e738-160">**TSCustomFieldSection::หัวข้อ** - ฟิลด์จะปรากฏในส่วน **ดูรายละเอียดเพิ่มเติม** ในแอป</span><span class="sxs-lookup"><span data-stu-id="7e738-160">**TSCustomFieldSection::Header** – The field will appear in the **View more details** section in the app.</span></span> <span data-ttu-id="7e738-161">ฟิลด์เหล่านี้เป็นแบบอ่านอย่างเดียวเสมอ</span><span class="sxs-lookup"><span data-stu-id="7e738-161">These fields are always read-only.</span></span>
- <span data-ttu-id="7e738-162">**TSCustomFieldSection::รายการ** - ฟิลด์นี้จะปรากฏขึ้นหลังฟิลด์รายการสำเร็จรูปทั้งหมดในรายการแผ่นเวลา</span><span class="sxs-lookup"><span data-stu-id="7e738-162">**TSCustomFieldSection::Line** – The field will appear after all the out-of-box line fields on timesheet entries.</span></span> <span data-ttu-id="7e738-163">ฟิลด์เหล่านี้สามารถแก้ไขได้หรือเป็นแบบอ่านอย่างเดียว</span><span class="sxs-lookup"><span data-stu-id="7e738-163">These fields can be either editable or read-only.</span></span>

### <a name="fieldname-fieldnameshort"></a><span data-ttu-id="7e738-164">fieldName (FieldNameShort)</span><span class="sxs-lookup"><span data-stu-id="7e738-164">fieldName (FieldNameShort)</span></span>

<span data-ttu-id="7e738-165">คุณสมบัตินี้ระบุฟิลด์เมื่อค่าที่แอปให้ไว้จะถูกบันทึกกลับไปที่ฐานข้อมูล</span><span class="sxs-lookup"><span data-stu-id="7e738-165">This property identifies the field when values that the app provides are saved back to the database.</span></span>

### <a name="tablename-tablenameshort"></a><span data-ttu-id="7e738-166">tableName (TableNameShort)</span><span class="sxs-lookup"><span data-stu-id="7e738-166">tableName (TableNameShort)</span></span>

<span data-ttu-id="7e738-167">คุณสมบัตินี้ระบุฟิลด์เมื่อค่าที่แอปให้ไว้จะถูกบันทึกกลับไปที่ฐานข้อมูล</span><span class="sxs-lookup"><span data-stu-id="7e738-167">This property identifies the field when values that the app provides are saved back to the database.</span></span>

### <a name="iseditable-noyes"></a><span data-ttu-id="7e738-168">isEditable (NoYes)</span><span class="sxs-lookup"><span data-stu-id="7e738-168">isEditable (NoYes)</span></span>

<span data-ttu-id="7e738-169">ตั้งค่าคุณสมบัตินี้เป็น **ใช่** เพื่อระบุว่าผู้ใช้ควรแก้ไขฟิลด์ในส่วนรายการแผ่นเวลา</span><span class="sxs-lookup"><span data-stu-id="7e738-169">Set this property to **Yes** to specify that the field in the timesheet entry section should be editable by users.</span></span> <span data-ttu-id="7e738-170">ตั้งค่าคุณสมบัติเป็น **ไม่** เพื่อทำให้ฟิลด์เป็นแบบอ่านอย่างเดียว</span><span class="sxs-lookup"><span data-stu-id="7e738-170">Set the property to **No** to make the field read-only.</span></span>

### <a name="ismandatory-noyes"></a><span data-ttu-id="7e738-171">isMandatory (NoYes)</span><span class="sxs-lookup"><span data-stu-id="7e738-171">isMandatory (NoYes)</span></span>

<span data-ttu-id="7e738-172">ตั้งค่าคุณสมบัตินี้เป็น **ใช่** เพื่อระบุว่าผู้ใช้ควรบังคับใช้ฟิลด์ในส่วนรายการแผ่นเวลา</span><span class="sxs-lookup"><span data-stu-id="7e738-172">Set this property to **Yes** to specify that the field in the timesheet entry section should be mandatory.</span></span>

### <a name="label-str"></a><span data-ttu-id="7e738-173">ป้ายกำกับ (str)</span><span class="sxs-lookup"><span data-stu-id="7e738-173">label (str)</span></span>

<span data-ttu-id="7e738-174">คุณสมบัตินี้ระบุป้ายกำกับที่แสดงถัดจากฟิลด์ในแอป</span><span class="sxs-lookup"><span data-stu-id="7e738-174">This property specifies the label that is shown next the field in the app.</span></span>

### <a name="stringoptions-list-of-strings"></a><span data-ttu-id="7e738-175">stringOptions (รายการสตริง)</span><span class="sxs-lookup"><span data-stu-id="7e738-175">stringOptions (List of Strings)</span></span>

<span data-ttu-id="7e738-176">คุณสมบัตินี้จะใช้ได้ก็ต่อเมื่อ **fieldBaseType** ถูกตั้งค่าเป็น **สตริง**</span><span class="sxs-lookup"><span data-stu-id="7e738-176">This property is applicable only when **fieldBaseType** is set to **String**.</span></span> <span data-ttu-id="7e738-177">ถ้า **stringOptions** ถูกตั้งค่าสตริงที่พร้อมใช้งานสำหรับการเลือกผ่านปุ่มตัวเลือก (ปุ่มตัวเลือก) จะถูกระบุโดยสตริงในรายการ</span><span class="sxs-lookup"><span data-stu-id="7e738-177">If **stringOptions** is set, the string values that are available for selection via option buttons (radio buttons) are specified by the strings in the list.</span></span> <span data-ttu-id="7e738-178">หากไม่มีการระบุสตริง จะอนุญาตให้ป้อนข้อความอิสระในฟิลด์สตริงได้ (โปรดดูที่ส่วน "ใช้ชุดคำสั่งบนคลาส TSTimesheetEntryService เพื่อบันทึกรายการแผ่นเวลาจากแอปกลับไปที่ฐานข้อมูล" ในหัวข้อนี้เป็นตัวอย่าง)</span><span class="sxs-lookup"><span data-stu-id="7e738-178">If no strings are provided, free-text entry in the string field is allowed (see the “Use chain of command on the TSTimesheetEntryService class to save a timesheet entry from the app back to the database” section later in this topic for an example).</span></span>

### <a name="stringlength-int"></a><span data-ttu-id="7e738-179">stringLength (int)</span><span class="sxs-lookup"><span data-stu-id="7e738-179">stringLength (int)</span></span>

<span data-ttu-id="7e738-180">คุณสมบัตินี้ระบุความยาวสูงสุดสำหรับฟิลด์สตริง</span><span class="sxs-lookup"><span data-stu-id="7e738-180">This property specifies the maximum length for a string field.</span></span> <span data-ttu-id="7e738-181">คุณสมบัตินี้จะใช้ได้ก็ต่อเมื่อ **fieldBaseType** ถูกตั้งค่าเป็น **สตริง**</span><span class="sxs-lookup"><span data-stu-id="7e738-181">It's applicable only when **fieldBaseType** is set to **String**.</span></span>

### <a name="numberofdecimals-int"></a><span data-ttu-id="7e738-182">numberOfDecimals (int)</span><span class="sxs-lookup"><span data-stu-id="7e738-182">numberOfDecimals (int)</span></span>

<span data-ttu-id="7e738-183">คุณสมบัตินี้ระบุจำนวนตำแหน่งทศนิยมที่แสดงสำหรับฟิลด์จริง</span><span class="sxs-lookup"><span data-stu-id="7e738-183">This property specifies the number of decimal places that are shown for a real field.</span></span> <span data-ttu-id="7e738-184">คุณสมบัตินี้จะใช้ได้ก็ต่อเมื่อ **fieldBaseType** ถูกตั้งค่าเป็น **จริง**</span><span class="sxs-lookup"><span data-stu-id="7e738-184">It's applicable only when **fieldBaseType** is set to **Real**.</span></span>

### <a name="ordersequence-int"></a><span data-ttu-id="7e738-185">orderSequence (int)</span><span class="sxs-lookup"><span data-stu-id="7e738-185">orderSequence (int)</span></span>

<span data-ttu-id="7e738-186">คุณสมบัตินี้ควบคุมลำดับการแสดงฟิลด์แบบกำหนดเองในแอปเมื่อระบุฟิลด์แบบกำหนดเองมากกว่าหนึ่งฟิลด์</span><span class="sxs-lookup"><span data-stu-id="7e738-186">This property controls the order in which the custom fields are shown in the app when more than one custom field is specified.</span></span> <span data-ttu-id="7e738-187">ฟิลด์ที่มีตัวเลขต่ำกว่าจะแสดงก่อน</span><span class="sxs-lookup"><span data-stu-id="7e738-187">Fields that have lower numbers are shown first.</span></span>

### <a name="booleanvalue-boolean"></a><span data-ttu-id="7e738-188">booleanValue (บูลีน)</span><span class="sxs-lookup"><span data-stu-id="7e738-188">booleanValue (boolean)</span></span>

<span data-ttu-id="7e738-189">สำหรับฟิลด์ของประเภท **บูลีน** คุณสมบัตินี้ส่งผ่านค่าบูลีนของฟิลด์ระหว่างเซิร์ฟเวอร์และแอป</span><span class="sxs-lookup"><span data-stu-id="7e738-189">For fields of the **Boolean** type, this property passes the Boolean value of the field between the server and the app.</span></span>

### <a name="guidvalue-guid"></a><span data-ttu-id="7e738-190">guidValue (guid)</span><span class="sxs-lookup"><span data-stu-id="7e738-190">guidValue (guid)</span></span>

<span data-ttu-id="7e738-191">สำหรับฟิลด์ของประเภท **GUID** คุณสมบัตินี้ส่งผ่านตัวระบุที่ไม่ซ้ำแบบส่วนกลาง (GUID) ของฟิลด์ระหว่างเซิร์ฟเวอร์และแอป</span><span class="sxs-lookup"><span data-stu-id="7e738-191">For fields of the **GUID** type, this property passes the globally unique identifier (GUID) value of the field between the server and the app.</span></span>

### <a name="int64value-int64"></a><span data-ttu-id="7e738-192">int64Value (int64)</span><span class="sxs-lookup"><span data-stu-id="7e738-192">int64Value (int64)</span></span>

<span data-ttu-id="7e738-193">สำหรับฟิลด์ของประเภท **Int64** คุณสมบัตินี้ส่งผ่านค่า Int64 ของฟิลด์ระหว่างเซิร์ฟเวอร์และแอป</span><span class="sxs-lookup"><span data-stu-id="7e738-193">For fields of the **Int64** type, this property passes the int64 value of the field between the server and the app.</span></span>

### <a name="intvalue-int"></a><span data-ttu-id="7e738-194">intValue (int)</span><span class="sxs-lookup"><span data-stu-id="7e738-194">intValue (int)</span></span>

<span data-ttu-id="7e738-195">สำหรับฟิลด์ของประเภท **Int** คุณสมบัตินี้ส่งผ่านค่า Int ของฟิลด์ระหว่างเซิร์ฟเวอร์และแอป</span><span class="sxs-lookup"><span data-stu-id="7e738-195">For fields of the **Int** type, this property passes the int value of the field between the server and the app.</span></span>

### <a name="realvalue-real"></a><span data-ttu-id="7e738-196">realValue (จริง)</span><span class="sxs-lookup"><span data-stu-id="7e738-196">realValue (real)</span></span>

<span data-ttu-id="7e738-197">สำหรับฟิลด์ของประเภท **จริง** คุณสมบัตินี้ส่งผ่านค่าจริงของฟิลด์ระหว่างเซิร์ฟเวอร์และแอป</span><span class="sxs-lookup"><span data-stu-id="7e738-197">For fields of the **Real** type, this property passes the real value of the field between the server and the app .</span></span>

### <a name="stringvalue-str"></a><span data-ttu-id="7e738-198">stringValue (str)</span><span class="sxs-lookup"><span data-stu-id="7e738-198">stringValue (str)</span></span>

<span data-ttu-id="7e738-199">สำหรับฟิลด์ของประเภท **สตริง** คุณสมบัตินี้ส่งผ่านค่าสตริงของฟิลด์ระหว่างเซิร์ฟเวอร์และแอป</span><span class="sxs-lookup"><span data-stu-id="7e738-199">For fields of the **String** type, this property passes the string value of the field between the server and the app.</span></span> <span data-ttu-id="7e738-200">นอกจากนี้ยังใช้สำหรับฟิลด์ของประเภท **จริง** ที่จัดรูปแบบเป็นสกุลเงิน</span><span class="sxs-lookup"><span data-stu-id="7e738-200">It's also used for fields of the **Real** type that are formatted as currency.</span></span> <span data-ttu-id="7e738-201">สำหรับช่องเหล่านั้น คุณสมบัติจะใช้เพื่อส่งรหัสสกุลเงินไปยังแอป</span><span class="sxs-lookup"><span data-stu-id="7e738-201">For those fields, the property is used to pass the currency code to the app.</span></span>

### <a name="datevalue-date"></a><span data-ttu-id="7e738-202">dateValue (วันที่)</span><span class="sxs-lookup"><span data-stu-id="7e738-202">dateValue (date)</span></span>

<span data-ttu-id="7e738-203">สำหรับฟิลด์ของประเภท **วันที่** คุณสมบัตินี้ส่งผ่านค่าวันที่ของฟิลด์ระหว่างเซิร์ฟเวอร์และแอป</span><span class="sxs-lookup"><span data-stu-id="7e738-203">For fields of the **Date** type, this property passes the date value of the field between the server and the app.</span></span>

## <a name="show-and-save-a-custom-field-in-the-timesheet-entry-section"></a><span data-ttu-id="7e738-204">แสดงและบันทึกฟิลด์ที่กำหนดเองในส่วนรายการแผ่นเวลา</span><span class="sxs-lookup"><span data-stu-id="7e738-204">Show and save a custom field in the timesheet entry section</span></span>

<span data-ttu-id="7e738-205">ด้านล่างนี้เป็นภาพหน้าจอจากแอปบนมือถือของการสร้างรายการแผ่นเวลา</span><span class="sxs-lookup"><span data-stu-id="7e738-205">Below is a screenshot from the mobile app of a timesheet entry creation.</span></span> <span data-ttu-id="7e738-206">โดยจะแสดงฟิลด์แบบสำเร็จรูปและฟิลด์ที่กำหนดเองในส่วน "รายการเวลา" ที่เรียกว่า "สตริงการทดสอบ" พร้อมด้วยค่า enum ของ "ตัวเลือกที่สอง" ที่กำหนดไว้แล้ว</span><span class="sxs-lookup"><span data-stu-id="7e738-206">It shows the out-of-box fields and a custom field in the "Time entry" section called "Test string" with an enum value of "Second option" already set.</span></span>

![ฟิลด์ตริงทดสอบที่กำหนดเองในแอป](media/timesheet-entry.jpg)



<span data-ttu-id="7e738-208">ด้านล่างนี้คือภาพหน้าจอจากแอปบนมือถือของผู้ใช้ที่เลือกหนึ่งในตัวเลือก enum ที่มีให้สำหรับฟิลด์ "สตริงทดสอบ" ที่กำหนดเอง</span><span class="sxs-lookup"><span data-stu-id="7e738-208">Below is a screenshot from the mobile app of the user selecting one of the enum options available for the "Test string" custom field.</span></span>  <span data-ttu-id="7e738-209">สองตัวเลือกคือ "ตัวเลือกแรก" และ "ตัวเลือกที่สอง" แสดงเป็นปุ่มตัวเลือก</span><span class="sxs-lookup"><span data-stu-id="7e738-209">The two options are "First option" and "Second option" shown as radio buttons.</span></span> <span data-ttu-id="7e738-210">ขณะนี้ตัวเลือกที่สองถูกเลือก</span><span class="sxs-lookup"><span data-stu-id="7e738-210">The second option is currently selected.</span></span>

![ปุ่มตัวเลือก (ปุ่มตัวเลือก) สำหรับฟิลด์แบบกำหนดเองของสตริงทดสอบ](media/enum-option.jpg)



### <a name="extend-the-tstimesheetline-table-so-that-it-has-a-custom-field"></a><span data-ttu-id="7e738-212">ขยายตาราง TSTimesheetLine เพื่อให้มีฟิลด์ที่กำหนดเอง</span><span class="sxs-lookup"><span data-stu-id="7e738-212">Extend the TSTimesheetLine table so that it has a custom field</span></span>

<span data-ttu-id="7e738-213">ในสถานการณ์ทั่วไปมีแนวโน้มว่าข้อมูลสำหรับฟิลด์ที่กำหนดเองในส่วนรายการแผ่นเวลาจะถูกบันทึกลงในตาราง TSTimesheetLine</span><span class="sxs-lookup"><span data-stu-id="7e738-213">In typical scenarios, it's likely that the data for a custom field in the timesheet entry section will be saved to the TSTimesheetLine table.</span></span> <span data-ttu-id="7e738-214">อย่างไรก็ตามสามารถใช้ตารางอื่นๆ ได้หากสามารถดึงข้อมูลโดยยึดตามเรกคอร์ด TSTimesheetTrans ที่มีให้หรือถ้าไม่มีบริบทของเรกคอร์ดที่เฉพาะเจาะจง (ตัวอย่างเช่น หากฟิลด์ถูกตั้งค่าเป็นแบบอ่านอย่างเดียวในพารามิเตอร์โครงการ)</span><span class="sxs-lookup"><span data-stu-id="7e738-214">However, other tables can be used if the data can be retrieved based on a TSTimesheetTrans record that is provided, or if it doesn't have specific record context (for example, if the field is set as read-only in the project parameters).</span></span>

<span data-ttu-id="7e738-215">โปรดทราบว่าช่องที่กำหนดเองไม่จำเป็นต้องมีเรกคอร์ดฐานข้อมูลสำรอง</span><span class="sxs-lookup"><span data-stu-id="7e738-215">Note that custom fields don't have to have any backing database records.</span></span> <span data-ttu-id="7e738-216">สามารถสร้างแบบไดนามิกตามตรรกะ X++</span><span class="sxs-lookup"><span data-stu-id="7e738-216">They can be dynamically generated based on X++ logic.</span></span> <span data-ttu-id="7e738-217">แนวทางนี้มีประโยชน์ในสถานการณ์แบบอ่านอย่างเดียว (ดูหัวข้อ "ใช้ชุดคำสั่งบนคลาส TSTimesheetDetails โดยวิธี buildCustomFieldListForHeader เพื่อกรอกรายละเอียดแผ่นเวลา" สำหรับตัวอย่างของค่าฟิลด์แบบกำหนดเองที่สร้างขึ้นแบบไดนามิก)</span><span class="sxs-lookup"><span data-stu-id="7e738-217">This approach can be useful in read-only scenarios (see the “Use chain of command on the TSTimesheetDetails class, buildCustomFieldListForHeader method to fill in timesheet details” section for an example of dynamically generated custom field values.)</span></span>

<span data-ttu-id="7e738-218">ด้านล่างนี้คือภาพหน้าจอจาก Visual Studio ของ Application Object Tree</span><span class="sxs-lookup"><span data-stu-id="7e738-218">Below is a screenshot from Visual Studio of the Application Object Tree.</span></span> <span data-ttu-id="7e738-219">แสดงส่วนขยายของตาราง TSTimesheetLine พร้อมกับฟิลด์ TestLineString ที่เพิ่มเป็นฟิลด์แบบกำหนดเอง</span><span class="sxs-lookup"><span data-stu-id="7e738-219">It shows an extension of the TSTimesheetLine table with the TestLineString field added as a custom field.</span></span>

![สตริงรายการ](media/b6756b4a3fc5298093327a088a7710fd.png)

### <a name="use-chain-of-command-on-the-buildcustomfieldlist-method-of-the-tstimesheetsettings-class-to-show-a-field-in-the-timesheet-entry-section"></a><span data-ttu-id="7e738-221">ใช้ชุดคำสั่งบนวิธี buildCustomFieldList ของคลาส TSTimesheetSettings เพื่อแสดงฟิลด์ในส่วนรายการแผ่นเวลา</span><span class="sxs-lookup"><span data-stu-id="7e738-221">Use chain of command on the buildCustomFieldList method of the TSTimesheetSettings class to show a field in the timesheet entry section</span></span>

<span data-ttu-id="7e738-222">รหัสนี้ควบคุมการตั้งค่าการแสดงผลสำหรับฟิลด์ในแอป</span><span class="sxs-lookup"><span data-stu-id="7e738-222">This code controls the display settings for the field in the app.</span></span> <span data-ttu-id="7e738-223">ตัวอย่างเช่น จะควบคุมประเภทของฟิลด์ ป้ายกำกับว่าฟิลด์บังคับหรือไม่ และส่วนใดที่ฟิลด์ปรากฏ</span><span class="sxs-lookup"><span data-stu-id="7e738-223">For example, it controls the type of field, the label, whether the field is mandatory, and what section the field appears in.</span></span>

<span data-ttu-id="7e738-224">ตัวอย่างต่อไปนี้แสดงฟิลด์สตริงในรายการเวลา</span><span class="sxs-lookup"><span data-stu-id="7e738-224">The following example shows a string field on time entries.</span></span> <span data-ttu-id="7e738-225">ฟิลด์นี้มีสองตัวเลือก **ตัวเลือกแรก** และ **ตัวเลือกที่สอง** ซึ่งมีให้ใช้งานผ่านปุ่มตัวเลือก (ปุ่มตัวเลือก)</span><span class="sxs-lookup"><span data-stu-id="7e738-225">This field has two options, **First option** and **Second option**, that are available via option buttons (radio buttons).</span></span> <span data-ttu-id="7e738-226">ฟิลด์ในแอปเชื่อมโยงกับฟิลด์ **TestLineString** ที่เพิ่มลงในตาราง TSTimesheetLine</span><span class="sxs-lookup"><span data-stu-id="7e738-226">The field in the app is associated with the **TestLineString** field that is added to the TSTimesheetLine table.</span></span>

<span data-ttu-id="7e738-227">หมายเหตุการใช้วิธี **TSTimesheetCustomField::newFromMetatdata()** เพื่อลดความซับซ้อนของการเริ่มต้นคุณสมบัติฟิลด์ที่กำหนดเอง: **fieldBaseType** **tableName** **ชื่อฟิลด์** **label** **isEditable** **isMandatory** **stringLength** และ **numberOfDecimals**</span><span class="sxs-lookup"><span data-stu-id="7e738-227">Note the use of the **TSTimesheetCustomField::newFromMetatdata()** method to simplify the initialization of the custom field properties: **fieldBaseType**, **tableName**, **fieldname**, **label**, **isEditable**, **isMandatory**, **stringLength**, and **numberOfDecimals**.</span></span> <span data-ttu-id="7e738-228">คุณยังสามารถตั้งค่าพารามิเตอร์เหล่านี้ด้วยตนเองได้ตามต้องการ</span><span class="sxs-lookup"><span data-stu-id="7e738-228">You can also set these parameters manually, as you prefer.</span></span>

```xpp
...
[ExtensionOf(classStr(TsTimesheetSettings))]
final class TSTimesheetSettings_Extension
{
    protected List buildCustomFieldList()
    {
        List customFieldList = next buildCustomFieldList();
        TSTimesheetCustomField tsTimesheetCustomField;
        tsTimesheetCustomField =
        TSTimesheetCustomField::newFromMetadata(tableNum(TsTimesheetLine),
        fieldNum(TSTimesheetLine, TestLineString));
        tsTimesheetCustomField.parmFieldSection(TSCustomFieldSection::Line);
        tsTimesheetCustomField.parmOrderSequence(1);
        List stringOptions = new List(Types::String);
        stringOptions.addEnd('First option');
        stringOptions.addEnd('Second option');
        tsTimesheetCustomField.parmStringOptions(stringOptions);
        customFieldList.addEnd(tsTimesheetCustomField);
        return customFieldList;
    }
}
...
```

### <a name="use-chain-of-command-on-the-buildcustomfieldlistforentry-method-of-the-tstimesheetentry-class-to-enter-values-in-a-timesheet-entry"></a><span data-ttu-id="7e738-229">ใช้ชุดคำสั่งบนวิธี buildCustomFieldListForEntry ของคลาส TSTimesheetEntry เพื่อป้อนค่าในรายการแผ่นเวลา</span><span class="sxs-lookup"><span data-stu-id="7e738-229">Use chain of command on the buildCustomFieldListForEntry method of the TSTimesheetEntry class to enter values in a timesheet entry</span></span>

<span data-ttu-id="7e738-230">วิธี **buildCustomFieldListForEntry** ถูกใช้เพื่อป้อนค่าในบรรทัดแผ่นเวลาที่บันทึกไว้ในแอปมือถือ</span><span class="sxs-lookup"><span data-stu-id="7e738-230">The **buildCustomFieldListForEntry** method is used to enter values on the saved timesheet lines in the mobile app.</span></span> <span data-ttu-id="7e738-231">ใช้เรกคอร์ด TSTimesheetTrans เป็นพารามิเตอร์</span><span class="sxs-lookup"><span data-stu-id="7e738-231">It takes a TSTimesheetTrans record as a parameter.</span></span> <span data-ttu-id="7e738-232">คุณสามารถใช้ฟิลด์จากเรกคอร์ดนั้นเพื่อกรอกค่าฟิลด์ที่กำหนดเองในแอป</span><span class="sxs-lookup"><span data-stu-id="7e738-232">Fields from that record can be used to fill in the custom field value in the app.</span></span>

```xpp
...
[ExtensionOf(classStr(TsTimesheetEntry))]
final class TsTimesheetEntry_Extension
{
    protected List buildCustomFieldListForEntry(TSTimesheetTrans _tsTimesheetTrans)
    {
        List customFieldList = next buildCustomFieldListForEntry(_tsTimesheetTrans);
        TSTimesheetLine tsTimesheetLine = _tsTimesheetTrans.timesheetLine();
        TSTimesheetCustomField tsTimesheetCustomField;
        tsTimesheetCustomField =
        TSTimesheetCustomField::newFromMetadata(tableNum(TsTimesheetLine),
        fieldNum(TSTimesheetLine, TestLineString));
        tsTimesheetCustomField.parmFieldSection(TSCustomFieldSection::Line);
        tsTimesheetCustomField.parmOrderSequence(1);
        tsTimesheetCustomField.parmStringValue(tsTimesheetLine.TestLineString);
        List stringOptions = new List(Types::String);
        stringOptions.addEnd('First option');
        stringOptions.addEnd('second option;);
        tsTimesheetCustomField.parmStringOptions(stringOptions);
        customFieldList.addEnd(tsTimesheetCustomField);
        return customFieldList;
    }
}
...
```

### <a name="use-chain-of-command-on-the-tstimesheetentryservice-class-to-save-a-timesheet-entry-from-the-app-back-to-the-database"></a><span data-ttu-id="7e738-233">ใช้ชุดคำสั่งบนคลาส TSTimesheetEntryService เพื่อบันทึกรายการแผ่นเวลาจากแอปกลับไปที่ฐานข้อมูล</span><span class="sxs-lookup"><span data-stu-id="7e738-233">Use chain of command on the TSTimesheetEntryService class to save a timesheet entry from the app back to the database</span></span>

<span data-ttu-id="7e738-234">ในการบันทึกฟิลด์ที่กำหนดเองกลับไปที่ฐานข้อมูลในการใช้งานทั่วไป คุณต้องขยายหลายวิธี:</span><span class="sxs-lookup"><span data-stu-id="7e738-234">To save a custom field back to the database in typical usage, you must extend multiple methods:</span></span>

- <span data-ttu-id="7e738-235">วิธี **timesheetLineNeedsUpdating** ใช้เพื่อตรวจสอบว่าผู้ใช้ในแอปเปลี่ยนแปลงเรกคอร์ดรายการหรือไม่และต้องบันทึกลงในฐานข้อมูล</span><span class="sxs-lookup"><span data-stu-id="7e738-235">The **timesheetLineNeedsUpdating** method is used to determine whether the line record has been changed by the user in the app and must be saved to the database.</span></span> <span data-ttu-id="7e738-236">หากประสิทธิภาพไม่น่ากังวล วิธีนี้สามารถทำให้ง่ายขึ้นเพื่อให้กลับมา **จริง** เสมอ</span><span class="sxs-lookup"><span data-stu-id="7e738-236">If performance isn't a concern, this method can be simplified so that it always returns **true**.</span></span>
- <span data-ttu-id="7e738-237">วิธี **populateTimesheetLineFromEntryDuringCreate** และ **populateTimesheetLineFromEntryDuringUpdate** สามารถขยายวิธีการเพื่อให้ป้อนค่าในเรกคอร์ดฐานข้อมูล TSTimesheetLine จากเรกคอร์ดสัญญาข้อมูล TSTimesheetEntry ที่มีให้</span><span class="sxs-lookup"><span data-stu-id="7e738-237">The **populateTimesheetLineFromEntryDuringCreate** and **populateTimesheetLineFromEntryDuringUpdate** methods can be extended so that they enter values in the TSTimesheetLine database record from the TSTimesheetEntry data contract record that is provided.</span></span> <span data-ttu-id="7e738-238">ในตัวอย่างต่อไปนี้ ให้สังเกตว่าการแม็ประหว่างฟิลด์ฐานข้อมูลและฟิลด์รายการทำได้ด้วยตนเองผ่านรหัส X++ อย่างไร</span><span class="sxs-lookup"><span data-stu-id="7e738-238">In the example that follows, notice how the mapping between the database field and the entry field is manually done via X++ code.</span></span>
- <span data-ttu-id="7e738-239">วิธี **populateTimesheetWeekFromEntry** ยังสามารถขยายได้หากฟิลด์แบบกำหนดเองที่แม็ปกับออบเจ็กต์ **TSTimesheetEntry** ต้องเขียนกลับไปที่ตารางฐานข้อมูล TSTimesheetLineweek</span><span class="sxs-lookup"><span data-stu-id="7e738-239">The **populateTimesheetWeekFromEntry** method can also be extended if the custom field that is mapped to the **TSTimesheetEntry** object must write back to the TSTimesheetLineweek database table.</span></span>

> [!NOTE]
> <span data-ttu-id="7e738-240">ตัวอย่างต่อไปนี้บันทึกค่า **firstOption** หรือ **secondOption** ที่ผู้ใช้เลือกไปยังฐานข้อมูลเป็นค่าสตริงดิบ</span><span class="sxs-lookup"><span data-stu-id="7e738-240">The following example saves the **firstOption** or **secondOption** value that the user selects to the database as a raw string value.</span></span> <span data-ttu-id="7e738-241">หากฟิลด์ฐานข้อมูลเป็นฟิลด์ของประเภท **Enum** ค่าเหล่านั้นสามารถแม็ปกับค่า enum ด้วยตนเองจากนั้นบันทึกลงในฟิลด์ enum บนตารางฐานข้อมูล</span><span class="sxs-lookup"><span data-stu-id="7e738-241">If the database field is a field of the **Enum** type, those values can be manually mapped to an enum value and then saved to an enum field on the database table.</span></span>

```xpp
...
[ExtensionOf(classStr(TSTimesheetEntryService))]
final class TSTimesheetEntryService_Extension
{
    protected boolean timesheetLineNeedsUpdating(TSTimesheetLine _tsTimesheetLine,
    TsTimesheetEntry _tsTimesheetEntry)
    {
        boolean ret = next timesheetLineNeedsUpdating(_tsTimesheetLine,
        _tsTimesheetEntry);
        if (!ret)
        {
            */ Loop through custom fields to see if value needs updating*/
            ListEnumerator enumerator =  _tsTimesheetEntry.parmCustomFields().getEnumerator();
            while (enumerator.moveNext())
            {
                TSTimesheetCustomField customField = enumerator.current();
                if (customField.parmFieldName() == fieldId2Name(tableNum(TsTimesheetLine),
                fieldNum(TSTimesheetLine, TestLineString)))
                {
                    */ If Custom field value for TestLineString field has changed, We need to update the timesheet line.*/
                    if (_tsTimesheetLine.TestLineString != customField.parmStringValue())
                    {
                        ret = true;
                    }
                }
            }
        }
        return ret;
    }
    protected void populateTimesheetLineFromEntryDuringCreate(TSTimesheetLine
    _tsTimesheetLine, TSTimesheetEntry _tsTimesheetEntry)
    {
        next populateTimesheetLineFromEntryDuringCreate(_tsTimesheetLine,
        _tsTimesheetEntry);
        this.populateTimesheetLineFromCustomFields(_tsTimesheetLine,
        _tsTimesheetEntry);
        }
        protected void populateTimesheetLineFromEntryDuringUpdate(TSTimesheetLine
        \_tsTimesheetLine, TSTimesheetEntry _tsTimesheetEntry)
        {
            next populateTimesheetLineFromEntryDuringUpdate(_tsTimesheetLine,
            _tsTimesheetEntry);
            this.populateTimesheetLineFromCustomFields(_tsTimesheetLine,
            _tsTimesheetEntry);
        }
        private void populateTimesheetLineFromCustomFields(TSTimesheetLine
        _tsTimesheetLine, TSTimesheetEntry _tsTimesheetEntry)
        {
            ListEnumerator enumerator =
            _tsTimesheetEntry.parmCustomFields().getEnumerator();
            while (enumerator.moveNext())
            {
                TSTimesheetCustomField customField = enumerator.current();
                if (customField.parmFieldName() == fieldId2Name(tableNum(TsTimesheetLine),
                fieldNum(TSTimesheetLine, TestLineString)))
                {
                    _tsTimesheetLine.TestLineString = customField.parmStringValue();
                }
            }
        }
    }
...
```

## <a name="show-a-custom-field-in-the-timesheet-header-section"></a><span data-ttu-id="7e738-242">แสดงฟิลด์ที่กำหนดเองในส่วนหัวของแผ่นเวลา</span><span class="sxs-lookup"><span data-stu-id="7e738-242">Show a custom field in the timesheet header section</span></span>

<span data-ttu-id="7e738-243">ด้านล่างนี้เป็นภาพหน้าจอจากแอปบนมือถือของผู้ใช้ที่กำลังดูแผ่นเวลา</span><span class="sxs-lookup"><span data-stu-id="7e738-243">Below is a screenshot from the mobile app of a user viewing a timesheet.</span></span> <span data-ttu-id="7e738-244">ปุ่ม "ข้อมูลเพิ่มเติม" ถูกเลือกไว้ที่มุมขวาบนเพื่อแสดงตัวเลือก "ดูรายละเอียดเพิ่มเติม"</span><span class="sxs-lookup"><span data-stu-id="7e738-244">The "More information" button has been selected in the upper-right corner to show the "View more details" option.</span></span>  

![ดูคำสั่งรายละเอียดเพิ่มเติม](media/show-more.png)

<span data-ttu-id="7e738-246">ด้านล่างนี้เป็นภาพหน้าจอจากแอปบนมือถือที่แสดงส่วน "เพิ่มเติม" ของแผ่นเวลา</span><span class="sxs-lookup"><span data-stu-id="7e738-246">Below is a screenshot from the mobile app showing the “More” section of a timesheet.</span></span> <span data-ttu-id="7e738-247">มีการเพิ่มฟิลด์ที่กำหนดเองที่เรียกว่า "อัตราการใช้งานของแผ่นเวลานี้ (ฟิลด์ที่กำหนดเองจากการคำนวณ)" ในส่วนหัวของแผ่นเวลา</span><span class="sxs-lookup"><span data-stu-id="7e738-247">A custom field called “Utilization rate of this timesheet (computed custom field)” has been added to the timesheet header section.</span></span> <span data-ttu-id="7e738-248">ค่าแบบอ่านอย่างเดียวคือ "0.667" ถูกตั้งค่าในฟิลด์ที่กำหนดเอง</span><span class="sxs-lookup"><span data-stu-id="7e738-248">A read-only value of "0.667" is set on the custom field.</span></span>

![ส่วนเพิ่มเติม](media/more-section.jpg)

### <a name="extend-the-tstimesheettable-table-so-that-it-has-a-custom-field"></a><span data-ttu-id="7e738-250">ขยายตาราง TSTimesheetTable เพื่อให้มีฟิลด์ที่กำหนดเอง</span><span class="sxs-lookup"><span data-stu-id="7e738-250">Extend the TSTimesheetTable table so that it has a custom field</span></span>

<span data-ttu-id="7e738-251">ในสถานการณ์ทั่วไป มีแนวโน้มว่าข้อมูลสำหรับฟิลด์ที่กำหนดเองในส่วนหัวจะถูกดึงจากตาราง TSTimesheetHeader</span><span class="sxs-lookup"><span data-stu-id="7e738-251">In typical scenarios, it's likely that the data for a custom field in the header section will be pulled from the TSTimesheetHeader table.</span></span> <span data-ttu-id="7e738-252">อย่างไรก็ตามสามารถใช้ตารางอื่นๆ ได้หากสามารถดึงข้อมูลโดยยึดตามเรกคอร์ด TSTimesheetTable ที่มีให้หรือถ้าไม่มีบริบทของเรกคอร์ดที่เฉพาะเจาะจง (ตัวอย่างเช่น หากฟิลด์ถูกตั้งค่าเป็นแบบอ่านอย่างเดียวในพารามิเตอร์โครงการ)</span><span class="sxs-lookup"><span data-stu-id="7e738-252">However, other tables can be used if the data can be retrieved based on a TSTimesheetTable record that is provided, or if it doesn't have specific record context (for example, if the field is set as read-only in the project parameters).</span></span>

<span data-ttu-id="7e738-253">โปรดทราบว่าช่องที่กำหนดเองไม่จำเป็นต้องมีเรกคอร์ดฐานข้อมูลสำรอง</span><span class="sxs-lookup"><span data-stu-id="7e738-253">Note that custom fields don't have to have any backing database records.</span></span> <span data-ttu-id="7e738-254">สามารถสร้างแบบไดนามิกตามตรรกะ X++</span><span class="sxs-lookup"><span data-stu-id="7e738-254">They can be dynamically generated based on X++ logic.</span></span> <span data-ttu-id="7e738-255">ตัวอย่างต่อไปนี้แสดงให้เห็นถึงแนวทางนี้</span><span class="sxs-lookup"><span data-stu-id="7e738-255">The example that follows shows this approach.</span></span>

<span data-ttu-id="7e738-256">ฟิลด์ในส่วนส่วนหัวมักเป็นแบบอ่านอย่างเดียวในแอป</span><span class="sxs-lookup"><span data-stu-id="7e738-256">Fields in the header section are always read-only in the app.</span></span>

### <a name="use-chain-of-command-on-the-buildcustomfieldlist-method-of-the-tstimesheetsettings-class-to-show-a-field-in-the-header-section"></a><span data-ttu-id="7e738-257">ใช้ชุดคำสั่งบนวิธี buildCustomFieldList ของคลาส TSTimesheetSettings เพื่อแสดงฟิลด์ในส่วนหัว</span><span class="sxs-lookup"><span data-stu-id="7e738-257">Use chain of command on the buildCustomFieldList method of the TSTimesheetSettings class to show a field in the header section</span></span>

<span data-ttu-id="7e738-258">รหัสนี้ควบคุมการตั้งค่าการแสดงผลสำหรับฟิลด์ในแอป</span><span class="sxs-lookup"><span data-stu-id="7e738-258">This code controls the display settings for the field in the app.</span></span> <span data-ttu-id="7e738-259">ตัวอย่างเช่น จะควบคุมประเภทของฟิลด์ ป้ายกำกับว่าฟิลด์บังคับหรือไม่ และส่วนใดที่ฟิลด์ปรากฏ</span><span class="sxs-lookup"><span data-stu-id="7e738-259">For example, it controls the type of field, the label, whether the field is mandatory, and what section the field appears in.</span></span>

<span data-ttu-id="7e738-260">ตัวอย่างต่อไปนี้แสดงค่าที่คำนวณในส่วนส่วนหัวในแอป</span><span class="sxs-lookup"><span data-stu-id="7e738-260">The following example shows a computed value in the header section in the app.</span></span>

```xpp
...
[ExtensionOf(classStr(TsTimesheetSettings))]
final class TSTimesheetSettings_Extension
{
    protected List buildCustomFieldList()
    {
        List customFieldList = next buildCustomFieldList();
        TSTimesheetCustomField tsTimesheetCustomField;

        */ Computed utilization rate*/
        tsTimesheetCustomField = new TSTimesheetCustomField();
        tsTimesheetCustomField.parmFieldBaseType(Types::Real);
        tsTimesheetCustomField.parmLabel("Utilization rate of this timesheet (computed
        custom field)");
        tsTimesheetCustomField.parmFieldSection(TSCustomFieldSection::Header);
        tsTimesheetCustomField.parmOrderSequence(2);
        tsTimesheetCustomField.parmNumberOfDecimals(3);
        customFieldList.addEnd(tsTimesheetCustomField);
        return customFieldList;
    }
}
...
```

### <a name="use-chain-of-command-on-the-buildcustomfieldlistforheader-method-of-the-tstimesheetdetails-class-to-fill-in-timesheet-details"></a><span data-ttu-id="7e738-261">ใช้ชุดคำสั่งบนวิธี buildCustomFieldListForHeader ของคลาส TSTimesheetDetails เพื่อป้อนรายละเอียดแผ่นเวลา</span><span class="sxs-lookup"><span data-stu-id="7e738-261">Use chain of command on the buildCustomFieldListForHeader method of the TSTimesheetDetails class to fill in timesheet details</span></span>

<span data-ttu-id="7e738-262">วิธี **buildCustomFieldListForHeader** ถูกใช้กรอกรายละเอียดในส่วนหัวของแผ่นเวลาในแอปมือถือ</span><span class="sxs-lookup"><span data-stu-id="7e738-262">The **buildCustomFieldListForHeader** method is used to fill in the timesheet header details in the mobile app.</span></span> <span data-ttu-id="7e738-263">ใช้เรกคอร์ด TSTimesheetTable เป็นพารามิเตอร์</span><span class="sxs-lookup"><span data-stu-id="7e738-263">It takes a TSTimesheetTable record as a parameter.</span></span> <span data-ttu-id="7e738-264">คุณสามารถใช้ฟิลด์จากเรกคอร์ดนั้นเพื่อกรอกค่าฟิลด์ที่กำหนดเองในแอป</span><span class="sxs-lookup"><span data-stu-id="7e738-264">Fields from that record can be used to fill in the custom field value in the app.</span></span> <span data-ttu-id="7e738-265">ตัวอย่างต่อไปนี้ไม่อ่านค่าใดๆ จากฐานข้อมูล</span><span class="sxs-lookup"><span data-stu-id="7e738-265">The following example doesn't read any values from the database.</span></span> <span data-ttu-id="7e738-266">แต่จะใช้ตรรกะ X++ เพื่อสร้างค่าที่คำนวณแล้วซึ่งจะแสดงในแอป</span><span class="sxs-lookup"><span data-stu-id="7e738-266">Instead, it uses X++ logic to generate a computed value that is then shown in the app.</span></span>


```xpp
...
[ExtensionOf(classStr(TSTimesheetDetails))]
final class TSTimesheetDetails_Extension
{
    protected List buildCustomFieldListForHeader(TSTimesheetTable
    _tsTimesheetTable)
    {
        List customFieldList = next buildCustomFieldListForHeader(_tsTimesheetTable);
        TSTimesheetCustomField tsTimesheetCustomField;

        */ Computed utilization rate*/
        tsTimesheetCustomField = new TSTimesheetCustomField();
        tsTimesheetCustomField.parmFieldBaseType(Types::Real);
        tsTimesheetCustomField.parmLabel("Utilization rate of this timesheet (computed
        custom field)");
        tsTimesheetCustomField.parmFieldSection(TSCustomFieldSection::Header);
        tsTimesheetCustomField.parmOrderSequence(2);
        tsTimesheetCustomField.parmNumberOfDecimals(3);
        real utilizationRate = 0;
        if (_tsTimesheetTable.totalHours() != 0)
        {
            utilizationRate = _tsTimesheetTable.totalHoursBillable() /
            _tsTimesheetTable.totalHours();
        }
        tsTimesheetCustomField.parmRealValue(utilizationRate);
        customFieldList.addEnd(tsTimesheetCustomField);
        return customFieldList;
    }
}
...
```

## <a name="other-configurabilityextensibility-opportunities"></a><span data-ttu-id="7e738-267">โอกาสในการกำหนดค่า/ความสามารถในการขยายอื่นๆ</span><span class="sxs-lookup"><span data-stu-id="7e738-267">Other configurability/extensibility opportunities</span></span>

### <a name="adding-additional-validation-for-the-app"></a><span data-ttu-id="7e738-268">การเพิ่มการตรวจสอบความถูกต้องเพิ่มเติมสำหรับแอป</span><span class="sxs-lookup"><span data-stu-id="7e738-268">Adding additional validation for the app</span></span>

<span data-ttu-id="7e738-269">ตรรกะที่มีอยู่สำหรับการทำงานของแผ่นเวลาในระดับฐานข้อมูลจะยังคงทำงานได้ตามที่คาดไว้</span><span class="sxs-lookup"><span data-stu-id="7e738-269">Existing logic for timesheet functionality at the database level will still work as expected.</span></span> <span data-ttu-id="7e738-270">หากต้องการขัดจังหวะการดำเนินการบันทึกหรือส่งให้เสร็จสิ้นและแสดงข้อความแสดงข้อผิดพลาด คุณสามารถเพิ่ม **แสดงข้อผิดพลาด ("ข้อความถึงผู้ใช้")** ไปยังรหัสผ่านส่วนขยายของชุดคำสั่ง</span><span class="sxs-lookup"><span data-stu-id="7e738-270">To interrupt the completion of save or submit operations and show a specific error message, you can add **throw error("message to user")** to the code via a chain of command extension.</span></span> <span data-ttu-id="7e738-271">นี่คือสามตัวอย่างของวิธีการขยายที่มีประโยชน์:</span><span class="sxs-lookup"><span data-stu-id="7e738-271">Here are three examples of useful extensible methods:</span></span>

- <span data-ttu-id="7e738-272">ถ้า **validateWrite** ในตาราง TSTimesheetLine ส่งกลับ **เท็จ** ในระหว่างการดำเนินการบันทึกสำหรับรายการแผ่นเวลา ข้อความแสดงข้อผิดพลาดจะปรากฏในแอปมือถือ</span><span class="sxs-lookup"><span data-stu-id="7e738-272">If **validateWrite** on the TSTimesheetLine table returns **false** during a save operation for a timesheet line, an error message is shown in the mobile app.</span></span>
- <span data-ttu-id="7e738-273">ถ้า **validateSubmit** ในตาราง TSTimesheetTable ส่งกลับ **เท็จ** ในระหว่างการส่งรายการแผ่นเวลา ข้อความแสดงข้อผิดพลาดจะปรากฏกับผู้ใช้</span><span class="sxs-lookup"><span data-stu-id="7e738-273">If **validateSubmit** on the TSTimesheetTable table returns **false** during timesheet submission in the app, an error message is shown to the user.</span></span>
- <span data-ttu-id="7e738-274">ตรรกะที่เติมในฟิลด์ (ตัวอย่างเช่น **คุณสมบัติรายการ**) ในระหว่างวิธี **แทรก** บนตาราง TSTimesheetLine จะยังคงทำงานอยู่</span><span class="sxs-lookup"><span data-stu-id="7e738-274">Logic that fills in fields (for example, **Line Property**) during the **insert** method on the TSTimesheetLine table will still run.</span></span>

### <a name="hiding-and-marking-out-of-box-fields-as-read-only-via-configuration"></a><span data-ttu-id="7e738-275">การซ่อนและทำเครื่องหมายฟิลด์สำเร็จรูปเป็นแบบอ่านอย่างเดียวผ่านการกำหนดค่า</span><span class="sxs-lookup"><span data-stu-id="7e738-275">Hiding and marking out-of-box fields as read-only via configuration</span></span>

<span data-ttu-id="7e738-276">จากพารามิเตอร์โครงการ คุณสามารถสร้างฟิลด์สำเร็จรูปแบบอ่านอย่างเดียวหรือซ่อนไว้ในแอปมือถือ</span><span class="sxs-lookup"><span data-stu-id="7e738-276">From the project parameters, you can make out-of-box fields read-only or hidden in the mobile app.</span></span> <span data-ttu-id="7e738-277">ตั้งค่าตัวเลือกในส่วน **แผ่นเวลามือถือ** ในส่วนแท็บ **แผ่นเวลา** ของหน้า **พารามิเตอร์การจัดการโครงการและการบัญชี**</span><span class="sxs-lookup"><span data-stu-id="7e738-277">Set the options in the **Mobile timesheets** section on the **Timesheet** tab of the **Project management and accounting parameters** page.</span></span>

![พารามิเตอร์โครงการ](media/5753b8ecccd1d8bb2b002dd538b3f762.png)

### <a name="changing-the-activities-that-are-available-for-selection-via-extensions"></a><span data-ttu-id="7e738-279">การเปลี่ยนกิจกรรมที่มีให้เลือกผ่านส่วนขยาย</span><span class="sxs-lookup"><span data-stu-id="7e738-279">Changing the activities that are available for selection via extensions</span></span>

<span data-ttu-id="7e738-280">กิจกรรมที่มีให้เลือกสำหรับโครงการกรอกผ่านวิธี **getActivitiesForProject()** และ **getActivityQuery()** ในคลาส **TsTimesheetProjectService**</span><span class="sxs-lookup"><span data-stu-id="7e738-280">The activities that are available for selection for a project are filled in via the **getActivitiesForProject()** and **getActivityQuery()** methods in the **TsTimesheetProjectService** class.</span></span> <span data-ttu-id="7e738-281">คุณสามารถใช้ชุดคำสั่งเพื่อเปลี่ยนลักษณะการทำงานนี้เพื่อให้เข้ากับสถานการณ์ทางธุรกิจของคุณสำหรับกิจกรรมที่พร้อมให้เลือกสำหรับโครงการเฉพาะ</span><span class="sxs-lookup"><span data-stu-id="7e738-281">You can use chain of command to change this behavior to match your business scenario for the activities that are available for selection for a specific project.</span></span>

### <a name="entering-a-default-project-category-on-timesheet-entries"></a><span data-ttu-id="7e738-282">การป้อนประเภทโครงการเริ่มต้นในรายการแผ่นเวลา</span><span class="sxs-lookup"><span data-stu-id="7e738-282">Entering a default project category on timesheet entries</span></span>

<span data-ttu-id="7e738-283">รายการประเภทโครงการเริ่มต้นในรายการแผ่นเวลาเกิดขึ้นในสามระดับ</span><span class="sxs-lookup"><span data-stu-id="7e738-283">Entry of a default project category on timesheet entries occurs at three levels.</span></span> <span data-ttu-id="7e738-284">คุณสามารถใช้ชุดคำสั่งเพื่อขยายลักษณะการทำงานในระดับใดระดับหนึ่งหรือทั้งหมดเพื่อให้บรรลุลักษณะการทำงานที่ต้องการ</span><span class="sxs-lookup"><span data-stu-id="7e738-284">You can use chain of command to extend the behavior at any or all of these levels to achieve the desired behavior.</span></span> <span data-ttu-id="7e738-285">ใช้ลำดับชั้นต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="7e738-285">The following hierarchy is used:</span></span>

1. <span data-ttu-id="7e738-286">แอปพยายามใส่หมวดหมู่เริ่มต้นจากทรัพยากรโครงการ</span><span class="sxs-lookup"><span data-stu-id="7e738-286">The app tries to put the default category from the project resource.</span></span> <span data-ttu-id="7e738-287">ประเภทเริ่มต้นนี้ถูกตั้งค่าในวิธี **getCurrentUserResource** และ **getDelegatedResourcesForCurrentUser** ในคลาส **TSTimesheetSettingsService**</span><span class="sxs-lookup"><span data-stu-id="7e738-287">This default category is set in the **getCurrentUserResource** and **getDelegatedResourcesForCurrentUser** methods in the **TSTimesheetSettingsService** class.</span></span>
2. <span data-ttu-id="7e738-288">หากไม่ได้ระบุหมวดหมู่เริ่มต้นที่ระดับทรัพยากรโครงการ แอปจะพยายามดึงออกจากกิจกรรมโครงการ</span><span class="sxs-lookup"><span data-stu-id="7e738-288">If the default category isn't provided at the project resource level, the app tries to pull it from the project activity.</span></span> <span data-ttu-id="7e738-289">ประเภทเริ่มต้นนี้ถูกตั้งค่าในวิธี **getActivitiesForProject** ในคลาส **TSTimesheetProjectService**</span><span class="sxs-lookup"><span data-stu-id="7e738-289">This default category is set in the **getActivitiesForProject** method in the **TSTimesheetProjectService** class.</span></span>
3. <span data-ttu-id="7e738-290">หากไม่ได้ระบุหมวดหมู่เริ่มต้นที่ระดับกิจกรรมโครงการ ประเภทเริ่มต้นจะถูกดึงออกจากพารามิเตอร์โครงการ</span><span class="sxs-lookup"><span data-stu-id="7e738-290">If the default category isn't provided at the project activity level, the default category it taken from the project parameters.</span></span> <span data-ttu-id="7e738-291">ประเภทเริ่มต้นนี้ถูกตั้งค่าในวิธี **getProjectDetailsbyRule** ในคลาส **TSTimesheetProjectService**</span><span class="sxs-lookup"><span data-stu-id="7e738-291">This default category is set in the **getProjectDetailsbyRule** method in the **TSTimesheetProjectService** class.</span></span>
