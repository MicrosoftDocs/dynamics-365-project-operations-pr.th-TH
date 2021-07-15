---
title: ใช้ API กำหนดการโครงการเพื่อดำเนินการกับเอนทิตีการจัดกำหนดการ
description: หัวข้อนี้ให้ข้อมูลและตัวอย่างสำหรับการใช้ API กำหนดการโครงการ
author: sigitac
ms.date: 06/22/2021
ms.topic: article
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 4915261c08a3271a919e04084e92a14b297c1b35
ms.sourcegitcommit: 2f16c2bc7c8350676a6a380c61fffa9958db6a0b
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 06/22/2021
ms.locfileid: "6293250"
---
# <a name="use-project-schedule-apis-to-perform-operations-with-scheduling-entities"></a><span data-ttu-id="8ec2b-103">ใช้ API กำหนดการโครงการเพื่อดำเนินการกับเอนทิตีการจัดกำหนดการ</span><span class="sxs-lookup"><span data-stu-id="8ec2b-103">Use Project schedule APIs to perform operations with Scheduling entities</span></span>

<span data-ttu-id="8ec2b-104">_**นำไปใช้กับ:** Project Operations สำหรับสถานการณ์ตามทรัพยากร/วัสดุที่ไม่ได้เก็บในคลัง การปรับใช้งานแบบ Lite - จัดการกับการออกใบแจ้งหนี้ชั่วคราว_</span><span class="sxs-lookup"><span data-stu-id="8ec2b-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

> [!IMPORTANT] 
> <span data-ttu-id="8ec2b-105">ฟังก์ชันการทำงานบางส่วนหรือทั้งหมดที่ระบุไว้ในหัวข้อนี้มีให้โดยเป็นส่วนหนึ่งของรุ่นพรีวิว</span><span class="sxs-lookup"><span data-stu-id="8ec2b-105">Some or all of the functionality noted in this topic is available as part of a preview release.</span></span> <span data-ttu-id="8ec2b-106">เนื้อหาและฟังก์ชันการทำงานอาจเปลี่ยนแปลงได้</span><span class="sxs-lookup"><span data-stu-id="8ec2b-106">The content and the functionality are subject to change.</span></span> 

## <a name="scheduling-entities"></a><span data-ttu-id="8ec2b-107">เอนทิตีการจัดกำหนดการ</span><span class="sxs-lookup"><span data-stu-id="8ec2b-107">Scheduling entities</span></span>

<span data-ttu-id="8ec2b-108">API กำหนดการโครงการให้ความสามารถในการสร้าง อัปเดต และลบการดำเนินการด้วย **เอนทิตีการจัดกำหนดการ**</span><span class="sxs-lookup"><span data-stu-id="8ec2b-108">Project schedule APIs provide the ability to perform create, update, and delete operations with **Scheduling entities**.</span></span> <span data-ttu-id="8ec2b-109">เอนทิตีเหล่านี้ได้รับการจัดการผ่านกลไกการจัดกำหนดการในโครงการสำหรับเว็บ</span><span class="sxs-lookup"><span data-stu-id="8ec2b-109">These entities are managed through the Scheduling engine in Project for the web.</span></span> <span data-ttu-id="8ec2b-110">สร้าง ปรับปรุง และลบการดำเนินงานกับ **เอนทิตีการจัดกำหนดการ** มีการจำกัดใน Dynamics 365 Project Operations รุ่นก่อนหน้า</span><span class="sxs-lookup"><span data-stu-id="8ec2b-110">Create, update, and delete operations with **Scheduling entities** were restricted in earlier Dynamics 365 Project Operations releases.</span></span>

<span data-ttu-id="8ec2b-111">ตารางต่อไปนี้แสดงรายการเอนทิตีกำหนดการโครงการทั้งหมด</span><span class="sxs-lookup"><span data-stu-id="8ec2b-111">The following table provides a full list of the Project schedule entities.</span></span>

| <span data-ttu-id="8ec2b-112">ชื่อเอนทิตี</span><span class="sxs-lookup"><span data-stu-id="8ec2b-112">Entity name</span></span>  | <span data-ttu-id="8ec2b-113">ชื่อตรรกะของเอนทิตี</span><span class="sxs-lookup"><span data-stu-id="8ec2b-113">Entity logical name</span></span> |
| --- | --- |
| <span data-ttu-id="8ec2b-114">Project</span><span class="sxs-lookup"><span data-stu-id="8ec2b-114">Project</span></span> | <span data-ttu-id="8ec2b-115">msdyn_project</span><span class="sxs-lookup"><span data-stu-id="8ec2b-115">msdyn_project</span></span> |
| <span data-ttu-id="8ec2b-116">งานโครงการ</span><span class="sxs-lookup"><span data-stu-id="8ec2b-116">Project Task</span></span>  | <span data-ttu-id="8ec2b-117">msdyn_projecttask</span><span class="sxs-lookup"><span data-stu-id="8ec2b-117">msdyn_projecttask</span></span>  |
| <span data-ttu-id="8ec2b-118">การขึ้นต่อกันของงานโครงการ</span><span class="sxs-lookup"><span data-stu-id="8ec2b-118">Project Task Dependency</span></span>  | <span data-ttu-id="8ec2b-119">msdyn_projecttaskdependency</span><span class="sxs-lookup"><span data-stu-id="8ec2b-119">msdyn_projecttaskdependency</span></span>  |
| <span data-ttu-id="8ec2b-120">การมอบหมายทรัพยากร</span><span class="sxs-lookup"><span data-stu-id="8ec2b-120">Resource Assignment</span></span> | <span data-ttu-id="8ec2b-121">msdyn_resourceassignment</span><span class="sxs-lookup"><span data-stu-id="8ec2b-121">msdyn_resourceassignment</span></span> |
| <span data-ttu-id="8ec2b-122">บักเก็ตโครงการ</span><span class="sxs-lookup"><span data-stu-id="8ec2b-122">Project Bucket</span></span>  | <span data-ttu-id="8ec2b-123">msdyn_projectbucket</span><span class="sxs-lookup"><span data-stu-id="8ec2b-123">msdyn_projectbucket</span></span> |
| <span data-ttu-id="8ec2b-124">สมาชิกของทีมโครงการ</span><span class="sxs-lookup"><span data-stu-id="8ec2b-124">Project Team Member</span></span> | <span data-ttu-id="8ec2b-125">msdyn_projectteam</span><span class="sxs-lookup"><span data-stu-id="8ec2b-125">msdyn_projectteam</span></span> |

## <a name="operationset"></a><span data-ttu-id="8ec2b-126">OperationSet</span><span class="sxs-lookup"><span data-stu-id="8ec2b-126">OperationSet</span></span>

<span data-ttu-id="8ec2b-127">OperationSet เป็นรูปแบบหน่วยการทำงานที่สามารถใช้เมื่อต้องดำเนินการตามกำหนดการหลายรายการที่ส่งผลกระทบต่อคำขอภายในธุรกรรม</span><span class="sxs-lookup"><span data-stu-id="8ec2b-127">OperationSet is a unit-of-work pattern that can be used when several schedule impacting requests must be processed within a transaction.</span></span>

## <a name="project-schedule-apis"></a><span data-ttu-id="8ec2b-128">API กำหนดการโครงการ</span><span class="sxs-lookup"><span data-stu-id="8ec2b-128">Project schedule APIs</span></span>

<span data-ttu-id="8ec2b-129">ต่อไปนี้คือรายการ API กำหนดการโครงการปัจจุบัน</span><span class="sxs-lookup"><span data-stu-id="8ec2b-129">The following is a list of current Project schedule APIs.</span></span>

- <span data-ttu-id="8ec2b-130">**msdyn_CreateProjectV1**: API นี้สามารถใช้ในการสร้างโครงการ</span><span class="sxs-lookup"><span data-stu-id="8ec2b-130">**msdyn_CreateProjectV1**: This API can be used to create a project.</span></span> <span data-ttu-id="8ec2b-131">โครงการและบักเก็ตโครงการเริ่มต้นจะมีการสร้างในทันที</span><span class="sxs-lookup"><span data-stu-id="8ec2b-131">The project and default project bucket is created immediately.</span></span>
- <span data-ttu-id="8ec2b-132">**msdyn_CreateTeamMemberV1**: API นี้สามารถใช้เพื่อสร้างสมาชิกทีมโครงการ</span><span class="sxs-lookup"><span data-stu-id="8ec2b-132">**msdyn_CreateTeamMemberV1**: This API can be used to create a project team member.</span></span> <span data-ttu-id="8ec2b-133">โดยจะมีการสร้างสมาชิกทีมในทันที</span><span class="sxs-lookup"><span data-stu-id="8ec2b-133">The team member record is created immediately.</span></span>
- <span data-ttu-id="8ec2b-134">**msdyn_CreateOperationSetV1**: API นี้สามารถใช้เพื่อจัดกำหนดการคำขอต่างๆ ที่ต้องดำเนินการภายในธุรกรรม</span><span class="sxs-lookup"><span data-stu-id="8ec2b-134">**msdyn_CreateOperationSetV1**: This API can be used to schedule several requests that must be performed within a transaction.</span></span>
- <span data-ttu-id="8ec2b-135">**msdyn_PSSCreateV1**: API นี้สามารถใช้เพื่อสร้างเอนทิตี</span><span class="sxs-lookup"><span data-stu-id="8ec2b-135">**msdyn_PSSCreateV1**: This API can be used to create an entity.</span></span> <span data-ttu-id="8ec2b-136">เอนทิตีสามารถเป็นเอนทิตีการจัดกำหนดการโครงการใดๆ ที่สนับสนุนการดำเนินการสร้าง</span><span class="sxs-lookup"><span data-stu-id="8ec2b-136">The entity can be any of the Project scheduling entities that support the create operation.</span></span>
- <span data-ttu-id="8ec2b-137">**msdyn_PSSUpdateV1**: API นี้สามารถใช้เพื่อปรับปรุงเอนทิตี</span><span class="sxs-lookup"><span data-stu-id="8ec2b-137">**msdyn_PSSUpdateV1**: This API can be used to update an entity.</span></span> <span data-ttu-id="8ec2b-138">เอนทิตีสามารถเป็นเอนทิตีการจัดกำหนดการโครงการใดๆ ที่สนับสนุนการดำเนินการอัปเดต</span><span class="sxs-lookup"><span data-stu-id="8ec2b-138">The entity can be any of the Project scheduling entities that support the update operation.</span></span>
- <span data-ttu-id="8ec2b-139">**msdyn_PSSDeleteV1**: API นี้สามารถใช้เพื่อลบเอนทิตี</span><span class="sxs-lookup"><span data-stu-id="8ec2b-139">**msdyn_PSSDeleteV1**: This API can be used to delete an entity.</span></span> <span data-ttu-id="8ec2b-140">เอนทิตีสามารถเป็นเอนทิตีการจัดกำหนดการโครงการใดๆ ที่สนับสนุนการดำเนินการลบ</span><span class="sxs-lookup"><span data-stu-id="8ec2b-140">The entity can be any of the Project scheduling entities that support the delete operation.</span></span>
- <span data-ttu-id="8ec2b-141">**msdyn_ExecuteOperationSetV1**: API นี้ใช้เพื่อดำเนินงานทั้งหมดภายในชุดการดำเนินงานที่กำหนด</span><span class="sxs-lookup"><span data-stu-id="8ec2b-141">**msdyn_ExecuteOperationSetV1**: This API is used to execute all of the operations within the given operation set.</span></span>

## <a name="using-project-schedule-apis-with-operationset"></a><span data-ttu-id="8ec2b-142">การใช้ API กำหนดการโครงการกับ OperationSet</span><span class="sxs-lookup"><span data-stu-id="8ec2b-142">Using Project schedule APIs with OperationSet</span></span>

<span data-ttu-id="8ec2b-143">เนื่องจากเรกคอร์ด **CreateProjectV1** และ **CreateTeamMemberV1** ทั้งคู่มีการสร้างขึ้นในทันที API เหล่านี้จึงไม่สามารถใช้ใน **OperationSet** ได้โดยตรง</span><span class="sxs-lookup"><span data-stu-id="8ec2b-143">Because records with both **CreateProjectV1** and **CreateTeamMemberV1** are created immediately, these APIs can't be used in the **OperationSet** directly.</span></span> <span data-ttu-id="8ec2b-144">อย่างไรก็ตาม คุณสามารถใช้ API ดังกล่าวเพื่อสร้างเรกคอร์ดที่จำเป็น สร้าง **OperationSet** จากนั้นใช้เรกคอร์ดที่สร้างไว้ล่วงหน้าเหล่านี้ใน **OperationSet**</span><span class="sxs-lookup"><span data-stu-id="8ec2b-144">However, you can use the API to create needed records, create an **OperationSet**, and then use these pre-created records in the **OperationSet**.</span></span>

## <a name="supported-operations"></a><span data-ttu-id="8ec2b-145">การดำเนินการที่รองรับ</span><span class="sxs-lookup"><span data-stu-id="8ec2b-145">Supported operations</span></span>

