---
title: เสนอทรัพยากรโครงการ
description: หัวข้อนี้แสดงข้อมูลเกี่ยวกับการเสนอทรัพยากรโครงการ
author: ruhercul
ms.custom:
- dyn365-projectservice
ms.date: 03/28/2019
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
ms.openlocfilehash: 02e47338e34a37e05455e2bc6e6a175210ed6bc7
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 05/10/2021
ms.locfileid: "5997984"
---
# <a name="propose-project-resources"></a><span data-ttu-id="8072c-103">เสนอทรัพยากรโครงการ</span><span class="sxs-lookup"><span data-stu-id="8072c-103">Propose project resources</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

<span data-ttu-id="8072c-104">ผู้จัดการทรัพยากรสามารถเสนอทรัพยากรกับผู้จัดการโครงการโดยใช้คำขอทรัพยากร</span><span class="sxs-lookup"><span data-stu-id="8072c-104">Resource managers can propose a resource to the project manager by using a resource request.</span></span>

1. <span data-ttu-id="8072c-105">จากกริดคำขอหรือตัวคำขอเอง ให้เลือก **ค้นหาทรัพยากร**</span><span class="sxs-lookup"><span data-stu-id="8072c-105">From the request grid or the request itself, select **Find Resources**.</span></span>
2. <span data-ttu-id="8072c-106">ในเพจ **ตัวช่วยจัดกำหนดการ** เลือกทรัพยากร และในบานหน้าต่าง **สร้างการจองทรัพยากร** ในฟิลด์ **สถานะการจอง** ให้เลือก **จอง**</span><span class="sxs-lookup"><span data-stu-id="8072c-106">On the **Schedule Assistant** page, select the resource, and then, in the **Create Resource Booking** pane, in the **Booking Status** field, select **Book**.</span></span>

    ![ทรัพยากรที่เคยเสนอถูกเลือก](media/Resource-Management-image62.png)

<span data-ttu-id="8072c-108">การปรับปรุงสถานะต่อไปนี้เกิดขึ้น:</span><span class="sxs-lookup"><span data-stu-id="8072c-108">The following status updates occur:</span></span>

- <span data-ttu-id="8072c-109">ในหน้า **ตัวช่วยจัดกำหนดการ** จะมีการปรับปรุงตัวบ่งชี้สถานะเพื่อบ่งชี้ว่าการจองถูกเสนอไว้ ไม่ได้ถูกจองแบบตายตัว</span><span class="sxs-lookup"><span data-stu-id="8072c-109">On the **Schedule Assistant** page, the status indicators are updated to indicate that the booking is proposed, not hard-booked.</span></span>

    ![ตัวบ่งชี้สถานะสำหรับการจองที่เสนอบนเพจตัวช่วยจัดกำหนดการ](media/Resource-Management-image63.png)

- <span data-ttu-id="8072c-111">ในคำขอทรัพยากร สถานะจะถูกเปลี่ยนเป็น **ต้องมีการตรวจทาน**</span><span class="sxs-lookup"><span data-stu-id="8072c-111">On the resource request, the status is changed to **Needs Review**.</span></span>

    ![สถานะของคำขอทรัพยากรถูกเปลี่ยนเป็น ต้องมีการตรวจทาน](media/Resource-Management-image64.png)

- <span data-ttu-id="8072c-113">บนแท็บ **ทีม** ของโครงการ ค่า **สถานะคำขอ** ของสมาชิกทีมทั่วไปจะถูกเปลี่ยนเป็น **ต้องมีการตรวจทาน**</span><span class="sxs-lookup"><span data-stu-id="8072c-113">On the **Team** tab of the project, the generic team member's **Request Status** value is changed to **Needs Review**.</span></span>

    ![สถานะคำของของสมาชิกทีมทั่วไปจะถูกเปลี่ยนเป็น ต้องมีการตรวจทาน ในแท็บทีม](media/Resource-Management-image48.png)

