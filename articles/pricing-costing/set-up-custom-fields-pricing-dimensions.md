---
title: ตั้งค่าฟิลด์ที่กำหนดเองเป็นมิติการกำหนดราคา
description: หัวข้อนี้ให้ข้อมูลเกี่ยวกับวิธีการตั้งค่ามิติการกำหนดราคาโดยใช้ฟิลด์แบบกำหนดเอง
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
ms.author: rumant
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: 1468c3396a01c1bee1bc0f47eac1ee8b44eaa459
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 02/15/2021
ms.locfileid: "5274886"
---
# <a name="set-up-custom-fields-as-pricing-dimensions"></a><span data-ttu-id="a62b5-103">ตั้งค่าฟิลด์ที่กำหนดเองเป็นมิติการกำหนดราคา</span><span class="sxs-lookup"><span data-stu-id="a62b5-103">Set up custom fields as pricing dimensions</span></span>

<span data-ttu-id="a62b5-104">_**นำไปใช้กับ:** Project Operations สำหรับสถานการณ์ที่อิงตามทรัพยากร/ที่ไม่ได้เก็บในสต็อก การปรับใช้ Lite - จัดการกับการออกใบแจ้งหนี้ชั่วคราว_</span><span class="sxs-lookup"><span data-stu-id="a62b5-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="a62b5-105">ก่อนที่คุณจะเริ่ม หัวข้อนี้สมมติว่าคุณได้ทำตามขั้นตอนในหัวข้อ [สร้างฟิลด์และเอนทิตี้แบบกำหนดเอง](create-custom-fields-entities-pricing-dimensions.md) และ [เพิ่มฟิลด์แบบกำหนดเองที่ต้องการให้การตั้งค่าราคาและเอนทิตีทางธุรกรรม](add-custom-fields-price-setup-transactional-entities.md) แล้ว</span><span class="sxs-lookup"><span data-stu-id="a62b5-105">Before you begin, this topic assumes that you have completed the procedures in the topics, [Create custom fields and entities](create-custom-fields-entities-pricing-dimensions.md) and [Add required custom fields to price setup and transactional entities](add-custom-fields-price-setup-transactional-entities.md).</span></span> <span data-ttu-id="a62b5-106">ถ้าคุณยังไม่ได้ดำเนินการตามขั้นตอนเหล่านั้น ให้ย้อนกลับและทำให้เสร็จสมบูรณ์แล้วกลับมายังหัวข้อนี้</span><span class="sxs-lookup"><span data-stu-id="a62b5-106">If you haven't completed those procedures, go back and complete them and then return to this topic.</span></span> 

<span data-ttu-id="a62b5-107">หัวข้อนี้แสดงข้อมูลเกี่ยวกับการตั้งค่ามิติการกำหนดราคาแบบกำหนดเอง</span><span class="sxs-lookup"><span data-stu-id="a62b5-107">This topic provides information about setting up custom pricing dimensions.</span></span> <span data-ttu-id="a62b5-108">บนเพจ **พารามิเตอร์** แท็บ **มิติการกำหนดราคาตามจำนวนเงิน** แสดงเรกคอร์ดในเอนทิตีมิติการกำหนดราคา</span><span class="sxs-lookup"><span data-stu-id="a62b5-108">On the **Parameters** page, the **Amount-Based Pricing Dimensions** tab shows the records in the pricing dimension entities.</span></span> <span data-ttu-id="a62b5-109">ตามค่าเริ่มต้น มีสองแถวในตารางบนแท็บนี้:</span><span class="sxs-lookup"><span data-stu-id="a62b5-109">By default, there are two rows in the grid on this tab:</span></span>

- <span data-ttu-id="a62b5-110">**msdyn_resourcecategory** (บทบาท)</span><span class="sxs-lookup"><span data-stu-id="a62b5-110">**msdyn_resourcecategory** (Role)</span></span>
- <span data-ttu-id="a62b5-111">**msdyn_OrganizationalUnit** (หน่วยองค์กร)</span><span class="sxs-lookup"><span data-stu-id="a62b5-111">**msdyn_OrganizationalUnit** (Organizational Unit)</span></span>

