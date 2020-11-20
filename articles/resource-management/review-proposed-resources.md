---
title: ตรวจทานทรัพยากรที่เสนอ
description: หัวข้อนี้แสดงข้อมูลเกี่ยวกับวิธีการเสนอทรัพยากรโครงการ
author: ruhercul
manager: AnnBe
ms.date: 11/05/2020
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
ms.author: ruhercul
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: 54a0924da17eac86e2fa400540e629f6d803aa35
ms.sourcegitcommit: 14aa380759214713d9bf560f5a7f619b7f4bd5b8
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 11/05/2020
ms.locfileid: "4401196"
---
# <a name="review-proposed-resources"></a><span data-ttu-id="97312-103">ตรวจทานทรัพยากรที่เสนอ</span><span class="sxs-lookup"><span data-stu-id="97312-103">Review proposed resources</span></span>

<span data-ttu-id="97312-104">_**นำไปใช้กับ:** Project Operations สำหรับสถานการณ์ที่อิงตามทรัพยากร/ที่ไม่ได้เก็บในสต็อก การปรับใช้ Lite - จัดการกับการออกใบแจ้งหนี้ชั่วคราว_</span><span class="sxs-lookup"><span data-stu-id="97312-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="97312-105">ผู้จัดการทรัพยากรสามารถเสนอทรัพยากรกับผู้จัดการโครงการโดยใช้คำขอทรัพยากร</span><span class="sxs-lookup"><span data-stu-id="97312-105">Resource managers can propose a resource to the project manager by using a resource request.</span></span>

1. <span data-ttu-id="97312-106">จากกริดคำขอหรือตัวคำขอเอง ให้เลือก **ค้นหาทรัพยากร**</span><span class="sxs-lookup"><span data-stu-id="97312-106">From the request grid or the request itself, select **Find Resources**.</span></span>
2. <span data-ttu-id="97312-107">ในเพจ **ตัวช่วยจัดกำหนดการ** เลือกทรัพยากร และในบานหน้าต่าง **สร้างการจองทรัพยากร** ในฟิลด์ **สถานะการจอง** ให้เลือก **จอง**</span><span class="sxs-lookup"><span data-stu-id="97312-107">On the **Schedule Assistant** page, select the resource, and then, in the **Create Resource Booking** pane, in the **Booking Status** field, select **Book**.</span></span>

<span data-ttu-id="97312-108">การปรับปรุงสถานะต่อไปนี้เกิดขึ้น:</span><span class="sxs-lookup"><span data-stu-id="97312-108">The following status updates occur:</span></span>

- <span data-ttu-id="97312-109">ในหน้า **ตัวช่วยจัดกำหนดการ** จะมีการปรับปรุงตัวบ่งชี้สถานะเพื่อบ่งชี้ว่าการจองถูกเสนอไว้ ไม่ได้ถูกจองแบบตายตัว</span><span class="sxs-lookup"><span data-stu-id="97312-109">On the **Schedule Assistant** page, the status indicators are updated to indicate that the booking is proposed, not hard-booked.</span></span>
- <span data-ttu-id="97312-110">ในคำขอทรัพยากร สถานะจะถูกเปลี่ยนเป็น **ต้องมีการตรวจทาน**</span><span class="sxs-lookup"><span data-stu-id="97312-110">On the resource request, the status is changed to **Needs Review**.</span></span>
- <span data-ttu-id="97312-111">บนแท็บ **ทีม** ของโครงการ ค่า **สถานะคำขอ** ของสมาชิกทีมทั่วไปจะถูกเปลี่ยนเป็น **ต้องมีการตรวจทาน**</span><span class="sxs-lookup"><span data-stu-id="97312-111">On the **Team** tab of the project, the generic team member's **Request Status** value is changed to **Needs Review**.</span></span>

<span data-ttu-id="97312-112">ผู้จัดการโครงการสามารถยอมรับหรือปฏิเสธข้อเสนอได้</span><span class="sxs-lookup"><span data-stu-id="97312-112">The project manager can either accept or reject the proposal.</span></span>