<span data-ttu-id="8072c-115">ผู้จัดการโครงการสามารถยอมรับหรือปฏิเสธข้อเสนอได้</span><span class="sxs-lookup"><span data-stu-id="8072c-115">The project manager can either accept or reject the proposal.</span></span>

<span data-ttu-id="8072c-116">เมื่อผู้จัดการทรัพยากรประมวลผลการร้องขอทรัพยากร พวกเขาสามารถใช้วิธีการใดก็ได้จากวิธีการต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="8072c-116">When resource managers process resource requests, they can use any of the following approaches:</span></span>

- <span data-ttu-id="8072c-117">นำเสนอทรัพยากรหลายอย่างเพื่อตอบสนองความต้องการหากไม่มีทรัพยากรเดียวที่พร้อมใช้งานเพื่อตอบสนองชั่วโมงที่ต้องการ</span><span class="sxs-lookup"><span data-stu-id="8072c-117">Propose multiple resources to satisfy the demand if no single resource is available to fulfill the required hours.</span></span> <span data-ttu-id="8072c-118">ชั่วโมงที่เสนอจะถูกแบ่งระหว่างทรัพยากรหลายรายการที่สามารถตอบสนองชั่วโมงที่ต้องการ</span><span class="sxs-lookup"><span data-stu-id="8072c-118">Proposed hours are then split among multiple resources that can satisfy the required hours.</span></span> <span data-ttu-id="8072c-119">ในสถานการณ์สมมตินี้ ชั่วโมงไม่สามารถทับซ้อนกันได้</span><span class="sxs-lookup"><span data-stu-id="8072c-119">In this scenario, the hours can't overlap.</span></span>
- <span data-ttu-id="8072c-120">นำเสนอทรัพยากรน้อยกว่าที่ต้องการ</span><span class="sxs-lookup"><span data-stu-id="8072c-120">Propose fewer resources than are required.</span></span> <span data-ttu-id="8072c-121">ในสถานการณ์สมมตินี้ กำลังการผลิตทรัพยากรที่นำเสนอน้อยกว่าชั่วโมงที่ต้องการที่ผู้ขอระบุ</span><span class="sxs-lookup"><span data-stu-id="8072c-121">In this scenario, the proposed resource capacity is less than the required hours that the requestor specified.</span></span> <span data-ttu-id="8072c-122">ดังนั้น เมื่อผู้ขอยอมรับทรัพยากรที่เสนอ ความต้องการทรัพยากรที่ยังไม่บรรลุเป้าหมายจะถูกสร้างขึ้นเพื่อรวบรวมตามความต้องการที่เหลือ</span><span class="sxs-lookup"><span data-stu-id="8072c-122">Therefore, when the requestor accepts the proposed resources, an unfulfilled resource requirement is created to capture the remaining demand.</span></span>
- <span data-ttu-id="8072c-123">จองทรัพยากรหลายอย่างเพื่อตอบสนองความต้องการ หากไม่มีทรัพยากรเดียวที่พร้อมใช้งานเพื่อทำงานให้แล้วเสร็จ</span><span class="sxs-lookup"><span data-stu-id="8072c-123">Book multiple resources to satisfy the demand if no single resource is available to complete the work.</span></span>
- <span data-ttu-id="8072c-124">จองทรัพยากรน้อยกว่าที่ต้องการ</span><span class="sxs-lookup"><span data-stu-id="8072c-124">Book fewer resources than are required.</span></span> <span data-ttu-id="8072c-125">ในสถานการณ์สมมตินี้ ชั่วโมงที่จองน้อยกว่าชั่วโมงที่ต้องการ</span><span class="sxs-lookup"><span data-stu-id="8072c-125">In this scenario, the booked hours are fewer than the required hours.</span></span> <span data-ttu-id="8072c-126">ระบบจะแนะนำให้คุณนำเสนอทรัพยากรแทนการจอง เพื่อให้ผู้ร้องขอหรือสามารถตรวจสอบและติดตามความต้องการที่เหลืออยู่ได้</span><span class="sxs-lookup"><span data-stu-id="8072c-126">The system guides you to propose resources instead of bookings, so that the requestor can verify and keep track of remaining demand.</span></span>