> [!IMPORTANT]
> <span data-ttu-id="a62b5-112">ห้ามลบแถวเหล่านี้</span><span class="sxs-lookup"><span data-stu-id="a62b5-112">Do not delete these rows.</span></span> <span data-ttu-id="a62b5-113">อย่างไรก็ตาม หากคุณไม่ต้องการ คุณสามารถไม่ใช้งานกับบริบทที่ระบุได้โดยการตั้งค่า **สามารถใช้งานได้กับต้นทุน** **สามารใช้งานได้กับการขาย** และ **สามารถใช้งานได้กับการซื้อ** เป็น **ไม่** ทั้งหมด</span><span class="sxs-lookup"><span data-stu-id="a62b5-113">However, if you do not need them, you can make them not applicable in a specific context by setting **Applicable to Cost**, **Applicable to Sales**, and **Applicable to Purchase** all to **No**.</span></span> <span data-ttu-id="a62b5-114">การตั้งค่าแอตทริเหล่านี้เป็น **ไม่** ส่งผลกระทบเหมือนกันกับการไม่ให้ฟิลด์มีฐานะเป็นมิติการกำหนดราคา</span><span class="sxs-lookup"><span data-stu-id="a62b5-114">Setting these attribute values to **No** has the same effect of not having the field as a pricing dimension.</span></span>

<span data-ttu-id="a62b5-115">สำหรับฟิลด์ที่จะเป็นมิติการกำหนดราคา จะต้อง:</span><span class="sxs-lookup"><span data-stu-id="a62b5-115">For a field to become a pricing dimension, it must be:</span></span>

- <span data-ttu-id="a62b5-116">สร้างเป็นฟิลด์ในเอนทิตี้ **ราคาตามบททบาท** และ **ส่วนเพิ่มราคาตามบทบาท**</span><span class="sxs-lookup"><span data-stu-id="a62b5-116">Created as a field in the **Role Price** and **Role Price markup** entities.</span></span> <span data-ttu-id="a62b5-117">สำหรับข้อมูลเพิ่มเติมเกี่ยวกับวิธีการทำเช่นนี้ ดูที่ [การเพิ่มฟิลด์ที่กำหนดเองสำหรับการตั้งค่าราคาและเอนทิตี้ทางธุรกรรม](add-custom-fields-price-setup-transactional-entities.md)</span><span class="sxs-lookup"><span data-stu-id="a62b5-117">For more information on how to do this, see [Add custom fields to price setup and transactional entities](add-custom-fields-price-setup-transactional-entities.md).</span></span>

- <span data-ttu-id="a62b5-118">สร้างเป็นแถวใน **มิติการกำหนดราคา**</span><span class="sxs-lookup"><span data-stu-id="a62b5-118">Created as a row in the **Pricing Dimension** table.</span></span> <span data-ttu-id="a62b5-119">ตัวอย่างเช่น เพิ่มแถวมิติการกำหนดราคาตามที่แสดงในรูปภาพต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="a62b5-119">For example, add pricing dimension rows as shown in the following graphic.</span></span> 

![จำนวนเงิน - อิงตามแถวมิติการกำหนดราคา](media/Amt-based-PD.png)

<span data-ttu-id="a62b5-121">ชั่วโมงทำงานของทรัพยากร (**msdyn_resourceworkhours**) มีการเพิ่มเป็นมิติตามส่วนเพิ่มราคาและเพิ่มไปยังตารางในแท็บ **มิติการกำหนดราคาตามส่วนเพิ่มราคา**</span><span class="sxs-lookup"><span data-stu-id="a62b5-121">Resource Work hours (**msdyn_resourceworkhours**) is added as a markup-based dimension and has been added to the grid on the **Markup Based Pricing Dimension** tab.</span></span>

![ส่วนเพิ่มราคา - อิงตามแถวมิติ](media/Markup-based-PD.png)


