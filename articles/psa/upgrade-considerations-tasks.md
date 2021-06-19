---
title: ข้อควรพิจารณาในการอัพเกรดสำหรับโครงสร้างการแบ่งงาน
description: หัวข้อนี้แสดงข้อมูลเกี่ยวกับการอัพเกรดโครงสร้างการแบ่งงานจาก Project Service Automation 2.x เป็น 3.x.
ms.custom:
- dyn365-projectservice
ms.date: 10/18/2019
ms.topic: article
author: ruhercul
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
ms.openlocfilehash: 868b0daadaf6cf96ca7bf847914bca8014412f26
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 05/10/2021
ms.locfileid: "6005634"
---
# <a name="upgrade-considerations-for-the-work-breakdown-structure"></a><span data-ttu-id="c69e0-103">ข้อควรพิจารณาในการอัพเกรดสำหรับโครงสร้างการแบ่งงาน</span><span class="sxs-lookup"><span data-stu-id="c69e0-103">Upgrade considerations for the work breakdown structure</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

<span data-ttu-id="c69e0-104">หัวข้อนี้แสดงข้อมูลเกี่ยวกับการอัพเกรดโครงสร้างการแบ่งงานจาก Project Service Automation 2.x เป็น 3.x.</span><span class="sxs-lookup"><span data-stu-id="c69e0-104">This topic provides information about upgrading the work breakdown structure from Project Service Automation 2.x to 3.x.</span></span> <span data-ttu-id="c69e0-105">หัวข้อนี้กำหนดสถานะสุขภาพของโครงการใน Project Service Automation (PSA) ที่จำเป็นสำหรับการอัพเกรดที่ประสบความสำเร็จ</span><span class="sxs-lookup"><span data-stu-id="c69e0-105">This topic defines the healthy state of a project in Project Service Automation (PSA) that is required for a successful upgrade.</span></span> <span data-ttu-id="c69e0-106">นอกจากนี้ยังมีข้อมูลเกี่ยวกับเงื่อนไขการปิดกั้นทั่วไปที่จะทำให้การอัพเกรดล้มเหลว</span><span class="sxs-lookup"><span data-stu-id="c69e0-106">There is also information about the common blocking conditions that will cause upgrade to fail.</span></span> <span data-ttu-id="c69e0-107">สำหรับข้อมูลเพิ่มเติมเกี่ยวกับการกำหนดงานของโครงการและฟังก์ชันภายในกำหนดการโครงการ ให้ดูที่ [ตารางเวลาโครงการ](project-creating.md)</span><span class="sxs-lookup"><span data-stu-id="c69e0-107">For more information about defining project tasks and their functions within a project schedule, see [Project schedules](project-creating.md).</span></span>

## <a name="key-entities"></a><span data-ttu-id="c69e0-108">เอนทิตีคีย์</span><span class="sxs-lookup"><span data-stu-id="c69e0-108">Key entities</span></span>
<span data-ttu-id="c69e0-109">สำหรับโครงสร้างการแบ่งงานที่ถูกต้องที่ถูกโหลดด้วยทรัพยากรอยู่แล้ว จำเป็นต้องมีเอนทิตีต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="c69e0-109">For an accurate work breakdown structure that is already loaded with resources, the following entities are required:</span></span>

- [<span data-ttu-id="c69e0-110">โครงการ</span><span class="sxs-lookup"><span data-stu-id="c69e0-110">Project</span></span>](/dynamics365/customerengagement/on-premises/developer/entities/msdyn_project)
- [<span data-ttu-id="c69e0-111">ทีมโครงการ</span><span class="sxs-lookup"><span data-stu-id="c69e0-111">Project Team</span></span>](/dynamics365/customerengagement/on-premises/developer/entities/msdyn_projectteam)
- [<span data-ttu-id="c69e0-112">งานโครงการ</span><span class="sxs-lookup"><span data-stu-id="c69e0-112">Project Task</span></span>](/dynamics365/customerengagement/on-premises/developer/entities/msdyn_projecttask)
- [<span data-ttu-id="c69e0-113">การมอบหมายทรัพยากร</span><span class="sxs-lookup"><span data-stu-id="c69e0-113">Resource Assignments</span></span>](/dynamics365/customerengagement/on-premises/developer/entities/msdyn_resourceassignment)
- [<span data-ttu-id="c69e0-114">การขึ้นต่อกันของงานโครงการ</span><span class="sxs-lookup"><span data-stu-id="c69e0-114">Project Task Dependency</span></span>](/dynamics365/customerengagement/on-premises/developer/entities/msdyn_projecttaskdependency)
- [<span data-ttu-id="c69e0-115">ทรัพยากรที่สามารถจองได้</span><span class="sxs-lookup"><span data-stu-id="c69e0-115">Bookable Resources</span></span>](/dynamics365/customerengagement/on-premises/developer/entities/bookableresource)