## <a name="billable-utilization"></a><span data-ttu-id="8072c-127">การใช้ประโยชน์ที่เรียกเก็บเงินได้</span><span class="sxs-lookup"><span data-stu-id="8072c-127">Billable utilization</span></span>

<span data-ttu-id="8072c-128">ทรัพยากรสามารถมีการใช้ประโยชน์ที่เรียกเก็บเงินได้ของเป้าหมาย</span><span class="sxs-lookup"><span data-stu-id="8072c-128">Resources can have a target billable utilization.</span></span> <span data-ttu-id="8072c-129">การใช้ประโยชน์เป้าหมายนี้ถูกกำหนดเป็นแอตทริบิวต์ในบทบาทเริ่มต้นของทรัพยากร หรือตั้งค่าในเรกคอร์ดของทรัพยากรที่สามารถจองได้แต่ละรายการ</span><span class="sxs-lookup"><span data-stu-id="8072c-129">This target utilization is either defined as an attribute on a resource's default role or set on the record of the individual bookable resource.</span></span> <span data-ttu-id="8072c-130">การคำนวณการใช้ประโยชน์จะขึ้นอยู่กับชั่วโมงจริงที่ทรัพยากรได้ถูกรายงานโดยใช้รายการเวลาที่ได้รับอนุมัติ</span><span class="sxs-lookup"><span data-stu-id="8072c-130">Utilization calculations are based on the actual hours that resources have reported by using approved time entries.</span></span>

<span data-ttu-id="8072c-131">สูตรต่อไปนี้จะใช้ในการคำนวณการใช้ประโยชน์:</span><span class="sxs-lookup"><span data-stu-id="8072c-131">The following formulas are used to calculate utilization:</span></span>

- <span data-ttu-id="8072c-132">การใช้ประโยชน์ที่เรียกเก็บเงินได้ = ชั่วโมงที่คิดค่าธรรมเนียมจริง ÷ กำลังการผลิตทรัพยากร</span><span class="sxs-lookup"><span data-stu-id="8072c-132">Billable utilization = Chargeable actual hours ÷ Resource capacity</span></span>
- <span data-ttu-id="8072c-133">การใช้ประโยชน์ที่เรียกเก็บเงินไม่ได้ = เวลาจริงกับรหัสชนิดของการชำระเงิน = ไม่สามารถคิดค่าธรรมเนียมได้หรือไม่มีอยู่ ÷ กำลังการผลิตของทรัพยากร</span><span class="sxs-lookup"><span data-stu-id="8072c-133">Non-billable utilization = Actual time with billing type ID = Non-chargeable, Complementary, or Not available ÷ Resource capacity</span></span>
- <span data-ttu-id="8072c-134">ภายใน = เวลาจริงโดยไม่มีสัญญาขาย ÷ กำลังการผลิตของทรัพยากร</span><span class="sxs-lookup"><span data-stu-id="8072c-134">Internal = Actual time with no sales contract ÷ Resource capacity</span></span>
- <span data-ttu-id="8072c-135">กำลังการผลิตทรัพยากร = ชั่วโมงทำงานของทรัพยากร – ไม่อยู่ที่สำนักงาน – วันที่ไม่ใช่วันทำงาน</span><span class="sxs-lookup"><span data-stu-id="8072c-135">Resource capacity = Resource work hours – Out-of-office – Non-working days</span></span>

<span data-ttu-id="8072c-136">คุณสามารถพบมุมมอง **การใช้ประโยชน์ทรัพยากร** ได้ในบานหน้าต่าง **ทรัพยากร**</span><span class="sxs-lookup"><span data-stu-id="8072c-136">You can find the **Resource Utilization** view in the **Resources** pane.</span></span>

