---
title: สร้างฟิลด์และเอนทิตีแบบกำหนดเองเป็นมิติการกำหนดราคา
description: หัวข้อนี้ให้ข้อมูลเกี่ยวกับวิธีสร้างชุดตัวเลือกหรือเอนทิตีแบบกำหนดเอง
author: rumant
manager: AnnBe
ms.date: 09/18/2020
ms.topic: article
ms.prod: ''
ms.service: project-operations
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: suvaidya
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: 616bcd5758b434b45bd06aa1a026f32efc8b7f99
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 10/28/2020
ms.locfileid: "4130916"
---
# <a name="create-custom-fields-and-entities-as-pricing-dimensions"></a><span data-ttu-id="d9560-103">สร้างฟิลด์และเอนทิตีแบบกำหนดเองเป็นมิติการกำหนดราคา</span><span class="sxs-lookup"><span data-stu-id="d9560-103">Create custom fields and entities as pricing dimensions</span></span>

<span data-ttu-id="d9560-104">_**นำไปใช้กับ:** Project Operations สำหรับสถานการณ์ที่อิงตามทรัพยากร/ที่ไม่ได้เก็บในสต็อก การปรับใช้ Lite - จัดการกับการออกใบแจ้งหนี้ชั่วคราว_</span><span class="sxs-lookup"><span data-stu-id="d9560-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="d9560-105">ทำตามขั้นตอนต่อไปนี้ทุกครั้งที่คุณต้องการสร้างชุดตัวเลือกหรือเอนทิตีแบบกำหนดเอง</span><span class="sxs-lookup"><span data-stu-id="d9560-105">Complete the following steps any time that you want to create a custom option set or entity.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="d9560-106">เราขอแนะนำให้คุณทำการเปลี่ยนแปลงมิติการกำหนดราคาแบบกำหนดเองทั้งหมดในโซลูชันแยกต่างหาก</span><span class="sxs-lookup"><span data-stu-id="d9560-106">We recommend that you make all custom pricing dimension changes in a separate solution.</span></span> <span data-ttu-id="d9560-107">หลักปฏิบัติที่สำคัญที่สุดนี้ให้ความยืดหยุ่นสำหรับการปรับปรุง หรือลบการเปลี่ยนแปลงตามความจำเป็นในอนาคต จะช่วยให้มีการใช้นำงานของคุณกลับมาใช้อีกครััง และทำให้การส่งการเปลี่ยนแปลงเหล่านี้ไปยังอินสแตนซ์อื่นเป็นไปได้ง่ายกว่าเดิม</span><span class="sxs-lookup"><span data-stu-id="d9560-107">This important best practice provides flexibility in the future to update or remove changes as needed, will help with re-use of your work, and makes it easier to port these changes to another instance.</span></span> <span data-ttu-id="d9560-108">หลังจากที่คุณได้ทำการเปลี่ยนแปลงที่จำเป็นทั้งหมดแล้ว ส่งออกโซลูชันนี้เป็น **โซลูชันที่ถูกจัดการแล้ว** และนำเข้าไปยังอินสแตนซ์อื่น ๆ เพื่อนำการตั้งค่าการกำหนดราคาของคุณมาใช้ใหม่</span><span class="sxs-lookup"><span data-stu-id="d9560-108">After you have made all of the required changes, export this solution as a **Managed solution** and import it into other instances to reuse your pricing setup.</span></span>


## <a name="create-a-custom-solution-for-pricing-dimensions"></a><span data-ttu-id="d9560-109">สร้างโซลูชันแบบกำหนดเองสำหรับมิติการกำหนดราคา</span><span class="sxs-lookup"><span data-stu-id="d9560-109">Create a custom solution for pricing dimensions</span></span>
1. <span data-ttu-id="d9560-110">ไปที่ **การตั้งค่า** > **โซลูชัน** และจากนั้นเลือก **สร้าง** เพื่อสร้างโซลูชันใหม่</span><span class="sxs-lookup"><span data-stu-id="d9560-110">Go to **Settings** > **Solutions**, and then select **New** to create a new solution.</span></span> 
2. <span data-ttu-id="d9560-111">ตั้งชื่อโซลูชันเป็น **มิติการกำหนดราคาของ \<your organization name>** ให้ป้อนข้อมูลจำเป็นที่เหลือ แล้วเลือก **บันทึก**</span><span class="sxs-lookup"><span data-stu-id="d9560-111">Name the solution, **\<your organization name> pricing dimensions**, enter the remaining required information, and then select **Save**.</span></span>
  
