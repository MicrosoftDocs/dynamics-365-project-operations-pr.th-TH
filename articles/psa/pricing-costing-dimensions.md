---
title: โฮมเพจมิติการกำหนดราคาและการคิดต้นทุน
description: หัวข้อนี้มีภาพรวมของมิติการกำหนดราคา
author: rumant
manager: kfend
ms.custom:
- dyn365-projectservice
ms.date: 10/01/2020
ms.topic: article
ms.service: business-applications
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365PS
- ProjectOperations
ms.openlocfilehash: 515a2e2e518614884b414ca43702e8bfea2c6919
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 10/16/2020
ms.locfileid: "4085973"
---
# <a name="pricing-and-costing-dimensions-home-page"></a><span data-ttu-id="05a5d-103">โฮมเพจมิติการกำหนดราคาและการคิดต้นทุน</span><span class="sxs-lookup"><span data-stu-id="05a5d-103">Pricing and costing dimensions home page</span></span>

<span data-ttu-id="05a5d-104">มิติที่ใช้ในการกำหนดราคาค่าแรงและการคิดต้นทุนในองค์กรตามโครงการได้รับอิทธิพลจากแอตทริบิวต์ต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="05a5d-104">The dimensions used to set labor pricing and costing in project-based organizations are influenced by the following attributes:</span></span>

- <span data-ttu-id="05a5d-105">บุคลากรที่ทำงานคล้ายกับประสบการณ์ บทบาท หรือภูมิศาสตร์ของพวกเขา</span><span class="sxs-lookup"><span data-stu-id="05a5d-105">People doing work similar to their experience, role, or geography</span></span>
- <span data-ttu-id="05a5d-106">งานที่ต้องทำคล้ายกับความซับซ้อนหรือช่วงเวลาของวัน</span><span class="sxs-lookup"><span data-stu-id="05a5d-106">Work to be performed similar to its complexity or time of day</span></span>

<span data-ttu-id="05a5d-107">เมื่อพิจารณาจากลักษณะทั่วไปของแอตทริบิวต์เหล่านี้ของงานและบุคลากรที่ต้องใช้ในการทำงาน มีค่ามิติการกำหนดราคาสองประเภทอยู่ใน Project Service Automation:</span><span class="sxs-lookup"><span data-stu-id="05a5d-107">Given the typical nature of these attrubutes of the work and the people required to perform the work, there are two types of pricing dimension values available in Project Service Automation:</span></span> 

- <span data-ttu-id="05a5d-108">**ชุดตัวเลือก** - แอตทริบิวต์ที่มีการแจกแจกคงที่สำหรับชุดของค่า</span><span class="sxs-lookup"><span data-stu-id="05a5d-108">**Option sets** - Attributes that are fixed enumerations for a set of values.</span></span>
- <span data-ttu-id="05a5d-109">**ค่าตามเอนทิตี** - แอตทริบิวต์ที่สามารถมีชุดค่าต่างๆ ที่จำกัด แต่สามารถเปลี่ยนแปลงได้ตลอดเวลา</span><span class="sxs-lookup"><span data-stu-id="05a5d-109">**Entity-based values** - Attributes that can have a varied set of values that are finite but can change over time.</span></span>

## <a name="pricing-dimensions"></a><span data-ttu-id="05a5d-110">มิติการกำหนดราคา</span><span class="sxs-lookup"><span data-stu-id="05a5d-110">Pricing dimensions</span></span>

<span data-ttu-id="05a5d-111">PSA จัดส่งกับชุดการกำหนดราคาเริ่มต้น</span><span class="sxs-lookup"><span data-stu-id="05a5d-111">PSA ships with a default set of pricing dimensions.</span></span> <span data-ttu-id="05a5d-112">คุณสามารถดูสิ่งเหล่านี้ได้โดยไปที่ **Project Service** > **พารามิเตอร์**</span><span class="sxs-lookup"><span data-stu-id="05a5d-112">You can view these by going to **Project Service** > **Parameters**.</span></span> <span data-ttu-id="05a5d-113">ในบันทึกพารามิเตอร์ บนแท็บ **Amount-based pricing dimensions** ตรวจสอบบทบาทนั้น **msdyn_resourcecategory** และจัดเตรียมทรัพยากรหน่อยองค์กร **msdyn_organizationalunit** มีฟิล์ด **Applicable to sales** และ **Applicable to cost** ให้ตั้งเป็น **Yes**</span><span class="sxs-lookup"><span data-stu-id="05a5d-113">In the parameter record, on the **Amount-based pricing dimensions** tab, verify that the role, **msdyn_resourcecategory** and resourcing organizational unit, **msdyn_organizationalunit** have the fields **Applicable to sales** and **Applicable to cost** set to **Yes**.</span></span> <span data-ttu-id="05a5d-114">สิ่งนี้จะอนุญาตให้คุณตั้งค่าการกำหนดราคาและการคิดต้นทุนสำหรับทุกบทบาทและการรวมหน่วยองค์กร</span><span class="sxs-lookup"><span data-stu-id="05a5d-114">This will allow you to set up the price and cost for each role and organizational unit combination.</span></span>