<span data-ttu-id="97312-113">เมื่อผู้จัดการทรัพยากรประมวลผลการร้องขอทรัพยากร พวกเขาสามารถใช้วิธีการใดก็ได้จากวิธีการต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="97312-113">When resource managers process resource requests, they can use any of the following approaches:</span></span>

- <span data-ttu-id="97312-114">นำเสนอทรัพยากรหลายอย่างเพื่อตอบสนองความต้องการหากไม่มีทรัพยากรเดียวที่พร้อมใช้งานเพื่อตอบสนองชั่วโมงที่ต้องการ</span><span class="sxs-lookup"><span data-stu-id="97312-114">Propose multiple resources to satisfy the demand if no single resource is available to fulfill the required hours.</span></span> <span data-ttu-id="97312-115">ชั่วโมงที่เสนอจะถูกแบ่งระหว่างทรัพยากรหลายรายการที่สามารถตอบสนองชั่วโมงที่ต้องการ</span><span class="sxs-lookup"><span data-stu-id="97312-115">Proposed hours are then split among multiple resources that can satisfy the required hours.</span></span> <span data-ttu-id="97312-116">ในสถานการณ์สมมตินี้ ชั่วโมงไม่สามารถทับซ้อนกันได้</span><span class="sxs-lookup"><span data-stu-id="97312-116">In this scenario, the hours can't overlap.</span></span>
- <span data-ttu-id="97312-117">นำเสนอทรัพยากรน้อยกว่าที่ต้องการ</span><span class="sxs-lookup"><span data-stu-id="97312-117">Propose fewer resources than are required.</span></span> <span data-ttu-id="97312-118">ในสถานการณ์สมมตินี้ กำลังการผลิตทรัพยากรที่นำเสนอน้อยกว่าชั่วโมงที่ต้องการที่ผู้ขอระบุ</span><span class="sxs-lookup"><span data-stu-id="97312-118">In this scenario, the proposed resource capacity is less than the required hours that the requestor specified.</span></span> <span data-ttu-id="97312-119">ดังนั้น เมื่อผู้ขอยอมรับทรัพยากรที่เสนอ ความต้องการทรัพยากรที่ยังไม่บรรลุเป้าหมายจะถูกสร้างขึ้นเพื่อรวบรวมตามความต้องการที่เหลือ</span><span class="sxs-lookup"><span data-stu-id="97312-119">Therefore, when the requestor accepts the proposed resources, an unfulfilled resource requirement is created to capture the remaining demand.</span></span>
- <span data-ttu-id="97312-120">จองทรัพยากรหลายอย่างเพื่อตอบสนองความต้องการ หากไม่มีทรัพยากรเดียวที่พร้อมใช้งานเพื่อทำงานให้แล้วเสร็จ</span><span class="sxs-lookup"><span data-stu-id="97312-120">Book multiple resources to satisfy the demand if no single resource is available to complete the work.</span></span>
- <span data-ttu-id="97312-121">จองทรัพยากรน้อยกว่าที่ต้องการ</span><span class="sxs-lookup"><span data-stu-id="97312-121">Book fewer resources than are required.</span></span> <span data-ttu-id="97312-122">ในสถานการณ์สมมตินี้ ชั่วโมงที่จองน้อยกว่าชั่วโมงที่ต้องการ</span><span class="sxs-lookup"><span data-stu-id="97312-122">In this scenario, the booked hours are fewer than the required hours.</span></span> <span data-ttu-id="97312-123">ระบบจะแนะนำให้คุณนำเสนอทรัพยากรแทนการจอง เพื่อให้ผู้ร้องขอหรือสามารถตรวจสอบและติดตามความต้องการที่เหลืออยู่ได้</span><span class="sxs-lookup"><span data-stu-id="97312-123">The system guides you to propose resources instead of bookings, so that the requestor can verify and keep track of remaining demand.</span></span>

## <a name="resource-availability"></a><span data-ttu-id="97312-124">ความพร้อมใช้งานของทรัพยากร</span><span class="sxs-lookup"><span data-stu-id="97312-124">Resource availability</span></span>

