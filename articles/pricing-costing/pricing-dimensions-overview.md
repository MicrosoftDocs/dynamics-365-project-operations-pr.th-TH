---
title: ภาพรวมมิติการกำหนดราคา
description: หัวข้อนี้ให้ข้อมูลเกี่ยวกับมิติการกำหนดราคาใน Dynamics 365 Project Operations
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
ms.openlocfilehash: ec2e350e0e4c28ea1c9540d70c83fdf0a75dc408
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 10/28/2020
ms.locfileid: "4128486"
---
# <a name="pricing-dimensions-overview"></a><span data-ttu-id="e283d-103">ภาพรวมมิติการกำหนดราคา</span><span class="sxs-lookup"><span data-stu-id="e283d-103">Pricing dimensions overview</span></span>

<span data-ttu-id="e283d-104">_**นำไปใช้กับ:** Project Operations สำหรับสถานการณ์ที่อิงตามทรัพยากร/ที่ไม่ได้เก็บในสต็อก การปรับใช้ Lite - จัดการกับการออกใบแจ้งหนี้ชั่วคราว_</span><span class="sxs-lookup"><span data-stu-id="e283d-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="e283d-105">มิติที่ใช้ในทรัพยากรบุคคลเพื่อตั้งค่าการกำหนดราคาและการคิดต้นทุนจะแบ่งออกเป็นสองประเภท: </span><span class="sxs-lookup"><span data-stu-id="e283d-105">The dimensions that are used in human resources to set up pricing and costs fall into two categories:</span></span>

- <span data-ttu-id="e283d-106">บุคคล</span><span class="sxs-lookup"><span data-stu-id="e283d-106">People</span></span>
- <span data-ttu-id="e283d-107">งานตามแผน</span><span class="sxs-lookup"><span data-stu-id="e283d-107">Planned work</span></span>

<span data-ttu-id="e283d-108">ด้วยเหตุนี้ จึงมีมิติข้อมูลการกำหนดราคาสองประเภทที่พร้อมใช้งาน:</span><span class="sxs-lookup"><span data-stu-id="e283d-108">Because of this, there are two types of pricing dimension values available:</span></span>

- <span data-ttu-id="e283d-109">**ชุดตัวเลือก**: มิติที่มีการแจกแจกคงที่สำหรับชุดของค่า</span><span class="sxs-lookup"><span data-stu-id="e283d-109">**Option sets**: Dimensions that are fixed enumerations for a set of values.</span></span>
- <span data-ttu-id="e283d-110">**ค่าตามเอนทิตี**: มิติที่สามารถเป็นชุดของค่าที่หลากหลายได้</span><span class="sxs-lookup"><span data-stu-id="e283d-110">**Entity-based values**: Dimensions that can be a varied set of values.</span></span>

## <a name="pricing-dimensions"></a><span data-ttu-id="e283d-111">มิติการกำหนดราคา</span><span class="sxs-lookup"><span data-stu-id="e283d-111">Pricing dimensions</span></span>

<span data-ttu-id="e283d-112">Dynamics 365 Project Operations มาพร้อมกับชุดมิติการกำหนดราคาเริ่มต้น</span><span class="sxs-lookup"><span data-stu-id="e283d-112">Dynamics 365 Project Operations ships with a default set of pricing dimensions.</span></span> <span data-ttu-id="e283d-113">คุณสามารถมิติการกำหนดราคาเหล่านี้ได้โดยไปที่ **Project Operations** > **พารามิเตอร์**</span><span class="sxs-lookup"><span data-stu-id="e283d-113">You can view these pricing dimensions by going to **Project Operations** > **Parameters**.</span></span> <span data-ttu-id="e283d-114">ในบันทึกพารามิเตอร์ บนแท็บ **Amount-based pricing dimensions** ตรวจสอบบทบาทนั้น **msdyn_resourcecategory** และจัดเตรียมทรัพยากรหน่อยองค์กร **msdyn_organizationalunit** มีฟิล์ด **Applicable to sales** และ **Applicable to cost** ให้ตั้งเป็น **Yes**</span><span class="sxs-lookup"><span data-stu-id="e283d-114">In the parameter record, on the **Amount-based pricing dimensions** tab, verify that the role, **msdyn_resourcecategory** and resourcing organizational unit, **msdyn_organizationalunit** have the fields **Applicable to sales** and **Applicable to cost** set to **Yes**.</span></span> <span data-ttu-id="e283d-115">เมื่อเปิดใช้งานฟิลด์เหล่านี้ คุณสามารถตั้งค่าการกำหนดราคาและการคิดต้นทุนสำหรับทุกบทบาทและการรวมหน่วยองค์กร</span><span class="sxs-lookup"><span data-stu-id="e283d-115">With these fields enabled, you can set up the price and cost for each role and organizational unit combination.</span></span>

<span data-ttu-id="e283d-116">ถ้าคุณต้องการกำหนดราคาหรือคิดต้นทุนสำหรับทรัพยากรของคุณโดยใช้แอตทริบิวต์เพิ่มเติม คุณสามารถสร้างฟิล์ดที่กำหนดเอง เอนทิตี และมิติ</span><span class="sxs-lookup"><span data-stu-id="e283d-116">If you need to price or cost for your resources using additional attributes, you can create customized fields, entities, and dimensions.</span></span>

