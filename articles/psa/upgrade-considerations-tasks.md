---
title: ข้อควรพิจารณาในการอัพเกรดสำหรับโครงสร้างการแบ่งงาน
description: หัวข้อนี้แสดงข้อมูลเกี่ยวกับการอัพเกรดโครงสร้างการแบ่งงานจาก Project Service Automation 2.x เป็น 3.x.
manager: kfend
ms.service: project-operations
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
ms.openlocfilehash: 0b75fd372732f42a3557aaa5eccec1f24a644941
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 10/28/2020
ms.locfileid: "4121826"
---
# <a name="upgrade-considerations-for-the-work-breakdown-structure"></a><span data-ttu-id="6cb2b-103">ข้อควรพิจารณาในการอัพเกรดสำหรับโครงสร้างการแบ่งงาน</span><span class="sxs-lookup"><span data-stu-id="6cb2b-103">Upgrade considerations for the work breakdown structure</span></span>
<span data-ttu-id="6cb2b-104">หัวข้อนี้แสดงข้อมูลเกี่ยวกับการอัพเกรดโครงสร้างการแบ่งงานจาก Project Service Automation 2.x เป็น 3.x.</span><span class="sxs-lookup"><span data-stu-id="6cb2b-104">This topic provides information about upgrading the work breakdown structure from Project Service Automation 2.x to 3.x.</span></span> <span data-ttu-id="6cb2b-105">หัวข้อนี้กำหนดสถานะสุขภาพของโครงการใน Project Service Automation (PSA) ที่จำเป็นสำหรับการอัพเกรดที่ประสบความสำเร็จ</span><span class="sxs-lookup"><span data-stu-id="6cb2b-105">This topic defines the healthy state of a project in Project Service Automation (PSA) that is required for a successful upgrade.</span></span> <span data-ttu-id="6cb2b-106">นอกจากนี้ยังมีข้อมูลเกี่ยวกับเงื่อนไขการปิดกั้นทั่วไปที่จะทำให้การอัพเกรดล้มเหลว</span><span class="sxs-lookup"><span data-stu-id="6cb2b-106">There is also information about the common blocking conditions that will cause upgrade to fail.</span></span> <span data-ttu-id="6cb2b-107">สำหรับข้อมูลเพิ่มเติมเกี่ยวกับการกำหนดงานของโครงการและฟังก์ชันภายในกำหนดการโครงการ ให้ดูที่ [ตารางเวลาโครงการ](project-creating.md)</span><span class="sxs-lookup"><span data-stu-id="6cb2b-107">For more information about defining project tasks and their functions within a project schedule, see [Project schedules](project-creating.md).</span></span>

## <a name="key-entities"></a><span data-ttu-id="6cb2b-108">เอนทิตีคีย์</span><span class="sxs-lookup"><span data-stu-id="6cb2b-108">Key entities</span></span>
<span data-ttu-id="6cb2b-109">สำหรับโครงสร้างการแบ่งงานที่ถูกต้องที่ถูกโหลดด้วยทรัพยากรอยู่แล้ว จำเป็นต้องมีเอนทิตีต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="6cb2b-109">For an accurate work breakdown structure that is already loaded with resources, the following entities are required:</span></span>