| <span data-ttu-id="8ec2b-146">เอนทิตีการจัดกำหนดการ</span><span class="sxs-lookup"><span data-stu-id="8ec2b-146">Scheduling entity</span></span> | <span data-ttu-id="8ec2b-147">สร้าง</span><span class="sxs-lookup"><span data-stu-id="8ec2b-147">Create</span></span> | <span data-ttu-id="8ec2b-148">อัปเดต</span><span class="sxs-lookup"><span data-stu-id="8ec2b-148">Update</span></span> | <span data-ttu-id="8ec2b-149">Delete</span><span class="sxs-lookup"><span data-stu-id="8ec2b-149">Delete</span></span> | <span data-ttu-id="8ec2b-150">ข้อควรพิจารณาที่สำคัญ</span><span class="sxs-lookup"><span data-stu-id="8ec2b-150">Important considerations</span></span> |
| --- | --- | --- | --- | --- |
<span data-ttu-id="8ec2b-151">งานโครงการ</span><span class="sxs-lookup"><span data-stu-id="8ec2b-151">Project task</span></span> | <span data-ttu-id="8ec2b-152">ใช่</span><span class="sxs-lookup"><span data-stu-id="8ec2b-152">Yes</span></span> | <span data-ttu-id="8ec2b-153">ใช่</span><span class="sxs-lookup"><span data-stu-id="8ec2b-153">Yes</span></span> | <span data-ttu-id="8ec2b-154">ใช่</span><span class="sxs-lookup"><span data-stu-id="8ec2b-154">Yes</span></span> | <span data-ttu-id="8ec2b-155">ไม่มี</span><span class="sxs-lookup"><span data-stu-id="8ec2b-155">None</span></span> |
| <span data-ttu-id="8ec2b-156">การขึ้นต่อกันของงานโครงการ</span><span class="sxs-lookup"><span data-stu-id="8ec2b-156">Project task dependency</span></span> | <span data-ttu-id="8ec2b-157">ใช่</span><span class="sxs-lookup"><span data-stu-id="8ec2b-157">Yes</span></span> | <span data-ttu-id="8ec2b-158">ใช่</span><span class="sxs-lookup"><span data-stu-id="8ec2b-158">Yes</span></span> | | <span data-ttu-id="8ec2b-159">ไม่ปรับปรุงเรกคอร์ดการขึ้นต่อกันของงานโครงการ</span><span class="sxs-lookup"><span data-stu-id="8ec2b-159">Project task dependency records aren't updated.</span></span> <span data-ttu-id="8ec2b-160">แต่สามารถลบเรกคอร์ดเก่าและสร้างเรกคอร์ดใหม่ได้</span><span class="sxs-lookup"><span data-stu-id="8ec2b-160">Instead, an old record can be deleted and a new record can be created.</span></span> |
| <span data-ttu-id="8ec2b-161">การกำหนดทรัพยากร</span><span class="sxs-lookup"><span data-stu-id="8ec2b-161">Resource assignment</span></span> | <span data-ttu-id="8ec2b-162">ใช่</span><span class="sxs-lookup"><span data-stu-id="8ec2b-162">Yes</span></span> | <span data-ttu-id="8ec2b-163">ใช่</span><span class="sxs-lookup"><span data-stu-id="8ec2b-163">Yes</span></span> | | <span data-ttu-id="8ec2b-164">ไม่รองรับการดำเนินการกับฟิลด์ต่อไปนี้: **BookableResourceID**, **Effort**, **EffortCompleted**, **EffortRemaining** และ **PlannedWork**</span><span class="sxs-lookup"><span data-stu-id="8ec2b-164">Operations with the following fields aren't supported: **BookableResourceID**, **Effort**, **EffortCompleted**, **EffortRemaining**, and **PlannedWork**.</span></span> <span data-ttu-id="8ec2b-165">ไม่ปรับปรุงเรกคอร์ดการกำหนดทรัพยากร</span><span class="sxs-lookup"><span data-stu-id="8ec2b-165">Resource assignment records aren't updated.</span></span> <span data-ttu-id="8ec2b-166">แต่สามารถลบเรกคอร์ดเก่าและสร้างเรกคอร์ดใหม่ได้</span><span class="sxs-lookup"><span data-stu-id="8ec2b-166">Instead, the old record can be deleted and a new record can be created.</span></span> |
| <span data-ttu-id="8ec2b-167">บักเก็ตโครงการ</span><span class="sxs-lookup"><span data-stu-id="8ec2b-167">Project bucket</span></span> | <span data-ttu-id="8ec2b-168">ไม่พร้อมใช้งาน</span><span class="sxs-lookup"><span data-stu-id="8ec2b-168">N/A</span></span> | <span data-ttu-id="8ec2b-169">ไม่พร้อมใช้งาน</span><span class="sxs-lookup"><span data-stu-id="8ec2b-169">N/A</span></span> | <span data-ttu-id="8ec2b-170">ไม่พร้อมใช้งาน</span><span class="sxs-lookup"><span data-stu-id="8ec2b-170">N/A</span></span> | <span data-ttu-id="8ec2b-171">มีการสร้างบักเก็ตโครงการเริ่มต้นโดยใช้ **CreateProjectV1** API</span><span class="sxs-lookup"><span data-stu-id="8ec2b-171">The default bucket is created using the **CreateProjectV1** API.</span></span> |
| <span data-ttu-id="8ec2b-172">สมาชิกของทีมโครงการ</span><span class="sxs-lookup"><span data-stu-id="8ec2b-172">Project team member</span></span> | <span data-ttu-id="8ec2b-173">ใช่</span><span class="sxs-lookup"><span data-stu-id="8ec2b-173">Yes</span></span> | <span data-ttu-id="8ec2b-174">ใช่</span><span class="sxs-lookup"><span data-stu-id="8ec2b-174">Yes</span></span> | <span data-ttu-id="8ec2b-175">ใช่</span><span class="sxs-lookup"><span data-stu-id="8ec2b-175">Yes</span></span> | <span data-ttu-id="8ec2b-176">สำหรับการดำเนินการสร้าง ให้ใช้ **CreateTeamMemberV1** API</span><span class="sxs-lookup"><span data-stu-id="8ec2b-176">For the create operation, use the **CreateTeamMemberV1** API.</span></span> |
| <span data-ttu-id="8ec2b-177">Project</span><span class="sxs-lookup"><span data-stu-id="8ec2b-177">Project</span></span> | <span data-ttu-id="8ec2b-178">ใช่</span><span class="sxs-lookup"><span data-stu-id="8ec2b-178">Yes</span></span> | <span data-ttu-id="8ec2b-179">ใช่</span><span class="sxs-lookup"><span data-stu-id="8ec2b-179">Yes</span></span> | <span data-ttu-id="8ec2b-180">ไม่พร้อมใช้งาน</span><span class="sxs-lookup"><span data-stu-id="8ec2b-180">N/A</span></span> | <span data-ttu-id="8ec2b-181">ไม่รองรับการดำเนินการกับฟิลด์ต่อไปนี้: **StateCode**, **BulkGenerationStatus**, **GlobalRevisionToken**, **CalendarID**, **Effort**, **EffortCompleted**, **EffortRemaining**, **Progress**, **Finish**, **TaskEarliestStart** และ **Duration**</span><span class="sxs-lookup"><span data-stu-id="8ec2b-181">Operations with the following fields aren't supported: **StateCode**, **BulkGenerationStatus**, **GlobalRevisionToken**, **CalendarID**, **Effort**, **EffortCompleted**, **EffortRemaining**, **Progress**, **Finish**, **TaskEarliestStart**, and **Duration**.</span></span> |

<span data-ttu-id="8ec2b-182">API เหล่านี้สามารถเรียกใช้กับเอนทิตีอ็อบเจ็กต์ที่มีฟิลด์แบบกำหนดเอง</span><span class="sxs-lookup"><span data-stu-id="8ec2b-182">These APIs can be called with entity objects that include custom fields.</span></span>

<span data-ttu-id="8ec2b-183">รหัสคุณสมบัติเป็นแบบระบุหรือไม่ก็ได้</span><span class="sxs-lookup"><span data-stu-id="8ec2b-183">The ID property is optional.</span></span> <span data-ttu-id="8ec2b-184">หากระบุ ระบบจะพยายามใช้และแสดงข้อยกเว้นหากไม่สามารถใช้งานได้</span><span class="sxs-lookup"><span data-stu-id="8ec2b-184">If it's provided, the system attempts to use it and throws an exception if it can't be used.</span></span> <span data-ttu-id="8ec2b-185">หากไม่ระบบ ระบบจะสร้างขึ้นเอง</span><span class="sxs-lookup"><span data-stu-id="8ec2b-185">If it isn't provided, the system will generate it.</span></span>

## <a name="restricted-fields"></a><span data-ttu-id="8ec2b-186">ฟิลด์ที่ถูกจำกัด</span><span class="sxs-lookup"><span data-stu-id="8ec2b-186">Restricted fields</span></span>

<span data-ttu-id="8ec2b-187">ตารางต่อไปนี้กำหนดฟิลด์ที่ถูกจำกัดจาก **สร้าง** และ **แก้ไข**</span><span class="sxs-lookup"><span data-stu-id="8ec2b-187">The following tables define the fields that are restricted from **Create** and **Edit.**</span></span>

### <a name="project-task"></a><span data-ttu-id="8ec2b-188">งานโครงการ</span><span class="sxs-lookup"><span data-stu-id="8ec2b-188">Project task</span></span>