## <a name="pricing-human-resource-time"></a><span data-ttu-id="e283d-117">การกำหนดราคาเวลาทรัพยากรบุลคล</span><span class="sxs-lookup"><span data-stu-id="e283d-117">Pricing human resource time</span></span>
<span data-ttu-id="e283d-118">วิธีที่องค์กรกำหนดราคาเวลาทรัพยากรบุลคลมักจะเป็นการพิจารณาเชิงกุลยุทธ์ที่สำคัญที่ส่งผลกับผลกำไรขององค์กรโดยตรง</span><span class="sxs-lookup"><span data-stu-id="e283d-118">How an organization prices human resource time is often an important strategic consideration that directly affects the organization's profitability.</span></span> <span data-ttu-id="e283d-119">ทำงานร่วมกับทีมการเงินและปฏิบัติกับหัวหน้าเมื่อองค์กรของคุณพร้อมที่จะระบุวิธีที่ต้องการจะตั้งค่าบิลและอัตราต้นทุนสำหรับเวลาทรัพยยากรบุคคล</span><span class="sxs-lookup"><span data-stu-id="e283d-119">Work with the finance teams and practice heads when your organization is ready to identify how it wants to set up bill and cost rates for human resource time.</span></span>

<span data-ttu-id="e283d-120">การพิจารณาอื่นๆสำหรับการกำหนดราคารวมถึงว่าจะใช้ฟิล์ดหรือเอนทิตีซ้ำที่ไม่ใช่มิติการกำหนดราคาปัจจุบันแต่ใช้เป็นมิติการกำหนดราคาสำหรับองค์กรของคุณ</span><span class="sxs-lookup"><span data-stu-id="e283d-120">Other considerations for pricing include whether to re-use fields or entities that are not currently pricing dimensions but apply as a pricing dimension for your organization.</span></span> <span data-ttu-id="e283d-121">ฟิล์ดอย่าง **Transaction Category** (**msdyn_transactioncategory**) และ **Bookable Resource** (**bookableresource**) เป็นตัวอย่างของมิติที่น่าสนใจจ</span><span class="sxs-lookup"><span data-stu-id="e283d-121">Fields like **Transaction Category** (**msdyn_transactioncategory**) and **Bookable Resource** (**bookableresource**) are examples of candidate dimensions.</span></span> 

<span data-ttu-id="e283d-122">พิจารณาว่ามิติการกำหนดราคาของคุณควรจะเป็นแบบตารางหรือชุดตัวเลือก</span><span class="sxs-lookup"><span data-stu-id="e283d-122">Consider whether your pricing dimension should be a table or an option set.</span></span> <span data-ttu-id="e283d-123">ถ้าคุณรู้ว่าจะมีการเปลี่ยนแปลงมิติของค่าล่วงหน้าซึ่งจะเกิน 10 หรือ 12 และคุณต้องการแอตทริบิวต์เพิ่มเติมเกี่ยวกับค่าเหล่านี้ คุณสามารถสร้างเอนทิตีแทนที่จะเป็นชุดตัวเลือก</span><span class="sxs-lookup"><span data-stu-id="e283d-123">If you foresee changes to the values of a dimension which will exceed 10 or 12 and you need additional attributes on these values, you could create an entity rather than an option set.</span></span> <span data-ttu-id="e283d-124">การรักษาชุดตัวเลือกเช่น การเพิ่มหรือลดค่า ต้องใช้ผู้ดูแลหรือนักพัฒนาในขณะที่การเพิ่มแถวใหม่ไปในตารางสามารทำได้โดยผู้ใช้ส่วนใหญ่</span><span class="sxs-lookup"><span data-stu-id="e283d-124">Maintaining an option set, such as adding or removing values, requires an admin or developer whereas adding new rows to a table can be done by most users.</span></span>

<span data-ttu-id="e283d-125">ตัวอย่างต่อไปนี้แสดงอัตราการเรียกเก็บเงินที่ตั้งค่าตามบทบาทและหน่วยการจัดหาทรัพยากรองค์กรที่เป็นของทรัพยากร</span><span class="sxs-lookup"><span data-stu-id="e283d-125">The following example shows bill rates that are set up based on the role and the resourcing org unit to which the resource belongs.</span></span> <span data-ttu-id="e283d-126">อัตราต้นทุนโดยทั่วไปจะขึ้นอยู่กับแถบเงินเดือนของพนักงานและหน่วยองค์กรที่พนักงานเป็นสมาชิก</span><span class="sxs-lookup"><span data-stu-id="e283d-126">Cost rates are typically based on the salary band of the employee and the org unit that they belong to.</span></span> <span data-ttu-id="e283d-127">ตัวอย่างต่อไปนี้ ตารางอัตราเรียกเก็บเงินและอัตราต้นทุนจะมีลักษณะดังต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="e283d-127">In this example, the bill rate and cost rate tables will look like the following.</span></span>

