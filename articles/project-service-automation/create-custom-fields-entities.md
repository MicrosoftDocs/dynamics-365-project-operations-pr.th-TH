---
title: การสร้างฟิลด์และเอนทิตีแบบกำหนดเอง
description: หัวข้อนี้อธิบายถึงวิธีการสร้างชุดตัวเลือกและเอนทิตีในโซลูชันของคุณในแพลตฟอร์ม Power Apps
author: Rumant
manager: kfend
ms.custom:
- dyn365-projectservice
ms.date: 11/26/2018
ms.topic: article
ms.prod: Project Service
ms.service: business-applications
ms.assetid: fb160bfd-e037-4a21-a968-3ff2e6e16481
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365PS
ms.openlocfilehash: 7ee30e3bb6b8034ef226e2e9181195685355011f
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 03/24/2020
ms.locfileid: "3756491"
---
# <a name="create-custom-fields-and-entities"></a><span data-ttu-id="1a9dc-103">การสร้างฟิลด์และเอนทิตีแบบกำหนดเอง</span><span class="sxs-lookup"><span data-stu-id="1a9dc-103">Create custom fields and entities</span></span> 

<span data-ttu-id="1a9dc-104">ทำตามขั้นตอนต่อไปนี้ทุกครั้งที่คุณต้องการสร้างชุดตัวเลือกหรือเอนทิตีแบบกำหนดบนแพลตฟอร์ม Power Apps</span><span class="sxs-lookup"><span data-stu-id="1a9dc-104">Complete the following steps any time that you want to create a custom option set or entity on the Power Apps platform.</span></span>  
<span data-ttu-id="1a9dc-105">ขั้นตอนในหัวข้อนี้ควรจะทำให้เสร็จโดยใช้ส่วนติดต่อเว็บของ Project Service Automation (PSA)</span><span class="sxs-lookup"><span data-stu-id="1a9dc-105">The procedures in this topic should be completed using the web interface of Project Service Automation (PSA).</span></span>

> [!IMPORTANT]
> <span data-ttu-id="1a9dc-106">เราขอแนะนำให้คุณทำการเปลี่ยนแปลงมิติการกำหนดราคาแบบกำหนดเองทั้งหมดในโซลูชันแยกต่างหาก</span><span class="sxs-lookup"><span data-stu-id="1a9dc-106">We recommend that you make all custom pricing dimension changes in a separate solution.</span></span> <span data-ttu-id="1a9dc-107">หลักปฏิบัติที่สำคัญที่สุดนี้ให้ความยืดหยุ่นสำหรับการปรับปรุง หรือลบการเปลี่ยนแปลงตามความจำเป็นในอนาคต จะช่วยให้มีการใช้นำงานของคุณกลับมาใช้อีกครััง และทำให้การส่งการเปลี่ยนแปลงเหล่านี้ไปยังอินสแตนซ์อื่นเป็นไปได้ง่ายกว่าเดิม</span><span class="sxs-lookup"><span data-stu-id="1a9dc-107">This important best practice provides flexibility in the future to update or remove changes as needed, will help with re-use of your work, and makes it easier to port these changes to another instance.</span></span> <span data-ttu-id="1a9dc-108">หลังจากที่คุณได้ทำการเปลี่ยนแปลงที่จำเป็นทั้งหมดแล้ว ส่งออกโซลูชันนี้เป็น **โซลูชันที่ถูกจัดการแล้ว** และนำเข้าไปยังอินสแตนซ์อื่น ๆ เพื่อนำการตั้งค่าการกำหนดราคาของคุณมาใช้ใหม่</span><span class="sxs-lookup"><span data-stu-id="1a9dc-108">After you have made all of the required changes, export this solution as a **Managed solution** and import it into other instances to reuse your pricing setup.</span></span>