<span data-ttu-id="c69e0-116">ในการกำหนดโครงสร้างการแบ่งงานที่โหลดทรัพยากร คุณต้องดำเนินการขั้นตอนต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="c69e0-116">To define a resource loaded work breakdown structure, you must complete the following steps:</span></span>

1. <span data-ttu-id="c69e0-117">สร้างโครงการใหม่</span><span class="sxs-lookup"><span data-stu-id="c69e0-117">Create a new project.</span></span> <span data-ttu-id="c69e0-118">สำหรับข้อมูลเพิ่มเติมเกี่ยวกับวิธีการสร้างโครงการใหม่ ให้ดูที่ [msdyn_project](/dynamics365/customerengagement/on-premises/developer/entities/msdyn_project)</span><span class="sxs-lookup"><span data-stu-id="c69e0-118">For more information about how to create a new project, see [msdyn_project](/dynamics365/customerengagement/on-premises/developer/entities/msdyn_project).</span></span>
2. <span data-ttu-id="c69e0-119">สร้างงานอย่างน้อยหนึ่งภารกิจ</span><span class="sxs-lookup"><span data-stu-id="c69e0-119">Create one or more tasks.</span></span> <span data-ttu-id="c69e0-120">สำหรับข้อมูลเพิ่มเติมเกี่ยวกับวิธีการสร้างงาน ให้ดูที่ [msdyn_projecttask](/dynamics365/customerengagement/on-premises/developer/entities/msdyn_projecttask)</span><span class="sxs-lookup"><span data-stu-id="c69e0-120">For more information about how to create a task, see [msdyn_projecttask](/dynamics365/customerengagement/on-premises/developer/entities/msdyn_projecttask).</span></span>
3. <span data-ttu-id="c69e0-121">กำหนดการขึ้นต่อกันของงาน</span><span class="sxs-lookup"><span data-stu-id="c69e0-121">Define the task dependencies.</span></span> <span data-ttu-id="c69e0-122">สำหรับข้อมูลเพิ่มเติม โปรดดูที่ [Project Task Dependency](/dynamics365/customerengagement/on-premises/developer/entities/msdyn_projecttaskdependency)</span><span class="sxs-lookup"><span data-stu-id="c69e0-122">For more information, see [Project Task Dependency](/dynamics365/customerengagement/on-premises/developer/entities/msdyn_projecttaskdependency).</span></span>
4. <span data-ttu-id="c69e0-123">มอบหมายสมาชิกทีมโครงการให้กับโครงการ</span><span class="sxs-lookup"><span data-stu-id="c69e0-123">Assign project team members to the project.</span></span> <span data-ttu-id="c69e0-124">สำหรับข้อมูลเพิ่มเติม ให้ดูที่ [msdyn_projectteam](/dynamics365/customerengagement/on-premises/developer/entities/msdyn_projectteam)</span><span class="sxs-lookup"><span data-stu-id="c69e0-124">For more information, see [msdyn_projectteam](/dynamics365/customerengagement/on-premises/developer/entities/msdyn_projectteam).</span></span>
5. <span data-ttu-id="c69e0-125">มอบหมายสมาชิกทีมโครงการให้กับงาน</span><span class="sxs-lookup"><span data-stu-id="c69e0-125">Assign project team members to the tasks.</span></span> <span data-ttu-id="c69e0-126">สำหรับข้อมูลเพิ่มเติม ให้ดูที่ [msdyn_resourceassignment](/dynamics365/customerengagement/on-premises/developer/entities/msdyn_resourceassignment)</span><span class="sxs-lookup"><span data-stu-id="c69e0-126">For more information, see [msdyn_resourceassignment](/dynamics365/customerengagement/on-premises/developer/entities/msdyn_resourceassignment).</span></span>