| <span data-ttu-id="8ec2b-189">**ชื่อตรรกะ**</span><span class="sxs-lookup"><span data-stu-id="8ec2b-189">**Logical name**</span></span>                       | <span data-ttu-id="8ec2b-190">**สามารถสร้าง**</span><span class="sxs-lookup"><span data-stu-id="8ec2b-190">**Can create**</span></span> | <span data-ttu-id="8ec2b-191">**สามารถแก้ไข**</span><span class="sxs-lookup"><span data-stu-id="8ec2b-191">**Can edit**</span></span>     |
|----------------------------------------|----------------|------------------|
| <span data-ttu-id="8ec2b-192">msdyn_actualcost</span><span class="sxs-lookup"><span data-stu-id="8ec2b-192">msdyn_actualcost</span></span>                       | <span data-ttu-id="8ec2b-193">ไม่ใช่</span><span class="sxs-lookup"><span data-stu-id="8ec2b-193">no</span></span>             | <span data-ttu-id="8ec2b-194">ไม่ใช่</span><span class="sxs-lookup"><span data-stu-id="8ec2b-194">no</span></span>               |
| <span data-ttu-id="8ec2b-195">msdyn_actualcost_base</span><span class="sxs-lookup"><span data-stu-id="8ec2b-195">msdyn_actualcost_base</span></span>                  | <span data-ttu-id="8ec2b-196">ไม่ใช่</span><span class="sxs-lookup"><span data-stu-id="8ec2b-196">no</span></span>             | <span data-ttu-id="8ec2b-197">ไม่ใช่</span><span class="sxs-lookup"><span data-stu-id="8ec2b-197">no</span></span>               |
| <span data-ttu-id="8ec2b-198">msdyn_actualend</span><span class="sxs-lookup"><span data-stu-id="8ec2b-198">msdyn_actualend</span></span>                        | <span data-ttu-id="8ec2b-199">ไม่ใช่</span><span class="sxs-lookup"><span data-stu-id="8ec2b-199">no</span></span>             | <span data-ttu-id="8ec2b-200">ไม่ใช่</span><span class="sxs-lookup"><span data-stu-id="8ec2b-200">no</span></span>               |
| <span data-ttu-id="8ec2b-201">msdyn_actualend</span><span class="sxs-lookup"><span data-stu-id="8ec2b-201">msdyn_actualsales</span></span>                      | <span data-ttu-id="8ec2b-202">ไม่ใช่</span><span class="sxs-lookup"><span data-stu-id="8ec2b-202">no</span></span>             | <span data-ttu-id="8ec2b-203">ไม่ใช่</span><span class="sxs-lookup"><span data-stu-id="8ec2b-203">no</span></span>               |
| <span data-ttu-id="8ec2b-204">msdyn_actualsales_base</span><span class="sxs-lookup"><span data-stu-id="8ec2b-204">msdyn_actualsales_base</span></span>                 | <span data-ttu-id="8ec2b-205">ไม่ใช่</span><span class="sxs-lookup"><span data-stu-id="8ec2b-205">no</span></span>             | <span data-ttu-id="8ec2b-206">ไม่ใช่</span><span class="sxs-lookup"><span data-stu-id="8ec2b-206">no</span></span>               |
| <span data-ttu-id="8ec2b-207">msdyn_actualstart</span><span class="sxs-lookup"><span data-stu-id="8ec2b-207">msdyn_actualstart</span></span>                      | <span data-ttu-id="8ec2b-208">ไม่ใช่</span><span class="sxs-lookup"><span data-stu-id="8ec2b-208">no</span></span>             | <span data-ttu-id="8ec2b-209">ไม่ใช่</span><span class="sxs-lookup"><span data-stu-id="8ec2b-209">no</span></span>               |
| <span data-ttu-id="8ec2b-210">msdyn_costatcompleteestimate</span><span class="sxs-lookup"><span data-stu-id="8ec2b-210">msdyn_costatcompleteestimate</span></span>           | <span data-ttu-id="8ec2b-211">ไม่ใช่</span><span class="sxs-lookup"><span data-stu-id="8ec2b-211">no</span></span>             | <span data-ttu-id="8ec2b-212">ไม่ใช่</span><span class="sxs-lookup"><span data-stu-id="8ec2b-212">no</span></span>               |
| <span data-ttu-id="8ec2b-213">msdyn_costatcompleteestimate_base</span><span class="sxs-lookup"><span data-stu-id="8ec2b-213">msdyn_costatcompleteestimate_base</span></span>      | <span data-ttu-id="8ec2b-214">ไม่ใช่</span><span class="sxs-lookup"><span data-stu-id="8ec2b-214">no</span></span>             | <span data-ttu-id="8ec2b-215">ไม่ใช่</span><span class="sxs-lookup"><span data-stu-id="8ec2b-215">no</span></span>               |
| <span data-ttu-id="8ec2b-216">msdyn_costconsumptionpercentage</span><span class="sxs-lookup"><span data-stu-id="8ec2b-216">msdyn_costconsumptionpercentage</span></span>        | <span data-ttu-id="8ec2b-217">ไม่ใช่</span><span class="sxs-lookup"><span data-stu-id="8ec2b-217">no</span></span>             | <span data-ttu-id="8ec2b-218">ไม่ใช่</span><span class="sxs-lookup"><span data-stu-id="8ec2b-218">no</span></span>               |
| <span data-ttu-id="8ec2b-219">msdyn_effortcompleted</span><span class="sxs-lookup"><span data-stu-id="8ec2b-219">msdyn_effortcompleted</span></span>                  | <span data-ttu-id="8ec2b-220">ไม่ใช่</span><span class="sxs-lookup"><span data-stu-id="8ec2b-220">no</span></span>             | <span data-ttu-id="8ec2b-221">ไม่ใช่</span><span class="sxs-lookup"><span data-stu-id="8ec2b-221">no</span></span>               |
| <span data-ttu-id="8ec2b-222">msdyn_effortestimateatcomplete</span><span class="sxs-lookup"><span data-stu-id="8ec2b-222">msdyn_effortestimateatcomplete</span></span>         | <span data-ttu-id="8ec2b-223">ไม่ใช่</span><span class="sxs-lookup"><span data-stu-id="8ec2b-223">no</span></span>             | <span data-ttu-id="8ec2b-224">ไม่ใช่</span><span class="sxs-lookup"><span data-stu-id="8ec2b-224">no</span></span>               |
| <span data-ttu-id="8ec2b-225">msdyn_iscritical</span><span class="sxs-lookup"><span data-stu-id="8ec2b-225">msdyn_iscritical</span></span>                       | <span data-ttu-id="8ec2b-226">ไม่ใช่</span><span class="sxs-lookup"><span data-stu-id="8ec2b-226">no</span></span>             | <span data-ttu-id="8ec2b-227">ไม่ใช่</span><span class="sxs-lookup"><span data-stu-id="8ec2b-227">no</span></span>               |
| <span data-ttu-id="8ec2b-228">msdyn_iscriticalname</span><span class="sxs-lookup"><span data-stu-id="8ec2b-228">msdyn_iscriticalname</span></span>                   | <span data-ttu-id="8ec2b-229">ไม่ใช่</span><span class="sxs-lookup"><span data-stu-id="8ec2b-229">no</span></span>             | <span data-ttu-id="8ec2b-230">ไม่ใช่</span><span class="sxs-lookup"><span data-stu-id="8ec2b-230">no</span></span>               |
| <span data-ttu-id="8ec2b-231">msdyn_ismanual</span><span class="sxs-lookup"><span data-stu-id="8ec2b-231">msdyn_ismanual</span></span>                         | <span data-ttu-id="8ec2b-232">ไม่ใช่</span><span class="sxs-lookup"><span data-stu-id="8ec2b-232">no</span></span>             | <span data-ttu-id="8ec2b-233">ไม่ใช่</span><span class="sxs-lookup"><span data-stu-id="8ec2b-233">no</span></span>               |
| <span data-ttu-id="8ec2b-234">msdyn_ismanualname</span><span class="sxs-lookup"><span data-stu-id="8ec2b-234">msdyn_ismanualname</span></span>                     | <span data-ttu-id="8ec2b-235">ไม่ใช่</span><span class="sxs-lookup"><span data-stu-id="8ec2b-235">no</span></span>             | <span data-ttu-id="8ec2b-236">ไม่ใช่</span><span class="sxs-lookup"><span data-stu-id="8ec2b-236">no</span></span>               |
| <span data-ttu-id="8ec2b-237">msdyn_ismilestone</span><span class="sxs-lookup"><span data-stu-id="8ec2b-237">msdyn_ismilestone</span></span>                      | <span data-ttu-id="8ec2b-238">ไม่ใช่</span><span class="sxs-lookup"><span data-stu-id="8ec2b-238">no</span></span>             | <span data-ttu-id="8ec2b-239">ไม่ใช่</span><span class="sxs-lookup"><span data-stu-id="8ec2b-239">no</span></span>               |
| <span data-ttu-id="8ec2b-240">msdyn_ismilestonename</span><span class="sxs-lookup"><span data-stu-id="8ec2b-240">msdyn_ismilestonename</span></span>                  | <span data-ttu-id="8ec2b-241">ไม่ใช่</span><span class="sxs-lookup"><span data-stu-id="8ec2b-241">no</span></span>             | <span data-ttu-id="8ec2b-242">ไม่ใช่</span><span class="sxs-lookup"><span data-stu-id="8ec2b-242">no</span></span>               |
| <span data-ttu-id="8ec2b-243">msdyn_LinkStatus</span><span class="sxs-lookup"><span data-stu-id="8ec2b-243">msdyn_LinkStatus</span></span>                       | <span data-ttu-id="8ec2b-244">ไม่ใช่</span><span class="sxs-lookup"><span data-stu-id="8ec2b-244">no</span></span>             | <span data-ttu-id="8ec2b-245">ไม่ใช่</span><span class="sxs-lookup"><span data-stu-id="8ec2b-245">no</span></span>               |
| <span data-ttu-id="8ec2b-246">msdyn_linkstatusname</span><span class="sxs-lookup"><span data-stu-id="8ec2b-246">msdyn_linkstatusname</span></span>                   | <span data-ttu-id="8ec2b-247">ไม่ใช่</span><span class="sxs-lookup"><span data-stu-id="8ec2b-247">no</span></span>             | <span data-ttu-id="8ec2b-248">ไม่ใช่</span><span class="sxs-lookup"><span data-stu-id="8ec2b-248">no</span></span>               |
| <span data-ttu-id="8ec2b-249">msdyn_msprojectclientid</span><span class="sxs-lookup"><span data-stu-id="8ec2b-249">msdyn_msprojectclientid</span></span>                | <span data-ttu-id="8ec2b-250">ไม่ใช่</span><span class="sxs-lookup"><span data-stu-id="8ec2b-250">no</span></span>             | <span data-ttu-id="8ec2b-251">ไม่ใช่</span><span class="sxs-lookup"><span data-stu-id="8ec2b-251">no</span></span>               |
| <span data-ttu-id="8ec2b-252">msdyn_plannedcost</span><span class="sxs-lookup"><span data-stu-id="8ec2b-252">msdyn_plannedcost</span></span>                      | <span data-ttu-id="8ec2b-253">ไม่ใช่</span><span class="sxs-lookup"><span data-stu-id="8ec2b-253">no</span></span>             | <span data-ttu-id="8ec2b-254">ไม่ใช่</span><span class="sxs-lookup"><span data-stu-id="8ec2b-254">no</span></span>               |
| <span data-ttu-id="8ec2b-255">msdyn_plannedcost_base</span><span class="sxs-lookup"><span data-stu-id="8ec2b-255">msdyn_plannedcost_base</span></span>                 | <span data-ttu-id="8ec2b-256">ไม่ใช่</span><span class="sxs-lookup"><span data-stu-id="8ec2b-256">no</span></span>             | <span data-ttu-id="8ec2b-257">ไม่ใช่</span><span class="sxs-lookup"><span data-stu-id="8ec2b-257">no</span></span>               |
| <span data-ttu-id="8ec2b-258">msdyn_plannedsales</span><span class="sxs-lookup"><span data-stu-id="8ec2b-258">msdyn_plannedsales</span></span>                     | <span data-ttu-id="8ec2b-259">ไม่ใช่</span><span class="sxs-lookup"><span data-stu-id="8ec2b-259">no</span></span>             | <span data-ttu-id="8ec2b-260">ไม่ใช่</span><span class="sxs-lookup"><span data-stu-id="8ec2b-260">no</span></span>               |
| <span data-ttu-id="8ec2b-261">msdyn_plannedsales_base</span><span class="sxs-lookup"><span data-stu-id="8ec2b-261">msdyn_plannedsales_base</span></span>                | <span data-ttu-id="8ec2b-262">ไม่ใช่</span><span class="sxs-lookup"><span data-stu-id="8ec2b-262">no</span></span>             | <span data-ttu-id="8ec2b-263">ไม่ใช่</span><span class="sxs-lookup"><span data-stu-id="8ec2b-263">no</span></span>               |
| <span data-ttu-id="8ec2b-264">msdyn_pluginprocessingdata</span><span class="sxs-lookup"><span data-stu-id="8ec2b-264">msdyn_pluginprocessingdata</span></span>             | <span data-ttu-id="8ec2b-265">ไม่ใช่</span><span class="sxs-lookup"><span data-stu-id="8ec2b-265">no</span></span>             | <span data-ttu-id="8ec2b-266">ไม่ใช่</span><span class="sxs-lookup"><span data-stu-id="8ec2b-266">no</span></span>               |
| <span data-ttu-id="8ec2b-267">msdyn_progress</span><span class="sxs-lookup"><span data-stu-id="8ec2b-267">msdyn_progress</span></span>                         | <span data-ttu-id="8ec2b-268">ไม่ใช่</span><span class="sxs-lookup"><span data-stu-id="8ec2b-268">no</span></span>             | <span data-ttu-id="8ec2b-269">ไม่ (ใช่ สำหรับ P4W)</span><span class="sxs-lookup"><span data-stu-id="8ec2b-269">no (yes for P4W)</span></span> |
| <span data-ttu-id="8ec2b-270">msdyn_remainingcost</span><span class="sxs-lookup"><span data-stu-id="8ec2b-270">msdyn_remainingcost</span></span>                    | <span data-ttu-id="8ec2b-271">ไม่ใช่</span><span class="sxs-lookup"><span data-stu-id="8ec2b-271">no</span></span>             | <span data-ttu-id="8ec2b-272">ไม่ใช่</span><span class="sxs-lookup"><span data-stu-id="8ec2b-272">no</span></span>               |
| <span data-ttu-id="8ec2b-273">msdyn_remainingcost_base</span><span class="sxs-lookup"><span data-stu-id="8ec2b-273">msdyn_remainingcost_base</span></span>               | <span data-ttu-id="8ec2b-274">ไม่ใช่</span><span class="sxs-lookup"><span data-stu-id="8ec2b-274">no</span></span>             | <span data-ttu-id="8ec2b-275">ไม่ใช่</span><span class="sxs-lookup"><span data-stu-id="8ec2b-275">no</span></span>               |
| <span data-ttu-id="8ec2b-276">msdyn_remainingsales</span><span class="sxs-lookup"><span data-stu-id="8ec2b-276">msdyn_remainingsales</span></span>                   | <span data-ttu-id="8ec2b-277">ไม่ใช่</span><span class="sxs-lookup"><span data-stu-id="8ec2b-277">no</span></span>             | <span data-ttu-id="8ec2b-278">ไม่ใช่</span><span class="sxs-lookup"><span data-stu-id="8ec2b-278">no</span></span>               |
| <span data-ttu-id="8ec2b-279">msdyn_remainingsales_base</span><span class="sxs-lookup"><span data-stu-id="8ec2b-279">msdyn_remainingsales_base</span></span>              | <span data-ttu-id="8ec2b-280">ไม่ใช่</span><span class="sxs-lookup"><span data-stu-id="8ec2b-280">no</span></span>             | <span data-ttu-id="8ec2b-281">ไม่ใช่</span><span class="sxs-lookup"><span data-stu-id="8ec2b-281">no</span></span>               |
| <span data-ttu-id="8ec2b-282">msdyn_requestedhours</span><span class="sxs-lookup"><span data-stu-id="8ec2b-282">msdyn_requestedhours</span></span>                   | <span data-ttu-id="8ec2b-283">ไม่ใช่</span><span class="sxs-lookup"><span data-stu-id="8ec2b-283">no</span></span>             | <span data-ttu-id="8ec2b-284">ไม่ใช่</span><span class="sxs-lookup"><span data-stu-id="8ec2b-284">no</span></span>               |
| <span data-ttu-id="8ec2b-285">msdyn_resourcecategory</span><span class="sxs-lookup"><span data-stu-id="8ec2b-285">msdyn_resourcecategory</span></span>                 | <span data-ttu-id="8ec2b-286">ไม่ใช่</span><span class="sxs-lookup"><span data-stu-id="8ec2b-286">no</span></span>             | <span data-ttu-id="8ec2b-287">ไม่ใช่</span><span class="sxs-lookup"><span data-stu-id="8ec2b-287">no</span></span>               |
| <span data-ttu-id="8ec2b-288">msdyn_resourcecategoryname</span><span class="sxs-lookup"><span data-stu-id="8ec2b-288">msdyn_resourcecategoryname</span></span>             | <span data-ttu-id="8ec2b-289">ไม่ใช่</span><span class="sxs-lookup"><span data-stu-id="8ec2b-289">no</span></span>             | <span data-ttu-id="8ec2b-290">ไม่ใช่</span><span class="sxs-lookup"><span data-stu-id="8ec2b-290">no</span></span>               |
| <span data-ttu-id="8ec2b-291">msdyn_resourceorganizationalunitid</span><span class="sxs-lookup"><span data-stu-id="8ec2b-291">msdyn_resourceorganizationalunitid</span></span>     | <span data-ttu-id="8ec2b-292">ไม่ใช่</span><span class="sxs-lookup"><span data-stu-id="8ec2b-292">no</span></span>             | <span data-ttu-id="8ec2b-293">ไม่ใช่</span><span class="sxs-lookup"><span data-stu-id="8ec2b-293">no</span></span>               |
| <span data-ttu-id="8ec2b-294">msdyn_resourceorganizationalunitidname</span><span class="sxs-lookup"><span data-stu-id="8ec2b-294">msdyn_resourceorganizationalunitidname</span></span> | <span data-ttu-id="8ec2b-295">ไม่ใช่</span><span class="sxs-lookup"><span data-stu-id="8ec2b-295">no</span></span>             | <span data-ttu-id="8ec2b-296">ไม่ใช่</span><span class="sxs-lookup"><span data-stu-id="8ec2b-296">no</span></span>               |
| <span data-ttu-id="8ec2b-297">msdyn_salesconsumptionpercentage</span><span class="sxs-lookup"><span data-stu-id="8ec2b-297">msdyn_salesconsumptionpercentage</span></span>       | <span data-ttu-id="8ec2b-298">ไม่ใช่</span><span class="sxs-lookup"><span data-stu-id="8ec2b-298">no</span></span>             | <span data-ttu-id="8ec2b-299">ไม่ใช่</span><span class="sxs-lookup"><span data-stu-id="8ec2b-299">no</span></span>               |
| <span data-ttu-id="8ec2b-300">msdyn_salesestimateatcomplete</span><span class="sxs-lookup"><span data-stu-id="8ec2b-300">msdyn_salesestimateatcomplete</span></span>          | <span data-ttu-id="8ec2b-301">ไม่ใช่</span><span class="sxs-lookup"><span data-stu-id="8ec2b-301">no</span></span>             | <span data-ttu-id="8ec2b-302">ไม่ใช่</span><span class="sxs-lookup"><span data-stu-id="8ec2b-302">no</span></span>               |
| <span data-ttu-id="8ec2b-303">msdyn_salesestimateatcomplete_base</span><span class="sxs-lookup"><span data-stu-id="8ec2b-303">msdyn_salesestimateatcomplete_base</span></span>     | <span data-ttu-id="8ec2b-304">ไม่ใช่</span><span class="sxs-lookup"><span data-stu-id="8ec2b-304">no</span></span>             | <span data-ttu-id="8ec2b-305">ไม่ใช่</span><span class="sxs-lookup"><span data-stu-id="8ec2b-305">no</span></span>               |
| <span data-ttu-id="8ec2b-306">msdyn_salesvariance</span><span class="sxs-lookup"><span data-stu-id="8ec2b-306">msdyn_salesvariance</span></span>                    | <span data-ttu-id="8ec2b-307">ไม่ใช่</span><span class="sxs-lookup"><span data-stu-id="8ec2b-307">no</span></span>             | <span data-ttu-id="8ec2b-308">ไม่ใช่</span><span class="sxs-lookup"><span data-stu-id="8ec2b-308">no</span></span>               |
| <span data-ttu-id="8ec2b-309">msdyn_salesvariance_base</span><span class="sxs-lookup"><span data-stu-id="8ec2b-309">msdyn_salesvariance_base</span></span>               | <span data-ttu-id="8ec2b-310">ไม่ใช่</span><span class="sxs-lookup"><span data-stu-id="8ec2b-310">no</span></span>             | <span data-ttu-id="8ec2b-311">ไม่ใช่</span><span class="sxs-lookup"><span data-stu-id="8ec2b-311">no</span></span>               |
| <span data-ttu-id="8ec2b-312">msdyn_scheduleddurationminutes</span><span class="sxs-lookup"><span data-stu-id="8ec2b-312">msdyn_scheduleddurationminutes</span></span>         | <span data-ttu-id="8ec2b-313">ไม่ใช่</span><span class="sxs-lookup"><span data-stu-id="8ec2b-313">no</span></span>             | <span data-ttu-id="8ec2b-314">ไม่ใช่</span><span class="sxs-lookup"><span data-stu-id="8ec2b-314">no</span></span>               |
| <span data-ttu-id="8ec2b-315">msdyn_scheduledend</span><span class="sxs-lookup"><span data-stu-id="8ec2b-315">msdyn_scheduledend</span></span>                     | <span data-ttu-id="8ec2b-316">ไม่ใช่</span><span class="sxs-lookup"><span data-stu-id="8ec2b-316">no</span></span>             | <span data-ttu-id="8ec2b-317">ไม่ใช่</span><span class="sxs-lookup"><span data-stu-id="8ec2b-317">no</span></span>               |
| <span data-ttu-id="8ec2b-318">msdyn_scheduledstart</span><span class="sxs-lookup"><span data-stu-id="8ec2b-318">msdyn_scheduledstart</span></span>                   | <span data-ttu-id="8ec2b-319">ไม่ใช่</span><span class="sxs-lookup"><span data-stu-id="8ec2b-319">no</span></span>             | <span data-ttu-id="8ec2b-320">ไม่ใช่</span><span class="sxs-lookup"><span data-stu-id="8ec2b-320">no</span></span>               |
| <span data-ttu-id="8ec2b-321">msdyn_schedulevariance</span><span class="sxs-lookup"><span data-stu-id="8ec2b-321">msdyn_schedulevariance</span></span>                 | <span data-ttu-id="8ec2b-322">ไม่ใช่</span><span class="sxs-lookup"><span data-stu-id="8ec2b-322">no</span></span>             | <span data-ttu-id="8ec2b-323">ไม่ใช่</span><span class="sxs-lookup"><span data-stu-id="8ec2b-323">no</span></span>               |
| <span data-ttu-id="8ec2b-324">msdyn_skipupdateestimateline</span><span class="sxs-lookup"><span data-stu-id="8ec2b-324">msdyn_skipupdateestimateline</span></span>           | <span data-ttu-id="8ec2b-325">ไม่ใช่</span><span class="sxs-lookup"><span data-stu-id="8ec2b-325">no</span></span>             | <span data-ttu-id="8ec2b-326">ไม่ใช่</span><span class="sxs-lookup"><span data-stu-id="8ec2b-326">no</span></span>               |
| <span data-ttu-id="8ec2b-327">msdyn_skipupdateestimatelinename</span><span class="sxs-lookup"><span data-stu-id="8ec2b-327">msdyn_skipupdateestimatelinename</span></span>       | <span data-ttu-id="8ec2b-328">ไม่ใช่</span><span class="sxs-lookup"><span data-stu-id="8ec2b-328">no</span></span>             | <span data-ttu-id="8ec2b-329">ไม่ใช่</span><span class="sxs-lookup"><span data-stu-id="8ec2b-329">no</span></span>               |
| <span data-ttu-id="8ec2b-330">msdyn_summary</span><span class="sxs-lookup"><span data-stu-id="8ec2b-330">msdyn_summary</span></span>                          | <span data-ttu-id="8ec2b-331">ไม่ใช่</span><span class="sxs-lookup"><span data-stu-id="8ec2b-331">no</span></span>             | <span data-ttu-id="8ec2b-332">ไม่ใช่</span><span class="sxs-lookup"><span data-stu-id="8ec2b-332">no</span></span>               |
| <span data-ttu-id="8ec2b-333">msdyn_varianceofcost</span><span class="sxs-lookup"><span data-stu-id="8ec2b-333">msdyn_varianceofcost</span></span>                   | <span data-ttu-id="8ec2b-334">ไม่ใช่</span><span class="sxs-lookup"><span data-stu-id="8ec2b-334">no</span></span>             | <span data-ttu-id="8ec2b-335">ไม่ใช่</span><span class="sxs-lookup"><span data-stu-id="8ec2b-335">no</span></span>               |
| <span data-ttu-id="8ec2b-336">msdyn_varianceofcost_base</span><span class="sxs-lookup"><span data-stu-id="8ec2b-336">msdyn_varianceofcost_base</span></span>              | <span data-ttu-id="8ec2b-337">ไม่ใช่</span><span class="sxs-lookup"><span data-stu-id="8ec2b-337">no</span></span>             | <span data-ttu-id="8ec2b-338">ไม่ใช่</span><span class="sxs-lookup"><span data-stu-id="8ec2b-338">no</span></span>               |