![มุมมองการใช้ประโยชน์ของทรัพยากร](media/Resource-Management-image65.png)

<span data-ttu-id="8072c-138">แต่ละเซลล์ในกริดแสดงเปอร์เซ็นต์การใช้ประโยชน์ที่เรียกเก็บเงินได้ของทรัพยากรในรอบระยะเวลานึง เช่นเป็นวัน เป็นสัปดาห์ หรือเป็นเดือน</span><span class="sxs-lookup"><span data-stu-id="8072c-138">Each cell in the grid represents the billable utilization percentage of the resource in a period, such as a day, week, or month.</span></span> <span data-ttu-id="8072c-139">สูตรต่อไปนี้จะใช้ในการลงสีให้เซลล์:</span><span class="sxs-lookup"><span data-stu-id="8072c-139">The following formulas are used to color the cells:</span></span>

- <span data-ttu-id="8072c-140">**สีเขียว:** การใช้ประโยชน์ที่เรียกเก็บเงินได้ \>= การใช้ประโยชน์เป้าหมายทรัพยากร</span><span class="sxs-lookup"><span data-stu-id="8072c-140">**Green:** Billable utilization \>= Resource target utilization</span></span>
- <span data-ttu-id="8072c-141">**สีเหลือง:** การใช้ประโยชน์เป้าหมาย – 20 \<= การใช้ประโยชน์ที่เรียกเก็บเงินได้ \< การใช้ประโยชน์เป้าหมาย</span><span class="sxs-lookup"><span data-stu-id="8072c-141">**Yellow:** Target utilization – 20 \<= Billable utilization \< Target utilization</span></span>
- <span data-ttu-id="8072c-142">**สีแดง:** การใช้ประโยชน์ที่เรียกเก็บเงินได้ \< การใช้ประโยชน์เป้าหมาย – 20</span><span class="sxs-lookup"><span data-stu-id="8072c-142">**Red:** Billable utilization \< Target utilization – 20</span></span>

<span data-ttu-id="8072c-143">เนื่องจากมุมมอง **การใช้ทรัพยากร** อิงตามตารางกำหนดการ คุณสามารถใช้ความสามารถในการกรองของตารางกำหนดการเพื่อกรองผลลัพธ์ของคุณได้</span><span class="sxs-lookup"><span data-stu-id="8072c-143">Because the **Resource Utilization** view is based on the Schedule Board, you can use the filtering capabilities of the Schedule Board to filter your results.</span></span>

<span data-ttu-id="8072c-144">กริดจำเป็นต้องให้คุณตั้งค่าการใช้ประโยชน์เป้าหมายในบทบาทหรือทรัพยากรแต่ละอย่าง</span><span class="sxs-lookup"><span data-stu-id="8072c-144">The grid requires that you set a target utilization on either the role or the individual resource.</span></span> <span data-ttu-id="8072c-145">เมื่อต้องการดำเนินการนี้ ไปที่ **ทรัพยากร** \> **บทบาทของทรัพยากร**</span><span class="sxs-lookup"><span data-stu-id="8072c-145">To do this setup, go to **Resources** \> **Resource roles**.</span></span>