<span data-ttu-id="e283d-128">**ตัวอย่างอัตราเรียกเก็บ**</span><span class="sxs-lookup"><span data-stu-id="e283d-128">**Sample bill rates**</span></span>

| <span data-ttu-id="e283d-129">บทบาท</span><span class="sxs-lookup"><span data-stu-id="e283d-129">Role</span></span>        | <span data-ttu-id="e283d-130">หน่วยองค์กร</span><span class="sxs-lookup"><span data-stu-id="e283d-130">Org Unit</span></span>    |<span data-ttu-id="e283d-131">หน่วย</span><span class="sxs-lookup"><span data-stu-id="e283d-131">Unit</span></span>      |<span data-ttu-id="e283d-132">ราคา</span><span class="sxs-lookup"><span data-stu-id="e283d-132">Price</span></span>      |<span data-ttu-id="e283d-133">สกุลเงิน</span><span class="sxs-lookup"><span data-stu-id="e283d-133">Currency</span></span>  |
| ------------|-------------|----------|----------:|----------|
| <span data-ttu-id="e283d-134">นักพัฒนา</span><span class="sxs-lookup"><span data-stu-id="e283d-134">Developer</span></span>   | <span data-ttu-id="e283d-135">Contoso US</span><span class="sxs-lookup"><span data-stu-id="e283d-135">Contoso US</span></span>  |<span data-ttu-id="e283d-136">Hour</span><span class="sxs-lookup"><span data-stu-id="e283d-136">Hour</span></span> | <span data-ttu-id="e283d-137">200</span><span class="sxs-lookup"><span data-stu-id="e283d-137">200</span></span>|<span data-ttu-id="e283d-138">USD</span><span class="sxs-lookup"><span data-stu-id="e283d-138">USD</span></span>     |
| <span data-ttu-id="e283d-139">นักพัฒนา</span><span class="sxs-lookup"><span data-stu-id="e283d-139">Developer</span></span>   | <span data-ttu-id="e283d-140">Contoso India</span><span class="sxs-lookup"><span data-stu-id="e283d-140">Contoso India</span></span> |<span data-ttu-id="e283d-141">Hour</span><span class="sxs-lookup"><span data-stu-id="e283d-141">Hour</span></span>|   <span data-ttu-id="e283d-142">112</span><span class="sxs-lookup"><span data-stu-id="e283d-142">112</span></span>|<span data-ttu-id="e283d-143">USD</span><span class="sxs-lookup"><span data-stu-id="e283d-143">USD</span></span>     |


<span data-ttu-id="e283d-144">**ตัวอย่างอัตราต้นทุน**</span><span class="sxs-lookup"><span data-stu-id="e283d-144">**Sample cost rates**</span></span>

| <span data-ttu-id="e283d-145">แถบเงินเดือน</span><span class="sxs-lookup"><span data-stu-id="e283d-145">Salary Band</span></span>     | <span data-ttu-id="e283d-146">หน่วยองค์กร</span><span class="sxs-lookup"><span data-stu-id="e283d-146">Org Unit</span></span>    |<span data-ttu-id="e283d-147">หน่วย</span><span class="sxs-lookup"><span data-stu-id="e283d-147">Unit</span></span>      |<span data-ttu-id="e283d-148">ราคา</span><span class="sxs-lookup"><span data-stu-id="e283d-148">Price</span></span>      |<span data-ttu-id="e283d-149">สกุลเงิน</span><span class="sxs-lookup"><span data-stu-id="e283d-149">Currency</span></span>  |
| ----------------|-------------|----------|----------:|----------|
| <span data-ttu-id="e283d-150">บริษัทของฉัน_Band1</span><span class="sxs-lookup"><span data-stu-id="e283d-150">My company_Band1</span></span> | <span data-ttu-id="e283d-151">Contoso US</span><span class="sxs-lookup"><span data-stu-id="e283d-151">Contoso US</span></span>  |<span data-ttu-id="e283d-152">Hour</span><span class="sxs-lookup"><span data-stu-id="e283d-152">Hour</span></span> | <span data-ttu-id="e283d-153">145</span><span class="sxs-lookup"><span data-stu-id="e283d-153">145</span></span>|<span data-ttu-id="e283d-154">USD</span><span class="sxs-lookup"><span data-stu-id="e283d-154">USD</span></span>     |
| <span data-ttu-id="e283d-155">บริษัทของฉัน_Band2</span><span class="sxs-lookup"><span data-stu-id="e283d-155">My company_Band2</span></span> | <span data-ttu-id="e283d-156">Contoso India</span><span class="sxs-lookup"><span data-stu-id="e283d-156">Contoso India</span></span> |<span data-ttu-id="e283d-157">Hour</span><span class="sxs-lookup"><span data-stu-id="e283d-157">Hour</span></span>|   <span data-ttu-id="e283d-158">67</span><span class="sxs-lookup"><span data-stu-id="e283d-158">67</span></span>|<span data-ttu-id="e283d-159">USD</span><span class="sxs-lookup"><span data-stu-id="e283d-159">USD</span></span>     |