### <a name="project-task-dependency"></a><span data-ttu-id="8ec2b-339">การขึ้นต่อกันของงานโครงการ</span><span class="sxs-lookup"><span data-stu-id="8ec2b-339">Project task dependency</span></span>

| <span data-ttu-id="8ec2b-340">**ชื่อตรรกะ**</span><span class="sxs-lookup"><span data-stu-id="8ec2b-340">**Logical name**</span></span>              | <span data-ttu-id="8ec2b-341">**สามารถสร้าง**</span><span class="sxs-lookup"><span data-stu-id="8ec2b-341">**Can create**</span></span> | <span data-ttu-id="8ec2b-342">**สามารถแก้ไข**</span><span class="sxs-lookup"><span data-stu-id="8ec2b-342">**Can edit**</span></span> |
|-------------------------------|----------------|--------------|
| <span data-ttu-id="8ec2b-343">msdyn_linktype</span><span class="sxs-lookup"><span data-stu-id="8ec2b-343">msdyn_linktype</span></span>                | <span data-ttu-id="8ec2b-344">ไม่ใช่</span><span class="sxs-lookup"><span data-stu-id="8ec2b-344">no</span></span>             | <span data-ttu-id="8ec2b-345">ไม่ใช่</span><span class="sxs-lookup"><span data-stu-id="8ec2b-345">no</span></span>           |
| <span data-ttu-id="8ec2b-346">msdyn_linktypename</span><span class="sxs-lookup"><span data-stu-id="8ec2b-346">msdyn_linktypename</span></span>            | <span data-ttu-id="8ec2b-347">ไม่ใช่</span><span class="sxs-lookup"><span data-stu-id="8ec2b-347">no</span></span>             | <span data-ttu-id="8ec2b-348">ไม่ใช่</span><span class="sxs-lookup"><span data-stu-id="8ec2b-348">no</span></span>           |
| <span data-ttu-id="8ec2b-349">msdyn_predecessortask</span><span class="sxs-lookup"><span data-stu-id="8ec2b-349">msdyn_predecessortask</span></span>         | <span data-ttu-id="8ec2b-350">ใช่</span><span class="sxs-lookup"><span data-stu-id="8ec2b-350">yes</span></span>            | <span data-ttu-id="8ec2b-351">ไม่ใช่</span><span class="sxs-lookup"><span data-stu-id="8ec2b-351">no</span></span>           |
| <span data-ttu-id="8ec2b-352">msdyn_predecessortaskname</span><span class="sxs-lookup"><span data-stu-id="8ec2b-352">msdyn_predecessortaskname</span></span>     | <span data-ttu-id="8ec2b-353">ใช่</span><span class="sxs-lookup"><span data-stu-id="8ec2b-353">yes</span></span>            | <span data-ttu-id="8ec2b-354">ไม่ใช่</span><span class="sxs-lookup"><span data-stu-id="8ec2b-354">no</span></span>           |
| <span data-ttu-id="8ec2b-355">msdyn_project</span><span class="sxs-lookup"><span data-stu-id="8ec2b-355">msdyn_project</span></span>                 | <span data-ttu-id="8ec2b-356">ใช่</span><span class="sxs-lookup"><span data-stu-id="8ec2b-356">yes</span></span>            | <span data-ttu-id="8ec2b-357">ไม่ใช่</span><span class="sxs-lookup"><span data-stu-id="8ec2b-357">no</span></span>           |
| <span data-ttu-id="8ec2b-358">msdyn_projectname</span><span class="sxs-lookup"><span data-stu-id="8ec2b-358">msdyn_projectname</span></span>             | <span data-ttu-id="8ec2b-359">ใช่</span><span class="sxs-lookup"><span data-stu-id="8ec2b-359">yes</span></span>            | <span data-ttu-id="8ec2b-360">ไม่ใช่</span><span class="sxs-lookup"><span data-stu-id="8ec2b-360">no</span></span>           |
| <span data-ttu-id="8ec2b-361">msdyn_projecttaskdependencyid</span><span class="sxs-lookup"><span data-stu-id="8ec2b-361">msdyn_projecttaskdependencyid</span></span> | <span data-ttu-id="8ec2b-362">ใช่</span><span class="sxs-lookup"><span data-stu-id="8ec2b-362">yes</span></span>            | <span data-ttu-id="8ec2b-363">ไม่ใช่</span><span class="sxs-lookup"><span data-stu-id="8ec2b-363">no</span></span>           |
| <span data-ttu-id="8ec2b-364">msdyn_successortask</span><span class="sxs-lookup"><span data-stu-id="8ec2b-364">msdyn_successortask</span></span>           | <span data-ttu-id="8ec2b-365">ใช่</span><span class="sxs-lookup"><span data-stu-id="8ec2b-365">yes</span></span>            | <span data-ttu-id="8ec2b-366">ไม่ใช่</span><span class="sxs-lookup"><span data-stu-id="8ec2b-366">no</span></span>           |
| <span data-ttu-id="8ec2b-367">msdyn_successortaskname</span><span class="sxs-lookup"><span data-stu-id="8ec2b-367">msdyn_successortaskname</span></span>       | <span data-ttu-id="8ec2b-368">ใช่</span><span class="sxs-lookup"><span data-stu-id="8ec2b-368">yes</span></span>            | <span data-ttu-id="8ec2b-369">ไม่ใช่</span><span class="sxs-lookup"><span data-stu-id="8ec2b-369">no</span></span>           |

### <a name="resource-assignment"></a><span data-ttu-id="8ec2b-370">การกำหนดทรัพยากร</span><span class="sxs-lookup"><span data-stu-id="8ec2b-370">Resource assignment</span></span>

| <span data-ttu-id="8ec2b-371">**ชื่อตรรกะ**</span><span class="sxs-lookup"><span data-stu-id="8ec2b-371">**Logical name**</span></span>             | <span data-ttu-id="8ec2b-372">**สามารถสร้าง**</span><span class="sxs-lookup"><span data-stu-id="8ec2b-372">**Can create**</span></span> | <span data-ttu-id="8ec2b-373">**สามารถแก้ไข**</span><span class="sxs-lookup"><span data-stu-id="8ec2b-373">**Can edit**</span></span> |
|------------------------------|----------------|--------------|
| <span data-ttu-id="8ec2b-374">msdyn_bookableresourceid</span><span class="sxs-lookup"><span data-stu-id="8ec2b-374">msdyn_bookableresourceid</span></span>     | <span data-ttu-id="8ec2b-375">ใช่</span><span class="sxs-lookup"><span data-stu-id="8ec2b-375">yes</span></span>            | <span data-ttu-id="8ec2b-376">ไม่ใช่</span><span class="sxs-lookup"><span data-stu-id="8ec2b-376">no</span></span>           |
| <span data-ttu-id="8ec2b-377">msdyn_bookableresourceidname</span><span class="sxs-lookup"><span data-stu-id="8ec2b-377">msdyn_bookableresourceidname</span></span> | <span data-ttu-id="8ec2b-378">ใช่</span><span class="sxs-lookup"><span data-stu-id="8ec2b-378">yes</span></span>            | <span data-ttu-id="8ec2b-379">ไม่ใช่</span><span class="sxs-lookup"><span data-stu-id="8ec2b-379">no</span></span>           |
| <span data-ttu-id="8ec2b-380">msdyn_bookingstatusid</span><span class="sxs-lookup"><span data-stu-id="8ec2b-380">msdyn_bookingstatusid</span></span>        | <span data-ttu-id="8ec2b-381">ไม่ใช่</span><span class="sxs-lookup"><span data-stu-id="8ec2b-381">no</span></span>             | <span data-ttu-id="8ec2b-382">ไม่ใช่</span><span class="sxs-lookup"><span data-stu-id="8ec2b-382">no</span></span>           |
| <span data-ttu-id="8ec2b-383">msdyn_bookingstatusidname</span><span class="sxs-lookup"><span data-stu-id="8ec2b-383">msdyn_bookingstatusidname</span></span>    | <span data-ttu-id="8ec2b-384">ไม่ใช่</span><span class="sxs-lookup"><span data-stu-id="8ec2b-384">no</span></span>             | <span data-ttu-id="8ec2b-385">ไม่ใช่</span><span class="sxs-lookup"><span data-stu-id="8ec2b-385">no</span></span>           |
| <span data-ttu-id="8ec2b-386">msdyn_committype</span><span class="sxs-lookup"><span data-stu-id="8ec2b-386">msdyn_committype</span></span>             | <span data-ttu-id="8ec2b-387">ไม่ใช่</span><span class="sxs-lookup"><span data-stu-id="8ec2b-387">no</span></span>             | <span data-ttu-id="8ec2b-388">ไม่ใช่</span><span class="sxs-lookup"><span data-stu-id="8ec2b-388">no</span></span>           |
| <span data-ttu-id="8ec2b-389">msdyn_committypename</span><span class="sxs-lookup"><span data-stu-id="8ec2b-389">msdyn_committypename</span></span>         | <span data-ttu-id="8ec2b-390">ไม่ใช่</span><span class="sxs-lookup"><span data-stu-id="8ec2b-390">no</span></span>             | <span data-ttu-id="8ec2b-391">ไม่ใช่</span><span class="sxs-lookup"><span data-stu-id="8ec2b-391">no</span></span>           |
| <span data-ttu-id="8ec2b-392">msdyn_effort</span><span class="sxs-lookup"><span data-stu-id="8ec2b-392">msdyn_effort</span></span>                 | <span data-ttu-id="8ec2b-393">ไม่ใช่</span><span class="sxs-lookup"><span data-stu-id="8ec2b-393">no</span></span>             | <span data-ttu-id="8ec2b-394">ไม่ใช่</span><span class="sxs-lookup"><span data-stu-id="8ec2b-394">no</span></span>           |
| <span data-ttu-id="8ec2b-395">msdyn_effortcompleted</span><span class="sxs-lookup"><span data-stu-id="8ec2b-395">msdyn_effortcompleted</span></span>        | <span data-ttu-id="8ec2b-396">ไม่ใช่</span><span class="sxs-lookup"><span data-stu-id="8ec2b-396">no</span></span>             | <span data-ttu-id="8ec2b-397">ไม่ใช่</span><span class="sxs-lookup"><span data-stu-id="8ec2b-397">no</span></span>           |
| <span data-ttu-id="8ec2b-398">msdyn_effortremaining</span><span class="sxs-lookup"><span data-stu-id="8ec2b-398">msdyn_effortremaining</span></span>        | <span data-ttu-id="8ec2b-399">ไม่ใช่</span><span class="sxs-lookup"><span data-stu-id="8ec2b-399">no</span></span>             | <span data-ttu-id="8ec2b-400">ไม่ใช่</span><span class="sxs-lookup"><span data-stu-id="8ec2b-400">no</span></span>           |
| <span data-ttu-id="8ec2b-401">msdyn_finish</span><span class="sxs-lookup"><span data-stu-id="8ec2b-401">msdyn_finish</span></span>                 | <span data-ttu-id="8ec2b-402">ไม่ใช่</span><span class="sxs-lookup"><span data-stu-id="8ec2b-402">no</span></span>             | <span data-ttu-id="8ec2b-403">ไม่ใช่</span><span class="sxs-lookup"><span data-stu-id="8ec2b-403">no</span></span>           |
| <span data-ttu-id="8ec2b-404">msdyn_plannedcost</span><span class="sxs-lookup"><span data-stu-id="8ec2b-404">msdyn_plannedcost</span></span>            | <span data-ttu-id="8ec2b-405">ไม่ใช่</span><span class="sxs-lookup"><span data-stu-id="8ec2b-405">no</span></span>             | <span data-ttu-id="8ec2b-406">ไม่ใช่</span><span class="sxs-lookup"><span data-stu-id="8ec2b-406">no</span></span>           |
| <span data-ttu-id="8ec2b-407">msdyn_plannedcost_base</span><span class="sxs-lookup"><span data-stu-id="8ec2b-407">msdyn_plannedcost_base</span></span>       | <span data-ttu-id="8ec2b-408">ไม่ใช่</span><span class="sxs-lookup"><span data-stu-id="8ec2b-408">no</span></span>             | <span data-ttu-id="8ec2b-409">ไม่ใช่</span><span class="sxs-lookup"><span data-stu-id="8ec2b-409">no</span></span>           |
| <span data-ttu-id="8ec2b-410">msdyn_plannedcostcontour</span><span class="sxs-lookup"><span data-stu-id="8ec2b-410">msdyn_plannedcostcontour</span></span>     | <span data-ttu-id="8ec2b-411">ไม่ใช่</span><span class="sxs-lookup"><span data-stu-id="8ec2b-411">no</span></span>             | <span data-ttu-id="8ec2b-412">ไม่ใช่</span><span class="sxs-lookup"><span data-stu-id="8ec2b-412">no</span></span>           |
| <span data-ttu-id="8ec2b-413">msdyn_plannedsales</span><span class="sxs-lookup"><span data-stu-id="8ec2b-413">msdyn_plannedsales</span></span>           | <span data-ttu-id="8ec2b-414">ไม่ใช่</span><span class="sxs-lookup"><span data-stu-id="8ec2b-414">no</span></span>             | <span data-ttu-id="8ec2b-415">ไม่ใช่</span><span class="sxs-lookup"><span data-stu-id="8ec2b-415">no</span></span>           |
| <span data-ttu-id="8ec2b-416">msdyn_plannedsales_base</span><span class="sxs-lookup"><span data-stu-id="8ec2b-416">msdyn_plannedsales_base</span></span>      | <span data-ttu-id="8ec2b-417">ไม่ใช่</span><span class="sxs-lookup"><span data-stu-id="8ec2b-417">no</span></span>             | <span data-ttu-id="8ec2b-418">ไม่ใช่</span><span class="sxs-lookup"><span data-stu-id="8ec2b-418">no</span></span>           |
| <span data-ttu-id="8ec2b-419">msdyn_plannedsalescontour</span><span class="sxs-lookup"><span data-stu-id="8ec2b-419">msdyn_plannedsalescontour</span></span>    | <span data-ttu-id="8ec2b-420">ไม่ใช่</span><span class="sxs-lookup"><span data-stu-id="8ec2b-420">no</span></span>             | <span data-ttu-id="8ec2b-421">ไม่ใช่</span><span class="sxs-lookup"><span data-stu-id="8ec2b-421">no</span></span>           |
| <span data-ttu-id="8ec2b-422">msdyn_plannedwork</span><span class="sxs-lookup"><span data-stu-id="8ec2b-422">msdyn_plannedwork</span></span>            | <span data-ttu-id="8ec2b-423">ไม่ใช่</span><span class="sxs-lookup"><span data-stu-id="8ec2b-423">no</span></span>             | <span data-ttu-id="8ec2b-424">ไม่ใช่</span><span class="sxs-lookup"><span data-stu-id="8ec2b-424">no</span></span>           |
| <span data-ttu-id="8ec2b-425">msdyn_projectid</span><span class="sxs-lookup"><span data-stu-id="8ec2b-425">msdyn_projectid</span></span>              | <span data-ttu-id="8ec2b-426">ใช่</span><span class="sxs-lookup"><span data-stu-id="8ec2b-426">yes</span></span>            | <span data-ttu-id="8ec2b-427">ไม่ใช่</span><span class="sxs-lookup"><span data-stu-id="8ec2b-427">no</span></span>           |
| <span data-ttu-id="8ec2b-428">msdyn_projectidname</span><span class="sxs-lookup"><span data-stu-id="8ec2b-428">msdyn_projectidname</span></span>          | <span data-ttu-id="8ec2b-429">ไม่ใช่</span><span class="sxs-lookup"><span data-stu-id="8ec2b-429">no</span></span>             | <span data-ttu-id="8ec2b-430">ไม่ใช่</span><span class="sxs-lookup"><span data-stu-id="8ec2b-430">no</span></span>           |
| <span data-ttu-id="8ec2b-431">msdyn_projectteamid</span><span class="sxs-lookup"><span data-stu-id="8ec2b-431">msdyn_projectteamid</span></span>          | <span data-ttu-id="8ec2b-432">ไม่ใช่</span><span class="sxs-lookup"><span data-stu-id="8ec2b-432">no</span></span>             | <span data-ttu-id="8ec2b-433">ไม่ใช่</span><span class="sxs-lookup"><span data-stu-id="8ec2b-433">no</span></span>           |
| <span data-ttu-id="8ec2b-434">msdyn_projectteamidname</span><span class="sxs-lookup"><span data-stu-id="8ec2b-434">msdyn_projectteamidname</span></span>      | <span data-ttu-id="8ec2b-435">ไม่ใช่</span><span class="sxs-lookup"><span data-stu-id="8ec2b-435">no</span></span>             | <span data-ttu-id="8ec2b-436">ไม่ใช่</span><span class="sxs-lookup"><span data-stu-id="8ec2b-436">no</span></span>           |
| <span data-ttu-id="8ec2b-437">msdyn_start</span><span class="sxs-lookup"><span data-stu-id="8ec2b-437">msdyn_start</span></span>                  | <span data-ttu-id="8ec2b-438">ไม่ใช่</span><span class="sxs-lookup"><span data-stu-id="8ec2b-438">no</span></span>             | <span data-ttu-id="8ec2b-439">ไม่ใช่</span><span class="sxs-lookup"><span data-stu-id="8ec2b-439">no</span></span>           |
| <span data-ttu-id="8ec2b-440">msdyn_taskid</span><span class="sxs-lookup"><span data-stu-id="8ec2b-440">msdyn_taskid</span></span>                 | <span data-ttu-id="8ec2b-441">ไม่ใช่</span><span class="sxs-lookup"><span data-stu-id="8ec2b-441">no</span></span>             | <span data-ttu-id="8ec2b-442">ไม่ใช่</span><span class="sxs-lookup"><span data-stu-id="8ec2b-442">no</span></span>           |
| <span data-ttu-id="8ec2b-443">msdyn_taskidname</span><span class="sxs-lookup"><span data-stu-id="8ec2b-443">msdyn_taskidname</span></span>             | <span data-ttu-id="8ec2b-444">ไม่ใช่</span><span class="sxs-lookup"><span data-stu-id="8ec2b-444">no</span></span>             | <span data-ttu-id="8ec2b-445">ไม่ใช่</span><span class="sxs-lookup"><span data-stu-id="8ec2b-445">no</span></span>           |
| <span data-ttu-id="8ec2b-446">msdyn_userresourceid</span><span class="sxs-lookup"><span data-stu-id="8ec2b-446">msdyn_userresourceid</span></span>         | <span data-ttu-id="8ec2b-447">ไม่ใช่</span><span class="sxs-lookup"><span data-stu-id="8ec2b-447">no</span></span>             | <span data-ttu-id="8ec2b-448">ไม่ใช่</span><span class="sxs-lookup"><span data-stu-id="8ec2b-448">no</span></span>           |