<span data-ttu-id="97312-125">สิ่งสำคัญคือตัวจัดการทรัพยากรสามารถดูความพร้อมใช้งานของทรัพยากรและปรับปรุงการจองได้</span><span class="sxs-lookup"><span data-stu-id="97312-125">It's critical that resource managers be able to view the availability of resources and update bookings.</span></span> <span data-ttu-id="97312-126">ในบางกรณี ไม่มีความต้องการอย่างเป็นทางการ (คำขอทรัพยากร) แต่ผู้จัดการทรัพยากรต้องตอบสนองต่อความต้องการที่ไม่ได้วางแผนไว้ ซึ่งมาจากช่องทางต่างๆ เช่นอีเมล ติดต่อทางโทรศัพท์หรือข้อความโต้ตอบแบบทันที</span><span class="sxs-lookup"><span data-stu-id="97312-126">In some cases, there is no formal demand (resource request), but a resource manager must respond to an unplanned demand that comes through channels such as an email, phone call, or instant message.</span></span> <span data-ttu-id="97312-127">ผู้จัดการทรัพยากรใช้ตารางกำหนดการเพื่อปรับปรุงทรัพยากรและการจอง</span><span class="sxs-lookup"><span data-stu-id="97312-127">Resource managers use the Schedule Board to update resources and bookings.</span></span>

<span data-ttu-id="97312-128">ชั่วโมงทำงานของทรัพยากรจะใช้เป็นข้อมูลพื้นฐานสำหรับการคำนวณความพร้อมของทรัพยากร</span><span class="sxs-lookup"><span data-stu-id="97312-128">Resource work hours are used as the basis for calculating the availability of a resource.</span></span> <span data-ttu-id="97312-129">การจองทรัพยากรจะใช้กำลังการผลิตของทรัพยากร</span><span class="sxs-lookup"><span data-stu-id="97312-129">Resource bookings consume the capacity of the resources.</span></span>

<span data-ttu-id="97312-130">ตารางกำหนดการจะใช้สีและแรเงาเพื่อแสดงการจอง ความพร้อมใช้งาน และการจองเกิน และยังมีสถานะของการจองอีกด้วย</span><span class="sxs-lookup"><span data-stu-id="97312-130">The Schedule Board uses colors and shading to show bookings, availability, and overbookings, and also the status of bookings.</span></span> <span data-ttu-id="97312-131">มีการตั้งค่าในการตั้งค่าของตารางกำหนดการช่วยให้คุณสามารถแสดงคำอธิบายแผนภูมิได้</span><span class="sxs-lookup"><span data-stu-id="97312-131">A setting in the Schedule Board settings lets you show a legend.</span></span>

<span data-ttu-id="97312-132">ถ้าลูกศรชี้ขวาปรากฏถัดจากทรัพยากรที่สามารถจองได้แต่ละรายการบนบอร์ดกำหนดการ ทรัพยากรนั้นจะสามารถถูกขยายเพื่อแสดงรายละเอียดของงานที่ทรัพยากรนั้นถูกจองกับงานนั้น</span><span class="sxs-lookup"><span data-stu-id="97312-132">If a right-pointing arrow appears next to an individual bookable resource on the Schedule Board, the resource can be expanded to show details of the work that the resource is booked on.</span></span>

<span data-ttu-id="97312-133">เนืองจาก Dynamics 365 Project Operations ใช้กลไกจัดการ Universal Resource Scheduling ถ้าคุณยังได้ติดตั้ง Dynamics 365 Field Service ไว้ คุณสามารถดูรายละเอียดของการจองทรัพยากรสำหรับโครงการ ใบสั่งงานและเอนทิตีอื่นๆ ที่คุณขยายการจัดกำหนดการให้</span><span class="sxs-lookup"><span data-stu-id="97312-133">Because Dynamics 365 Project Operations uses the Universal Resource Scheduling engine, if you also have Dynamics 365 Field Service installed, you can view the details of resource bookings for projects, work orders, and any other entities that you've extended scheduling to.</span></span>

<span data-ttu-id="97312-134">หากต้องการดูรายละเอียดเพิ่มเติมเกี่ยวกับทรัพยากรแต่ละรายการ ให้คลิกขวาเพื่อเปิดบัตรทรัพยากร</span><span class="sxs-lookup"><span data-stu-id="97312-134">To view more details about an individual resource, right-click it to open the resource card.</span></span>

