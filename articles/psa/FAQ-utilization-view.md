---
title: ดูการใช้ประโยชน์ที่คิดค่าธรรมเนียมได้สำหรับทรัพยากร
description: หัวข้อนี้แสดงข้อมูลเกี่ยวกับมุมมองการใช้ประโยชน์ของทรัพยากร
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 9/26/2019
ms.topic: article
ms.author: ruhercul
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: 4516c562e7eaf35c5fef638183967eef5a033b11
ms.sourcegitcommit: 418fa1fe9d605b8faccc2d5dee1b04b4e753f194
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 02/10/2021
ms.locfileid: "5146416"
---
# <a name="view-chargeable-utilization-for-resources"></a><span data-ttu-id="c45b1-103">ดูการใช้ประโยชน์ที่คิดค่าธรรมเนียมได้สำหรับทรัพยากร</span><span class="sxs-lookup"><span data-stu-id="c45b1-103">View chargeable utilization for resources</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]
 
<span data-ttu-id="c45b1-104">**มุมมองการใช้ประโยชน์** บนเพจ **การใช้ประโยชน์ Project Service** แสดงการใช้ประโยชน์ที่คิดค่าธรรมเนียมได้สำหรับแต่ละทรัพยากรที่จองได้</span><span class="sxs-lookup"><span data-stu-id="c45b1-104">The **Utilization View** on the **Project Service Resource Utilization** page shows the chargeable utilization for each bookable resource.</span></span> <span data-ttu-id="c45b1-105">เนื่องจากมุมมองจะขึ้นอยู่กับตารางกำหนดการ ดังนั้นคุณจะพบฟังก์ชันเดียวกันจำนวนมาก</span><span class="sxs-lookup"><span data-stu-id="c45b1-105">Because the view is based on the schedule board, you’ll find many of the same functions.</span></span>

> ![ภาพหน้าจอของมุมมองการใช้ประโยชน์](media/FAQ-utilization-1.png)
 

<span data-ttu-id="c45b1-107">การคำนวณการใช้ประโยชน์ที่คิดค่าธรรมเนียมได้ทำงานดังต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="c45b1-107">The chargeable utilization calculation works as follows:</span></span>

   <span data-ttu-id="c45b1-108">การใช้ประโยชน์ที่คิดค่าธรรมเนียมได้ = (ชั่วโมงที่คิดค่าธรรมเนียมได้จริง) / (กำลังการผลิตทรัพยากร)</span><span class="sxs-lookup"><span data-stu-id="c45b1-108">Chargeable utilization = (Chargeable actual hours) / (resource capacity)</span></span>

<span data-ttu-id="c45b1-109">เซลล์แสดงถึงการใช้ประโยชน์ที่คิดค่าธรรมเนียมได้ซึ่งถูกคำนวณ สำหรับรอบระยะเวลาที่ถูกเลือก (วัน, สัปดาห์, หรือเดือน)</span><span class="sxs-lookup"><span data-stu-id="c45b1-109">The cells represent the calculated chargeable utilization for the selected period (days, weeks, or months).</span></span>

<span data-ttu-id="c45b1-110">สีในแต่ละเซลล์แสดงการใช้ประโยชน์ที่คิดค่าธรรมเนียมได้สำหรับทรัพยากร ตามที่เปรียบเทียบกับการใช้ประโยชน์ที่คิดค่าธรรมเนียมได้ของเป้าหมายของพวกเขา</span><span class="sxs-lookup"><span data-stu-id="c45b1-110">The colors in each cell show the chargeable utilization for a resource as compared to their target chargeable utilization.</span></span> 

<span data-ttu-id="c45b1-111">คุณสามารถตั้งการใช้งานเป้าหมายได้บนบทบาทค่าเริ่มต้นของทรัพยากร หรือตัวทรัพยากรแต่ละทรัพยากรเอง</span><span class="sxs-lookup"><span data-stu-id="c45b1-111">The target utilization can be set on the resource’s default role or on the individual resource itself.</span></span> <span data-ttu-id="c45b1-112">การคำนวณพิจารณาจากแต่ละรายการสำหรับเป้าหมายก่อน แล้วไปที่บทบาทค่าเริ่มต้นของทรัพยากร</span><span class="sxs-lookup"><span data-stu-id="c45b1-112">The calculation looks at the individual for the target first, and then to the resource’s default role.</span></span>