## <a name="create-a-custom-solution-for-pricing-dimensions"></a><span data-ttu-id="1a9dc-109">สร้างโซลูชันแบบกำหนดเองสำหรับมิติการกำหนดราคา</span><span class="sxs-lookup"><span data-stu-id="1a9dc-109">Create a custom solution for pricing dimensions</span></span>
1. <span data-ttu-id="1a9dc-110">ใน PSA คลิก **ตั้งค่า** > **โซลูชัน** และจากนั้นคลิก **สร้าง** เพื่อสร้างโซลูชันใหม่</span><span class="sxs-lookup"><span data-stu-id="1a9dc-110">In PSA, click **Settings** > **Solutions**, and then click **New** to create a new solution.</span></span> 
2. <span data-ttu-id="1a9dc-111">ตั้งชื่อโซลูชันเป็น **\<องค์กรของคุณ > มิติการกำหนดราคา** ให้ป้อนข้อมูลจำเป็นที่เหลือแล้วคลิก **บันทึก**</span><span class="sxs-lookup"><span data-stu-id="1a9dc-111">Name the solution, **\<your organization name> pricing dimensions**, enter the remaining required information, and then click **Save**.</span></span>

> ![การสร้างโซลูชันแบบกำหนดเองสำหรับมิติการกำหนดราคา](media/Creation-of-custom-pricing-dimension-solution.PNG)
  
## <a name="create-custom-fields-and-option-sets-in-the-pricing-dimension-solution"></a><span data-ttu-id="1a9dc-113">สร้างฟิลด์ที่กำหนดเองและชุดตัวเลือกในโซลูชันมิติการกำหนดราคา</span><span class="sxs-lookup"><span data-stu-id="1a9dc-113">Create custom fields and option sets in the pricing dimension solution</span></span>

<span data-ttu-id="1a9dc-114">มิติการกำหนดราคาอาจเป็นชุดตัวเลือกหรือเอนทิตี</span><span class="sxs-lookup"><span data-stu-id="1a9dc-114">A pricing dimension can be an option set or an entity.</span></span> <span data-ttu-id="1a9dc-115">ทั้งสองต้องถูกสร้างขึ้นในโซลูชันการกำหนดราคาของคุณ</span><span class="sxs-lookup"><span data-stu-id="1a9dc-115">Both must be created in your pricing solution.</span></span> <span data-ttu-id="1a9dc-116">ขั้นตอนในกระบวนงานนี้อธิบายวิธีการสร้างมิติตามเอนทิตีและมิติตามชุดตัวเลือก</span><span class="sxs-lookup"><span data-stu-id="1a9dc-116">The steps in this procedure explain how to create entity-based dimensions and option set-based dimensions.</span></span>

### <a name="entity-based-dimensions"></a><span data-ttu-id="1a9dc-117">มิติตามเอนทิตี</span><span class="sxs-lookup"><span data-stu-id="1a9dc-117">Entity-based dimensions</span></span>

1. <span data-ttu-id="1a9dc-118">ใน PSA คลิก **การตั้งค่า** > **โซลูชัน** จากนั้นคลิกสองครั้งที่ **\<ชื่อองค์กรของคุณ > มิติการกำหนดราคา**</span><span class="sxs-lookup"><span data-stu-id="1a9dc-118">In PSA, click **Settings** > **Solutions**, and then double-click **\<your organization name> pricing dimensions**.</span></span>
2. <span data-ttu-id="1a9dc-119">ใน Solution Explorer บนบานหน้าต่างการนำทางด้านซ้าย เลือก **เอนทิตี**</span><span class="sxs-lookup"><span data-stu-id="1a9dc-119">In Solution Explorer, on the left navigation pane, select **Entities**.</span></span>
3. <span data-ttu-id="1a9dc-120">คลิก **สร้าง** เพื่อสร้างเอนทิตีใหม่ที่เรียกว่า **ชื่อมาตรฐาน**</span><span class="sxs-lookup"><span data-stu-id="1a9dc-120">Click **New** to create a new entity called **Standard Title**.</span></span> <span data-ttu-id="1a9dc-121">ป้อนข้อมูลที่จำเป็นให้ครบ จากนั้นคลิก **บันทึก**</span><span class="sxs-lookup"><span data-stu-id="1a9dc-121">Enter the remaining required information, and then click **Save**.</span></span>

> ![คำนิยามเอนทิตีชื่อมาตรฐาน](media/Standard-Title-entity-definition.png)