## <a name="create-custom-fields-and-option-sets-in-the-pricing-dimension-solution"></a><span data-ttu-id="d9560-112">สร้างฟิลด์ที่กำหนดเองและชุดตัวเลือกในโซลูชันมิติการกำหนดราคา</span><span class="sxs-lookup"><span data-stu-id="d9560-112">Create custom fields and option sets in the pricing dimension solution</span></span>

<span data-ttu-id="d9560-113">มิติการกำหนดราคาอาจเป็นชุดตัวเลือกหรือเอนทิตี</span><span class="sxs-lookup"><span data-stu-id="d9560-113">A pricing dimension can be an option set or an entity.</span></span> <span data-ttu-id="d9560-114">ทั้งสองต้องถูกสร้างขึ้นในโซลูชันการกำหนดราคาของคุณ</span><span class="sxs-lookup"><span data-stu-id="d9560-114">Both must be created in your pricing solution.</span></span> <span data-ttu-id="d9560-115">ขั้นตอนในกระบวนงานนี้อธิบายวิธีการสร้างมิติตามเอนทิตีและมิติตามชุดตัวเลือก</span><span class="sxs-lookup"><span data-stu-id="d9560-115">The steps in this procedure explain how to create entity-based dimensions and option set-based dimensions.</span></span>

### <a name="entity-based-dimensions"></a><span data-ttu-id="d9560-116">มิติตามเอนทิตี</span><span class="sxs-lookup"><span data-stu-id="d9560-116">Entity-based dimensions</span></span>

1. <span data-ttu-id="d9560-117">ไปที่ **การตั้งค่า** > **โซลูชัน** แล้วดับเบิลคลิก **มิติการกำหนดราคาของ \<your organization name>**</span><span class="sxs-lookup"><span data-stu-id="d9560-117">Go to **Settings** > **Solutions**, and then double-click **\<your organization name> pricing dimensions**.</span></span>
2. <span data-ttu-id="d9560-118">ใน Solution Explorer บนบานหน้าต่างการนำทางด้านซ้าย เลือก **เอนทิตี**</span><span class="sxs-lookup"><span data-stu-id="d9560-118">In Solution Explorer, on the left navigation pane, select **Entities**.</span></span>
3. <span data-ttu-id="d9560-119">เลือก **สร้าง** เพื่อสร้างเอนทิตีใหม่ที่เรียกว่า **ชื่อมาตรฐาน**</span><span class="sxs-lookup"><span data-stu-id="d9560-119">Select **New** to create a new entity called **Standard Title**.</span></span> 
4. <span data-ttu-id="d9560-120">ป้อนข้อมูลที่จำเป็นให้ครบ จากนั้นเลือก **บันทึก**</span><span class="sxs-lookup"><span data-stu-id="d9560-120">Enter the remaining required information, and then select **Save**.</span></span>


### <a name="option-set-based-dimensions"></a><span data-ttu-id="d9560-121">มิติตามชุดตัวเลือก</span><span class="sxs-lookup"><span data-stu-id="d9560-121">Option set-based dimensions</span></span> 
<span data-ttu-id="d9560-122">คุณสามารถสร้างสองมิติตามชุดตัวเลือก</span><span class="sxs-lookup"><span data-stu-id="d9560-122">You can create two option set-based dimensions.</span></span> <span data-ttu-id="d9560-123">ใช้ **สถานที่ทำงานของทรัพยากร** เพื่อติดตามราคาของงานทำที่ **บ้าน** และการทำงาน **นอกสถานที่** และใช้ **ชั่วโมงการทำงานของทรัพยากร** กับมูลค่า **ในเวลา** และ **ล่วงเวลา** เพื่อนำมาคิดราคาเพิ่มเมื่องานสำเร็จ</span><span class="sxs-lookup"><span data-stu-id="d9560-123">Use **Resource Work Location** to track the price of **Home** location work and **Onsite** work and use **Resource Work hours** with values **Regular** and **Overtime** to apply a markup when work is completed.</span></span>