![ภาพหน้าจอของพารามิเตอร์ Project Service กับ “Applicable to Sales” ที่ไฮไลต์](media/PS-OOB-parameters.png)

> [!IMPORTANT]
> <span data-ttu-id="05a5d-116">ถ้าคุณเคยใช้ฟิลด์สำเร็จรูปของบทบาทและหน่วยองค์กรเป็นมิติการกำหนดราคาก่อนรุ่นที่ 3 ของ PSA จะไม่มีการเปลี่ยนแปลงใด ๆ ที่สังเกตได้</span><span class="sxs-lookup"><span data-stu-id="05a5d-116">If you have been the using out-of-the box fields of role and organizational unit as pricing dimensions prior to version 3 of PSA, there will not be any observable change.</span></span> <span data-ttu-id="05a5d-117">คุณสามารถใช้ Project Service ต่อได้ตามปกติ</span><span class="sxs-lookup"><span data-stu-id="05a5d-117">You can continue to use Project Service as usual.</span></span> 

<span data-ttu-id="05a5d-118">ถ้าคุณต้องการกำหนดราคาหรือคิดต้นทุนสำหรับทรัพยากรของคุณโดยใช้แอตทริบิวต์เพิ่มเติม คุณสามารถสร้างฟิล์ดที่กำหนดเอง เอนทิตี และมิติ</span><span class="sxs-lookup"><span data-stu-id="05a5d-118">If you need to price or cost for your resources using additional attributes, you can create customized fields, entities, and dimensions.</span></span> <span data-ttu-id="05a5d-119">สำหรับข้อมูลเพิ่มเติม โปรดดูหัวข้อต่อไปนี้ อย่างไรก็ตามโปรดทราบว่าคุณต้องทำตามขั้นตอนตามรายการที่ระบุไว้ด้านล่างจนเสร็จสมบูรณ์:</span><span class="sxs-lookup"><span data-stu-id="05a5d-119">For more information, see the following topics, however note that you must complete the procedures in the order listed below:</span></span>

- [<span data-ttu-id="05a5d-120">สร้างฟิลด์แบบกำหนดเองและเอนทิตี</span><span class="sxs-lookup"><span data-stu-id="05a5d-120">Create custom fields and entities</span></span>](create-custom-fields-entities.md)
- [<span data-ttu-id="05a5d-121">เพิ่มฟิลด์แบบกำหนดเองไปยังการตั้งค่าการกำหนดราคาและเอนทิตีธุรกรรม</span><span class="sxs-lookup"><span data-stu-id="05a5d-121">Add custom fields to price setup and transactional entities</span></span>](field-references.md)
- [<span data-ttu-id="05a5d-122">ตั้งค่าฟิลด์ที่กำหนดเองเป็นมิติการกำหนดราคา </span><span class="sxs-lookup"><span data-stu-id="05a5d-122">Set up custom fields as pricing dimensions</span></span>](set-up-pricing-dimensions.md)
- [<span data-ttu-id="05a5d-123">อัปเดตแอตทริบิวต์ปลั๊กอินเพื่อรวมมิติการกำหนดราคาแบบใหม่ไปด้วย</span><span class="sxs-lookup"><span data-stu-id="05a5d-123">Update plug-in attributes to include new pricing dimensions</span></span>](update-plug-in-attributes.md)

## <a name="pricing-human-resource-time"></a><span data-ttu-id="05a5d-124">การกำหนดราคาเวลาทรัพยากรบุลคล</span><span class="sxs-lookup"><span data-stu-id="05a5d-124">Pricing human resource time</span></span>
<span data-ttu-id="05a5d-125">วิธีที่องค์กรกำหนดราคาเวลาทรัพยากรบุลคลมักจะเป็นการพิจารณาเชิงกุลยุทธ์ที่สำคัญที่ส่งผลกับผลกำไรขององค์กรโดยตรง</span><span class="sxs-lookup"><span data-stu-id="05a5d-125">How an organization prices human resource time is often an important strategic consideration that directly affects the organization's profitability.</span></span> <span data-ttu-id="05a5d-126">ทำงานร่วมกับทีมการเงินและปฏิบัติกับหัวหน้าเมื่อองค์กรของคุณพร้อมที่จะระบุวิธีที่ต้องการจะตั้งค่าบิลและอัตราต้นทุนสำหรับเวลาทรัพยยากรบุคคล</span><span class="sxs-lookup"><span data-stu-id="05a5d-126">Work with the finance teams and practice heads when your organization is ready to identify how it wants to set up bill and cost rates for human resource time.</span></span>