### <a name="option-set-based-dimensions"></a><span data-ttu-id="1a9dc-123">มิติตามชุดตัวเลือก</span><span class="sxs-lookup"><span data-stu-id="1a9dc-123">Option set-based dimensions</span></span> 
<span data-ttu-id="1a9dc-124">คุณสามารถสร้างสองมิติตามชุดตัวเลือก</span><span class="sxs-lookup"><span data-stu-id="1a9dc-124">You can create two option set-based dimensions.</span></span> <span data-ttu-id="1a9dc-125">ใช้ **สถานที่ทำงานของทรัพยากร** เพื่อติดตามราคาของงานทำที่ **บ้าน** และการทำงาน **นอกสถานที่** และใช้ **ชั่วโมงการทำงานของทรัพยากร** กับมูลค่า **ในเวลา** และ **ล่วงเวลา** เพื่อนำมาคิดราคาเพิ่มเมื่องานสำเร็จ</span><span class="sxs-lookup"><span data-stu-id="1a9dc-125">Use **Resource Work Location** to track the price of **Home** location work and **Onsite** work and use **Resource Work hours** with values **Regular** and **Overtime** to apply a markup when work is completed.</span></span>


1. <span data-ttu-id="1a9dc-126">ใน PSA คลิก **การตั้งค่า** > **โซลูชัน** จากนั้นคลิกสองครั้งที่ **\<ชื่อองค์กรของคุณ > มิติการกำหนดราคา**</span><span class="sxs-lookup"><span data-stu-id="1a9dc-126">In PSA, click **Settings** > **Solutions**, and then double-click  **\<your organization name> pricing dimensions**.</span></span> 
2. <span data-ttu-id="1a9dc-127">ใน Solution Explorer บนบานหน้าต่างการนำทางด้านซ้าย เลือก **ชุดตัวเลือก**</span><span class="sxs-lookup"><span data-stu-id="1a9dc-127">In Solution Explorer, on the left navigation pane, select  **Option Sets**.</span></span> 
3. <span data-ttu-id="1a9dc-128">คลิก **สร้าง** เพื่อสร้างชุดตัวเลือกใหม่ ป้อนข้อมูลที่จำเป็นให้ครบ และจากนั้นคลิก **บันทึก**</span><span class="sxs-lookup"><span data-stu-id="1a9dc-128">Click **New** to create a new option set, enter the remaining required information, and then click **Save**.</span></span>

> ![<span data-ttu-id="1a9dc-129">มิติการกำหนดราคาตามชุดตัวเลือกที่เรียกว่า สถานที่ทำงานของทรัพยากร</span><span class="sxs-lookup"><span data-stu-id="1a9dc-129">Option set based pricing dimension called Resource Work Location</span></span> ](media/Option-set-PD-called-Resource-Work-Location.png)

> ![<span data-ttu-id="1a9dc-130">มิติการกำหนดราคาตามชุดตัวเลือกที่เรียกว่า ชั่วโมงทำงานของทรัพยากร</span><span class="sxs-lookup"><span data-stu-id="1a9dc-130">Option set based pricing dimension called Resource Work Hours</span></span> ](media/Option-set-PD-called-Resource-Work-Hours.PNG)


## <a name="create-data-for-entity-based-dimensions"></a><span data-ttu-id="1a9dc-131">สร้างข้อมูลสำหรับมิติตามเอนทิตี้</span><span class="sxs-lookup"><span data-stu-id="1a9dc-131">Create data for entity-based dimensions</span></span>

<span data-ttu-id="1a9dc-132">คุณสามารถสร้างข้อมูลสำหรับมิติตามเอนทิตี้ด้วยตนเอง หรือโดยใช้การนำเข้าหรือเรียกใช้บริการ Microsoft Excel</span><span class="sxs-lookup"><span data-stu-id="1a9dc-132">You can create data for entity-based dimensions manually, or by using Microsoft Excel import or service calls.</span></span> <span data-ttu-id="1a9dc-133">ใช้ขั้นตอนในกระบวนงานนี้สร้างสองชื่อมาตรฐาน ได้แก่ **วิศวกรระบบ** และ **วิศวกรระบบอาวุโส** จากมิติตามเอนทิตี **ชื่อมาตรฐาน**</span><span class="sxs-lookup"><span data-stu-id="1a9dc-133">Use the steps in this procedure to create two standard titles, **Systems Engineer** and **Senior Systems Engineer** from the entity-based dimension, **Standard Title**.</span></span> <span data-ttu-id="1a9dc-134">ถ้าข้อมูลที่คุณต้องการสร้างมีขนาดเล็ก ดังในตัวอย่างต่อไปนี้ คุณสามารถใช้ฟอร์มมาตรฐาน</span><span class="sxs-lookup"><span data-stu-id="1a9dc-134">If the data that you want to create is small, as in the following example, you can use a standard form.</span></span>