1. <span data-ttu-id="d9560-124">ไปที่ **การตั้งค่า** > **โซลูชัน** และดับเบิลคลิก **มิติการกำหนดราคาของ \<your organization name>**</span><span class="sxs-lookup"><span data-stu-id="d9560-124">Go to **Settings** > **Solutions**, and double-click  **\<your organization name> pricing dimensions**.</span></span> 
2. <span data-ttu-id="d9560-125">ใน Solution Explorer บนบานหน้าต่างการนำทางด้านซ้าย เลือก **ชุดตัวเลือก**</span><span class="sxs-lookup"><span data-stu-id="d9560-125">In Solution Explorer, on the left navigation pane, select  **Option Sets**.</span></span> 
3. <span data-ttu-id="d9560-126">เลือก **สร้าง** เพื่อสร้างชุดตัวเลือกใหม่ ป้อนข้อมูลที่จำเป็นให้ครบ และจากนั้นเลือก **บันทึก**</span><span class="sxs-lookup"><span data-stu-id="d9560-126">Select **New** to create a new option set, enter the remaining required information, and then select **Save**.</span></span>

## <a name="create-data-for-entity-based-dimensions"></a><span data-ttu-id="d9560-127">สร้างข้อมูลสำหรับมิติตามเอนทิตี้</span><span class="sxs-lookup"><span data-stu-id="d9560-127">Create data for entity-based dimensions</span></span>

<span data-ttu-id="d9560-128">คุณสามารถสร้างข้อมูลสำหรับมิติตามเอนทิตี้ด้วยตนเอง หรือโดยใช้การนำเข้าหรือเรียกใช้บริการ Microsoft Excel</span><span class="sxs-lookup"><span data-stu-id="d9560-128">You can create data for entity-based dimensions manually, or by using Microsoft Excel import or service calls.</span></span> <span data-ttu-id="d9560-129">ใช้ขั้นตอนในกระบวนงานนี้สร้างสองชื่อมาตรฐาน ได้แก่ **วิศวกรระบบ** และ **วิศวกรระบบอาวุโส** จากมิติตามเอนทิตี **ชื่อมาตรฐาน**</span><span class="sxs-lookup"><span data-stu-id="d9560-129">Use the steps in this procedure to create two standard titles, **Systems Engineer** and **Senior Systems Engineer** from the entity-based dimension, **Standard Title**.</span></span> <span data-ttu-id="d9560-130">ถ้าข้อมูลที่คุณต้องการสร้างมีขนาดเล็ก ดังในตัวอย่างต่อไปนี้ คุณสามารถใช้ฟอร์มมาตรฐาน</span><span class="sxs-lookup"><span data-stu-id="d9560-130">If the data that you want to create is small, as in the following example, you can use a standard form.</span></span>

1. <span data-ttu-id="d9560-131">เลือก **การค้นหาขั้นสูง** เลือกเอนทิตี **ชื่อมาตรฐาน** แล้วเลือก **ผลลัพธ์**</span><span class="sxs-lookup"><span data-stu-id="d9560-131">Select **Advanced Find**, select the entity **Standard Title**, and then select **Results**.</span></span> <span data-ttu-id="d9560-132">แถวทั้งหมดในเอนทิตี **ชื่อมาตรฐาน** จะแสดงขึ้น</span><span class="sxs-lookup"><span data-stu-id="d9560-132">All of the rows in the **Standard Title** entity will be shown.</span></span>
2. <span data-ttu-id="d9560-133">เลือก **ใหม่** จากนั้นในฟิลด์ **ชื่อ** ให้ป้อน "วิศวกรระบบ" แล้วเลือก **บันทึก**</span><span class="sxs-lookup"><span data-stu-id="d9560-133">Select **New**, and in the **Name** field, enter "Systems Engineer" and then select **Save**.</span></span>
3. <span data-ttu-id="d9560-134">ปิดฟอร์ม</span><span class="sxs-lookup"><span data-stu-id="d9560-134">Close the form.</span></span> 
4. <span data-ttu-id="d9560-135">ทำซ้ำขั้นตอนที่ 1-3 เพื่อสร้างชื่อมาตรฐานอื่นสำหรับ "Senior Systems Engineer"</span><span class="sxs-lookup"><span data-stu-id="d9560-135">Repeat steps 1 - 3 to create another standard title for "Senior Systems Engineer".</span></span>

## <a name="add-all-required-entities-and-related-components-to-the-pricing-dimension-solution"></a><span data-ttu-id="d9560-136">เพิ่มเอนทิตีที่จำเป็นทั้งหมด และส่วนประกอบที่เกี่ยวข้องกับโซลูชันมิติการกำหนดราคา</span><span class="sxs-lookup"><span data-stu-id="d9560-136">Add all required entities and related components to the Pricing Dimension Solution</span></span>
<span data-ttu-id="d9560-137">คุณจะต้องเพิ่มเอนทิตีต่อไปนี้ลงในโซลูชันการกำหนดราคาของคุณ</span><span class="sxs-lookup"><span data-stu-id="d9560-137">You will need to add the following entities to your pricing solution.</span></span> <span data-ttu-id="d9560-138">ใช้ขั้นตอนในกระบวนงานนี้เพื่อทำการเปลี่ยนแปลง Schema ที่สำคัญบางอย่างในโซลูชันการกำหนดราคา เพื่อให้เอนทิตีตระหนักถึงมิติการกำหนดราคาใหม่</span><span class="sxs-lookup"><span data-stu-id="d9560-138">Use the steps in this procedure to make some important schema changes in the pricing solution so that the entities become aware of the new pricing dimensions.</span></span>