### <a name="project-team-member"></a><span data-ttu-id="8ec2b-449">สมาชิกของทีมโครงการ</span><span class="sxs-lookup"><span data-stu-id="8ec2b-449">Project team member</span></span>

| <span data-ttu-id="8ec2b-450">**ชื่อตรรกะ**</span><span class="sxs-lookup"><span data-stu-id="8ec2b-450">**Logical name**</span></span>                                 | <span data-ttu-id="8ec2b-451">**สามารถสร้าง**</span><span class="sxs-lookup"><span data-stu-id="8ec2b-451">**Can create**</span></span> | <span data-ttu-id="8ec2b-452">**สามารถแก้ไข**</span><span class="sxs-lookup"><span data-stu-id="8ec2b-452">**Can edit**</span></span> |
|--------------------------------------------------|----------------|--------------|
| <span data-ttu-id="8ec2b-453">msdyn_calendarid</span><span class="sxs-lookup"><span data-stu-id="8ec2b-453">msdyn_calendarid</span></span>                                 | <span data-ttu-id="8ec2b-454">ไม่ใช่</span><span class="sxs-lookup"><span data-stu-id="8ec2b-454">no</span></span>             | <span data-ttu-id="8ec2b-455">ไม่ใช่</span><span class="sxs-lookup"><span data-stu-id="8ec2b-455">no</span></span>           |
| <span data-ttu-id="8ec2b-456">msdyn_creategenericteammemberwithrequirementname</span><span class="sxs-lookup"><span data-stu-id="8ec2b-456">msdyn_creategenericteammemberwithrequirementname</span></span> | <span data-ttu-id="8ec2b-457">ไม่ใช่</span><span class="sxs-lookup"><span data-stu-id="8ec2b-457">no</span></span>             | <span data-ttu-id="8ec2b-458">ไม่ใช่</span><span class="sxs-lookup"><span data-stu-id="8ec2b-458">no</span></span>           |
| <span data-ttu-id="8ec2b-459">msdyn_deletestatus</span><span class="sxs-lookup"><span data-stu-id="8ec2b-459">msdyn_deletestatus</span></span>                               | <span data-ttu-id="8ec2b-460">ไม่ใช่</span><span class="sxs-lookup"><span data-stu-id="8ec2b-460">no</span></span>             | <span data-ttu-id="8ec2b-461">ไม่ใช่</span><span class="sxs-lookup"><span data-stu-id="8ec2b-461">no</span></span>           |
| <span data-ttu-id="8ec2b-462">msdyn_deletestatusname</span><span class="sxs-lookup"><span data-stu-id="8ec2b-462">msdyn_deletestatusname</span></span>                           | <span data-ttu-id="8ec2b-463">ไม่ใช่</span><span class="sxs-lookup"><span data-stu-id="8ec2b-463">no</span></span>             | <span data-ttu-id="8ec2b-464">ไม่ใช่</span><span class="sxs-lookup"><span data-stu-id="8ec2b-464">no</span></span>           |
| <span data-ttu-id="8ec2b-465">msdyn_effort</span><span class="sxs-lookup"><span data-stu-id="8ec2b-465">msdyn_effort</span></span>                                     | <span data-ttu-id="8ec2b-466">ไม่ใช่</span><span class="sxs-lookup"><span data-stu-id="8ec2b-466">no</span></span>             | <span data-ttu-id="8ec2b-467">ไม่ใช่</span><span class="sxs-lookup"><span data-stu-id="8ec2b-467">no</span></span>           |
| <span data-ttu-id="8ec2b-468">msdyn_effortcompleted</span><span class="sxs-lookup"><span data-stu-id="8ec2b-468">msdyn_effortcompleted</span></span>                            | <span data-ttu-id="8ec2b-469">ไม่ใช่</span><span class="sxs-lookup"><span data-stu-id="8ec2b-469">no</span></span>             | <span data-ttu-id="8ec2b-470">ไม่ใช่</span><span class="sxs-lookup"><span data-stu-id="8ec2b-470">no</span></span>           |
| <span data-ttu-id="8ec2b-471">msdyn_effortremaining</span><span class="sxs-lookup"><span data-stu-id="8ec2b-471">msdyn_effortremaining</span></span>                            | <span data-ttu-id="8ec2b-472">ไม่ใช่</span><span class="sxs-lookup"><span data-stu-id="8ec2b-472">no</span></span>             | <span data-ttu-id="8ec2b-473">ไม่ใช่</span><span class="sxs-lookup"><span data-stu-id="8ec2b-473">no</span></span>           |
| <span data-ttu-id="8ec2b-474">msdyn_finish</span><span class="sxs-lookup"><span data-stu-id="8ec2b-474">msdyn_finish</span></span>                                     | <span data-ttu-id="8ec2b-475">ไม่ใช่</span><span class="sxs-lookup"><span data-stu-id="8ec2b-475">no</span></span>             | <span data-ttu-id="8ec2b-476">ไม่ใช่</span><span class="sxs-lookup"><span data-stu-id="8ec2b-476">no</span></span>           |
| <span data-ttu-id="8ec2b-477">msdyn_hardbookedhours</span><span class="sxs-lookup"><span data-stu-id="8ec2b-477">msdyn_hardbookedhours</span></span>                            | <span data-ttu-id="8ec2b-478">ไม่ใช่</span><span class="sxs-lookup"><span data-stu-id="8ec2b-478">no</span></span>             | <span data-ttu-id="8ec2b-479">ไม่ใช่</span><span class="sxs-lookup"><span data-stu-id="8ec2b-479">no</span></span>           |
| <span data-ttu-id="8ec2b-480">msdyn_hours</span><span class="sxs-lookup"><span data-stu-id="8ec2b-480">msdyn_hours</span></span>                                      | <span data-ttu-id="8ec2b-481">ไม่ใช่</span><span class="sxs-lookup"><span data-stu-id="8ec2b-481">no</span></span>             | <span data-ttu-id="8ec2b-482">ไม่ใช่</span><span class="sxs-lookup"><span data-stu-id="8ec2b-482">no</span></span>           |
| <span data-ttu-id="8ec2b-483">msdyn_markedfordeletiontimer</span><span class="sxs-lookup"><span data-stu-id="8ec2b-483">msdyn_markedfordeletiontimer</span></span>                     | <span data-ttu-id="8ec2b-484">ไม่ใช่</span><span class="sxs-lookup"><span data-stu-id="8ec2b-484">no</span></span>             | <span data-ttu-id="8ec2b-485">ไม่ใช่</span><span class="sxs-lookup"><span data-stu-id="8ec2b-485">no</span></span>           |
| <span data-ttu-id="8ec2b-486">msdyn_markedfordeletiontimestamp</span><span class="sxs-lookup"><span data-stu-id="8ec2b-486">msdyn_markedfordeletiontimestamp</span></span>                 | <span data-ttu-id="8ec2b-487">ไม่ใช่</span><span class="sxs-lookup"><span data-stu-id="8ec2b-487">no</span></span>             | <span data-ttu-id="8ec2b-488">ไม่ใช่</span><span class="sxs-lookup"><span data-stu-id="8ec2b-488">no</span></span>           |
| <span data-ttu-id="8ec2b-489">msdyn_msprojectclientid</span><span class="sxs-lookup"><span data-stu-id="8ec2b-489">msdyn_msprojectclientid</span></span>                          | <span data-ttu-id="8ec2b-490">ไม่ใช่</span><span class="sxs-lookup"><span data-stu-id="8ec2b-490">no</span></span>             | <span data-ttu-id="8ec2b-491">ไม่ใช่</span><span class="sxs-lookup"><span data-stu-id="8ec2b-491">no</span></span>           |
| <span data-ttu-id="8ec2b-492">msdyn_percentage</span><span class="sxs-lookup"><span data-stu-id="8ec2b-492">msdyn_percentage</span></span>                                 | <span data-ttu-id="8ec2b-493">ไม่ใช่</span><span class="sxs-lookup"><span data-stu-id="8ec2b-493">no</span></span>             | <span data-ttu-id="8ec2b-494">ไม่ใช่</span><span class="sxs-lookup"><span data-stu-id="8ec2b-494">no</span></span>           |
| <span data-ttu-id="8ec2b-495">msdyn_requiredhours</span><span class="sxs-lookup"><span data-stu-id="8ec2b-495">msdyn_requiredhours</span></span>                              | <span data-ttu-id="8ec2b-496">ไม่ใช่</span><span class="sxs-lookup"><span data-stu-id="8ec2b-496">no</span></span>             | <span data-ttu-id="8ec2b-497">ไม่ใช่</span><span class="sxs-lookup"><span data-stu-id="8ec2b-497">no</span></span>           |
| <span data-ttu-id="8ec2b-498">msdyn_softbookedhours</span><span class="sxs-lookup"><span data-stu-id="8ec2b-498">msdyn_softbookedhours</span></span>                            | <span data-ttu-id="8ec2b-499">ไม่ใช่</span><span class="sxs-lookup"><span data-stu-id="8ec2b-499">no</span></span>             | <span data-ttu-id="8ec2b-500">ไม่ใช่</span><span class="sxs-lookup"><span data-stu-id="8ec2b-500">no</span></span>           |
| <span data-ttu-id="8ec2b-501">msdyn_start</span><span class="sxs-lookup"><span data-stu-id="8ec2b-501">msdyn_start</span></span>                                      | <span data-ttu-id="8ec2b-502">ไม่ใช่</span><span class="sxs-lookup"><span data-stu-id="8ec2b-502">no</span></span>             | <span data-ttu-id="8ec2b-503">ไม่ใช่</span><span class="sxs-lookup"><span data-stu-id="8ec2b-503">no</span></span>           |

