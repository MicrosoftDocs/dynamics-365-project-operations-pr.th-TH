---
title: ภาพรวมมิติการกำหนดราคา
description: หัวข้อนี้ให้ข้อมูลเกี่ยวกับมิติการกำหนดราคาใน Dynamics 365 Project Operations
author: rumant
ms.date: 11/30/2020
ms.topic: article
ms.prod: ''
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 01ba11e34e7d8a59716fa9d8c8be3389ab380048
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 05/10/2021
ms.locfileid: "6005004"
---
# <a name="pricing-dimensions-overview"></a><span data-ttu-id="4739d-103">ภาพรวมมิติการกำหนดราคา</span><span class="sxs-lookup"><span data-stu-id="4739d-103">Pricing dimensions overview</span></span>

<span data-ttu-id="4739d-104">_**นำไปใช้กับ:** Project Operations สำหรับสถานการณ์ตามทรัพยากร/วัสดุที่ไม่ได้เก็บในคลัง การปรับใช้งานแบบ Lite - จัดการกับการออกใบแจ้งหนี้ชั่วคราว_</span><span class="sxs-lookup"><span data-stu-id="4739d-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="4739d-105">มิติที่ใช้ในทรัพยากรบุคคลเพื่อตั้งค่าการกำหนดราคาและการคิดต้นทุนจะแบ่งออกเป็นสองประเภท: </span><span class="sxs-lookup"><span data-stu-id="4739d-105">The dimensions that are used in human resources to set up pricing and costs fall into two categories:</span></span>

- <span data-ttu-id="4739d-106">บุคคล</span><span class="sxs-lookup"><span data-stu-id="4739d-106">People</span></span>
- <span data-ttu-id="4739d-107">งานตามแผน</span><span class="sxs-lookup"><span data-stu-id="4739d-107">Planned work</span></span>

<span data-ttu-id="4739d-108">ด้วยเหตุนี้ จึงมีมิติข้อมูลการกำหนดราคาสองประเภทที่พร้อมใช้งาน:</span><span class="sxs-lookup"><span data-stu-id="4739d-108">Because of this, there are two types of pricing dimension values available:</span></span>

- <span data-ttu-id="4739d-109">**ชุดตัวเลือก**: มิติที่มีการแจกแจกคงที่สำหรับชุดของค่า</span><span class="sxs-lookup"><span data-stu-id="4739d-109">**Option sets**: Dimensions that are fixed enumerations for a set of values.</span></span>
- <span data-ttu-id="4739d-110">**ค่าตามเอนทิตี**: มิติที่สามารถเป็นชุดของค่าที่หลากหลายได้</span><span class="sxs-lookup"><span data-stu-id="4739d-110">**Entity-based values**: Dimensions that can be a varied set of values.</span></span>

## <a name="pricing-dimensions"></a><span data-ttu-id="4739d-111">มิติการกำหนดราคา</span><span class="sxs-lookup"><span data-stu-id="4739d-111">Pricing dimensions</span></span>

<span data-ttu-id="4739d-112">Dynamics 365 Project Operations จัดส่งกับชุดการกำหนดราคาเริ่มต้น</span><span class="sxs-lookup"><span data-stu-id="4739d-112">Dynamics 365 Project Operations ships with a default set of pricing dimensions.</span></span> <span data-ttu-id="4739d-113">คุณสามารถมิติการกำหนดราคาเหล่านี้ได้โดยไปที่ **Project Operations** > **พารามิเตอร์**</span><span class="sxs-lookup"><span data-stu-id="4739d-113">You can view these pricing dimensions by going to **Project Operations** > **Parameters**.</span></span> <span data-ttu-id="4739d-114">ในบันทึกพารามิเตอร์ บนแท็บ **Amount-based pricing dimensions** ตรวจสอบบทบาทนั้น **msdyn_resourcecategory** และจัดเตรียมทรัพยากรหน่อยองค์กร **msdyn_organizationalunit** มีฟิล์ด **Applicable to sales** และ **Applicable to cost** ให้ตั้งเป็น **Yes**</span><span class="sxs-lookup"><span data-stu-id="4739d-114">In the parameter record, on the **Amount-based pricing dimensions** tab, verify that the role, **msdyn_resourcecategory** and resourcing organizational unit, **msdyn_organizationalunit** have the fields **Applicable to sales** and **Applicable to cost** set to **Yes**.</span></span> <span data-ttu-id="4739d-115">เมื่อเปิดใช้งานฟิลด์เหล่านี้ คุณสามารถตั้งค่าการกำหนดราคาและการคิดต้นทุนสำหรับทุกบทบาทและการรวมหน่วยองค์กร</span><span class="sxs-lookup"><span data-stu-id="4739d-115">With these fields enabled, you can set up the price and cost for each role and organizational unit combination.</span></span>