> [!IMPORTANT]
> <span data-ttu-id="a62b5-123">การเปลี่ยนแปลงใดๆ กับข้อมูลมิติการกำหนดราคาในตารางนี้ ที่มีอยู่หรืออันใหม่ จะถูกเผยแพร่ไปยังตรรกะทางธุรกิจของการกำหนดราคาหลังจากที่แคชถูกรีเฟรชเท่านั้น</span><span class="sxs-lookup"><span data-stu-id="a62b5-123">Any change to pricing dimension data in this table, existing or new, is propagated to the pricing business logic only after the cache is refreshed.</span></span> <span data-ttu-id="a62b5-124">การรีเฟรชแคชอาจใช้เวลาถึง 10 นาที</span><span class="sxs-lookup"><span data-stu-id="a62b5-124">The cache refresh time may take up to 10 minutes.</span></span> <span data-ttu-id="a62b5-125">อนุญาตให้ดำเนินการตามระยะเวลานั้นเพื่อให้เห็นการเปลี่ยนแปลงของตรรกะเริ่มต้นของการกำหนดราคาที่มีผลจากการเปลี่ยนแปลงไปยังข้อมูลมิติการกำหนดราคา</span><span class="sxs-lookup"><span data-stu-id="a62b5-125">Allow that length of time to see the changes in price defaulting logic that must result from changes to the Pricing Dimension data.</span></span>


## <a name="attributes-of-the-pricing-dimensions-table"></a><span data-ttu-id="a62b5-126">แอททริบิวต์ของตารางมิติการกำหนดราคา</span><span class="sxs-lookup"><span data-stu-id="a62b5-126">Attributes of the Pricing Dimensions table</span></span>
<span data-ttu-id="a62b5-127">ส่วนต่อไปนี้แสดงข้อมูลเกี่ยวกับแอททริบิวต์ต่างๆ ในตาราง **มิติการกำหนดราคา**</span><span class="sxs-lookup"><span data-stu-id="a62b5-127">The following sections provide information about the different attributes in the **Pricing Dimensions** table.</span></span>

### <a name="pricing-dimension-name"></a><span data-ttu-id="a62b5-128">ชื่อของมิริการกำหนดราคา</span><span class="sxs-lookup"><span data-stu-id="a62b5-128">Pricing Dimension Name</span></span>
<span data-ttu-id="a62b5-129">ค่านี้ควรจะตรงกันกับชื่อของ Schema ในฟิลด์ที่เพิ่มลงในตาราง **ราคาตามบทบาท** สำหรับมิติการกำหนดราคาแบบกำหนดเอง</span><span class="sxs-lookup"><span data-stu-id="a62b5-129">This value should be the exact same as the schema name of the field that is added to the **Role Price** table for custom pricing dimensions.</span></span> <span data-ttu-id="a62b5-130">สำหรับข้อมูลเพิ่มเติมเกี่ยวกับการเพิ่มฟิลด์ไปยังตาราง **ราคาตามบทบาท** ดูที่ [เพิ่มฟิลด์ที่กำหนดเองไปยังการตั้งค่าราคาและเอนทิตี้ทางธุรกรรม](add-custom-fields-price-setup-transactional-entities.md)</span><span class="sxs-lookup"><span data-stu-id="a62b5-130">For more information about adding fields to the **Role Price** table, see [Add custom fields to price setup and transactional entities](add-custom-fields-price-setup-transactional-entities.md).</span></span>

