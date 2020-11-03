---
title: ตรวจทานทรัพยากรที่เสนอ
description: หัวข้อนี้แสดงข้อมูลเกี่ยวกับวิธีการเสนอทรัพยากรโครงการ
author: ruhercul
manager: AnnBe
ms.date: 09/23/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-customerservice
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: ruhercul
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: ad5cbdeb5fe05e6115eb024833a8d58b626ea4c9
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 10/16/2020
ms.locfileid: "4085899"
---
# <a name="review-proposed-resources"></a><span data-ttu-id="8a27c-103">ตรวจทานทรัพยากรที่เสนอ</span><span class="sxs-lookup"><span data-stu-id="8a27c-103">Review proposed resources</span></span>

<span data-ttu-id="8a27c-104">_**นำไปใช้กับ:** Project Operations สำหรับสถานการณ์ที่อิงตามทรัพยากร/ที่ไม่ได้เก็บในสต็อก การปรับใช้ Lite - จัดการกับการออกใบแจ้งหนี้ชั่วคราว_</span><span class="sxs-lookup"><span data-stu-id="8a27c-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="8a27c-105">ผู้จัดการทรัพยากรสามารถเสนอทรัพยากรกับผู้จัดการโครงการโดยใช้คำขอทรัพยากร</span><span class="sxs-lookup"><span data-stu-id="8a27c-105">Resource managers can propose a resource to the project manager by using a resource request.</span></span>

1. <span data-ttu-id="8a27c-106">จากกริดคำขอหรือตัวคำขอเอง ให้เลือก **ค้นหาทรัพยากร**</span><span class="sxs-lookup"><span data-stu-id="8a27c-106">From the request grid or the request itself, select **Find Resources**.</span></span>
2. <span data-ttu-id="8a27c-107">ในเพจ **ตัวช่วยจัดกำหนดการ** เลือกทรัพยากร และในบานหน้าต่าง **สร้างการจองทรัพยากร** ในฟิลด์ **สถานะการจอง** ให้เลือก **จอง**</span><span class="sxs-lookup"><span data-stu-id="8a27c-107">On the **Schedule Assistant** page, select the resource, and then, in the **Create Resource Booking** pane, in the **Booking Status** field, select **Book**.</span></span>

<span data-ttu-id="8a27c-108">การปรับปรุงสถานะต่อไปนี้เกิดขึ้น:</span><span class="sxs-lookup"><span data-stu-id="8a27c-108">The following status updates occur:</span></span>

- <span data-ttu-id="8a27c-109">ในหน้า **ตัวช่วยจัดกำหนดการ** จะมีการปรับปรุงตัวบ่งชี้สถานะเพื่อบ่งชี้ว่าการจองถูกเสนอไว้ ไม่ได้ถูกจองแบบตายตัว</span><span class="sxs-lookup"><span data-stu-id="8a27c-109">On the **Schedule Assistant** page, the status indicators are updated to indicate that the booking is proposed, not hard-booked.</span></span>
- <span data-ttu-id="8a27c-110">ในคำขอทรัพยากร สถานะจะถูกเปลี่ยนเป็น **ต้องมีการตรวจทาน**</span><span class="sxs-lookup"><span data-stu-id="8a27c-110">On the resource request, the status is changed to **Needs Review**.</span></span>
- <span data-ttu-id="8a27c-111">บนแท็บ **ทีม** ของโครงการ ค่า **สถานะคำขอ** ของสมาชิกทีมทั่วไปจะถูกเปลี่ยนเป็น **ต้องมีการตรวจทาน**</span><span class="sxs-lookup"><span data-stu-id="8a27c-111">On the **Team** tab of the project, the generic team member's **Request Status** value is changed to **Needs Review**.</span></span>

<span data-ttu-id="8a27c-112">ผู้จัดการโครงการสามารถยอมรับหรือปฏิเสธข้อเสนอได้</span><span class="sxs-lookup"><span data-stu-id="8a27c-112">The project manager can either accept or reject the proposal.</span></span>

<span data-ttu-id="8a27c-113">เมื่อผู้จัดการทรัพยากรประมวลผลการร้องขอทรัพยากร พวกเขาสามารถใช้วิธีการใดก็ได้จากวิธีการต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="8a27c-113">When resource managers process resource requests, they can use any of the following approaches:</span></span>