![ภาพหน้าจอของพารามิเตอร์ Project Service กับ “Applicable to Sales” ที่ไฮไลต์](media/PS-OOB-parameters.png)

<span data-ttu-id="4739d-117">ถ้าคุณต้องการกำหนดราคาหรือคิดต้นทุนสำหรับทรัพยากรของคุณโดยใช้แอตทริบิวต์เพิ่มเติม คุณสามารถสร้างฟิล์ดที่กำหนดเอง เอนทิตี และมิติ</span><span class="sxs-lookup"><span data-stu-id="4739d-117">If you need to price or cost for your resources using additional attributes, you can create customized fields, entities, and dimensions.</span></span> <span data-ttu-id="4739d-118">สำหรับข้อมูลเพิ่มเติม ดูหัวข้อต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="4739d-118">For more information, see the following topics.</span></span> 
  
  > [!NOTE]
  > <span data-ttu-id="4739d-119">ขั้นตอนจะต้องเสร็จสมบูรณ์ตามลำดับที่ระบุไว้</span><span class="sxs-lookup"><span data-stu-id="4739d-119">The procedures must be completed in the order they are listed.</span></span>

1. [<span data-ttu-id="4739d-120">สร้างโซลูชันสำหรับมิติการกำหนดราคาที่กำหนดเอง</span><span class="sxs-lookup"><span data-stu-id="4739d-120">Create a solution for custom pricing dimensions</span></span>](../sales/create-solution-custompd.md)
2. [<span data-ttu-id="4739d-121">สร้างฟิลด์แบบกำหนดเองและเอนทิตี</span><span class="sxs-lookup"><span data-stu-id="4739d-121">Create custom fields and entities</span></span>](create-custom-fields-entities-pricing-dimensions.md)
3. [<span data-ttu-id="4739d-122">เพิ่มฟิลด์ที่กำหนดเองในการตั้งค่าราคาและเอนทิตีธุรกรรม </span><span class="sxs-lookup"><span data-stu-id="4739d-122">Add custom fields to price setup and transactional entities</span></span>](add-custom-fields-price-setup-transactional-entities.md)
4. [<span data-ttu-id="4739d-123">ตั้งค่าฟิลด์ที่กำหนดเองเป็นมิติการกำหนดราคา </span><span class="sxs-lookup"><span data-stu-id="4739d-123">Set up custom fields as pricing dimensions</span></span>](set-up-custom-fields-pricing-dimensions.md)
5. [<span data-ttu-id="4739d-124">อัปเดตแอตทริบิวต์ปลั๊กอินเพื่อรวมมิติการกำหนดราคาแบบใหม่ไปด้วย</span><span class="sxs-lookup"><span data-stu-id="4739d-124">Update plug-in attributes to include new pricing dimensions</span></span>](update-plugin-attributes-pd.md)


## <a name="pricing-human-resource-time"></a><span data-ttu-id="4739d-125">การกำหนดราคาเวลาทรัพยากรบุลคล</span><span class="sxs-lookup"><span data-stu-id="4739d-125">Pricing human resource time</span></span>
<span data-ttu-id="4739d-126">วิธีที่องค์กรกำหนดราคาเวลาทรัพยากรบุลคลมักจะเป็นการพิจารณาเชิงกุลยุทธ์ที่สำคัญที่ส่งผลกับผลกำไรขององค์กรโดยตรง</span><span class="sxs-lookup"><span data-stu-id="4739d-126">How an organization prices human resource time is often an important strategic consideration that directly affects the organization's profitability.</span></span> <span data-ttu-id="4739d-127">ทำงานร่วมกับทีมการเงินและปฏิบัติกับหัวหน้าเมื่อองค์กรของคุณพร้อมที่จะระบุวิธีที่ต้องการจะตั้งค่าบิลและอัตราต้นทุนสำหรับเวลาทรัพยยากรบุคคล</span><span class="sxs-lookup"><span data-stu-id="4739d-127">Work with the finance teams and practice heads when your organization is ready to identify how it wants to set up bill and cost rates for human resource time.</span></span>