### <a name="type-of-dimension"></a><span data-ttu-id="a62b5-131">ชนิดของมิติ</span><span class="sxs-lookup"><span data-stu-id="a62b5-131">Type of dimension</span></span>
<span data-ttu-id="a62b5-132">มิติการกำหนดราคาจะมีสองชนิด</span><span class="sxs-lookup"><span data-stu-id="a62b5-132">There are two types of pricing dimensions:</span></span>
  
  - <span data-ttu-id="a62b5-133">**มิติตามจำนวนเงิน**: ค่ามิติจากบริบทการป้อนข้อมูลตรงกันกับค่าของมิติในรายการ **ราคาตามบทบาท** และราคา/ต้นทุนที่เป็นค่าเริ่มต้นโดยตรงจากตาราง **ราคาตามบทบาท**</span><span class="sxs-lookup"><span data-stu-id="a62b5-133">**Amount-based dimensions**: The dimension values from the input context are matched to the dimension values on **Role Price** line and the price/cost is defaulted directly from the **Role Price** table.</span></span>
  - <span data-ttu-id="a62b5-134">**มิติตามส่วนเพิ่มราคา**: เป็นมิติที่จะใช้กระบวนการสามขั้นตอนต่อไปนี้เพื่อให้ได้ราคา/ต้นทุนมา:</span><span class="sxs-lookup"><span data-stu-id="a62b5-134">**Markup-based dimensions**: These are dimensions where the following three-step process to get the price/cost is used:</span></span>
 
    1. <span data-ttu-id="a62b5-135">ระบบจะจับคู่กับค่ามิติที่ไม่ได้อิงตามส่วนเพิ่มราคาจากบริบทการป้อนข้อมูลกับรายการราคาตามบทบาทเพื่อให้ได้อัตราพื้นฐาน</span><span class="sxs-lookup"><span data-stu-id="a62b5-135">The non-markup-based dimension values from the input context are matched to the Role Price line to get the base rate.</span></span>
    2. <span data-ttu-id="a62b5-136">ระบบจะจับคู่กับค่ามิติทั้งหมดจากบริบทการป้อนข้อมูลกับรายการ **ส่วนเพิ่มราคาของราคาตามบทบาท** เพื่อให้ได้เปอร์เซ็นต์การเพิ่มราคา</span><span class="sxs-lookup"><span data-stu-id="a62b5-136">The dimension values from the input context are matched to the **Role Price Markup** line to get a markup percentage.</span></span>
    3. <span data-ttu-id="a62b5-137">ระบบจะนำเปอร์เซ็นต์การเพิ่มราคาจากขั้นตอนที่สองไปใช้กับอัตราพื้นฐานที่ได้รับมาจากตาราง **ราคาตามบทบาท** ตามขั้นตอนแรกแล้วนะไปยังราคา/ต้นทุนขั้นสุดท้าย</span><span class="sxs-lookup"><span data-stu-id="a62b5-137">The markup percentage from the second step is applied to the base rate obtained from the **Role Price** table in the first step to arrive at final price/cost.</span></span>
   
   <span data-ttu-id="a62b5-138">ตารางต่อไปนี้แสดงการคำนวณของส่วนเพิ่มราคา</span><span class="sxs-lookup"><span data-stu-id="a62b5-138">The following table illustrates the calculation of price markups.</span></span>
  
| <span data-ttu-id="a62b5-139">บทบาท</span><span class="sxs-lookup"><span data-stu-id="a62b5-139">Role</span></span>        | <span data-ttu-id="a62b5-140">หน่วยองค์กร</span><span class="sxs-lookup"><span data-stu-id="a62b5-140">Org Unit</span></span>    |<span data-ttu-id="a62b5-141">สถานที่ปฏิบัติงาน</span><span class="sxs-lookup"><span data-stu-id="a62b5-141">Work Location</span></span>      |<span data-ttu-id="a62b5-142">ชื่อมาตรฐาน</span><span class="sxs-lookup"><span data-stu-id="a62b5-142">Standard Title</span></span>      |<span data-ttu-id="a62b5-143">ชั่วโมงการทำงานของทรัพยากร</span><span class="sxs-lookup"><span data-stu-id="a62b5-143">Resource Work Hours</span></span>      |  <span data-ttu-id="a62b5-144">ส่วนเพิ่มราคา</span><span class="sxs-lookup"><span data-stu-id="a62b5-144">Mark Up</span></span>|
| ------------|-------------|-------------------|--------------------|-------------------------|--------:|
|             | <span data-ttu-id="a62b5-145">Contoso อินเดีย</span><span class="sxs-lookup"><span data-stu-id="a62b5-145">Contoso India</span></span>|<span data-ttu-id="a62b5-146">นอกสถานที่</span><span class="sxs-lookup"><span data-stu-id="a62b5-146">Onsite</span></span>            |                    |<span data-ttu-id="a62b5-147">ล่วงเวลา</span><span class="sxs-lookup"><span data-stu-id="a62b5-147">Overtime</span></span>                 |<span data-ttu-id="a62b5-148">15</span><span class="sxs-lookup"><span data-stu-id="a62b5-148">15</span></span>     |
|             | <span data-ttu-id="a62b5-149">Contoso อินเดีย</span><span class="sxs-lookup"><span data-stu-id="a62b5-149">Contoso India</span></span>|<span data-ttu-id="a62b5-150">ภายใน</span><span class="sxs-lookup"><span data-stu-id="a62b5-150">Local</span></span>             |                    |<span data-ttu-id="a62b5-151">ล่วงเวลา</span><span class="sxs-lookup"><span data-stu-id="a62b5-151">Overtime</span></span>                 |<span data-ttu-id="a62b5-152">10</span><span class="sxs-lookup"><span data-stu-id="a62b5-152">10</span></span>     |
|             | <span data-ttu-id="a62b5-153">Contoso US</span><span class="sxs-lookup"><span data-stu-id="a62b5-153">Contoso US</span></span>   |<span data-ttu-id="a62b5-154">ภายใน</span><span class="sxs-lookup"><span data-stu-id="a62b5-154">Local</span></span>             |                    |<span data-ttu-id="a62b5-155">ล่วงเวลา</span><span class="sxs-lookup"><span data-stu-id="a62b5-155">Overtime</span></span>                 |<span data-ttu-id="a62b5-156">20</span><span class="sxs-lookup"><span data-stu-id="a62b5-156">20</span></span>     |