- <span data-ttu-id="8a27c-114">นำเสนอทรัพยากรหลายอย่างเพื่อตอบสนองความต้องการหากไม่มีทรัพยากรเดียวที่พร้อมใช้งานเพื่อตอบสนองชั่วโมงที่ต้องการ</span><span class="sxs-lookup"><span data-stu-id="8a27c-114">Propose multiple resources to satisfy the demand if no single resource is available to fulfill the required hours.</span></span> <span data-ttu-id="8a27c-115">ชั่วโมงที่เสนอจะถูกแบ่งระหว่างทรัพยากรหลายรายการที่สามารถตอบสนองชั่วโมงที่ต้องการ</span><span class="sxs-lookup"><span data-stu-id="8a27c-115">Proposed hours are then split among multiple resources that can satisfy the required hours.</span></span> <span data-ttu-id="8a27c-116">ในสถานการณ์สมมตินี้ ชั่วโมงไม่สามารถทับซ้อนกันได้</span><span class="sxs-lookup"><span data-stu-id="8a27c-116">In this scenario, the hours can't overlap.</span></span>
- <span data-ttu-id="8a27c-117">นำเสนอทรัพยากรน้อยกว่าที่ต้องการ</span><span class="sxs-lookup"><span data-stu-id="8a27c-117">Propose fewer resources than are required.</span></span> <span data-ttu-id="8a27c-118">ในสถานการณ์สมมตินี้ กำลังการผลิตทรัพยากรที่นำเสนอน้อยกว่าชั่วโมงที่ต้องการที่ผู้ขอระบุ</span><span class="sxs-lookup"><span data-stu-id="8a27c-118">In this scenario, the proposed resource capacity is less than the required hours that the requestor specified.</span></span> <span data-ttu-id="8a27c-119">ดังนั้น เมื่อผู้ขอยอมรับทรัพยากรที่เสนอ ความต้องการทรัพยากรที่ยังไม่บรรลุเป้าหมายจะถูกสร้างขึ้นเพื่อรวบรวมตามความต้องการที่เหลือ</span><span class="sxs-lookup"><span data-stu-id="8a27c-119">Therefore, when the requestor accepts the proposed resources, an unfulfilled resource requirement is created to capture the remaining demand.</span></span>
- <span data-ttu-id="8a27c-120">จองทรัพยากรหลายอย่างเพื่อตอบสนองความต้องการ หากไม่มีทรัพยากรเดียวที่พร้อมใช้งานเพื่อทำงานให้แล้วเสร็จ</span><span class="sxs-lookup"><span data-stu-id="8a27c-120">Book multiple resources to satisfy the demand if no single resource is available to complete the work.</span></span>
- <span data-ttu-id="8a27c-121">จองทรัพยากรน้อยกว่าที่ต้องการ</span><span class="sxs-lookup"><span data-stu-id="8a27c-121">Book fewer resources than are required.</span></span> <span data-ttu-id="8a27c-122">ในสถานการณ์สมมตินี้ ชั่วโมงที่จองน้อยกว่าชั่วโมงที่ต้องการ</span><span class="sxs-lookup"><span data-stu-id="8a27c-122">In this scenario, the booked hours are fewer than the required hours.</span></span> <span data-ttu-id="8a27c-123">ระบบจะแนะนำให้คุณนำเสนอทรัพยากรแทนการจอง เพื่อให้ผู้ร้องขอหรือสามารถตรวจสอบและติดตามความต้องการที่เหลืออยู่ได้</span><span class="sxs-lookup"><span data-stu-id="8a27c-123">The system guides you to propose resources instead of bookings, so that the requestor can verify and keep track of remaining demand.</span></span>

## <a name="billable-utilization"></a><span data-ttu-id="8a27c-124">การใช้ประโยชน์ที่เรียกเก็บเงินได้</span><span class="sxs-lookup"><span data-stu-id="8a27c-124">Billable utilization</span></span>

<span data-ttu-id="8a27c-125">ทรัพยากรสามารถมีการใช้ประโยชน์ที่เรียกเก็บเงินได้ของเป้าหมาย</span><span class="sxs-lookup"><span data-stu-id="8a27c-125">Resources can have a target billable utilization.</span></span> <span data-ttu-id="8a27c-126">การใช้ประโยชน์เป้าหมายนี้ถูกกำหนดเป็นแอตทริบิวต์ในบทบาทเริ่มต้นของทรัพยากร หรือตั้งค่าในเรกคอร์ดของทรัพยากรที่สามารถจองได้แต่ละรายการ</span><span class="sxs-lookup"><span data-stu-id="8a27c-126">This target utilization is either defined as an attribute on a resource's default role or set on the record of the individual bookable resource.</span></span> <span data-ttu-id="8a27c-127">การคำนวณการใช้ประโยชน์จะขึ้นอยู่กับชั่วโมงจริงที่ทรัพยากรได้ถูกรายงานโดยใช้รายการเวลาที่ได้รับอนุมัติ</span><span class="sxs-lookup"><span data-stu-id="8a27c-127">Utilization calculations are based on the actual hours that resources have reported by using approved time entries.</span></span>