1. <span data-ttu-id="d9560-139">เลือก **การตั้งค่า** > **โซลูชัน** และดับเบิลคลิก **มิติการกำหนดราคาของ \<your organization name>**</span><span class="sxs-lookup"><span data-stu-id="d9560-139">Select **Settings** > **Solutions**, and double-click **\<your organization name> pricing dimensions**.</span></span> 
2. <span data-ttu-id="d9560-140">ใน Solution Explorer บนบานหน้าต่างการนำทางด้านซ้าย เลือก **เพิ่มสิ่งที่มีอยู่** > **เอนทิตี**</span><span class="sxs-lookup"><span data-stu-id="d9560-140">In Solution Explorer, on the left navigation pane, select **Add Existing** > **Entities**.</span></span>
3. <span data-ttu-id="d9560-141">ในกล่องโต้ตอบ **ส่วนประกอบโซลูชัน** เลือกเอนทิตีดังต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="d9560-141">In the **Solution Components** dialog box, select the following entities:</span></span>

  - <span data-ttu-id="d9560-142">ตามจริง</span><span class="sxs-lookup"><span data-stu-id="d9560-142">Actual</span></span>
  - <span data-ttu-id="d9560-143">ทรัพยากรที่สามารถจองได้</span><span class="sxs-lookup"><span data-stu-id="d9560-143">Bookable Resource</span></span>
  - <span data-ttu-id="d9560-144">รายการการประมาณการ</span><span class="sxs-lookup"><span data-stu-id="d9560-144">Estimate Line</span></span>
  - <span data-ttu-id="d9560-145">รายละเอียดรายการใบแจ้งหนี้</span><span class="sxs-lookup"><span data-stu-id="d9560-145">Invoice Line Detail</span></span>
  - <span data-ttu-id="d9560-146">รายการสมุดรายวัน</span><span class="sxs-lookup"><span data-stu-id="d9560-146">Journal Line</span></span>
  - <span data-ttu-id="d9560-147">รายละเอียดการให้บริการตามสัญญาโครงการ</span><span class="sxs-lookup"><span data-stu-id="d9560-147">Project Contract Line Detail</span></span>
  - <span data-ttu-id="d9560-148">สมาชิกของทีมโครงการ</span><span class="sxs-lookup"><span data-stu-id="d9560-148">Project Team Member</span></span>
  - <span data-ttu-id="d9560-149">รายละเอียดรายการใบเสนอราคา</span><span class="sxs-lookup"><span data-stu-id="d9560-149">Quote Line Detail</span></span>
  - <span data-ttu-id="d9560-150">ส่วนเพิ่มราคาของราคาตามบทบาท</span><span class="sxs-lookup"><span data-stu-id="d9560-150">Role Price Markup</span></span>
  - <span data-ttu-id="d9560-151">ราคาตามบทบาท</span><span class="sxs-lookup"><span data-stu-id="d9560-151">Role Price</span></span> 
  - <span data-ttu-id="d9560-152">รายการเวลา</span><span class="sxs-lookup"><span data-stu-id="d9560-152">Time Entry</span></span> 


> [!NOTE]
> <span data-ttu-id="d9560-153">ตรวจสอบให้แน่ใจว่าได้รวมฟอร์มและมุมมองทั้งหมดสำหรับแต่ละเอนทิตีที่ถูกเลือก</span><span class="sxs-lookup"><span data-stu-id="d9560-153">Make sure to include all forms and views for each of the entities selected.</span></span>

4. <span data-ttu-id="d9560-154">เมื่อถูกพร้อมท์ให้รวมเอนทิตีที่ไม่เป็นอิสระใด ๆ เข้ากับเอนทิตีที่เลือกไว้ข้างต้น เลือก **ไม่**</span><span class="sxs-lookup"><span data-stu-id="d9560-154">When prompted to include any dependent entities for the entities selected above, select **No**.</span></span>