## <a name="set-target-on-a-resource"></a><span data-ttu-id="c45b1-113">การตั้งค่าเป้าหมายในทรัพยากร</span><span class="sxs-lookup"><span data-stu-id="c45b1-113">Set target on a resource</span></span>

1. <span data-ttu-id="c45b1-114">ไปที่ **ทรัพยากร** \> **ทรัพยากร**</span><span class="sxs-lookup"><span data-stu-id="c45b1-114">Go to **Resources** \> **Resources**.</span></span> 
2. <span data-ttu-id="c45b1-115">เลือกทรัพยากรที่จะเปิดเรกคอร์ด</span><span class="sxs-lookup"><span data-stu-id="c45b1-115">Select a resource to open the record.</span></span> 
3. <span data-ttu-id="c45b1-116">บนแท็บ **Project Service** คุณสามารถตั้งค่าการใช้งานเป้าหมายของทรัพยากรได้</span><span class="sxs-lookup"><span data-stu-id="c45b1-116">On the **Project Service** tab, you can set the resource’s target utilization.</span></span>

> ![ภาพหน้าจอของการใช้แท็บ Project Service เมื่อต้องการตั้งการใช้ประโยชน์เป้าหมาย](media/FAQ-utilization-2.png)
 
## <a name="set-target-utilization-on-a-role"></a><span data-ttu-id="c45b1-118">ตั้งค่าการใช้ประโยชน์เป้าหมายในบทบาท</span><span class="sxs-lookup"><span data-stu-id="c45b1-118">Set target utilization on a role</span></span>

1. <span data-ttu-id="c45b1-119">ไปที่ **ทรัพยากร** \> **บทบาทของทรัพยากร**</span><span class="sxs-lookup"><span data-stu-id="c45b1-119">Go to **Resources** \> **Resource Roles**.</span></span> 
2. <span data-ttu-id="c45b1-120">เลือกบทบาทและเปิดเรกคอร์ด</span><span class="sxs-lookup"><span data-stu-id="c45b1-120">Select a role and open the record.</span></span> 
3. <span data-ttu-id="c45b1-121">ตั้งการใช้ประโยชน์เป้าหมายสำหรับบทบาท</span><span class="sxs-lookup"><span data-stu-id="c45b1-121">Set the target utilization for the role.</span></span>

> ![ภาพหน้าจอของการใช้บทบาทของทรัพยากร เมื่อต้องการตั้งการใช้ประโยชน์เป้าหมาย](media/FAQ-utilization-3.png)
 
## <a name="calculate-chargeable-utilization-for-a-resource"></a><span data-ttu-id="c45b1-123">คำนวณการใช้ประโยชน์ที่คิดค่าธรรมเนียมได้สำหรับทรัพยากร</span><span class="sxs-lookup"><span data-stu-id="c45b1-123">Calculate chargeable utilization for a resource</span></span>

<span data-ttu-id="c45b1-124">เพื่อคำนวณการใช้ประโยชน์ที่คิดค่าธรรมเนียมได้สำหรับทรัพยากร คุณจำเป็นต้องทำข้อกำหนดเบื้องต้นบางข้อให้สำเร็จ</span><span class="sxs-lookup"><span data-stu-id="c45b1-124">To calculate chargeable utilization for a resource, you will need to complete some pre-requisites.</span></span> 

### <a name="set-default-role-for-individual-resource"></a><span data-ttu-id="c45b1-125">ตั้งค่าบทบาทเริ่มต้นสำหรับทรัพยากรแต่ละรายการ</span><span class="sxs-lookup"><span data-stu-id="c45b1-125">Set default role for individual resource</span></span>

<span data-ttu-id="c45b1-126">อันดับแรก การใช้ประโยชน์เป้าหมายต้องถูกตั้งค่าบนแต่ละทรัพยากรหรือบทบาททรัพยากร</span><span class="sxs-lookup"><span data-stu-id="c45b1-126">First, the target utilization must be set on either the individual resource or on resource roles.</span></span> <span data-ttu-id="c45b1-127">ถ้าคุณกำลังใช้บทบาททรัพยากรสำหรับเป้าหมาย ทรัพยากรแต่ละรายการต้องมีบทบาทเริ่มต้น</span><span class="sxs-lookup"><span data-stu-id="c45b1-127">If you are using resource roles for targets, each individual resource must have a default role.</span></span> 