<span data-ttu-id="05a5d-127">การพิจารณาอื่นๆสำหรับการกำหนดราคารวมถึงว่าจะใช้ฟิล์ดหรือเอนทิตีซ้ำที่ไม่ใช่มิติการกำหนดราคาปัจจุบันแต่ใช้เป็นมิติการกำหนดราคาสำหรับองค์กรของคุณ</span><span class="sxs-lookup"><span data-stu-id="05a5d-127">Other considerations for pricing include whether to re-use fields or entities that are not currently pricing dimensions but apply as a pricing dimension for your organization.</span></span> <span data-ttu-id="05a5d-128">ฟิล์ดอย่าง **Transaction Category** ( **msdyn_transactioncategory** ) และ **Bookable Resource** ( **bookableresource** ) เป็นตัวอย่างของมิติที่น่าสนใจจ</span><span class="sxs-lookup"><span data-stu-id="05a5d-128">Fields like **Transaction Category** ( **msdyn_transactioncategory** ) and **Bookable Resource** ( **bookableresource** ) are examples of candidate dimensions.</span></span> 

<span data-ttu-id="05a5d-129">พิจารณาว่ามิติการกำหนดราคาของคุณควรจะเป็นแบบตารางหรือชุดตัวเลือก</span><span class="sxs-lookup"><span data-stu-id="05a5d-129">Consider whether your pricing dimension should be a table or an option set.</span></span> <span data-ttu-id="05a5d-130">ถ้าคุณรู้ว่าจะมีการเปลี่ยนแปลงมิติของค่าล่วงหน้าซึ่งจะเกิน 10 หรือ 12 และคุณต้องการแอตทริบิวต์เพิ่มเติมเกี่ยวกับค่าเหล่านี้ ให้สร้างเอนทิตีแทนที่จะเป็นชุดตัวเลือก</span><span class="sxs-lookup"><span data-stu-id="05a5d-130">If you foresee changes to the values of a dimension which will exceed 10 or 12 and you need additional attributes on these values, create an entity rather than an option set.</span></span> <span data-ttu-id="05a5d-131">การรักษาชุดตัวเลือกเช่น การเพิ่มหรือลดค่า ต้องใช้ผู้ดูแลหรือนักพัฒนาในขณะที่การเพิ่มแถวใหม่ไปในตารางสามารทำได้โดยผู้ใช้ทางธุรกิจส่วนใหญ่</span><span class="sxs-lookup"><span data-stu-id="05a5d-131">Maintaining an option set, such as adding or removing values, requires an admin or developer whereas adding new rows to a table can be done by most business users.</span></span>

<span data-ttu-id="05a5d-132">ตัวอย่างต่อไปนี้แสดงอัตราการเรียกเก็บเงินที่ตั้งค่าตามบทบาทและหน่วยการจัดหาทรัพยากรองค์กรที่เป็นของทรัพยากร</span><span class="sxs-lookup"><span data-stu-id="05a5d-132">The following example shows bill rates that are set up based on the role and the resourcing org unit to which the resource belongs.</span></span> <span data-ttu-id="05a5d-133">อัตราต้นทุนโดยทั่วไปจะขึ้นอยู่กับแถบเงินเดือนของพนักงานและหน่วยองค์กรที่พนักงานเป็นสมาชิก</span><span class="sxs-lookup"><span data-stu-id="05a5d-133">Cost rates are typically based on the salary band of the employee and the org unit that they belong to.</span></span> <span data-ttu-id="05a5d-134">ตัวอย่างต่อไปนี้ ตารางอัตราเรียกเก็บเงินและอัตราต้นทุนจะมีลักษณะดังต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="05a5d-134">In this example, the bill rate and cost rate tables will look like the following.</span></span>

<span data-ttu-id="05a5d-135">**ตัวอย่างอัตราเรียกเก็บ**</span><span class="sxs-lookup"><span data-stu-id="05a5d-135">**Sample bill rates**</span></span>