<span data-ttu-id="4739d-128">การพิจารณาอื่นๆสำหรับการกำหนดราคารวมถึงว่าจะใช้ฟิล์ดหรือเอนทิตีซ้ำที่ไม่ใช่มิติการกำหนดราคาปัจจุบันแต่ใช้เป็นมิติการกำหนดราคาสำหรับองค์กรของคุณ</span><span class="sxs-lookup"><span data-stu-id="4739d-128">Other considerations for pricing include whether to re-use fields or entities that are not currently pricing dimensions but apply as a pricing dimension for your organization.</span></span> <span data-ttu-id="4739d-129">ฟิล์ดอย่าง **Transaction Category** (**msdyn_transactioncategory**) และ **Bookable Resource** (**bookableresource**) เป็นตัวอย่างของมิติที่น่าสนใจจ</span><span class="sxs-lookup"><span data-stu-id="4739d-129">Fields like **Transaction Category** (**msdyn_transactioncategory**) and **Bookable Resource** (**bookableresource**) are examples of candidate dimensions.</span></span> 

<span data-ttu-id="4739d-130">พิจารณาว่ามิติการกำหนดราคาของคุณควรจะเป็นแบบตารางหรือชุดตัวเลือก</span><span class="sxs-lookup"><span data-stu-id="4739d-130">Consider whether your pricing dimension should be a table or an option set.</span></span> <span data-ttu-id="4739d-131">ถ้าคุณรู้ว่าจะมีการเปลี่ยนแปลงมิติของค่าล่วงหน้าซึ่งจะเกิน 10 หรือ 12 และคุณต้องการแอตทริบิวต์เพิ่มเติมเกี่ยวกับค่าเหล่านี้ คุณสามารถสร้างเอนทิตีแทนที่จะเป็นชุดตัวเลือก</span><span class="sxs-lookup"><span data-stu-id="4739d-131">If you foresee changes to the values of a dimension which will exceed 10 or 12 and you need additional attributes on these values, you could create an entity rather than an option set.</span></span> <span data-ttu-id="4739d-132">การรักษาชุดตัวเลือกเช่น การเพิ่มหรือลดค่า ต้องใช้ผู้ดูแลหรือนักพัฒนาในขณะที่การเพิ่มแถวใหม่ไปในตารางสามารทำได้โดยผู้ใช้ส่วนใหญ่</span><span class="sxs-lookup"><span data-stu-id="4739d-132">Maintaining an option set, such as adding or removing values, requires an admin or developer whereas adding new rows to a table can be done by most users.</span></span>

<span data-ttu-id="4739d-133">ตัวอย่างต่อไปนี้แสดงอัตราการเรียกเก็บเงินที่ตั้งค่าตามบทบาทและหน่วยการจัดหาทรัพยากรองค์กรที่เป็นของทรัพยากร</span><span class="sxs-lookup"><span data-stu-id="4739d-133">The following example shows bill rates that are set up based on the role and the resourcing org unit to which the resource belongs.</span></span> <span data-ttu-id="4739d-134">อัตราต้นทุนโดยทั่วไปจะขึ้นอยู่กับแถบเงินเดือนของพนักงานและหน่วยองค์กรที่พนักงานเป็นสมาชิก</span><span class="sxs-lookup"><span data-stu-id="4739d-134">Cost rates are typically based on the salary band of the employee and the org unit that they belong to.</span></span> <span data-ttu-id="4739d-135">ตัวอย่างต่อไปนี้ ตารางอัตราเรียกเก็บเงินและอัตราต้นทุนจะมีลักษณะดังต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="4739d-135">In this example, the bill rate and cost rate tables will look like the following.</span></span>

<span data-ttu-id="4739d-136">**ตัวอย่างอัตราเรียกเก็บ**</span><span class="sxs-lookup"><span data-stu-id="4739d-136">**Sample bill rates**</span></span>