1. <span data-ttu-id="c45b1-128">เพื่อตั้งค่านี้ ไปที่ **ทรัพยากร** \> **ทรัพยากร**</span><span class="sxs-lookup"><span data-stu-id="c45b1-128">To set this, go to **Resources** \> **Resources**.</span></span> 
2. <span data-ttu-id="c45b1-129">เลือกทรัพยากร, เปิดเรกคอร์ด และจากนั้นเลือกแท็บ **Project Service**</span><span class="sxs-lookup"><span data-stu-id="c45b1-129">Select a resource, open the record, and then select the **Project Service** tab.</span></span> 
3. <span data-ttu-id="c45b1-130">ในกริด **บทบาททรัพยากร** ตรวจสอบให้แน่ใจว่ามีบทบาทหนึ่งสำหรับทรัพยากร และ **เป็นค่าเริ่มต้น** ตั้งค่าไว้เป็น **ใช่**</span><span class="sxs-lookup"><span data-stu-id="c45b1-130">In the **Resource Role** grid, make sure there’s one role for the resource and **Is Default** is set to **Yes**.</span></span>
 
### <a name="change-billing-type-for-resource-role"></a><span data-ttu-id="c45b1-131">เปลี่ยนชนิดการเรียกเก็บเงินสำหรับบทบาทของทรัพยากร</span><span class="sxs-lookup"><span data-stu-id="c45b1-131">Change billing type for resource role</span></span>

<span data-ttu-id="c45b1-132">บทบาททรัพยากรต้องถูกตั้งค่าให้มีชนิดการเรียกเก็บเงินเป็น **สามารถคิดค่าธรรมเนียมได้**</span><span class="sxs-lookup"><span data-stu-id="c45b1-132">The resource roles must be set to have a billing type of **Chargeable**.</span></span> 

1. <span data-ttu-id="c45b1-133">ไปที่ **ทรัพยากร** \> **บทบาทของทรัพยากร**</span><span class="sxs-lookup"><span data-stu-id="c45b1-133">Go to **Resources** \> **Resource Roles**.</span></span> 
2. <span data-ttu-id="c45b1-134">เปิดเรกคอร์ดที่คุณต้องการปรับปรุง และจากนั้น ตั้งค่าค่าเริ่มต้นชนิดการเรียกเก็บเงิน เป็น **คิดค่าธรรมเนียมได้**</span><span class="sxs-lookup"><span data-stu-id="c45b1-134">Open the record you want to update, and then set the billing type default to **Chargeable**.</span></span>

### <a name="set-working-hours-for-resource-role"></a><span data-ttu-id="c45b1-135">ตั้งค่าชั่วโมงทำงานสำหรับบทบาททรัพยากร</span><span class="sxs-lookup"><span data-stu-id="c45b1-135">Set working hours for resource role</span></span>
 
<span data-ttu-id="c45b1-136">ทรัพยากรต้องมีชั่วโมงการทำงานสำหรับการคำนวณกำลังการผลิต</span><span class="sxs-lookup"><span data-stu-id="c45b1-136">The resource must have working hours for the capacity calculation.</span></span> 

1. <span data-ttu-id="c45b1-137">ไปที่ **ทรัพยากร** \> **ทรัพยากร**</span><span class="sxs-lookup"><span data-stu-id="c45b1-137">Go to **Resources** \> **Resources**.</span></span> 
2. <span data-ttu-id="c45b1-138">เลือกทรัพยากรเพื่อเปิดเรกคอร์ด และจากนั้นเลือก **แสดงชั่วโมงการทำงาน**</span><span class="sxs-lookup"><span data-stu-id="c45b1-138">Select a resource to open the record, and then select **Show Work Hours**.</span></span> 
3. <span data-ttu-id="c45b1-139">คุณสามารถปรับปรุงรายการของทรัพยากรจำนวนมากได้ โดยการใช้ **เท็มเพลตชั่วโมงการทำงาน** จากมุมมอง **รายการทรัพยากร**</span><span class="sxs-lookup"><span data-stu-id="c45b1-139">You can bulk-update the list of resources by applying a **Work Hour Template** from the **Resource List** view.</span></span>