<span data-ttu-id="8072c-146">นอกจากนี้ บทบาทเริ่มต้นต้องถูกมอบหมายให้กับทรัพยากรที่สามารถจองได้แต่ละรายการ</span><span class="sxs-lookup"><span data-stu-id="8072c-146">Additionally, a default role must be assigned to each bookable resource.</span></span> <span data-ttu-id="8072c-147">ไปที่ **ทรัพยากร** \> **ทรัพยากร**</span><span class="sxs-lookup"><span data-stu-id="8072c-147">Go to **Resources** \> **Resources**.</span></span> <span data-ttu-id="8072c-148">ในแท็บ **Project Service** ให้ตรวจสอบว่ามีการมอบหมายบทบาททรัพยากร และฟิลด์ **เป็นค่าเริ่มต้น** ถูกตั้งค่าเป็น **ใช่**</span><span class="sxs-lookup"><span data-stu-id="8072c-148">On the **Project Service** tab, verify that a resource role is defined, and that the **Is Default** field for it is set to **Yes**.</span></span> <span data-ttu-id="8072c-149">คุณสามารถเพิ่มบทบาทเพิ่มเติมที่การตั้งค่า **เป็นค่าเริ่มต้น = ไม่**</span><span class="sxs-lookup"><span data-stu-id="8072c-149">You can add additional roles where **Is Default = No**.</span></span> <span data-ttu-id="8072c-150">บทบาทที่ **เป็นค่าเริ่มต้น = ใช่** จะถูกใช้ในการประเมินผลการใช้ของทรัพยากรเทียบกับเป้าหมายสำหรับบทบาทนั้น</span><span class="sxs-lookup"><span data-stu-id="8072c-150">The role where the **Is Default = Yes** is used to evaluate the resource's utilization against the target for that role.</span></span>

![บทบาทเริ่มต้นถูกตั้งค่าแล้ว](media/Resource-Management-image67.png)

<span data-ttu-id="8072c-152">บนแท็บ **Project Service** คุณสามารถตั้งค่าการใช้งานเป้าหมายแต่ละรายการสำหรับทรัพยากรได้ด้วย</span><span class="sxs-lookup"><span data-stu-id="8072c-152">On the **Project Service** tab, you can also set an individual target utilization for the resource.</span></span> <span data-ttu-id="8072c-153">การคำนวณการใช้ประโยชน์จะใช้การใช้ประโยชน์เป้าหมายนั้นเพื่อประเมินเป้าหมายของทรัพยากรแทนที่จะประเมินจากเป้าหมายของบทบาทเริ่มต้นของทรัพยากร</span><span class="sxs-lookup"><span data-stu-id="8072c-153">The utilization calculation then uses that target utilization to evaluate the resource's target instead of the target of the resource's default role.</span></span>

<span data-ttu-id="8072c-154">การใช้ประโยชน์จะแสดงขึ้นสำหรับทรัพยากรเท่านั้น หากทรัพยากรนั้นได้การรับอนุมัติ เวลาที่คิดค่าธรรมเนียมในระหว่างรอบระยะเวลาจะแสดงในกริด</span><span class="sxs-lookup"><span data-stu-id="8072c-154">Utilization is shown for a resource only if that resource has approved, chargeable time during the period that is shown in the grid.</span></span>

## <a name="resource-availability"></a><span data-ttu-id="8072c-155">ความพร้อมใช้งานของทรัพยากร</span><span class="sxs-lookup"><span data-stu-id="8072c-155">Resource availability</span></span>

<span data-ttu-id="8072c-156">สิ่งสำคัญคือตัวจัดการทรัพยากรสามารถดูความพร้อมใช้งานของทรัพยากรและปรับปรุงการจองได้</span><span class="sxs-lookup"><span data-stu-id="8072c-156">It's critical that resource managers be able to view the availability of resources and update bookings.</span></span> <span data-ttu-id="8072c-157">ในบางกรณี ไม่มีความต้องการอย่างเป็นทางการ (คำขอทรัพยากร) แต่ผู้จัดการทรัพยากรต้องตอบสนองต่อความต้องการที่ไม่ได้วางแผนไว้ ซึ่งมาจากช่องทางต่างๆ เช่นอีเมล ติดต่อทางโทรศัพท์หรือข้อความโต้ตอบแบบทันที</span><span class="sxs-lookup"><span data-stu-id="8072c-157">In some cases, there is no formal demand (resource request), but a resource manager must respond to an unplanned demand that comes through channels such as an email, phone call, or instant message.</span></span> <span data-ttu-id="8072c-158">ผู้จัดการทรัพยากรใช้ตารางกำหนดการเพื่อปรับปรุงทรัพยากรและการจอง</span><span class="sxs-lookup"><span data-stu-id="8072c-158">Resource managers use the Schedule Board to update resources and bookings.</span></span>