## <a name="project-team-relationships"></a><span data-ttu-id="c69e0-127">ความสัมพันธ์ของสมาชิกทีมโครงการ</span><span class="sxs-lookup"><span data-stu-id="c69e0-127">Project team relationships</span></span>

<span data-ttu-id="c69e0-128">เพื่อให้แน่ใจว่าการอัพเกรดประสบความสำเร็จ จะต้องมีการรักษาความสัมพันธ์ต่อไปนี้อย่างถูกต้อง:</span><span class="sxs-lookup"><span data-stu-id="c69e0-128">To ensure a successful upgrade, the following relationships must be correctly maintained:</span></span>
- <span data-ttu-id="c69e0-129">สมาชิกในทีมโครงการทั้งหมดต้องเชื่อมโยงกับทรัพยากรที่สามารถจองได้</span><span class="sxs-lookup"><span data-stu-id="c69e0-129">All project team members must be associated with a bookable resource.</span></span>
- <span data-ttu-id="c69e0-130">สมาชิกในทีมโครงการทั้งหมดต้องเชื่อมโยงกับโครงการเดียวกัน</span><span class="sxs-lookup"><span data-stu-id="c69e0-130">All project team members must be associated with the same project.</span></span> 

## <a name="project-task-relationships"></a><span data-ttu-id="c69e0-131">ความสัมพันธ์ของงานโครงการ</span><span class="sxs-lookup"><span data-stu-id="c69e0-131">Project task relationships</span></span>
<span data-ttu-id="c69e0-132">เพื่อให้แน่ใจว่าการอัพเกรดประสบความสำเร็จ จะต้องมีการรักษาความสัมพันธ์ต่อไปนี้อย่างถูกต้อง:</span><span class="sxs-lookup"><span data-stu-id="c69e0-132">To ensure a successful upgrade, the following relationships must be correctly maintained:</span></span>

- <span data-ttu-id="c69e0-133">งานที่เกี่ยวข้องใดๆต้องเชื่อมโยงกับโครงการเดียวกัน</span><span class="sxs-lookup"><span data-stu-id="c69e0-133">Any related tasks must be associated with the same project.</span></span>
- <span data-ttu-id="c69e0-134">ทุกงานในรายการต้องมีงานหลัก</span><span class="sxs-lookup"><span data-stu-id="c69e0-134">Every line task must have a parent task.</span></span>
- <span data-ttu-id="c69e0-135">ทุกงานต้องมีโครงการหลัก</span><span class="sxs-lookup"><span data-stu-id="c69e0-135">Every task must have a parent project.</span></span>

### <a name="valid-conditions"></a><span data-ttu-id="c69e0-136">เงื่อนไขที่ถูกต้อง</span><span class="sxs-lookup"><span data-stu-id="c69e0-136">Valid conditions</span></span>

- <span data-ttu-id="c69e0-137">ระยะเวลาของงานทั้งหมดต้องมากกว่าหรือเท่ากับ (> =) หนึ่งชั่วโมงและน้อยกว่า 1,800,000 นาที (1,250 วัน)\*</span><span class="sxs-lookup"><span data-stu-id="c69e0-137">All task durations must be greater than or equal to (>=) one hour and less than 1,800,000 minutes (1,250 days).\*</span></span>
- <span data-ttu-id="c69e0-138">งานทั้งหมดต้องมีวันที่เริ่มต้นไม่เร็วกว่า 2000/01/01 \*</span><span class="sxs-lookup"><span data-stu-id="c69e0-138">All tasks must have a start date no earlier than 2000/01/01.\*</span></span>
- <span data-ttu-id="c69e0-139">งานทั้งหมดต้องมีวันที่เริ่มต้นไม่เกิน 17 ปีนับจากวันปัจจุบัน\*</span><span class="sxs-lookup"><span data-stu-id="c69e0-139">All tasks must have a start date no later than 17 years from the present day.\*</span></span>
- <span data-ttu-id="c69e0-140">งานทั้งหมดต้องมีวันที่เริ่มต้นเร็วกว่าหรือเท่ากับวันที่เสร็จสิ้น</span><span class="sxs-lookup"><span data-stu-id="c69e0-140">All tasks must have a start date earlier or equal to their finish date.</span></span>
- <span data-ttu-id="c69e0-141">ชนิดธุรกรรมทั้งหมดในการจัดประเภท (ค่าใช้จ่าย วัสดุ ภาษี และเวลา) ต้องมีค่าสำหรับ **หน่วยเริ่มต้น** และ **กลุ่มของหน่วยนับ**</span><span class="sxs-lookup"><span data-stu-id="c69e0-141">All transaction types on classifications (Expense, Material, Tax, and Time) must have values for **Default Unit** and **Unit Group**.</span></span>
- <span data-ttu-id="c69e0-142">ควรหลีกเลี่ยงรูปแบบวันที่ที่มีตัวอักษร</span><span class="sxs-lookup"><span data-stu-id="c69e0-142">Date formats with letters should be avoided.</span></span>