| <span data-ttu-id="05a5d-136">บทบาท</span><span class="sxs-lookup"><span data-stu-id="05a5d-136">Role</span></span>        | <span data-ttu-id="05a5d-137">หน่วยองค์กร</span><span class="sxs-lookup"><span data-stu-id="05a5d-137">Org Unit</span></span>    |<span data-ttu-id="05a5d-138">หน่วย</span><span class="sxs-lookup"><span data-stu-id="05a5d-138">Unit</span></span>      |<span data-ttu-id="05a5d-139">ราคา</span><span class="sxs-lookup"><span data-stu-id="05a5d-139">Price</span></span>      |<span data-ttu-id="05a5d-140">สกุลเงิน</span><span class="sxs-lookup"><span data-stu-id="05a5d-140">Currency</span></span>  |
| ------------|-------------|----------|----------:|----------|
| <span data-ttu-id="05a5d-141">นักพัฒนา</span><span class="sxs-lookup"><span data-stu-id="05a5d-141">Developer</span></span>   | <span data-ttu-id="05a5d-142">Contoso US</span><span class="sxs-lookup"><span data-stu-id="05a5d-142">Contoso US</span></span>  |<span data-ttu-id="05a5d-143">Hour</span><span class="sxs-lookup"><span data-stu-id="05a5d-143">Hour</span></span> | <span data-ttu-id="05a5d-144">200</span><span class="sxs-lookup"><span data-stu-id="05a5d-144">200</span></span>|<span data-ttu-id="05a5d-145">USD</span><span class="sxs-lookup"><span data-stu-id="05a5d-145">USD</span></span>     |
| <span data-ttu-id="05a5d-146">นักพัฒนา</span><span class="sxs-lookup"><span data-stu-id="05a5d-146">Developer</span></span>   | <span data-ttu-id="05a5d-147">Contoso India</span><span class="sxs-lookup"><span data-stu-id="05a5d-147">Contoso India</span></span> |<span data-ttu-id="05a5d-148">Hour</span><span class="sxs-lookup"><span data-stu-id="05a5d-148">Hour</span></span>|   <span data-ttu-id="05a5d-149">112</span><span class="sxs-lookup"><span data-stu-id="05a5d-149">112</span></span>|<span data-ttu-id="05a5d-150">USD</span><span class="sxs-lookup"><span data-stu-id="05a5d-150">USD</span></span>     |


<span data-ttu-id="05a5d-151">**ตัวอย่างอัตราต้นทุน**</span><span class="sxs-lookup"><span data-stu-id="05a5d-151">**Sample cost rates**</span></span>

| <span data-ttu-id="05a5d-152">แถบเงินเดือน</span><span class="sxs-lookup"><span data-stu-id="05a5d-152">Salary Band</span></span>     | <span data-ttu-id="05a5d-153">หน่วยองค์กร</span><span class="sxs-lookup"><span data-stu-id="05a5d-153">Org Unit</span></span>    |<span data-ttu-id="05a5d-154">หน่วย</span><span class="sxs-lookup"><span data-stu-id="05a5d-154">Unit</span></span>      |<span data-ttu-id="05a5d-155">ราคา</span><span class="sxs-lookup"><span data-stu-id="05a5d-155">Price</span></span>      |<span data-ttu-id="05a5d-156">สกุลเงิน</span><span class="sxs-lookup"><span data-stu-id="05a5d-156">Currency</span></span>  |
| ----------------|-------------|----------|----------:|----------|
| <span data-ttu-id="05a5d-157">บริษัทของฉัน_Band1</span><span class="sxs-lookup"><span data-stu-id="05a5d-157">My company_Band1</span></span> | <span data-ttu-id="05a5d-158">Contoso US</span><span class="sxs-lookup"><span data-stu-id="05a5d-158">Contoso US</span></span>  |<span data-ttu-id="05a5d-159">Hour</span><span class="sxs-lookup"><span data-stu-id="05a5d-159">Hour</span></span> | <span data-ttu-id="05a5d-160">145</span><span class="sxs-lookup"><span data-stu-id="05a5d-160">145</span></span>|<span data-ttu-id="05a5d-161">USD</span><span class="sxs-lookup"><span data-stu-id="05a5d-161">USD</span></span>     |
| <span data-ttu-id="05a5d-162">บริษัทของฉัน_Band2</span><span class="sxs-lookup"><span data-stu-id="05a5d-162">My company_Band2</span></span> | <span data-ttu-id="05a5d-163">Contoso India</span><span class="sxs-lookup"><span data-stu-id="05a5d-163">Contoso India</span></span> |<span data-ttu-id="05a5d-164">Hour</span><span class="sxs-lookup"><span data-stu-id="05a5d-164">Hour</span></span>|   <span data-ttu-id="05a5d-165">67</span><span class="sxs-lookup"><span data-stu-id="05a5d-165">67</span></span>|<span data-ttu-id="05a5d-166">USD</span><span class="sxs-lookup"><span data-stu-id="05a5d-166">USD</span></span>     |