<span data-ttu-id="a62b5-157">ถ้าทรัพยากรจาก Contoso อินเดียที่มีอัตราพื้นฐานเป็น 100 USD กำลังทำงานอยู่ในสถานที่และพวกเขาบันทึก 8 ชั่วโมงของเวลาปกติและ 2 ชั่วโมงของงานล่วงเวลาในรายการเวลา เอ็นจินการกำหนดราคาจะใช้อัตราพื้นฐานของ 100 สำหรับ 8 ชั่วโมงเพื่อบันทึกเป็น 800 USD</span><span class="sxs-lookup"><span data-stu-id="a62b5-157">If a resource from Contoso India whose base rate is 100 USD is working onsite, and they log 8 hours of Regular time and 2 hours of overtime on the time entry, the pricing engine will use the base rate of 100 for the 8 hours to record 800 USD.</span></span> <span data-ttu-id="a62b5-158">สำหรับการทำงานล่วงเวลา 2 ชั่วโมง ส่วนเพิ่มราคา 15% จะถูกปรับใช้กับอัตราพื้นฐานของ 100 เพื่อให้ได้ราคาหน่วย 115 USD และจะบันทึกเป็นต้นทุนทั้งหมด 230 USD</span><span class="sxs-lookup"><span data-stu-id="a62b5-158">For the 2 hours overtime, a markup of 15% will be applied to the base rate of 100 to get a unit price of 115 USD and will record a total cost of 230 USD.</span></span>

### <a name="applicable-to-cost"></a><span data-ttu-id="a62b5-159">ใช้งานได้กับต้นทุน</span><span class="sxs-lookup"><span data-stu-id="a62b5-159">Applicable to Cost</span></span> 
<span data-ttu-id="a62b5-160">ถ้ามีการตั้งค่าสิ่งนี้เป็น **ใช่** จะบ่งชี้ว่าค่ามิติจากบริบทการป้อนข้อมูลควรจะใช้เพื่อจับคู่ **ราคาตามบทบาท** และ **ส่วนเพิ่มราคาของราคาตามบทบาท** เมื่อรับข้อมูลจากอัตราของต้นทุนและส่วนเพิ่มราคา</span><span class="sxs-lookup"><span data-stu-id="a62b5-160">If this is set to **Yes**, it indicates that the dimension value from the input context should be used to match to the **Role Price** and **Role Price Markup** when retrieving the cost and markup rates.</span></span>

### <a name="applicable-to-sales"></a><span data-ttu-id="a62b5-161">ใช้งานได้กับการขาย</span><span class="sxs-lookup"><span data-stu-id="a62b5-161">Applicable to Sales</span></span>
<span data-ttu-id="a62b5-162">ถ้ามีการตั้งค่าสิ่งนี้เป็น **ใช่** จะบ่งชี้ว่าค่ามิติจากบริบทการป้อนข้อมูลควรจะใช้เพื่อจับคู่ **ราคาตามบทบาท** และ **ส่วนเพิ่มราคาของราคาตามบทบาท** เมื่อรับข้อมูลจากอัตราของการเรียกเก็บเงินและส่วนเพิ่มราคา</span><span class="sxs-lookup"><span data-stu-id="a62b5-162">If this is set to **Yes**, it indicates that the dimension value from the input context should be used to match to the **Role Price** and **Role Price Markup** when retrieving the bill and markup rates.</span></span>