<span data-ttu-id="8072c-159">ชั่วโมงทำงานของทรัพยากรจะใช้เป็นข้อมูลพื้นฐานสำหรับการคำนวณความพร้อมของทรัพยากร</span><span class="sxs-lookup"><span data-stu-id="8072c-159">Resource work hours are used as the basis for calculating the availability of a resource.</span></span> <span data-ttu-id="8072c-160">การจองทรัพยากรจะใช้กำลังการผลิตของทรัพยากร</span><span class="sxs-lookup"><span data-stu-id="8072c-160">Resource bookings consume the capacity of the resources.</span></span>

![ตารางกำหนดการ](media/Resource-Management-image68.png)

<span data-ttu-id="8072c-162">ตารางกำหนดการจะใช้สีและแรเงาเพื่อแสดงการจอง ความพร้อมใช้งาน และการจองเกิน และยังมีสถานะของการจองอีกด้วย</span><span class="sxs-lookup"><span data-stu-id="8072c-162">The Schedule Board uses colors and shading to show bookings, availability, and overbookings, and also the status of bookings.</span></span> <span data-ttu-id="8072c-163">มีการตั้งค่าในการตั้งค่าของตารางกำหนดการช่วยให้คุณสามารถแสดงคำอธิบายแผนภูมิได้</span><span class="sxs-lookup"><span data-stu-id="8072c-163">A setting in the Schedule Board settings lets you show a legend.</span></span>

<span data-ttu-id="8072c-164">ถ้าลูกศรชี้ขวาปรากฏถัดจากทรัพยากรที่สามารถจองได้แต่ละรายการบนบอร์ดกำหนดการ ทรัพยากรนั้นจะสามารถถูกขยายเพื่อแสดงรายละเอียดของงานที่ทรัพยากรนั้นถูกจองกับงานนั้น</span><span class="sxs-lookup"><span data-stu-id="8072c-164">If a right-pointing arrow appears next to an individual bookable resource on the Schedule Board, the resource can be expanded to show details of the work that the resource is booked on.</span></span>

![ทรัพยากรที่สามารถจองได้ในตารางกำหนดการ](media/Resource-Management-image69.png)

<span data-ttu-id="8072c-166">เนืองจาก Dynamics 365 Project Service Automation ใช้เอ็นจิน Universal Resource Scheduling ถ้าคุณยังได้ติดตั้ง Dynamics 365 Field Service ไว้ คุณสามารถดูรายละเอียดของการจองทรัพยากรสำหรับโครงการ ใบสั่งงานและเอนทิตี้อื่นๆ ที่คุณขยายการจัดกำหนดการให้</span><span class="sxs-lookup"><span data-stu-id="8072c-166">Because Dynamics 365 Project Service Automation uses the Universal Resource Scheduling engine, if you also have Dynamics 365 Field Service installed, you can view the details of resource bookings for projects, work orders, and any other entities that you've extended scheduling to.</span></span>

![รายละเอียดของการจองทรัพยากรสำหรับโครงการและใบสั่งงาน](media/Resource-Management-image70.png)

<span data-ttu-id="8072c-168">หากต้องการดูรายละเอียดเพิ่มเติมเกี่ยวกับทรัพยากรแต่ละรายการ ให้คลิกขวาเพื่อเปิดบัตรทรัพยากร</span><span class="sxs-lookup"><span data-stu-id="8072c-168">To view more details about an individual resource, right-click it to open the resource card.</span></span>

![บัตรทรัพยากร](media/Resource-Management-image71.png)


[!INCLUDE[footer-include](../includes/footer-banner.md)]