### <a name="potential-mitigation-steps"></a><span data-ttu-id="c69e0-143">ขั้นตอนการบรรเทาที่มีศักยภาพ</span><span class="sxs-lookup"><span data-stu-id="c69e0-143">Potential mitigation steps</span></span>
- <span data-ttu-id="c69e0-144">ใช้การค้นหาขั้นสูงเพื่อระบุงานโครงการที่ไม่มีรหัสโครงการ</span><span class="sxs-lookup"><span data-stu-id="c69e0-144">Use Advanced Find to identify Project tasks that do not contain a Project ID.</span></span>
- <span data-ttu-id="c69e0-145">ใช้การค้นหาขั้นสูงเพื่อระบุงานโครงการที่ระยะเวลาที่กำหนดมากกว่า > 1,800,000</span><span class="sxs-lookup"><span data-stu-id="c69e0-145">Use Advanced Find to identify Project tasks where the scheduled duration is greater than > 1,800,000.</span></span>
- <span data-ttu-id="c69e0-146">ก่อนทำการเปลี่ยนแปลงข้อมูลใดๆ คุณควรตรวจสอบการปรับแต่งใดๆ ที่เกี่ยวข้องกับเอนทิตีที่อาจนำไปสู่การนำข้อมูลเข้าสู่สถานะไม่ดี</span><span class="sxs-lookup"><span data-stu-id="c69e0-146">Prior to making any data changes, you should investigate any customizations associated with the entity that may have led to getting the data into a bad state.</span></span> <span data-ttu-id="c69e0-147">การกำหนดการเหล่านี้ควรได้รับการแก้ไขก่อนที่จะดำเนินการอัปเดตที่เกี่ยวข้องกับข้อมูลใดๆ</span><span class="sxs-lookup"><span data-stu-id="c69e0-147">These customizations should be addressed before proceeding with any data-related updates.</span></span>
- <span data-ttu-id="c69e0-148">สำหรับงานที่ระบุที่ได้รับการลงทะเบียนแล้ว ให้พิจารณาลบงานเหล่านี้หากไม่จำเป็น หรือหากคิดว่าควรเกี่ยวข้องกับโครงการหลักที่ถูกต้อง</span><span class="sxs-lookup"><span data-stu-id="c69e0-148">For the identified tasks that have been orphaned, consider deleting these tasks if they are not needed or if they should be associated with the correct parent project.</span></span>
- <span data-ttu-id="c69e0-149">สำหรับงานใดๆ ที่มีระยะเวลามากกว่า 1,250 วัน ให้พิจารณาเพิ่มงานหลายรายการเพื่อแสดงระยะเวลารวมหากเป็นไปได้</span><span class="sxs-lookup"><span data-stu-id="c69e0-149">For any tasks where the duration is greater than 1,250 days, consider adding multiple tasks to represent the total duration, if feasible.</span></span>