- [<span data-ttu-id="6cb2b-110">โครงการ</span><span class="sxs-lookup"><span data-stu-id="6cb2b-110">Project</span></span>](https://docs.microsoft.com/dynamics365/customerengagement/on-premises/developer/entities/msdyn_project)
- [<span data-ttu-id="6cb2b-111">ทีมโครงการ</span><span class="sxs-lookup"><span data-stu-id="6cb2b-111">Project Team</span></span>](https://docs.microsoft.com/dynamics365/customerengagement/on-premises/developer/entities/msdyn_projectteam)
- [<span data-ttu-id="6cb2b-112">งานโครงการ</span><span class="sxs-lookup"><span data-stu-id="6cb2b-112">Project Task</span></span>](https://docs.microsoft.com/dynamics365/customerengagement/on-premises/developer/entities/msdyn_projecttask)
- [<span data-ttu-id="6cb2b-113">การมอบหมายทรัพยากร</span><span class="sxs-lookup"><span data-stu-id="6cb2b-113">Resource Assignments</span></span>](https://docs.microsoft.com/dynamics365/customerengagement/on-premises/developer/entities/msdyn_resourceassignment)
- [<span data-ttu-id="6cb2b-114">การขึ้นต่อกันของงานโครงการ</span><span class="sxs-lookup"><span data-stu-id="6cb2b-114">Project Task Dependency</span></span>](https://docs.microsoft.com/dynamics365/customerengagement/on-premises/developer/entities/msdyn_projecttaskdependency)
- [<span data-ttu-id="6cb2b-115">ทรัพยากรที่สามารถจองได้</span><span class="sxs-lookup"><span data-stu-id="6cb2b-115">Bookable Resources</span></span>](https://docs.microsoft.com/dynamics365/customerengagement/on-premises/developer/entities/bookableresource)

<span data-ttu-id="6cb2b-116">ในการกำหนดโครงสร้างการแบ่งงานที่โหลดทรัพยากร คุณต้องดำเนินการขั้นตอนต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="6cb2b-116">To define a resource loaded work breakdown structure, you must complete the following steps:</span></span>

1. <span data-ttu-id="6cb2b-117">สร้างโครงการใหม่</span><span class="sxs-lookup"><span data-stu-id="6cb2b-117">Create a new project.</span></span> <span data-ttu-id="6cb2b-118">สำหรับข้อมูลเพิ่มเติมเกี่ยวกับวิธีการสร้างโครงการใหม่ ให้ดูที่ [msdyn_project](https://docs.microsoft.com/dynamics365/customerengagement/on-premises/developer/entities/msdyn_project)</span><span class="sxs-lookup"><span data-stu-id="6cb2b-118">For more information about how to create a new project, see [msdyn_project](https://docs.microsoft.com/dynamics365/customerengagement/on-premises/developer/entities/msdyn_project).</span></span>
2. <span data-ttu-id="6cb2b-119">สร้างงานอย่างน้อยหนึ่งภารกิจ</span><span class="sxs-lookup"><span data-stu-id="6cb2b-119">Create one or more tasks.</span></span> <span data-ttu-id="6cb2b-120">สำหรับข้อมูลเพิ่มเติมเกี่ยวกับวิธีการสร้างงาน ให้ดูที่ [msdyn_projecttask](https://docs.microsoft.com/dynamics365/customerengagement/on-premises/developer/entities/msdyn_projecttask)</span><span class="sxs-lookup"><span data-stu-id="6cb2b-120">For more information about how to create a task, see [msdyn_projecttask](https://docs.microsoft.com/dynamics365/customerengagement/on-premises/developer/entities/msdyn_projecttask).</span></span>
3. <span data-ttu-id="6cb2b-121">กำหนดการขึ้นต่อกันของงาน</span><span class="sxs-lookup"><span data-stu-id="6cb2b-121">Define the task dependencies.</span></span> <span data-ttu-id="6cb2b-122">สำหรับข้อมูลเพิ่มเติม โปรดดูที่ [Project Task Dependency](https://docs.microsoft.com/dynamics365/customerengagement/on-premises/developer/entities/msdyn_projecttaskdependency)</span><span class="sxs-lookup"><span data-stu-id="6cb2b-122">For more information, see [Project Task Dependency](https://docs.microsoft.com/dynamics365/customerengagement/on-premises/developer/entities/msdyn_projecttaskdependency).</span></span>
4. <span data-ttu-id="6cb2b-123">มอบหมายสมาชิกทีมโครงการให้กับโครงการ</span><span class="sxs-lookup"><span data-stu-id="6cb2b-123">Assign project team members to the project.</span></span> <span data-ttu-id="6cb2b-124">สำหรับข้อมูลเพิ่มเติม ให้ดูที่ [msdyn_projectteam](https://docs.microsoft.com/dynamics365/customerengagement/on-premises/developer/entities/msdyn_projectteam)</span><span class="sxs-lookup"><span data-stu-id="6cb2b-124">For more information, see [msdyn_projectteam](https://docs.microsoft.com/dynamics365/customerengagement/on-premises/developer/entities/msdyn_projectteam).</span></span>
5. <span data-ttu-id="6cb2b-125">มอบหมายสมาชิกทีมโครงการให้กับงาน</span><span class="sxs-lookup"><span data-stu-id="6cb2b-125">Assign project team members to the tasks.</span></span> <span data-ttu-id="6cb2b-126">สำหรับข้อมูลเพิ่มเติม ให้ดูที่ [msdyn_resourceassignment](https://docs.microsoft.com/dynamics365/customerengagement/on-premises/developer/entities/msdyn_resourceassignment)</span><span class="sxs-lookup"><span data-stu-id="6cb2b-126">For more information, see [msdyn_resourceassignment](https://docs.microsoft.com/dynamics365/customerengagement/on-premises/developer/entities/msdyn_resourceassignment).</span></span>

## <a name="project-team-relationships"></a><span data-ttu-id="6cb2b-127">ความสัมพันธ์ของสมาชิกทีมโครงการ</span><span class="sxs-lookup"><span data-stu-id="6cb2b-127">Project team relationships</span></span>

<span data-ttu-id="6cb2b-128">เพื่อให้แน่ใจว่าการอัพเกรดประสบความสำเร็จ จะต้องมีการรักษาความสัมพันธ์ต่อไปนี้อย่างถูกต้อง:</span><span class="sxs-lookup"><span data-stu-id="6cb2b-128">To ensure a successful upgrade, the following relationships must be correctly maintained:</span></span>
- <span data-ttu-id="6cb2b-129">สมาชิกในทีมโครงการทั้งหมดต้องเชื่อมโยงกับทรัพยากรที่สามารถจองได้</span><span class="sxs-lookup"><span data-stu-id="6cb2b-129">All project team members must be associated with a bookable resource.</span></span>
- <span data-ttu-id="6cb2b-130">สมาชิกในทีมโครงการทั้งหมดต้องเชื่อมโยงกับโครงการเดียวกัน</span><span class="sxs-lookup"><span data-stu-id="6cb2b-130">All project team members must be associated with the same project.</span></span> 

## <a name="project-task-relationships"></a><span data-ttu-id="6cb2b-131">ความสัมพันธ์ของงานโครงการ</span><span class="sxs-lookup"><span data-stu-id="6cb2b-131">Project task relationships</span></span>
<span data-ttu-id="6cb2b-132">เพื่อให้แน่ใจว่าการอัพเกรดประสบความสำเร็จ จะต้องมีการรักษาความสัมพันธ์ต่อไปนี้อย่างถูกต้อง:</span><span class="sxs-lookup"><span data-stu-id="6cb2b-132">To ensure a successful upgrade, the following relationships must be correctly maintained:</span></span>

- <span data-ttu-id="6cb2b-133">งานที่เกี่ยวข้องใดๆต้องเชื่อมโยงกับโครงการเดียวกัน</span><span class="sxs-lookup"><span data-stu-id="6cb2b-133">Any related tasks must be associated with the same project.</span></span>
- <span data-ttu-id="6cb2b-134">ทุกงานในรายการต้องมีงานหลัก</span><span class="sxs-lookup"><span data-stu-id="6cb2b-134">Every line task must have a parent task.</span></span>
- <span data-ttu-id="6cb2b-135">ทุกงานต้องมีโครงการหลัก</span><span class="sxs-lookup"><span data-stu-id="6cb2b-135">Every task must have a parent project.</span></span>

### <a name="valid-conditions"></a><span data-ttu-id="6cb2b-136">เงื่อนไขที่ถูกต้อง</span><span class="sxs-lookup"><span data-stu-id="6cb2b-136">Valid conditions</span></span>

- <span data-ttu-id="6cb2b-137">ระยะเวลาของงานทั้งหมดต้องมากกว่าหรือเท่ากับ (> =) หนึ่งชั่วโมงและน้อยกว่า 1,800,000 นาที (1,250 วัน)\*</span><span class="sxs-lookup"><span data-stu-id="6cb2b-137">All task durations must be greater than or equal to (>=) one hour and less than 1,800,000 minutes (1,250 days).\*</span></span>
- <span data-ttu-id="6cb2b-138">งานทั้งหมดต้องมีวันที่เริ่มต้นไม่เร็วกว่า 2000/01/01 \*</span><span class="sxs-lookup"><span data-stu-id="6cb2b-138">All tasks must have a start date no earlier than 2000/01/01.\*</span></span>
- <span data-ttu-id="6cb2b-139">งานทั้งหมดต้องมีวันที่เริ่มต้นไม่เกิน 17 ปีนับจากวันปัจจุบัน\*</span><span class="sxs-lookup"><span data-stu-id="6cb2b-139">All tasks must have a start date no later than 17 years from the present day.\*</span></span>
- <span data-ttu-id="6cb2b-140">งานทั้งหมดต้องมีวันที่เริ่มต้นเร็วกว่าหรือเท่ากับวันที่เสร็จสิ้น</span><span class="sxs-lookup"><span data-stu-id="6cb2b-140">All tasks must have a start date earlier or equal to their finish date.</span></span>
- <span data-ttu-id="6cb2b-141">ชนิดธุรกรรมทั้งหมดในการจัดประเภท (ค่าใช้จ่าย วัสดุ ภาษี และเวลา) ต้องมีค่าสำหรับ **หน่วยเริ่มต้น** และ **กลุ่มของหน่วยนับ**</span><span class="sxs-lookup"><span data-stu-id="6cb2b-141">All transaction types on classifications (Expense, Material, Tax, and Time) must have values for **Default Unit** and **Unit Group**.</span></span>
- <span data-ttu-id="6cb2b-142">ควรหลีกเลี่ยงรูปแบบวันที่ที่มีตัวอักษร</span><span class="sxs-lookup"><span data-stu-id="6cb2b-142">Date formats with letters should be avoided.</span></span>

### <a name="potential-mitigation-steps"></a><span data-ttu-id="6cb2b-143">ขั้นตอนการบรรเทาที่มีศักยภาพ</span><span class="sxs-lookup"><span data-stu-id="6cb2b-143">Potential mitigation steps</span></span>
- <span data-ttu-id="6cb2b-144">ใช้การค้นหาขั้นสูงเพื่อระบุงานโครงการที่ไม่มีรหัสโครงการ</span><span class="sxs-lookup"><span data-stu-id="6cb2b-144">Use Advanced Find to identify Project tasks that do not contain a Project ID.</span></span>
- <span data-ttu-id="6cb2b-145">ใช้การค้นหาขั้นสูงเพื่อระบุงานโครงการที่ระยะเวลาที่กำหนดมากกว่า > 1,800,000</span><span class="sxs-lookup"><span data-stu-id="6cb2b-145">Use Advanced Find to identify Project tasks where the scheduled duration is greater than > 1,800,000.</span></span>
- <span data-ttu-id="6cb2b-146">ก่อนทำการเปลี่ยนแปลงข้อมูลใดๆ คุณควรตรวจสอบการปรับแต่งใดๆ ที่เกี่ยวข้องกับเอนทิตีที่อาจนำไปสู่การนำข้อมูลเข้าสู่สถานะไม่ดี</span><span class="sxs-lookup"><span data-stu-id="6cb2b-146">Prior to making any data changes, you should investigate any customizations associated with the entity that may have led to getting the data into a bad state.</span></span> <span data-ttu-id="6cb2b-147">การกำหนดการเหล่านี้ควรได้รับการแก้ไขก่อนที่จะดำเนินการอัปเดตที่เกี่ยวข้องกับข้อมูลใดๆ</span><span class="sxs-lookup"><span data-stu-id="6cb2b-147">These customizations should be addressed before proceeding with any data-related updates.</span></span>
- <span data-ttu-id="6cb2b-148">สำหรับงานที่ระบุที่ได้รับการลงทะเบียนแล้ว ให้พิจารณาลบงานเหล่านี้หากไม่จำเป็น หรือหากคิดว่าควรเกี่ยวข้องกับโครงการหลักที่ถูกต้อง</span><span class="sxs-lookup"><span data-stu-id="6cb2b-148">For the identified tasks that have been orphaned, consider deleting these tasks if they are not needed or if they should be associated with the correct parent project.</span></span>
- <span data-ttu-id="6cb2b-149">สำหรับงานใดๆ ที่มีระยะเวลามากกว่า 1,250 วัน ให้พิจารณาเพิ่มงานหลายรายการเพื่อแสดงระยะเวลารวมหากเป็นไปได้</span><span class="sxs-lookup"><span data-stu-id="6cb2b-149">For any tasks where the duration is greater than 1,250 days, consider adding multiple tasks to represent the total duration, if feasible.</span></span>

> [!NOTE]
> <span data-ttu-id="6cb2b-150">รายการที่ระบุด้วยเครื่องหมายดอกจัน (\*) มีขีดจำกัดที่เนื่องจากข้อเท็จจริงที่ว่าการจัดการความสัมพันธ์ลูกค้า (CRM) สนับสนุนเฉพาะการขยายการเกิดขึ้นประจำ 7,320 รายการ</span><span class="sxs-lookup"><span data-stu-id="6cb2b-150">Items noted with an asterisk (\*) have limits that are due to the fact that customer relationship management (CRM) supports only 7,320 recurrence expansions.</span></span> <span data-ttu-id="6cb2b-151">คุณต้องอยู่ต่ำกว่าขีดจำกัดนี้</span><span class="sxs-lookup"><span data-stu-id="6cb2b-151">You must stay below this limit.</span></span>

## <a name="resource-assignment-relationships"></a><span data-ttu-id="6cb2b-152">ความสัมพันธ์การมอบหมายทรัพยากร</span><span class="sxs-lookup"><span data-stu-id="6cb2b-152">Resource Assignment relationships</span></span>
<span data-ttu-id="6cb2b-153">เพื่อให้แน่ใจว่าการอัพเกรดประสบความสำเร็จ จะต้องมีการรักษาความสัมพันธ์ต่อไปนี้อย่างถูกต้อง:</span><span class="sxs-lookup"><span data-stu-id="6cb2b-153">To ensure a successful upgrade, the following relationships must be correctly maintained:</span></span>

- <span data-ttu-id="6cb2b-154">การมอบหมายทรัพยากรทั้งหมดในโครงสร้างการแบ่งงานต้องเกี่ยวข้องกับโครงการเดียวกัน</span><span class="sxs-lookup"><span data-stu-id="6cb2b-154">All Resource Assignments in a work breakdown structure must be related to the same project.</span></span>
- <span data-ttu-id="6cb2b-155">การมอบหมายทรัพยากรทั้งหมดในโครงสร้างการแบ่งงานต้องเกี่ยวข้องกับสมาชิกทีมโครงการในโครงการเดียวกัน</span><span class="sxs-lookup"><span data-stu-id="6cb2b-155">All Resource Assignments in a work breakdown structure must be associated to project team members in the same project.</span></span>

### <a name="potential-mitigation-steps"></a><span data-ttu-id="6cb2b-156">ขั้นตอนการบรรเทาที่มีศักยภาพ</span><span class="sxs-lookup"><span data-stu-id="6cb2b-156">Potential mitigation steps</span></span>
- <span data-ttu-id="6cb2b-157">ระบุงานทั้งหมดที่อยู่นอกเงื่อนไขที่อธิบายไว้ข้างต้น</span><span class="sxs-lookup"><span data-stu-id="6cb2b-157">Identify all tasks that fall outside the conditions described above.</span></span>  
- <span data-ttu-id="6cb2b-158">ควรลบการกำหนดทรัพยากรใดๆ ที่ไม่ถูกต้องอีกต่อไป</span><span class="sxs-lookup"><span data-stu-id="6cb2b-158">Any Resource Assignments that are no longer valid should be deleted.</span></span>

## <a name="project-task-dependency-relationships"></a><span data-ttu-id="6cb2b-159">ความสัมพันธ์การขึ้นต่อกันของงานโครงการ</span><span class="sxs-lookup"><span data-stu-id="6cb2b-159">Project task dependency relationships</span></span>
<span data-ttu-id="6cb2b-160">เพื่อให้แน่ใจว่าการอัพเกรดประสบความสำเร็จ จะต้องมีการรักษาความสัมพันธ์ต่อไปนี้อย่างถูกต้อง:</span><span class="sxs-lookup"><span data-stu-id="6cb2b-160">To ensure a successful upgrade, the following relationships must be correctly maintained:</span></span>

- <span data-ttu-id="6cb2b-161">การขึ้นต่อกันของงานโครงการทั้งหมดต้องเกี่ยวข้องกับโครงการเดียวกัน</span><span class="sxs-lookup"><span data-stu-id="6cb2b-161">All project task dependencies must be related to the same project.</span></span>
- <span data-ttu-id="6cb2b-162">งานไม่สามารถมีการอ้างอิงการขึ้นต่อกันเหมือนกันมากกว่าหนึ่งครั้ง</span><span class="sxs-lookup"><span data-stu-id="6cb2b-162">A task can't have the same dependency referenced more than once.</span></span>