### <a name="project"></a><span data-ttu-id="8ec2b-504">Project</span><span class="sxs-lookup"><span data-stu-id="8ec2b-504">Project</span></span>

| <span data-ttu-id="8ec2b-505">**ชื่อตรรกะ**</span><span class="sxs-lookup"><span data-stu-id="8ec2b-505">**Logical name**</span></span>                       | <span data-ttu-id="8ec2b-506">**สามารถสร้าง**</span><span class="sxs-lookup"><span data-stu-id="8ec2b-506">**Can create**</span></span> | <span data-ttu-id="8ec2b-507">**สามารถแก้ไข**</span><span class="sxs-lookup"><span data-stu-id="8ec2b-507">**Can edit**</span></span> |
|----------------------------------------|----------------|--------------|
| <span data-ttu-id="8ec2b-508">msdyn_actualexpensecost</span><span class="sxs-lookup"><span data-stu-id="8ec2b-508">msdyn_actualexpensecost</span></span>                | <span data-ttu-id="8ec2b-509">ไม่ใช่</span><span class="sxs-lookup"><span data-stu-id="8ec2b-509">no</span></span>             | <span data-ttu-id="8ec2b-510">ไม่ใช่</span><span class="sxs-lookup"><span data-stu-id="8ec2b-510">no</span></span>           |
| <span data-ttu-id="8ec2b-511">msdyn_actualexpensecost_base</span><span class="sxs-lookup"><span data-stu-id="8ec2b-511">msdyn_actualexpensecost_base</span></span>           | <span data-ttu-id="8ec2b-512">ไม่ใช่</span><span class="sxs-lookup"><span data-stu-id="8ec2b-512">no</span></span>             | <span data-ttu-id="8ec2b-513">ไม่ใช่</span><span class="sxs-lookup"><span data-stu-id="8ec2b-513">no</span></span>           |
| <span data-ttu-id="8ec2b-514">msdyn_actuallaborcost</span><span class="sxs-lookup"><span data-stu-id="8ec2b-514">msdyn_actuallaborcost</span></span>                  | <span data-ttu-id="8ec2b-515">ไม่ใช่</span><span class="sxs-lookup"><span data-stu-id="8ec2b-515">no</span></span>             | <span data-ttu-id="8ec2b-516">ไม่ใช่</span><span class="sxs-lookup"><span data-stu-id="8ec2b-516">no</span></span>           |
| <span data-ttu-id="8ec2b-517">msdyn_actuallaborcost_base</span><span class="sxs-lookup"><span data-stu-id="8ec2b-517">msdyn_actuallaborcost_base</span></span>             | <span data-ttu-id="8ec2b-518">ไม่ใช่</span><span class="sxs-lookup"><span data-stu-id="8ec2b-518">no</span></span>             | <span data-ttu-id="8ec2b-519">ไม่ใช่</span><span class="sxs-lookup"><span data-stu-id="8ec2b-519">no</span></span>           |
| <span data-ttu-id="8ec2b-520">msdyn_actualsales</span><span class="sxs-lookup"><span data-stu-id="8ec2b-520">msdyn_actualsales</span></span>                      | <span data-ttu-id="8ec2b-521">ไม่ใช่</span><span class="sxs-lookup"><span data-stu-id="8ec2b-521">no</span></span>             | <span data-ttu-id="8ec2b-522">ไม่ใช่</span><span class="sxs-lookup"><span data-stu-id="8ec2b-522">no</span></span>           |
| <span data-ttu-id="8ec2b-523">msdyn_actualsales_base</span><span class="sxs-lookup"><span data-stu-id="8ec2b-523">msdyn_actualsales_base</span></span>                 | <span data-ttu-id="8ec2b-524">ไม่ใช่</span><span class="sxs-lookup"><span data-stu-id="8ec2b-524">no</span></span>             | <span data-ttu-id="8ec2b-525">ไม่ใช่</span><span class="sxs-lookup"><span data-stu-id="8ec2b-525">no</span></span>           |
| <span data-ttu-id="8ec2b-526">msdyn_contractlineproject</span><span class="sxs-lookup"><span data-stu-id="8ec2b-526">msdyn_contractlineproject</span></span>              | <span data-ttu-id="8ec2b-527">ใช่</span><span class="sxs-lookup"><span data-stu-id="8ec2b-527">yes</span></span>            | <span data-ttu-id="8ec2b-528">ไม่ใช่</span><span class="sxs-lookup"><span data-stu-id="8ec2b-528">no</span></span>           |
| <span data-ttu-id="8ec2b-529">msdyn_contractorganizationalunitid</span><span class="sxs-lookup"><span data-stu-id="8ec2b-529">msdyn_contractorganizationalunitid</span></span>     | <span data-ttu-id="8ec2b-530">ใช่</span><span class="sxs-lookup"><span data-stu-id="8ec2b-530">yes</span></span>            | <span data-ttu-id="8ec2b-531">ไม่ใช่</span><span class="sxs-lookup"><span data-stu-id="8ec2b-531">no</span></span>           |
| <span data-ttu-id="8ec2b-532">msdyn_contractorganizationalunitidname</span><span class="sxs-lookup"><span data-stu-id="8ec2b-532">msdyn_contractorganizationalunitidname</span></span> | <span data-ttu-id="8ec2b-533">ใช่</span><span class="sxs-lookup"><span data-stu-id="8ec2b-533">yes</span></span>            | <span data-ttu-id="8ec2b-534">ไม่ใช่</span><span class="sxs-lookup"><span data-stu-id="8ec2b-534">no</span></span>           |
| <span data-ttu-id="8ec2b-535">msdyn_costconsumption</span><span class="sxs-lookup"><span data-stu-id="8ec2b-535">msdyn_costconsumption</span></span>                  | <span data-ttu-id="8ec2b-536">ไม่ใช่</span><span class="sxs-lookup"><span data-stu-id="8ec2b-536">no</span></span>             | <span data-ttu-id="8ec2b-537">ไม่ใช่</span><span class="sxs-lookup"><span data-stu-id="8ec2b-537">no</span></span>           |
| <span data-ttu-id="8ec2b-538">msdyn_costestimateatcomplete</span><span class="sxs-lookup"><span data-stu-id="8ec2b-538">msdyn_costestimateatcomplete</span></span>           | <span data-ttu-id="8ec2b-539">ไม่ใช่</span><span class="sxs-lookup"><span data-stu-id="8ec2b-539">no</span></span>             | <span data-ttu-id="8ec2b-540">ไม่ใช่</span><span class="sxs-lookup"><span data-stu-id="8ec2b-540">no</span></span>           |
| <span data-ttu-id="8ec2b-541">msdyn_costestimateatcomplete_base</span><span class="sxs-lookup"><span data-stu-id="8ec2b-541">msdyn_costestimateatcomplete_base</span></span>      | <span data-ttu-id="8ec2b-542">ไม่ใช่</span><span class="sxs-lookup"><span data-stu-id="8ec2b-542">no</span></span>             | <span data-ttu-id="8ec2b-543">ไม่ใช่</span><span class="sxs-lookup"><span data-stu-id="8ec2b-543">no</span></span>           |
| <span data-ttu-id="8ec2b-544">msdyn_costvariance</span><span class="sxs-lookup"><span data-stu-id="8ec2b-544">msdyn_costvariance</span></span>                     | <span data-ttu-id="8ec2b-545">ไม่ใช่</span><span class="sxs-lookup"><span data-stu-id="8ec2b-545">no</span></span>             | <span data-ttu-id="8ec2b-546">ไม่ใช่</span><span class="sxs-lookup"><span data-stu-id="8ec2b-546">no</span></span>           |
| <span data-ttu-id="8ec2b-547">msdyn_costvariance_base</span><span class="sxs-lookup"><span data-stu-id="8ec2b-547">msdyn_costvariance_base</span></span>                | <span data-ttu-id="8ec2b-548">ไม่ใช่</span><span class="sxs-lookup"><span data-stu-id="8ec2b-548">no</span></span>             | <span data-ttu-id="8ec2b-549">ไม่ใช่</span><span class="sxs-lookup"><span data-stu-id="8ec2b-549">no</span></span>           |
| <span data-ttu-id="8ec2b-550">msdyn_duration</span><span class="sxs-lookup"><span data-stu-id="8ec2b-550">msdyn_duration</span></span>                         | <span data-ttu-id="8ec2b-551">ไม่ใช่</span><span class="sxs-lookup"><span data-stu-id="8ec2b-551">no</span></span>             | <span data-ttu-id="8ec2b-552">ไม่ใช่</span><span class="sxs-lookup"><span data-stu-id="8ec2b-552">no</span></span>           |
| <span data-ttu-id="8ec2b-553">msdyn_effort</span><span class="sxs-lookup"><span data-stu-id="8ec2b-553">msdyn_effort</span></span>                           | <span data-ttu-id="8ec2b-554">ไม่ใช่</span><span class="sxs-lookup"><span data-stu-id="8ec2b-554">no</span></span>             | <span data-ttu-id="8ec2b-555">ไม่ใช่</span><span class="sxs-lookup"><span data-stu-id="8ec2b-555">no</span></span>           |
| <span data-ttu-id="8ec2b-556">msdyn_effortcompleted</span><span class="sxs-lookup"><span data-stu-id="8ec2b-556">msdyn_effortcompleted</span></span>                  | <span data-ttu-id="8ec2b-557">ไม่ใช่</span><span class="sxs-lookup"><span data-stu-id="8ec2b-557">no</span></span>             | <span data-ttu-id="8ec2b-558">ไม่ใช่</span><span class="sxs-lookup"><span data-stu-id="8ec2b-558">no</span></span>           |
| <span data-ttu-id="8ec2b-559">msdyn_effortestimateatcompleteeac</span><span class="sxs-lookup"><span data-stu-id="8ec2b-559">msdyn_effortestimateatcompleteeac</span></span>      | <span data-ttu-id="8ec2b-560">ไม่ใช่</span><span class="sxs-lookup"><span data-stu-id="8ec2b-560">no</span></span>             | <span data-ttu-id="8ec2b-561">ไม่ใช่</span><span class="sxs-lookup"><span data-stu-id="8ec2b-561">no</span></span>           |
| <span data-ttu-id="8ec2b-562">msdyn_effortremaining</span><span class="sxs-lookup"><span data-stu-id="8ec2b-562">msdyn_effortremaining</span></span>                  | <span data-ttu-id="8ec2b-563">ไม่ใช่</span><span class="sxs-lookup"><span data-stu-id="8ec2b-563">no</span></span>             | <span data-ttu-id="8ec2b-564">ไม่ใช่</span><span class="sxs-lookup"><span data-stu-id="8ec2b-564">no</span></span>           |
| <span data-ttu-id="8ec2b-565">msdyn_finish</span><span class="sxs-lookup"><span data-stu-id="8ec2b-565">msdyn_finish</span></span>                           | <span data-ttu-id="8ec2b-566">ใช่</span><span class="sxs-lookup"><span data-stu-id="8ec2b-566">yes</span></span>            | <span data-ttu-id="8ec2b-567">ใช่</span><span class="sxs-lookup"><span data-stu-id="8ec2b-567">yes</span></span>          |
| <span data-ttu-id="8ec2b-568">msdyn_globalrevisiontoken</span><span class="sxs-lookup"><span data-stu-id="8ec2b-568">msdyn_globalrevisiontoken</span></span>              | <span data-ttu-id="8ec2b-569">ไม่ใช่</span><span class="sxs-lookup"><span data-stu-id="8ec2b-569">no</span></span>             | <span data-ttu-id="8ec2b-570">ไม่ใช่</span><span class="sxs-lookup"><span data-stu-id="8ec2b-570">no</span></span>           |
| <span data-ttu-id="8ec2b-571">msdyn_islinkedtomsprojectclient</span><span class="sxs-lookup"><span data-stu-id="8ec2b-571">msdyn_islinkedtomsprojectclient</span></span>        | <span data-ttu-id="8ec2b-572">ไม่ใช่</span><span class="sxs-lookup"><span data-stu-id="8ec2b-572">no</span></span>             | <span data-ttu-id="8ec2b-573">ไม่ใช่</span><span class="sxs-lookup"><span data-stu-id="8ec2b-573">no</span></span>           |
| <span data-ttu-id="8ec2b-574">msdyn_islinkedtomsprojectclientname</span><span class="sxs-lookup"><span data-stu-id="8ec2b-574">msdyn_islinkedtomsprojectclientname</span></span>    | <span data-ttu-id="8ec2b-575">ไม่ใช่</span><span class="sxs-lookup"><span data-stu-id="8ec2b-575">no</span></span>             | <span data-ttu-id="8ec2b-576">ไม่ใช่</span><span class="sxs-lookup"><span data-stu-id="8ec2b-576">no</span></span>           |
| <span data-ttu-id="8ec2b-577">msdyn_linkeddocumenturl</span><span class="sxs-lookup"><span data-stu-id="8ec2b-577">msdyn_linkeddocumenturl</span></span>                | <span data-ttu-id="8ec2b-578">ไม่ใช่</span><span class="sxs-lookup"><span data-stu-id="8ec2b-578">no</span></span>             | <span data-ttu-id="8ec2b-579">ไม่ใช่</span><span class="sxs-lookup"><span data-stu-id="8ec2b-579">no</span></span>           |
| <span data-ttu-id="8ec2b-580">msdyn_msprojectdocument</span><span class="sxs-lookup"><span data-stu-id="8ec2b-580">msdyn_msprojectdocument</span></span>                | <span data-ttu-id="8ec2b-581">ไม่ใช่</span><span class="sxs-lookup"><span data-stu-id="8ec2b-581">no</span></span>             | <span data-ttu-id="8ec2b-582">ไม่ใช่</span><span class="sxs-lookup"><span data-stu-id="8ec2b-582">no</span></span>           |
| <span data-ttu-id="8ec2b-583">msdyn_msprojectdocumentname</span><span class="sxs-lookup"><span data-stu-id="8ec2b-583">msdyn_msprojectdocumentname</span></span>            | <span data-ttu-id="8ec2b-584">ไม่ใช่</span><span class="sxs-lookup"><span data-stu-id="8ec2b-584">no</span></span>             | <span data-ttu-id="8ec2b-585">ไม่ใช่</span><span class="sxs-lookup"><span data-stu-id="8ec2b-585">no</span></span>           |
| <span data-ttu-id="8ec2b-586">msdyn_plannedexpensecost</span><span class="sxs-lookup"><span data-stu-id="8ec2b-586">msdyn_plannedexpensecost</span></span>               | <span data-ttu-id="8ec2b-587">ไม่ใช่</span><span class="sxs-lookup"><span data-stu-id="8ec2b-587">no</span></span>             | <span data-ttu-id="8ec2b-588">ไม่ใช่</span><span class="sxs-lookup"><span data-stu-id="8ec2b-588">no</span></span>           |
| <span data-ttu-id="8ec2b-589">msdyn_plannedexpensecost_base</span><span class="sxs-lookup"><span data-stu-id="8ec2b-589">msdyn_plannedexpensecost_base</span></span>          | <span data-ttu-id="8ec2b-590">ไม่ใช่</span><span class="sxs-lookup"><span data-stu-id="8ec2b-590">no</span></span>             | <span data-ttu-id="8ec2b-591">ไม่ใช่</span><span class="sxs-lookup"><span data-stu-id="8ec2b-591">no</span></span>           |
| <span data-ttu-id="8ec2b-592">msdyn_plannedlaborcost</span><span class="sxs-lookup"><span data-stu-id="8ec2b-592">msdyn_plannedlaborcost</span></span>                 | <span data-ttu-id="8ec2b-593">ไม่ใช่</span><span class="sxs-lookup"><span data-stu-id="8ec2b-593">no</span></span>             | <span data-ttu-id="8ec2b-594">ไม่ใช่</span><span class="sxs-lookup"><span data-stu-id="8ec2b-594">no</span></span>           |
| <span data-ttu-id="8ec2b-595">msdyn_plannedlaborcost_base</span><span class="sxs-lookup"><span data-stu-id="8ec2b-595">msdyn_plannedlaborcost_base</span></span>            | <span data-ttu-id="8ec2b-596">ไม่ใช่</span><span class="sxs-lookup"><span data-stu-id="8ec2b-596">no</span></span>             | <span data-ttu-id="8ec2b-597">ไม่ใช่</span><span class="sxs-lookup"><span data-stu-id="8ec2b-597">no</span></span>           |
| <span data-ttu-id="8ec2b-598">msdyn_plannedsales</span><span class="sxs-lookup"><span data-stu-id="8ec2b-598">msdyn_plannedsales</span></span>                     | <span data-ttu-id="8ec2b-599">ไม่ใช่</span><span class="sxs-lookup"><span data-stu-id="8ec2b-599">no</span></span>             | <span data-ttu-id="8ec2b-600">ไม่ใช่</span><span class="sxs-lookup"><span data-stu-id="8ec2b-600">no</span></span>           |
| <span data-ttu-id="8ec2b-601">msdyn_plannedsales_base</span><span class="sxs-lookup"><span data-stu-id="8ec2b-601">msdyn_plannedsales_base</span></span>                | <span data-ttu-id="8ec2b-602">ไม่ใช่</span><span class="sxs-lookup"><span data-stu-id="8ec2b-602">no</span></span>             | <span data-ttu-id="8ec2b-603">ไม่ใช่</span><span class="sxs-lookup"><span data-stu-id="8ec2b-603">no</span></span>           |
| <span data-ttu-id="8ec2b-604">msdyn_progress</span><span class="sxs-lookup"><span data-stu-id="8ec2b-604">msdyn_progress</span></span>                         | <span data-ttu-id="8ec2b-605">ไม่ใช่</span><span class="sxs-lookup"><span data-stu-id="8ec2b-605">no</span></span>             | <span data-ttu-id="8ec2b-606">ไม่ใช่</span><span class="sxs-lookup"><span data-stu-id="8ec2b-606">no</span></span>           |
| <span data-ttu-id="8ec2b-607">msdyn_remainingcost</span><span class="sxs-lookup"><span data-stu-id="8ec2b-607">msdyn_remainingcost</span></span>                    | <span data-ttu-id="8ec2b-608">ไม่ใช่</span><span class="sxs-lookup"><span data-stu-id="8ec2b-608">no</span></span>             | <span data-ttu-id="8ec2b-609">ไม่ใช่</span><span class="sxs-lookup"><span data-stu-id="8ec2b-609">no</span></span>           |
| <span data-ttu-id="8ec2b-610">msdyn_remainingcost_base</span><span class="sxs-lookup"><span data-stu-id="8ec2b-610">msdyn_remainingcost_base</span></span>               | <span data-ttu-id="8ec2b-611">ไม่ใช่</span><span class="sxs-lookup"><span data-stu-id="8ec2b-611">no</span></span>             | <span data-ttu-id="8ec2b-612">ไม่ใช่</span><span class="sxs-lookup"><span data-stu-id="8ec2b-612">no</span></span>           |
| <span data-ttu-id="8ec2b-613">msdyn_remainingsales</span><span class="sxs-lookup"><span data-stu-id="8ec2b-613">msdyn_remainingsales</span></span>                   | <span data-ttu-id="8ec2b-614">ไม่ใช่</span><span class="sxs-lookup"><span data-stu-id="8ec2b-614">no</span></span>             | <span data-ttu-id="8ec2b-615">ไม่ใช่</span><span class="sxs-lookup"><span data-stu-id="8ec2b-615">no</span></span>           |
| <span data-ttu-id="8ec2b-616">msdyn_remainingsales_base</span><span class="sxs-lookup"><span data-stu-id="8ec2b-616">msdyn_remainingsales_base</span></span>              | <span data-ttu-id="8ec2b-617">ไม่ใช่</span><span class="sxs-lookup"><span data-stu-id="8ec2b-617">no</span></span>             | <span data-ttu-id="8ec2b-618">ไม่ใช่</span><span class="sxs-lookup"><span data-stu-id="8ec2b-618">no</span></span>           |
| <span data-ttu-id="8ec2b-619">msdyn_replaylogheader</span><span class="sxs-lookup"><span data-stu-id="8ec2b-619">msdyn_replaylogheader</span></span>                  | <span data-ttu-id="8ec2b-620">ไม่ใช่</span><span class="sxs-lookup"><span data-stu-id="8ec2b-620">no</span></span>             | <span data-ttu-id="8ec2b-621">ไม่ใช่</span><span class="sxs-lookup"><span data-stu-id="8ec2b-621">no</span></span>           |
| <span data-ttu-id="8ec2b-622">msdyn_salesconsumption</span><span class="sxs-lookup"><span data-stu-id="8ec2b-622">msdyn_salesconsumption</span></span>                 | <span data-ttu-id="8ec2b-623">ไม่ใช่</span><span class="sxs-lookup"><span data-stu-id="8ec2b-623">no</span></span>             | <span data-ttu-id="8ec2b-624">ไม่ใช่</span><span class="sxs-lookup"><span data-stu-id="8ec2b-624">no</span></span>           |
| <span data-ttu-id="8ec2b-625">msdyn_salesestimateatcompleteeac</span><span class="sxs-lookup"><span data-stu-id="8ec2b-625">msdyn_salesestimateatcompleteeac</span></span>       | <span data-ttu-id="8ec2b-626">ไม่ใช่</span><span class="sxs-lookup"><span data-stu-id="8ec2b-626">no</span></span>             | <span data-ttu-id="8ec2b-627">ไม่ใช่</span><span class="sxs-lookup"><span data-stu-id="8ec2b-627">no</span></span>           |
| <span data-ttu-id="8ec2b-628">msdyn_salesestimateatcompleteeac_base</span><span class="sxs-lookup"><span data-stu-id="8ec2b-628">msdyn_salesestimateatcompleteeac_base</span></span>  | <span data-ttu-id="8ec2b-629">ไม่ใช่</span><span class="sxs-lookup"><span data-stu-id="8ec2b-629">no</span></span>             | <span data-ttu-id="8ec2b-630">ไม่ใช่</span><span class="sxs-lookup"><span data-stu-id="8ec2b-630">no</span></span>           |
| <span data-ttu-id="8ec2b-631">msdyn_salesvariance</span><span class="sxs-lookup"><span data-stu-id="8ec2b-631">msdyn_salesvariance</span></span>                    | <span data-ttu-id="8ec2b-632">ไม่ใช่</span><span class="sxs-lookup"><span data-stu-id="8ec2b-632">no</span></span>             | <span data-ttu-id="8ec2b-633">ไม่ใช่</span><span class="sxs-lookup"><span data-stu-id="8ec2b-633">no</span></span>           |
| <span data-ttu-id="8ec2b-634">msdyn_salesvariance_base</span><span class="sxs-lookup"><span data-stu-id="8ec2b-634">msdyn_salesvariance_base</span></span>               | <span data-ttu-id="8ec2b-635">ไม่ใช่</span><span class="sxs-lookup"><span data-stu-id="8ec2b-635">no</span></span>             | <span data-ttu-id="8ec2b-636">ไม่ใช่</span><span class="sxs-lookup"><span data-stu-id="8ec2b-636">no</span></span>           |
| <span data-ttu-id="8ec2b-637">msdyn_scheduleperformance</span><span class="sxs-lookup"><span data-stu-id="8ec2b-637">msdyn_scheduleperformance</span></span>              | <span data-ttu-id="8ec2b-638">ไม่ใช่</span><span class="sxs-lookup"><span data-stu-id="8ec2b-638">no</span></span>             | <span data-ttu-id="8ec2b-639">ไม่ใช่</span><span class="sxs-lookup"><span data-stu-id="8ec2b-639">no</span></span>           |
| <span data-ttu-id="8ec2b-640">msdyn_scheduleperformancename</span><span class="sxs-lookup"><span data-stu-id="8ec2b-640">msdyn_scheduleperformancename</span></span>          | <span data-ttu-id="8ec2b-641">ไม่ใช่</span><span class="sxs-lookup"><span data-stu-id="8ec2b-641">no</span></span>             | <span data-ttu-id="8ec2b-642">ไม่ใช่</span><span class="sxs-lookup"><span data-stu-id="8ec2b-642">no</span></span>           |
| <span data-ttu-id="8ec2b-643">msdyn_schedulevariance</span><span class="sxs-lookup"><span data-stu-id="8ec2b-643">msdyn_schedulevariance</span></span>                 | <span data-ttu-id="8ec2b-644">ไม่ใช่</span><span class="sxs-lookup"><span data-stu-id="8ec2b-644">no</span></span>             | <span data-ttu-id="8ec2b-645">ไม่ใช่</span><span class="sxs-lookup"><span data-stu-id="8ec2b-645">no</span></span>           |
| <span data-ttu-id="8ec2b-646">msdyn_taskearlieststart</span><span class="sxs-lookup"><span data-stu-id="8ec2b-646">msdyn_taskearlieststart</span></span>                | <span data-ttu-id="8ec2b-647">ไม่ใช่</span><span class="sxs-lookup"><span data-stu-id="8ec2b-647">no</span></span>             | <span data-ttu-id="8ec2b-648">ไม่ใช่</span><span class="sxs-lookup"><span data-stu-id="8ec2b-648">no</span></span>           |
| <span data-ttu-id="8ec2b-649">msdyn_teamsize</span><span class="sxs-lookup"><span data-stu-id="8ec2b-649">msdyn_teamsize</span></span>                         | <span data-ttu-id="8ec2b-650">ไม่ใช่</span><span class="sxs-lookup"><span data-stu-id="8ec2b-650">no</span></span>             | <span data-ttu-id="8ec2b-651">ไม่ใช่</span><span class="sxs-lookup"><span data-stu-id="8ec2b-651">no</span></span>           |
| <span data-ttu-id="8ec2b-652">msdyn_teamsize_date</span><span class="sxs-lookup"><span data-stu-id="8ec2b-652">msdyn_teamsize_date</span></span>                    | <span data-ttu-id="8ec2b-653">ไม่ใช่</span><span class="sxs-lookup"><span data-stu-id="8ec2b-653">no</span></span>             | <span data-ttu-id="8ec2b-654">ไม่ใช่</span><span class="sxs-lookup"><span data-stu-id="8ec2b-654">no</span></span>           |
| <span data-ttu-id="8ec2b-655">msdyn_teamsize_state</span><span class="sxs-lookup"><span data-stu-id="8ec2b-655">msdyn_teamsize_state</span></span>                   | <span data-ttu-id="8ec2b-656">ไม่ใช่</span><span class="sxs-lookup"><span data-stu-id="8ec2b-656">no</span></span>             | <span data-ttu-id="8ec2b-657">ไม่ใช่</span><span class="sxs-lookup"><span data-stu-id="8ec2b-657">no</span></span>           |
| <span data-ttu-id="8ec2b-658">msdyn_totalactualcost</span><span class="sxs-lookup"><span data-stu-id="8ec2b-658">msdyn_totalactualcost</span></span>                  | <span data-ttu-id="8ec2b-659">ไม่ใช่</span><span class="sxs-lookup"><span data-stu-id="8ec2b-659">no</span></span>             | <span data-ttu-id="8ec2b-660">ไม่ใช่</span><span class="sxs-lookup"><span data-stu-id="8ec2b-660">no</span></span>           |
| <span data-ttu-id="8ec2b-661">msdyn_totalactualcost_base</span><span class="sxs-lookup"><span data-stu-id="8ec2b-661">msdyn_totalactualcost_base</span></span>             | <span data-ttu-id="8ec2b-662">ไม่ใช่</span><span class="sxs-lookup"><span data-stu-id="8ec2b-662">no</span></span>             | <span data-ttu-id="8ec2b-663">ไม่ใช่</span><span class="sxs-lookup"><span data-stu-id="8ec2b-663">no</span></span>           |
| <span data-ttu-id="8ec2b-664">msdyn_totalplannedcost</span><span class="sxs-lookup"><span data-stu-id="8ec2b-664">msdyn_totalplannedcost</span></span>                 | <span data-ttu-id="8ec2b-665">ไม่ใช่</span><span class="sxs-lookup"><span data-stu-id="8ec2b-665">no</span></span>             | <span data-ttu-id="8ec2b-666">ไม่ใช่</span><span class="sxs-lookup"><span data-stu-id="8ec2b-666">no</span></span>           |
| <span data-ttu-id="8ec2b-667">msdyn_totalplannedcost_base</span><span class="sxs-lookup"><span data-stu-id="8ec2b-667">msdyn_totalplannedcost_base</span></span>            | <span data-ttu-id="8ec2b-668">ไม่ใช่</span><span class="sxs-lookup"><span data-stu-id="8ec2b-668">no</span></span>             | <span data-ttu-id="8ec2b-669">ไม่ใช่</span><span class="sxs-lookup"><span data-stu-id="8ec2b-669">no</span></span>           |