<span data-ttu-id="8a27c-128">สูตรต่อไปนี้จะใช้ในการคำนวณการใช้ประโยชน์:</span><span class="sxs-lookup"><span data-stu-id="8a27c-128">The following formulas are used to calculate utilization:</span></span>

- <span data-ttu-id="8a27c-129">การใช้ประโยชน์ที่เรียกเก็บเงินได้ = ชั่วโมงที่คิดค่าธรรมเนียมจริง ÷ กำลังการผลิตทรัพยากร</span><span class="sxs-lookup"><span data-stu-id="8a27c-129">Billable utilization = Chargeable actual hours ÷ Resource capacity</span></span>
- <span data-ttu-id="8a27c-130">การใช้ประโยชน์ที่เรียกเก็บเงินไม่ได้ = เวลาจริงกับรหัสชนิดของการชำระเงิน = ไม่สามารถคิดค่าธรรมเนียมได้หรือไม่มีอยู่ ÷ กำลังการผลิตของทรัพยากร</span><span class="sxs-lookup"><span data-stu-id="8a27c-130">Non-billable utilization = Actual time with billing type ID = Non-chargeable, Complementary, or Not available ÷ Resource capacity</span></span>
- <span data-ttu-id="8a27c-131">ภายใน = เวลาจริงโดยไม่มีสัญญาขาย ÷ กำลังการผลิตของทรัพยากร</span><span class="sxs-lookup"><span data-stu-id="8a27c-131">Internal = Actual time with no sales contract ÷ Resource capacity</span></span>
- <span data-ttu-id="8a27c-132">กำลังการผลิตทรัพยากร = ชั่วโมงทำงานของทรัพยากร – ไม่อยู่ที่สำนักงาน – วันที่ไม่ใช่วันทำงาน</span><span class="sxs-lookup"><span data-stu-id="8a27c-132">Resource capacity = Resource work hours – Out-of-office – Non-working days</span></span>

<span data-ttu-id="8a27c-133">คุณสามารถพบมุมมอง **การใช้ประโยชน์ทรัพยากร** ได้ในบานหน้าต่าง **ทรัพยากร**</span><span class="sxs-lookup"><span data-stu-id="8a27c-133">You can find the **Resource Utilization** view in the **Resources** pane.</span></span>

<span data-ttu-id="8a27c-134">แต่ละเซลล์ในกริดแสดงเปอร์เซ็นต์การใช้ประโยชน์ที่เรียกเก็บเงินได้ของทรัพยากรในรอบระยะเวลานึง เช่นเป็นวัน เป็นสัปดาห์ หรือเป็นเดือน</span><span class="sxs-lookup"><span data-stu-id="8a27c-134">Each cell in the grid represents the billable utilization percentage of the resource in a period, such as a day, week, or month.</span></span> <span data-ttu-id="8a27c-135">สูตรต่อไปนี้จะใช้ในการลงสีให้เซลล์:</span><span class="sxs-lookup"><span data-stu-id="8a27c-135">The following formulas are used to color the cells:</span></span>

- <span data-ttu-id="8a27c-136">**สีเขียว:** การใช้ประโยชน์ที่เรียกเก็บเงินได้ \>= การใช้ประโยชน์เป้าหมายทรัพยากร</span><span class="sxs-lookup"><span data-stu-id="8a27c-136">**Green:** Billable utilization \>= Resource target utilization</span></span>
- <span data-ttu-id="8a27c-137">**สีเหลือง:** การใช้ประโยชน์เป้าหมาย – 20 \<= การใช้ประโยชน์ที่เรียกเก็บเงินได้ \< การใช้ประโยชน์เป้าหมาย</span><span class="sxs-lookup"><span data-stu-id="8a27c-137">**Yellow:** Target utilization – 20 \<= Billable utilization \< Target utilization</span></span>
- <span data-ttu-id="8a27c-138">**สีแดง:** การใช้ประโยชน์ที่เรียกเก็บเงินได้ \< การใช้ประโยชน์เป้าหมาย – 20</span><span class="sxs-lookup"><span data-stu-id="8a27c-138">**Red:** Billable utilization \< Target utilization – 20</span></span>