1. <span data-ttu-id="1a9dc-135">ใน PSA คลิก **การค้นหาขั้นสูง**</span><span class="sxs-lookup"><span data-stu-id="1a9dc-135">In PSA, click **Advanced Find**.</span></span> <span data-ttu-id="1a9dc-136">เลือกเอนทิตี **ชื่อมาตรฐาน** จากนั้นคลิก **ผลลัพธ์**</span><span class="sxs-lookup"><span data-stu-id="1a9dc-136">Select the entity **Standard Title** and then click **Results**.</span></span> <span data-ttu-id="1a9dc-137">แถวทั้งหมดในเอนทิตี **ชื่อมาตรฐาน** จะแสดงขึ้น</span><span class="sxs-lookup"><span data-stu-id="1a9dc-137">All of the rows in the **Standard Title** entity will be shown.</span></span>
2. <span data-ttu-id="1a9dc-138">คลิก **สร้าง**</span><span class="sxs-lookup"><span data-stu-id="1a9dc-138">Click **New**.</span></span> <span data-ttu-id="1a9dc-139">ในฟิลด์ **ชื่อ** ให้ป้อน "Systems Engineer" แล้วคลิก **บันทึก**</span><span class="sxs-lookup"><span data-stu-id="1a9dc-139">In the **Name** field, enter "Systems Engineer" and then click **Save**.</span></span>
3. <span data-ttu-id="1a9dc-140">ปิดฟอร์ม</span><span class="sxs-lookup"><span data-stu-id="1a9dc-140">Close the form.</span></span> 
4. <span data-ttu-id="1a9dc-141">ทำซ้ำขั้นตอนที่ 1-3 เพื่อสร้างชื่อมาตรฐานอื่นสำหรับ "Senior Systems Engineer"</span><span class="sxs-lookup"><span data-stu-id="1a9dc-141">Repeat steps 1 - 3 to create another standard title for "Senior Systems Engineer".</span></span>

> ![<span data-ttu-id="1a9dc-142">ข้อมูลตัวอย่างสำหรับเอนทิตีชื่อมาตรฐาน</span><span class="sxs-lookup"><span data-stu-id="1a9dc-142">Sample Data for Standard Title entity</span></span> ](media/ST-data.png)

## <a name="add-all-required-psa-entities-and-related-components-to-the-pricing-dimension-solution"></a><span data-ttu-id="1a9dc-143">เพิ่มเอนทิตี PSA ที่จำเป็นทั้งหมด และส่วนประกอบที่เกี่ยวข้องกับโซลูชันมิติการกำหนดราคา</span><span class="sxs-lookup"><span data-stu-id="1a9dc-143">Add all required PSA entities and related components to the Pricing Dimension Solution</span></span>
<span data-ttu-id="1a9dc-144">คุณจะต้องเพิ่มเอนทิตี Project Service ต่อไปนี้ลงในโซลูชันการกำหนดราคาของคุณ</span><span class="sxs-lookup"><span data-stu-id="1a9dc-144">You will need to add the following Project Service entities to your pricing solution.</span></span> <span data-ttu-id="1a9dc-145">ใช้ขั้นตอนในกระบวนงานนี้เพื่อทำการเปลี่ยนแปลง Schema ที่สำคัญบางอย่างในโซลูชันการกำหนดราคา เพื่อให้เอนทิตีตระหนักถึงมิติการกำหนดราคาใหม่</span><span class="sxs-lookup"><span data-stu-id="1a9dc-145">Use the steps in this procedure to make some important schema changes in the pricing solution so that the entities become aware of the new pricing dimensions.</span></span>