## <a name="limitations-and-known-issues"></a><span data-ttu-id="8ec2b-670">ข้อจำกัดและปัญหาที่ทราบ</span><span class="sxs-lookup"><span data-stu-id="8ec2b-670">Limitations and known issues</span></span>
<span data-ttu-id="8ec2b-671">ต่อไปนี้เป็นรายการข้อจำกัดและปัญหาที่ทราบ:</span><span class="sxs-lookup"><span data-stu-id="8ec2b-671">The following is a list of limitations and known issues:</span></span>

- <span data-ttu-id="8ec2b-672">API กำหนดการโครงการสามารถใช้ได้โดย **ผู้ใช้ที่มีใบอนุญาต Microsoft Project** เท่านั้น</span><span class="sxs-lookup"><span data-stu-id="8ec2b-672">Project Schedule APIs can only be used by **Users with Microsoft Project License.**</span></span> <span data-ttu-id="8ec2b-673">แต่ไม่สามารถใช้โดย:</span><span class="sxs-lookup"><span data-stu-id="8ec2b-673">They can't be used by:</span></span>
    - <span data-ttu-id="8ec2b-674">ผู้ใช้แอปพลิเคชัน</span><span class="sxs-lookup"><span data-stu-id="8ec2b-674">Application users</span></span>
    - <span data-ttu-id="8ec2b-675">ผู้ใช้ของระบบ</span><span class="sxs-lookup"><span data-stu-id="8ec2b-675">System users</span></span>
    - <span data-ttu-id="8ec2b-676">ผู้ใช้การบูรณาการ</span><span class="sxs-lookup"><span data-stu-id="8ec2b-676">Integration users</span></span>
    - <span data-ttu-id="8ec2b-677">ผู้ใช้รายอื่นที่ไม่มีสิทธิ์การใช้งานที่จำเป็น</span><span class="sxs-lookup"><span data-stu-id="8ec2b-677">Other users that don't have the required license</span></span>