<span data-ttu-id="8a27c-139">เนื่องจากมุมมอง **การใช้ทรัพยากร** อิงตามตารางกำหนดการ คุณสามารถใช้ความสามารถในการกรองของตารางกำหนดการเพื่อกรองผลลัพธ์ของคุณได้</span><span class="sxs-lookup"><span data-stu-id="8a27c-139">Because the **Resource Utilization** view is based on the Schedule Board, you can use the filtering capabilities of the Schedule Board to filter your results.</span></span>

<span data-ttu-id="8a27c-140">กริดจำเป็นต้องให้คุณตั้งค่าการใช้ประโยชน์เป้าหมายในบทบาทหรือทรัพยากรแต่ละอย่าง</span><span class="sxs-lookup"><span data-stu-id="8a27c-140">The grid requires that you set a target utilization on either the role or the individual resource.</span></span> <span data-ttu-id="8a27c-141">เมื่อต้องการดำเนินการนี้ ไปที่ **ทรัพยากร** \> **บทบาทของทรัพยากร**</span><span class="sxs-lookup"><span data-stu-id="8a27c-141">To do this setup, go to **Resources** \> **Resource roles**.</span></span>

<span data-ttu-id="8a27c-142">นอกจากนี้ บทบาทเริ่มต้นต้องถูกมอบหมายให้กับทรัพยากรที่สามารถจองได้แต่ละรายการ</span><span class="sxs-lookup"><span data-stu-id="8a27c-142">Additionally, a default role must be assigned to each bookable resource.</span></span> <span data-ttu-id="8a27c-143">ไปที่ **ทรัพยากร** \> **ทรัพยากร**</span><span class="sxs-lookup"><span data-stu-id="8a27c-143">Go to **Resources** \> **Resources**.</span></span> <span data-ttu-id="8a27c-144">ในแท็บ **Project Service** ให้ตรวจสอบว่ามีการมอบหมายบทบาททรัพยากร และฟิลด์ **เป็นค่าเริ่มต้น** ถูกตั้งค่าเป็น **ใช่**</span><span class="sxs-lookup"><span data-stu-id="8a27c-144">On the **Project Service** tab, verify that a resource role is defined, and that the **Is Default** field for it is set to **Yes**.</span></span> <span data-ttu-id="8a27c-145">คุณสามารถเพิ่มบทบาทเพิ่มเติมที่การตั้งค่า **เป็นค่าเริ่มต้น = ไม่**</span><span class="sxs-lookup"><span data-stu-id="8a27c-145">You can add additional roles where **Is Default = No**.</span></span> <span data-ttu-id="8a27c-146">บทบาทที่ **เป็นค่าเริ่มต้น = ใช่** จะถูกใช้ในการประเมินผลการใช้ของทรัพยากรเทียบกับเป้าหมายสำหรับบทบาทนั้น</span><span class="sxs-lookup"><span data-stu-id="8a27c-146">The role where the **Is Default = Yes** is used to evaluate the resource's utilization against the target for that role.</span></span>

<span data-ttu-id="8a27c-147">บนแท็บ **Project Service** คุณสามารถตั้งค่าการใช้งานเป้าหมายแต่ละรายการสำหรับทรัพยากรได้ด้วย</span><span class="sxs-lookup"><span data-stu-id="8a27c-147">On the **Project Service** tab, you can also set an individual target utilization for the resource.</span></span> <span data-ttu-id="8a27c-148">การคำนวณการใช้ประโยชน์จะใช้การใช้ประโยชน์เป้าหมายนั้นเพื่อประเมินเป้าหมายของทรัพยากรแทนที่จะประเมินจากเป้าหมายของบทบาทเริ่มต้นของทรัพยากร</span><span class="sxs-lookup"><span data-stu-id="8a27c-148">The utilization calculation then uses that target utilization to evaluate the resource's target instead of the target of the resource's default role.</span></span>

<span data-ttu-id="8a27c-149">การใช้ประโยชน์จะแสดงขึ้นสำหรับทรัพยากรเท่านั้น หากทรัพยากรนั้นได้การรับอนุมัติ เวลาที่คิดค่าธรรมเนียมในระหว่างรอบระยะเวลาจะแสดงในกริด</span><span class="sxs-lookup"><span data-stu-id="8a27c-149">Utilization is shown for a resource only if that resource has approved, chargeable time during the period that is shown in the grid.</span></span>

## <a name="resource-availability"></a><span data-ttu-id="8a27c-150">ความพร้อมใช้งานของทรัพยากร</span><span class="sxs-lookup"><span data-stu-id="8a27c-150">Resource availability</span></span>