### <a name="applicable-to-purchase"></a><span data-ttu-id="a62b5-163">ใช้งานได้กับการซื้อ</span><span class="sxs-lookup"><span data-stu-id="a62b5-163">Applicable to Purchase</span></span>
<span data-ttu-id="a62b5-164">ถ้ามีการตั้งค่าสิ่งนี้เป็น **ใช่** จะบ่งชี้ว่าค่ามิติจากบริบทการป้อนข้อมูลควรจะใช้เพื่อจับคู่ **ราคาตามบทบาท** และ **ส่วนเพิ่มราคาของราคาตามบทบาท** เมื่อรับข้อมูลจากราคาซื้อ</span><span class="sxs-lookup"><span data-stu-id="a62b5-164">If this is set to **Yes**, it indicates that the dimension value from the input context should be used to match to the **Role Price** and **Role Price Markup** when retrieving the purchase price.</span></span> <span data-ttu-id="a62b5-165">ไม่รองรับสถานการณ์การรับเหมารายย่อย ดังนั้นจึงไม่ได้ใช้ฟิลด์นี้</span><span class="sxs-lookup"><span data-stu-id="a62b5-165">Subcontracting scenarios are not supported, so this field is not used.</span></span> 

### <a name="priority"></a><span data-ttu-id="a62b5-166">ลำดับความสำคัญ</span><span class="sxs-lookup"><span data-stu-id="a62b5-166">Priority</span></span>
<span data-ttu-id="a62b5-167">การตั้งค่าลำดับความสำคัญของมิติ จะช่วยให้การกำหนดราคาสร้างราคาได้แม้ว่าจะไม่สามารถหาค่าที่ตรงกันระหว่างค่ามิติที่ป้อนและค่าจากตาราง **ราคาตามบทบาท** หรือ **ส่วนเพิ่มราคาของราคาตามบทบาท**</span><span class="sxs-lookup"><span data-stu-id="a62b5-167">Setting the dimension priority helps pricing produce a price even when it can't find an exact match between the input dimension values and the values from the **Role Price** or **Role Price Markup** tables.</span></span> <span data-ttu-id="a62b5-168">ในสถานการณ์สมมตินี้ จะใช้ค่า Null สำหรับค่าขนาดที่ไม่ตรงกันโดยการชั่งน้ำหนักมิติตามลำดับความสำคัญ</span><span class="sxs-lookup"><span data-stu-id="a62b5-168">In this scenario, null values are used for unmatched dimension values by weighing the dimensions in order of their priority.</span></span>

- <span data-ttu-id="a62b5-169">**ลำดับความสำคัญของต้นทุน**: ค่าของลำดับความสำคัญของต้นทุนของมิติจะบ่งชี้ถึงน้ำหนักของมิติเมื่อเปรียบเทียบกับการตั้งค่าราคาต้นทุน</span><span class="sxs-lookup"><span data-stu-id="a62b5-169">**Cost Priority**: The value of a dimension's cost priority will indicate the weight of that dimension when matching against the setup of cost prices.</span></span> <span data-ttu-id="a62b5-170">ค่าของ **ลำดับความสำคัญของต้นทุน** ต้องไม่ซ้ำกันกับมิติต่างๆ ที่ **ใช้งานได้กับต้นทุน**</span><span class="sxs-lookup"><span data-stu-id="a62b5-170">The value of **Cost Priority** must be unique across dimensions that are **Applicable to Cost**.</span></span>
- <span data-ttu-id="a62b5-171">**ลำดับความสำคัญของการขาย**: ค่าของลำดับความสำคัญการขายของมิติจะบ่งชี้ถึงน้ำหนักของมิติเมื่อเปรียบเทียบกับการตั้งค่าราคาขายหรืออัตราเรียกเก็บเงิน</span><span class="sxs-lookup"><span data-stu-id="a62b5-171">**Sales Priority**: The value of dimension's sales priority will indicate the weight of that dimension when matching against the setup of sales prices or bill rates.</span></span> <span data-ttu-id="a62b5-172">ค่าของ **ลำดับความสำคัญของการขาย** ต้องไม่ซ้ำกันกับมิติต่างๆ ที่ **ใช้งานได้กับการขาย**</span><span class="sxs-lookup"><span data-stu-id="a62b5-172">The value of **Sales Priority** must be unique across dimensions that are **Applicable to Sales**.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]