| <span data-ttu-id="4739d-137">บทบาท</span><span class="sxs-lookup"><span data-stu-id="4739d-137">Role</span></span>        | <span data-ttu-id="4739d-138">หน่วยองค์กร</span><span class="sxs-lookup"><span data-stu-id="4739d-138">Org Unit</span></span>    |<span data-ttu-id="4739d-139">หน่วย</span><span class="sxs-lookup"><span data-stu-id="4739d-139">Unit</span></span>      |<span data-ttu-id="4739d-140">ราคา</span><span class="sxs-lookup"><span data-stu-id="4739d-140">Price</span></span>      |<span data-ttu-id="4739d-141">สกุลเงิน</span><span class="sxs-lookup"><span data-stu-id="4739d-141">Currency</span></span>  |
| ------------|-------------|----------|----------:|----------|
| <span data-ttu-id="4739d-142">นักพัฒนา</span><span class="sxs-lookup"><span data-stu-id="4739d-142">Developer</span></span>   | <span data-ttu-id="4739d-143">Contoso US</span><span class="sxs-lookup"><span data-stu-id="4739d-143">Contoso US</span></span>  |<span data-ttu-id="4739d-144">ชั่วโมง</span><span class="sxs-lookup"><span data-stu-id="4739d-144">Hour</span></span> | <span data-ttu-id="4739d-145">200</span><span class="sxs-lookup"><span data-stu-id="4739d-145">200</span></span>|<span data-ttu-id="4739d-146">USD</span><span class="sxs-lookup"><span data-stu-id="4739d-146">USD</span></span>     |
| <span data-ttu-id="4739d-147">นักพัฒนา</span><span class="sxs-lookup"><span data-stu-id="4739d-147">Developer</span></span>   | <span data-ttu-id="4739d-148">Contoso อินเดีย</span><span class="sxs-lookup"><span data-stu-id="4739d-148">Contoso India</span></span> |<span data-ttu-id="4739d-149">ชั่วโมง</span><span class="sxs-lookup"><span data-stu-id="4739d-149">Hour</span></span>|   <span data-ttu-id="4739d-150">112</span><span class="sxs-lookup"><span data-stu-id="4739d-150">112</span></span>|<span data-ttu-id="4739d-151">USD</span><span class="sxs-lookup"><span data-stu-id="4739d-151">USD</span></span>     |


<span data-ttu-id="4739d-152">**ตัวอย่างอัตราต้นทุน**</span><span class="sxs-lookup"><span data-stu-id="4739d-152">**Sample cost rates**</span></span>

| <span data-ttu-id="4739d-153">แถบเงินเดือน</span><span class="sxs-lookup"><span data-stu-id="4739d-153">Salary Band</span></span>     | <span data-ttu-id="4739d-154">หน่วยองค์กร</span><span class="sxs-lookup"><span data-stu-id="4739d-154">Org Unit</span></span>    |<span data-ttu-id="4739d-155">หน่วย</span><span class="sxs-lookup"><span data-stu-id="4739d-155">Unit</span></span>      |<span data-ttu-id="4739d-156">ราคา</span><span class="sxs-lookup"><span data-stu-id="4739d-156">Price</span></span>      |<span data-ttu-id="4739d-157">สกุลเงิน</span><span class="sxs-lookup"><span data-stu-id="4739d-157">Currency</span></span>  |
| ----------------|-------------|----------|----------:|----------|
| <span data-ttu-id="4739d-158">บริษัทของฉัน_Band1</span><span class="sxs-lookup"><span data-stu-id="4739d-158">My company_Band1</span></span> | <span data-ttu-id="4739d-159">Contoso US</span><span class="sxs-lookup"><span data-stu-id="4739d-159">Contoso US</span></span>  |<span data-ttu-id="4739d-160">ชั่วโมง</span><span class="sxs-lookup"><span data-stu-id="4739d-160">Hour</span></span> | <span data-ttu-id="4739d-161">145</span><span class="sxs-lookup"><span data-stu-id="4739d-161">145</span></span>|<span data-ttu-id="4739d-162">USD</span><span class="sxs-lookup"><span data-stu-id="4739d-162">USD</span></span>     |
| <span data-ttu-id="4739d-163">บริษัทของฉัน_Band2</span><span class="sxs-lookup"><span data-stu-id="4739d-163">My company_Band2</span></span> | <span data-ttu-id="4739d-164">Contoso อินเดีย</span><span class="sxs-lookup"><span data-stu-id="4739d-164">Contoso India</span></span> |<span data-ttu-id="4739d-165">ชั่วโมง</span><span class="sxs-lookup"><span data-stu-id="4739d-165">Hour</span></span>|   <span data-ttu-id="4739d-166">67</span><span class="sxs-lookup"><span data-stu-id="4739d-166">67</span></span>|<span data-ttu-id="4739d-167">USD</span><span class="sxs-lookup"><span data-stu-id="4739d-167">USD</span></span>     |


[!INCLUDE[footer-include](../includes/footer-banner.md)]