<span data-ttu-id="8a27c-151">สิ่งสำคัญคือตัวจัดการทรัพยากรสามารถดูความพร้อมใช้งานของทรัพยากรและปรับปรุงการจองได้</span><span class="sxs-lookup"><span data-stu-id="8a27c-151">It's critical that resource managers be able to view the availability of resources and update bookings.</span></span> <span data-ttu-id="8a27c-152">ในบางกรณี ไม่มีความต้องการอย่างเป็นทางการ (คำขอทรัพยากร) แต่ผู้จัดการทรัพยากรต้องตอบสนองต่อความต้องการที่ไม่ได้วางแผนไว้ ซึ่งมาจากช่องทางต่างๆ เช่นอีเมล ติดต่อทางโทรศัพท์หรือข้อความโต้ตอบแบบทันที</span><span class="sxs-lookup"><span data-stu-id="8a27c-152">In some cases, there is no formal demand (resource request), but a resource manager must respond to an unplanned demand that comes through channels such as an email, phone call, or instant message.</span></span> <span data-ttu-id="8a27c-153">ผู้จัดการทรัพยากรใช้ตารางกำหนดการเพื่อปรับปรุงทรัพยากรและการจอง</span><span class="sxs-lookup"><span data-stu-id="8a27c-153">Resource managers use the Schedule Board to update resources and bookings.</span></span>

<span data-ttu-id="8a27c-154">ชั่วโมงทำงานของทรัพยากรจะใช้เป็นข้อมูลพื้นฐานสำหรับการคำนวณความพร้อมของทรัพยากร</span><span class="sxs-lookup"><span data-stu-id="8a27c-154">Resource work hours are used as the basis for calculating the availability of a resource.</span></span> <span data-ttu-id="8a27c-155">การจองทรัพยากรจะใช้กำลังการผลิตของทรัพยากร</span><span class="sxs-lookup"><span data-stu-id="8a27c-155">Resource bookings consume the capacity of the resources.</span></span>

<span data-ttu-id="8a27c-156">ตารางกำหนดการจะใช้สีและแรเงาเพื่อแสดงการจอง ความพร้อมใช้งาน และการจองเกิน และยังมีสถานะของการจองอีกด้วย</span><span class="sxs-lookup"><span data-stu-id="8a27c-156">The Schedule Board uses colors and shading to show bookings, availability, and overbookings, and also the status of bookings.</span></span> <span data-ttu-id="8a27c-157">มีการตั้งค่าในการตั้งค่าของตารางกำหนดการช่วยให้คุณสามารถแสดงคำอธิบายแผนภูมิได้</span><span class="sxs-lookup"><span data-stu-id="8a27c-157">A setting in the Schedule Board settings lets you show a legend.</span></span>

<span data-ttu-id="8a27c-158">ถ้าลูกศรชี้ขวาปรากฏถัดจากทรัพยากรที่สามารถจองได้แต่ละรายการบนบอร์ดกำหนดการ ทรัพยากรนั้นจะสามารถถูกขยายเพื่อแสดงรายละเอียดของงานที่ทรัพยากรนั้นถูกจองกับงานนั้น</span><span class="sxs-lookup"><span data-stu-id="8a27c-158">If a right-pointing arrow appears next to an individual bookable resource on the Schedule Board, the resource can be expanded to show details of the work that the resource is booked on.</span></span>

<span data-ttu-id="8a27c-159">เนืองจาก Dynamics 365 Project Operations ใช้กลไกจัดการ Universal Resource Scheduling ถ้าคุณยังได้ติดตั้ง Dynamics 365 Field Service ไว้ คุณสามารถดูรายละเอียดของการจองทรัพยากรสำหรับโครงการ ใบสั่งงานและเอนทิตีอื่นๆ ที่คุณขยายการจัดกำหนดการให้</span><span class="sxs-lookup"><span data-stu-id="8a27c-159">Because Dynamics 365 Project Operations uses the Universal Resource Scheduling engine, if you also have Dynamics 365 Field Service installed, you can view the details of resource bookings for projects, work orders, and any other entities that you've extended scheduling to.</span></span>

<span data-ttu-id="8a27c-160">หากต้องการดูรายละเอียดเพิ่มเติมเกี่ยวกับทรัพยากรแต่ละรายการ ให้คลิกขวาเพื่อเปิดบัตรทรัพยากร</span><span class="sxs-lookup"><span data-stu-id="8a27c-160">To view more details about an individual resource, right-click it to open the resource card.</span></span>