> [!NOTE]
> <span data-ttu-id="c69e0-150">รายการที่ระบุด้วยเครื่องหมายดอกจัน (\*) มีขีดจำกัดที่เนื่องจากข้อเท็จจริงที่ว่าการจัดการความสัมพันธ์ลูกค้า (CRM) สนับสนุนเฉพาะการขยายการเกิดขึ้นประจำ 7,320 รายการ</span><span class="sxs-lookup"><span data-stu-id="c69e0-150">Items noted with an asterisk (\*) have limits that are due to the fact that customer relationship management (CRM) supports only 7,320 recurrence expansions.</span></span> <span data-ttu-id="c69e0-151">คุณต้องอยู่ต่ำกว่าขีดจำกัดนี้</span><span class="sxs-lookup"><span data-stu-id="c69e0-151">You must stay below this limit.</span></span>

## <a name="resource-assignment-relationships"></a><span data-ttu-id="c69e0-152">ความสัมพันธ์การมอบหมายทรัพยากร</span><span class="sxs-lookup"><span data-stu-id="c69e0-152">Resource Assignment relationships</span></span>
<span data-ttu-id="c69e0-153">เพื่อให้แน่ใจว่าการอัพเกรดประสบความสำเร็จ จะต้องมีการรักษาความสัมพันธ์ต่อไปนี้อย่างถูกต้อง:</span><span class="sxs-lookup"><span data-stu-id="c69e0-153">To ensure a successful upgrade, the following relationships must be correctly maintained:</span></span>

- <span data-ttu-id="c69e0-154">การมอบหมายทรัพยากรทั้งหมดในโครงสร้างการแบ่งงานต้องเกี่ยวข้องกับโครงการเดียวกัน</span><span class="sxs-lookup"><span data-stu-id="c69e0-154">All Resource Assignments in a work breakdown structure must be related to the same project.</span></span>
- <span data-ttu-id="c69e0-155">การมอบหมายทรัพยากรทั้งหมดในโครงสร้างการแบ่งงานต้องเกี่ยวข้องกับสมาชิกทีมโครงการในโครงการเดียวกัน</span><span class="sxs-lookup"><span data-stu-id="c69e0-155">All Resource Assignments in a work breakdown structure must be associated to project team members in the same project.</span></span>

### <a name="potential-mitigation-steps"></a><span data-ttu-id="c69e0-156">ขั้นตอนการบรรเทาที่มีศักยภาพ</span><span class="sxs-lookup"><span data-stu-id="c69e0-156">Potential mitigation steps</span></span>
- <span data-ttu-id="c69e0-157">ระบุงานทั้งหมดที่อยู่นอกเงื่อนไขที่อธิบายไว้ข้างต้น</span><span class="sxs-lookup"><span data-stu-id="c69e0-157">Identify all tasks that fall outside the conditions described above.</span></span>  
- <span data-ttu-id="c69e0-158">ควรลบการกำหนดทรัพยากรใดๆ ที่ไม่ถูกต้องอีกต่อไป</span><span class="sxs-lookup"><span data-stu-id="c69e0-158">Any Resource Assignments that are no longer valid should be deleted.</span></span>

## <a name="project-task-dependency-relationships"></a><span data-ttu-id="c69e0-159">ความสัมพันธ์การขึ้นต่อกันของงานโครงการ</span><span class="sxs-lookup"><span data-stu-id="c69e0-159">Project task dependency relationships</span></span>
<span data-ttu-id="c69e0-160">เพื่อให้แน่ใจว่าการอัพเกรดประสบความสำเร็จ จะต้องมีการรักษาความสัมพันธ์ต่อไปนี้อย่างถูกต้อง:</span><span class="sxs-lookup"><span data-stu-id="c69e0-160">To ensure a successful upgrade, the following relationships must be correctly maintained:</span></span>

- <span data-ttu-id="c69e0-161">การขึ้นต่อกันของงานโครงการทั้งหมดต้องเกี่ยวข้องกับโครงการเดียวกัน</span><span class="sxs-lookup"><span data-stu-id="c69e0-161">All project task dependencies must be related to the same project.</span></span>
- <span data-ttu-id="c69e0-162">งานไม่สามารถมีการอ้างอิงการขึ้นต่อกันเหมือนกันมากกว่าหนึ่งครั้ง</span><span class="sxs-lookup"><span data-stu-id="c69e0-162">A task can't have the same dependency referenced more than once.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]