## <a name="troubleshooting-chargeable-actual-hours"></a><span data-ttu-id="c45b1-140">การแก้ไขปัญหาชั่วโมงที่คิดค่าธรรมเนียมได้จริง</span><span class="sxs-lookup"><span data-stu-id="c45b1-140">Troubleshooting chargeable actual hours</span></span>

<span data-ttu-id="c45b1-141">ชั่วโมงที่คิดค่าธรรมเนียมได้จริงมีที่มาจากเอนทิตี **ตามจริง**</span><span class="sxs-lookup"><span data-stu-id="c45b1-141">The chargeable actual hours are sourced from the **Actuals** entity.</span></span> <span data-ttu-id="c45b1-142">รายการเกิดขึ้นจริงกับชนิดของการเรียกเก็บเงินที่ **คิดค่าธรรมเนียมได้** จะถูกรวมในการคำนวณ และด้วยเหตุนี้ คุณต้องมีโครงการที่จะคิดค่าธรรมเนียมรายการจริงได้</span><span class="sxs-lookup"><span data-stu-id="c45b1-142">Actuals with a billing type of **Chargeable** are included in the calculation and, for this reason, you must have projects where the actuals that are chargeable.</span></span>

<span data-ttu-id="c45b1-143">ถ้าคุณไม่เห็นการใช้งานที่คิดค่าธรรมเนียม ต่อไปนี้เป็นบางสิ่งที่คุณสามารถตรวจสอบได้:</span><span class="sxs-lookup"><span data-stu-id="c45b1-143">If you are not seeing chargeable utilization, here are some things you can check:</span></span>

- <span data-ttu-id="c45b1-144">ทรัพยากรมีชั่วโมงทำงานที่กำหนดไว้สำหรับกำลังการผลิต</span><span class="sxs-lookup"><span data-stu-id="c45b1-144">The resource has working hours defined for capacity.</span></span>
- <span data-ttu-id="c45b1-145">ทรัพยากรมีการเป้าหมายการใช้ประโยชน์ที่กำหนดแต่ละรายการ หรือมีบทบาทเริ่มต้นที่กำหนดไว้ อย่างใดอย่างหนึ่ง</span><span class="sxs-lookup"><span data-stu-id="c45b1-145">The resource has either an individually defined utilization target or has a default role assigned to it.</span></span> <span data-ttu-id="c45b1-146">บทบาทมีเป้าหมายของการใช้ประโยชน์ที่กำหนดไว้</span><span class="sxs-lookup"><span data-stu-id="c45b1-146">The role has a utilization target defined for it.</span></span>
- <span data-ttu-id="c45b1-147">รายการจริงมีชนิดของการเรียกเก็บเงินที่ **คิดค่าธรรมเนียมได้** สำหรับรอบระยะเวลาคุณคาดหวังว่าจะคำนวณการใช้ประโยชน์</span><span class="sxs-lookup"><span data-stu-id="c45b1-147">Actuals have a billing type of **Chargeable** for the period you are expecting a utilization calculation for.</span></span> <span data-ttu-id="c45b1-148">ถ้าคุณเห็นรายการจริงที่มีการเรียกเก็บเงินชนิดอื่นที่ไม่ใช่ แบบคิดค่าธรรมเนียมได้ ให้ตรวจสอบสิ่งต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="c45b1-148">Check the following if you are seeing actuals with billing types other than chargeable:</span></span>

  - <span data-ttu-id="c45b1-149">บทบาทที่ใช้ในรายการจริงมีชนิดการเรียกเก็บเงินเริ่มต้นชนิดของบางสิ่ง นอกเหนือจากที่คิดค่าธรรมเนียมได้</span><span class="sxs-lookup"><span data-stu-id="c45b1-149">The role used on the actual has a default billing type of something other than chargeable.</span></span>
  - <span data-ttu-id="c45b1-150">บทบาทในรายละเอียดการให้บริการตามสัญญาของโครงการที่สนับสนุนโครงการ ได้ถูกตั้งค่าให้ไม่คิดค่าธรรมเนียม</span><span class="sxs-lookup"><span data-stu-id="c45b1-150">The role on the project contract line backing the project has been set to non-chargeable.</span></span>
  - <span data-ttu-id="c45b1-151">แม่แบบสัญญานี้ไม่มีรายละเอียดการให้บริการตามสัญญาที่เชื่อมโยง</span><span class="sxs-lookup"><span data-stu-id="c45b1-151">The project does not have an associated contract line.</span></span>