- <span data-ttu-id="8ec2b-678">**OperationSet** แต่ละรายการสามารถดำเนินงานได้สูงสุด 100 รายการ</span><span class="sxs-lookup"><span data-stu-id="8ec2b-678">Each **OperationSet** can only have a maximum of 100 operations.</span></span>
- <span data-ttu-id="8ec2b-679">ผู้ใช้แต่ละรายสามารถมี **OperationSet** ที่เปิดอยู่ได้สูงสุด 10 รายการ</span><span class="sxs-lookup"><span data-stu-id="8ec2b-679">Each user can only have a maximum of 10 open **OperationSets**.</span></span>
- <span data-ttu-id="8ec2b-680">ปัจจุบัน Project Operations รองรับงานทั้งหมดสูงสุด 500 งานในโครงการ</span><span class="sxs-lookup"><span data-stu-id="8ec2b-680">Project Operations currently supports a maximum of 500 total tasks on a project.</span></span>
- <span data-ttu-id="8ec2b-681">ขณะนี้สถานะความล้มเหลวและบันทึกความล้มเหลวของ **OperationSet** ยังไม่พร้อมใช้งาน</span><span class="sxs-lookup"><span data-stu-id="8ec2b-681">**OperationSet** failure status and failure logs aren't currently available.</span></span>
- [<span data-ttu-id="8ec2b-682">ข้อจำกัดและขอบเขตในโครงการและงาน</span><span class="sxs-lookup"><span data-stu-id="8ec2b-682">Limits and boundaries on projects and tasks</span></span>](/project-for-the-web/project-for-the-web-limits-and-boundaries)

## <a name="error-handling"></a><span data-ttu-id="8ec2b-683">การจัดการข้อผิดพลาด</span><span class="sxs-lookup"><span data-stu-id="8ec2b-683">Error handling</span></span>

   - <span data-ttu-id="8ec2b-684">หากต้องการตรวจสอบข้อผิดพลาดที่เกิดจาก Operation Sets ไปที่ **การตั้งค่า** \> **การรวมกำหนดการ** \> **Operation Sets**</span><span class="sxs-lookup"><span data-stu-id="8ec2b-684">To review errors generated from the Operation Sets, go to **Settings** \> **Schedule Integration** \> **Operations Sets**.</span></span>
   - <span data-ttu-id="8ec2b-685">หากต้องการตรวจสอบข้อผิดพลาดที่เกิดจากบริการกำหนดการโครางการ ให้ไปที่ **การตั้งค่า** \> **การรวมกำหนดการ** \> **บันทึกข้อผิดพลาด PSS**</span><span class="sxs-lookup"><span data-stu-id="8ec2b-685">To review errors generated from the Project schedule Service, go to **Settings** \> **Schedule Integration** \> **PSS Error Logs**.</span></span>

## <a name="sample-scenario"></a><span data-ttu-id="8ec2b-686">สถานการณ์ตัวอย่าง</span><span class="sxs-lookup"><span data-stu-id="8ec2b-686">Sample scenario</span></span>

<span data-ttu-id="8ec2b-687">ในสถานการณ์นี้ คุณจะสร้างโครงการ สมาชิกทีม งานสี่งาน และการกำหนดทรัพยากรสองรายการ</span><span class="sxs-lookup"><span data-stu-id="8ec2b-687">In this scenario, you will create a project, a team member, four tasks, and two resource assignments.</span></span> <span data-ttu-id="8ec2b-688">จากนั้น คุณจะปรับปรุงหนึ่งงาน ปรับปรุงโครงการ ลบหนึ่งงาน ลบการกำหนดทรัพยากรหนึ่งรายการ และสร้างการขึ้นต่อกันของงาน</span><span class="sxs-lookup"><span data-stu-id="8ec2b-688">Next, you will update one task, update the project, delete one task, delete one resource assignment, and create a task dependency.</span></span>

```csharp
Entity project = CreateProject();
project.Id = CallCreateProjectAction(project);
var projectReference = project.ToEntityReference();

var teamMember = new Entity("msdyn_projectteam", Guid.NewGuid());
teamMember["msdyn_name"] = $"TM {DateTime.Now.ToShortTimeString()}";
teamMember["msdyn_project"] = projectReference;
var createTeamMemberResponse = CallCreateTeamMemberAction(teamMember);

var description = $"My demo {DateTime.Now.ToShortTimeString()}";
var operationSetId = CallCreateOperationSetAction(project.Id, description);

var task1 = GetTask("1WW", projectReference);
var task2 = GetTask("2XX", projectReference, task1.ToEntityReference());
var task3 = GetTask("3YY", projectReference);
var task4 = GetTask("4ZZ", projectReference);

var assignment1 = GetResourceAssignment("R1", teamMember, task2, project);
var assignment2 = GetResourceAssignment("R2", teamMember, task3, project);

var task1Response = CallPssCreateAction(task1, operationSetId);
var task2Response = CallPssCreateAction(task2, operationSetId);
var task3Response = CallPssCreateAction(task3, operationSetId);
var task4Response = CallPssCreateAction(task4, operationSetId);

var assignment1Response = CallPssCreateAction(assignment1, operationSetId);
var assignment2Response = CallPssCreateAction(assignment2, operationSetId);

task2["msdyn_subject"] = "Updated Task";
var task2UpdateResponse = CallPssUpdateAction(task2, operationSetId);

project["msdyn_subject"] = $"Proj update {DateTime.Now.ToShortTimeString()}";
var projectUpdateResponse = CallPssUpdateAction(project, operationSetId);

var task4DeleteResponse = CallPssDeleteAction(task4.Id.ToString(), task4.LogicalName, operationSetId);

var assignment2DeleteResponse = CallPssDeleteAction(assignment2.Id.ToString(), assignment2.LogicalName, operationSetId);

var dependency1 = GetTaskDependency(project, task2, task3);
var dependency1Response = CallPssCreateAction(dependency1, operationSetId);

CallExecuteOperationSetAction(operationSetId);
Console.WriteLine("Done....");
```

## <a name="additional-samples"></a><span data-ttu-id="8ec2b-689">ตัวอย่างเพิ่มเติม</span><span class="sxs-lookup"><span data-stu-id="8ec2b-689">Additional samples</span></span>

```csharp
#region Call actions --- Sample code ----

/// <summary>
/// Calls the action to create an operationSet
/// </summary>
/// <param name="projectId">project id for the operations to be included in this operationSet</param>
/// <param name="description">description of this operationSet</param>
/// <returns>operationSet id</returns>
private string CallCreateOperationSetAction(Guid projectId, string description)
{
    OrganizationRequest operationSetRequest = new OrganizationRequest("msdyn_CreateOperationSetV1");
    operationSetRequest["ProjectId"] = projectId.ToString();
    operationSetRequest["Description"] = description;
    OrganizationResponse response = organizationService.Execute(operationSetRequest);
    return response["OperationSetId"].ToString();
}

/// <summary>
/// Calls the action to create an entity, only Task and Resource Assignment for now
/// </summary>
/// <param name="entity">Task or Resource Assignment</param>
/// <param name="operationSetId">operationSet id</param>
/// <returns>OperationSetResponse</returns>

private OperationSetResponse CallPssCreateAction(Entity entity, string operationSetId)
{
    OrganizationRequest operationSetRequest = new OrganizationRequest("msdyn_PssCreateV1");
    operationSetRequest["Entity"] = entity;
    operationSetRequest["OperationSetId"] = operationSetId;
    return GetOperationSetResponseFromOrgResponse(organizationService.Execute(operationSetRequest));
}

/// <summary>
/// Calls the action to update an entity, only Task for now
/// </summary>
/// <param name="entity">Task or Resource Assignment</param>
/// <param name="operationSetId">operationSet Id</param>
/// <returns>OperationSetResponse</returns>
private OperationSetResponse CallPssUpdateAction(Entity entity, string operationSetId)
{
    OrganizationRequest operationSetRequest = new OrganizationRequest("msdyn_PssUpdateV1");
    operationSetRequest["Entity"] = entity;
    operationSetRequest["OperationSetId"] = operationSetId;
    return GetOperationSetResponseFromOrgResponse(organizationService.Execute(operationSetRequest));
}

/// <summary>
/// Calls the action to update an entity, only Task and Resource Assignment for now
/// </summary>
/// <param name="recordId">Id of the record to be deleted</param>
/// <param name="entityLogicalName">Entity logical name of the record</param>
/// <param name="operationSetId">OperationSet Id</param>
/// <returns>OperationSetResponse</returns>
private OperationSetResponse CallPssDeleteAction(string recordId, string entityLogicalName, string operationSetId)
{
    OrganizationRequest operationSetRequest = new OrganizationRequest("msdyn_PssDeleteV1");
    operationSetRequest["RecordId"] = recordId;
    operationSetRequest["EntityLogicalName"] = entityLogicalName;
    operationSetRequest["OperationSetId"] = operationSetId;
    return GetOperationSetResponseFromOrgResponse(organizationService.Execute(operationSetRequest));
}

/// <summary>
/// Calls the action to execute requests in an operationSet
/// </summary>
/// <param name="operationSetId">operationSet id</param>
/// <returns>OperationSetResponse</returns>
private OperationSetResponse CallExecuteOperationSetAction(string operationSetId)
{
    OrganizationRequest operationSetRequest = new OrganizationRequest("msdyn_ExecuteOperationSetV1");
    operationSetRequest["OperationSetId"] = operationSetId;
    return GetOperationSetResponseFromOrgResponse(organizationService.Execute(operationSetRequest));
}

/// <summary>
/// This can be used to abandon an operationSet that is no longer needed
/// </summary>
/// <param name="operationSetId">operationSet id</param>
/// <returns>OperationSetResponse</returns>
protected OperationSetResponse CallAbandonOperationSetAction(Guid operationSetId)
{
    OrganizationRequest operationSetRequest = new OrganizationRequest("msdyn_AbandonOperationSetV1");
    operationSetRequest["OperationSetId"] = operationSetId.ToString();
    return GetOperationSetResponseFromOrgResponse(organizationService.Execute(operationSetRequest));
}


/// <summary>
/// Calls the action to create a new project
/// </summary>
/// <param name="project">Project</param>
/// <returns>project Id</returns>
private Guid CallCreateProjectAction(Entity project)
{
    OrganizationRequest createProjectRequest = new OrganizationRequest("msdyn_CreateProjectV1");
    createProjectRequest["Project"] = project;
    OrganizationResponse response = organizationService.Execute(createProjectRequest);
    var projectId = Guid.Parse((string)response["ProjectId"]);
    return projectId;
}

/// <summary>
/// Calls the action to create a new project team member
/// </summary>
/// <param name="teamMember">Project team member</param>
/// <returns>project team member Id</returns>
private string CallCreateTeamMemberAction(Entity teamMember)
{
    OrganizationRequest request = new OrganizationRequest("msdyn_CreateTeamMemberV1");
    request["TeamMember"] = teamMember;
    OrganizationResponse response = organizationService.Execute(request);
    return (string)response["TeamMemberId"];
}

private OperationSetResponse GetOperationSetResponseFromOrgResponse(OrganizationResponse orgResponse)
{
    return JsonConvert.DeserializeObject<OperationSetResponse>((string)orgResponse.Results["OperationSetResponse"]);
}

private EntityCollection GetDefaultBucket(EntityReference projectReference)
{
    var columnsToFetch = new ColumnSet("msdyn_project", "msdyn_name");
    var getDefaultBucket = new QueryExpression("msdyn_projectbucket")
    {
        ColumnSet = columnsToFetch,
        Criteria =
        {
            Conditions =
            {
                new ConditionExpression("msdyn_project", ConditionOperator.Equal, projectReference.Id),
                new ConditionExpression("msdyn_name", ConditionOperator.Equal, "Bucket 1")
            }
        }
    };

    return organizationService.RetrieveMultiple(getDefaultBucket);
}

private Entity GetBucket(EntityReference projectReference)
{
    var bucketCollection = GetDefaultBucket(projectReference);
    if (bucketCollection.Entities.Count > 0)
    {
        return bucketCollection[0].ToEntity<Entity>();
    }

    throw new Exception($"Please open project with id {projectReference.Id} in the Dynamics UI and navigate to the Tasks tab");
}

private Entity CreateProject()
{
    var project = new Entity("msdyn_project", Guid.NewGuid());
    project["msdyn_subject"] = $"Proj {DateTime.Now.ToShortTimeString()}";

    return project;
}



private Entity GetTask(string name, EntityReference projectReference, EntityReference parentReference = null)
{
    var task = new Entity("msdyn_projecttask", Guid.NewGuid());
    task["msdyn_project"] = projectReference;
    task["msdyn_subject"] = name;
    task["msdyn_effort"] = 4d;
    task["msdyn_scheduledstart"] = DateTime.Today;
    task["msdyn_scheduledend"] = DateTime.Today.AddDays(5);
    task["msdyn_progress"] = 0.34m;
    task["msdyn_start"] = DateTime.Now.AddDays(1);
    task["msdyn_projectbucket"] = GetBucket(projectReference).ToEntityReference();
    task["msdyn_LinkStatus"] = new OptionSetValue(192350000);

    //Custom field handling
    /*
    task["new_custom1"] = "Just my test";
    task["new_age"] = 98;
    task["new_amount"] = 591.34m;
    task["new_isready"] = new OptionSetValue(100000000);
    */

    if (parentReference == null)
    {
        task["msdyn_outlinelevel"] = 1;
    }
    else
    {
        task["msdyn_parenttask"] = parentReference;
    }

    return task;
}

private Entity GetResourceAssignment(string name, Entity teamMember, Entity task, Entity project)
{
    var assignment = new Entity("msdyn_resourceassignment", Guid.NewGuid());
    assignment["msdyn_projectteamid"] = teamMember.ToEntityReference();
    assignment["msdyn_taskid"] = task.ToEntityReference();
    assignment["msdyn_projectid"] = project.ToEntityReference();
    assignment["msdyn_name"] = name;
    assignment["msdyn_start"] = DateTime.Now;
    assignment["msdyn_finish"] = DateTime.Now;

    return assignment;
}

protected Entity GetTaskDependency(Entity project, Entity predecessor, Entity successor)
{
    var taskDependency = new Entity("msdyn_projecttaskdependency", Guid.NewGuid());
    taskDependency["msdyn_project"] = project.ToEntityReference();
    taskDependency["msdyn_predecessortask"] = predecessor.ToEntityReference();
    taskDependency["msdyn_successortask"] = successor.ToEntityReference();
    taskDependency["msdyn_linktype"] = new OptionSetValue(192350000);

    return taskDependency;
}

#endregion


#region OperationSetResponse DataContract --- Sample code ----

[DataContract]
public class OperationSetResponse
{
[DataMember(Name = "operationSetId")]
public Guid OperationSetId { get; set; }

[DataMember(Name = "operationSetDetailId")]
public Guid OperationSetDetailId { get; set; }

[DataMember(Name = "operationType")]
public string OperationType { get; set; }

[DataMember(Name = "recordId")]
public string RecordId { get; set; }

[DataMember(Name = "correlationId")]
public string CorrelationId { get; set; }
}

#endregion
```