1. <span data-ttu-id="1a9dc-146">ใน PSA คลิก **การตั้งค่า** > **โซลูชัน** จากนั้นคลิกสองครั้งที่ **\<ชื่อองค์กรของคุณ > มิติการกำหนดราคา**</span><span class="sxs-lookup"><span data-stu-id="1a9dc-146">In PSA, click **Settings** > **Solutions**, and then double-click **\<your organization name> pricing dimensions**.</span></span> 
2. <span data-ttu-id="1a9dc-147">ใน Solution Explorer บนบานหน้าต่างการนำทางด้านซ้าย เลือก **เพิ่มสิ่งที่มีอยู่** > **เอนทิตี**</span><span class="sxs-lookup"><span data-stu-id="1a9dc-147">In Solution Explorer, on the left navigation pane, select **Add Existing** > **Entities**.</span></span>
3. <span data-ttu-id="1a9dc-148">ในกล่องโต้ตอบ **ส่วนประกอบโซลูชัน** เลือกเอนทิตีดังต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="1a9dc-148">In the **Solution Components** dialog box, select the following entities:</span></span>

- <span data-ttu-id="1a9dc-149">ตามจริง</span><span class="sxs-lookup"><span data-stu-id="1a9dc-149">Actual</span></span>
- <span data-ttu-id="1a9dc-150">ทรัพยากรที่สามารถจองได้</span><span class="sxs-lookup"><span data-stu-id="1a9dc-150">Bookable Resource</span></span>
- <span data-ttu-id="1a9dc-151">บรรทัดการประมาณการ</span><span class="sxs-lookup"><span data-stu-id="1a9dc-151">Estimate Line</span></span>
- <span data-ttu-id="1a9dc-152">รายละเอียดรายการใบแจ้งหนี้</span><span class="sxs-lookup"><span data-stu-id="1a9dc-152">Invoice Line Detail</span></span>
- <span data-ttu-id="1a9dc-153">บรรทัดสมุดรายวัน</span><span class="sxs-lookup"><span data-stu-id="1a9dc-153">Journal Line</span></span>
- <span data-ttu-id="1a9dc-154">รายละเอียดการให้บริการตามสัญญาโครงการ</span><span class="sxs-lookup"><span data-stu-id="1a9dc-154">Project Contract Line Detail</span></span>
- <span data-ttu-id="1a9dc-155">สมาชิกของทีมโครงการ</span><span class="sxs-lookup"><span data-stu-id="1a9dc-155">Project Team Member</span></span>
- <span data-ttu-id="1a9dc-156">รายละเอียดรายการใบเสนอราคา</span><span class="sxs-lookup"><span data-stu-id="1a9dc-156">Quote Line Detail</span></span>
- <span data-ttu-id="1a9dc-157">ส่วนเพิ่มราคาของราคาตามบทบาท</span><span class="sxs-lookup"><span data-stu-id="1a9dc-157">Role Price Markup</span></span>
- <span data-ttu-id="1a9dc-158">ราคาตามบทบาท</span><span class="sxs-lookup"><span data-stu-id="1a9dc-158">Role Price</span></span> 
- <span data-ttu-id="1a9dc-159">รายการเวลา</span><span class="sxs-lookup"><span data-stu-id="1a9dc-159">Time Entry</span></span> 

> ![เพิ่มเอนทิตีที่มีอยู่ไปยังโซลูชันมิติการกำหนดราคา](media/Existing-entities-to-PD-solution.png)

> ![เลือกส่วนประกอบของโซลูชัน](media/Dimension-Components.png)

> [!NOTE]
> <span data-ttu-id="1a9dc-162">ตรวจสอบให้แน่ใจว่าได้รวมฟอร์มและมุมมองทั้งหมดสำหรับแต่ละเอนทิตีที่ถูกเลือก</span><span class="sxs-lookup"><span data-stu-id="1a9dc-162">Make sure to include all forms and views for each of the entities selected.</span></span>

4. <span data-ttu-id="1a9dc-163">เมื่อถูกพร้อมท์ให้รวมเอนทิตีที่ไม่เป็นอิสระใด ๆ เข้ากับเอนทิตีที่เลือกไว้ข้างต้น คลิก **ไม่**</span><span class="sxs-lookup"><span data-stu-id="1a9dc-163">When prompted to include any dependent entities for the entities selected above, click **No**.</span></span>

> ![ไม่รวมถึงส่วนประกอบที่เกี่ยวข้องทั้งหมด](media/Do-not-include-required.png)


