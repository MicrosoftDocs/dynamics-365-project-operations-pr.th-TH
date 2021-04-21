---
title: ใช้ API กำหนดการเพื่อดำเนินงานกับเอนทิตีการจัดกำหนดการ
description: หัวข้อนี้ให้ข้อมูลและตัวอย่างสำหรับการใช้ API กำหนดการ
author: sigitac
manager: Annbe
ms.date: 04/07/2021
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: a50a2c6220bb49de8146d0758019827e120e0526
ms.sourcegitcommit: 8ff9fe396db6dec581c21cd6bb9acc2691c815b0
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 04/07/2021
ms.locfileid: "5868152"
---
# <a name="use-schedule-apis-to-perform-operations-with-scheduling-entities"></a><span data-ttu-id="60d78-103">ใช้ API กำหนดการเพื่อดำเนินงานกับเอนทิตีการจัดกำหนดการ</span><span class="sxs-lookup"><span data-stu-id="60d78-103">Use Schedule APIs to perform operations with Scheduling entities</span></span>

<span data-ttu-id="60d78-104">_**นำไปใช้กับ:** Project Operations สำหรับสถานการณ์ตามทรัพยากร/วัสดุที่ไม่ได้เก็บในคลัง การปรับใช้งานแบบ Lite - จัดการกับการออกใบแจ้งหนี้ชั่วคราว_</span><span class="sxs-lookup"><span data-stu-id="60d78-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

> [!IMPORTANT] 
> <span data-ttu-id="60d78-105">ฟังก์ชันการทำงานบางส่วนหรือทั้งหมดที่ระบุไว้ในหัวข้อนี้มีให้โดยเป็นส่วนหนึ่งของรุ่นพรีวิว</span><span class="sxs-lookup"><span data-stu-id="60d78-105">Some or all of the functionality noted in this topic is available as part of a preview release.</span></span> <span data-ttu-id="60d78-106">เนื้อหาและฟังก์ชันการทำงานอาจเปลี่ยนแปลงได้</span><span class="sxs-lookup"><span data-stu-id="60d78-106">The content and the functionality are subject to change.</span></span> 

## <a name="scheduling-entities"></a><span data-ttu-id="60d78-107">เอนทิตีการจัดกำหนดการ</span><span class="sxs-lookup"><span data-stu-id="60d78-107">Scheduling entities</span></span>

<span data-ttu-id="60d78-108">API กำหนดการ ให้ความสามารถในการสร้าง ปรับปรุง และลบการดำเนินงานกับ **เอนทิตีการจัดกำหนดการ**</span><span class="sxs-lookup"><span data-stu-id="60d78-108">Schedule APIs provide the ability to perform create, update, and delete operations with **Scheduling entities**.</span></span> <span data-ttu-id="60d78-109">เอนทิตีเหล่านี้ได้รับการจัดการผ่านกลไกการจัดกำหนดการในโครงการสำหรับเว็บ</span><span class="sxs-lookup"><span data-stu-id="60d78-109">These entities are managed through the Scheduling engine in Project for the web.</span></span> <span data-ttu-id="60d78-110">สร้าง ปรับปรุง และลบการดำเนินงานกับ **เอนทิตีการจัดกำหนดการ** มีการจำกัดใน Dynamics 365 Project Operations รุ่นก่อนหน้า</span><span class="sxs-lookup"><span data-stu-id="60d78-110">Create, update, and delete operations with **Scheduling entities** were restricted in earlier Dynamics 365 Project Operations releases.</span></span>

<span data-ttu-id="60d78-111">ตารางต่อไปนี้แสดงรายการของ **เอนทิตีการจัดกำหนดการ**</span><span class="sxs-lookup"><span data-stu-id="60d78-111">The following table provides a full list of the **Scheduling entities**.</span></span>

| <span data-ttu-id="60d78-112">ชื่อเอนทิตี</span><span class="sxs-lookup"><span data-stu-id="60d78-112">Entity name</span></span>  | <span data-ttu-id="60d78-113">ชื่อตรรกะของเอนทิตี</span><span class="sxs-lookup"><span data-stu-id="60d78-113">Entity logical name</span></span> |
| --- | --- |
| <span data-ttu-id="60d78-114">Project</span><span class="sxs-lookup"><span data-stu-id="60d78-114">Project</span></span> | <span data-ttu-id="60d78-115">msdyn_project</span><span class="sxs-lookup"><span data-stu-id="60d78-115">msdyn_project</span></span> |
| <span data-ttu-id="60d78-116">งานโครงการ</span><span class="sxs-lookup"><span data-stu-id="60d78-116">Project Task</span></span>  | <span data-ttu-id="60d78-117">msdyn_projecttask</span><span class="sxs-lookup"><span data-stu-id="60d78-117">msdyn_projecttask</span></span>  |
| <span data-ttu-id="60d78-118">การขึ้นต่อกันของงานโครงการ</span><span class="sxs-lookup"><span data-stu-id="60d78-118">Project Task Dependency</span></span>  | <span data-ttu-id="60d78-119">msdyn_projecttaskdependency</span><span class="sxs-lookup"><span data-stu-id="60d78-119">msdyn_projecttaskdependency</span></span>  |
| <span data-ttu-id="60d78-120">การมอบหมายทรัพยากร</span><span class="sxs-lookup"><span data-stu-id="60d78-120">Resource Assignment</span></span> | <span data-ttu-id="60d78-121">msdyn_resourceassignment</span><span class="sxs-lookup"><span data-stu-id="60d78-121">msdyn_resourceassignment</span></span> |
| <span data-ttu-id="60d78-122">บักเก็ตโครงการ</span><span class="sxs-lookup"><span data-stu-id="60d78-122">Project Bucket</span></span>  | <span data-ttu-id="60d78-123">msdyn_projectbucket</span><span class="sxs-lookup"><span data-stu-id="60d78-123">msdyn_projectbucket</span></span> |
| <span data-ttu-id="60d78-124">สมาชิกของทีมโครงการ</span><span class="sxs-lookup"><span data-stu-id="60d78-124">Project Team Member</span></span> | <span data-ttu-id="60d78-125">msdyn_projectteam</span><span class="sxs-lookup"><span data-stu-id="60d78-125">msdyn_projectteam</span></span> |

## <a name="operationset"></a><span data-ttu-id="60d78-126">OperationSet</span><span class="sxs-lookup"><span data-stu-id="60d78-126">OperationSet</span></span>

<span data-ttu-id="60d78-127">OperationSet เป็นรูปแบบหน่วยการทำงานที่สามารถใช้เมื่อต้องดำเนินการตามกำหนดการหลายรายการที่ส่งผลกระทบต่อคำขอภายในธุรกรรม</span><span class="sxs-lookup"><span data-stu-id="60d78-127">OperationSet is a unit-of-work pattern that can be used when several schedule impacting requests must be processed within a transaction.</span></span>

## <a name="schedule-apis"></a><span data-ttu-id="60d78-128">API กำหนดการ</span><span class="sxs-lookup"><span data-stu-id="60d78-128">Schedule APIs</span></span>

<span data-ttu-id="60d78-129">ต่อไปนี้เป็นรายการของ API กำหนดการปัจจุบัน</span><span class="sxs-lookup"><span data-stu-id="60d78-129">The following is a list of current Schedule APIs.</span></span>

- <span data-ttu-id="60d78-130">**msdyn_CreateProjectV1**: API นี้สามารถใช้ในการสร้างโครงการ</span><span class="sxs-lookup"><span data-stu-id="60d78-130">**msdyn_CreateProjectV1**: This API can be used to create a project.</span></span> <span data-ttu-id="60d78-131">โครงการและบักเก็ตโครงการเริ่มต้นจะมีการสร้างในทันที</span><span class="sxs-lookup"><span data-stu-id="60d78-131">The project and default project bucket is created immediately.</span></span>
- <span data-ttu-id="60d78-132">**msdyn_CreateTeamMemberV1**: API นี้สามารถใช้เพื่อสร้างสมาชิกทีมโครงการ</span><span class="sxs-lookup"><span data-stu-id="60d78-132">**msdyn_CreateTeamMemberV1**: This API can be used to create a project team member.</span></span> <span data-ttu-id="60d78-133">โดยจะมีการสร้างสมาชิกทีมในทันที</span><span class="sxs-lookup"><span data-stu-id="60d78-133">The team member record is created immediately.</span></span>
- <span data-ttu-id="60d78-134">**msdyn_CreateOperationSetV1**: API นี้สามารถใช้เพื่อจัดกำหนดการคำขอต่างๆ ที่ต้องดำเนินการภายในธุรกรรม</span><span class="sxs-lookup"><span data-stu-id="60d78-134">**msdyn_CreateOperationSetV1**: This API can be used to schedule several requests that must be performed within a transaction.</span></span>
- <span data-ttu-id="60d78-135">**msdyn_PSSCreateV1**: API นี้สามารถใช้เพื่อสร้างเอนทิตี</span><span class="sxs-lookup"><span data-stu-id="60d78-135">**msdyn_PSSCreateV1**: This API can be used to create an entity.</span></span> <span data-ttu-id="60d78-136">เอนทิตีสามารถเป็นเอนทิตีการจัดกำหนดการใดๆ ที่สนับสนุนการดำเนินการสร้าง</span><span class="sxs-lookup"><span data-stu-id="60d78-136">The entity can be any of the Scheduling entities that support the create operation.</span></span>
- <span data-ttu-id="60d78-137">**msdyn_PSSUpdateV1**: API นี้สามารถใช้เพื่อปรับปรุงเอนทิตี</span><span class="sxs-lookup"><span data-stu-id="60d78-137">**msdyn_PSSUpdateV1**: This API can be used to update an entity.</span></span> <span data-ttu-id="60d78-138">เอนทิตีสามารถเป็นเอนทิตีการจัดกำหนดการใดๆ ที่สนับสนุนการดำเนินการปรับปรุง</span><span class="sxs-lookup"><span data-stu-id="60d78-138">The entity can be any of the Scheduling entities that support the update operation.</span></span>
- <span data-ttu-id="60d78-139">**msdyn_PSSDeleteV1**: API นี้สามารถใช้เพื่อลบเอนทิตี</span><span class="sxs-lookup"><span data-stu-id="60d78-139">**msdyn_PSSDeleteV1**: This API can be used to delete an entity.</span></span> <span data-ttu-id="60d78-140">เอนทิตีสามารถเป็นเอนทิตีการจัดกำหนดการใดๆ ที่สนับสนุนการดำเนินการลบ</span><span class="sxs-lookup"><span data-stu-id="60d78-140">The entity can be any of the Scheduling entities that support the delete operation.</span></span>
- <span data-ttu-id="60d78-141">**msdyn_ExecuteOperationSetV1**: API นี้ใช้เพื่อดำเนินงานทั้งหมดภายในชุดการดำเนินงานที่กำหนด</span><span class="sxs-lookup"><span data-stu-id="60d78-141">**msdyn_ExecuteOperationSetV1**: This API is used to execute all of the operations within the given operation set.</span></span>

## <a name="using-schedule-apis-with-operationset"></a><span data-ttu-id="60d78-142">การใช้API กำหนดการกับ OperationSet</span><span class="sxs-lookup"><span data-stu-id="60d78-142">Using Schedule APIs with OperationSet</span></span>

<span data-ttu-id="60d78-143">เนื่องจากเรกคอร์ด **CreateProjectV1** และ **CreateTeamMemberV1** ทั้งคู่มีการสร้างขึ้นในทันที API เหล่านี้จึงไม่สามารถใช้ใน **OperationSet** ได้โดยตรง</span><span class="sxs-lookup"><span data-stu-id="60d78-143">Because records with both **CreateProjectV1** and **CreateTeamMemberV1** are created immediately, these APIs can't be used in the **OperationSet** directly.</span></span> <span data-ttu-id="60d78-144">อย่างไรก็ตาม คุณสามารถใช้ API ดังกล่าวเพื่อสร้างเรกคอร์ดที่จำเป็น สร้าง **OperationSet** จากนั้นใช้เรกคอร์ดที่สร้างไว้ล่วงหน้าเหล่านี้ใน **OperationSet**</span><span class="sxs-lookup"><span data-stu-id="60d78-144">However, you can use the API to create needed records, create an **OperationSet**, and then use these pre-created records in the **OperationSet**.</span></span>

## <a name="supported-operations"></a><span data-ttu-id="60d78-145">การดำเนินการที่รองรับ</span><span class="sxs-lookup"><span data-stu-id="60d78-145">Supported operations</span></span>

| <span data-ttu-id="60d78-146">เอนทิตีการจัดกำหนดการ</span><span class="sxs-lookup"><span data-stu-id="60d78-146">Scheduling entity</span></span> | <span data-ttu-id="60d78-147">สร้าง</span><span class="sxs-lookup"><span data-stu-id="60d78-147">Create</span></span> | <span data-ttu-id="60d78-148">อัปเดต</span><span class="sxs-lookup"><span data-stu-id="60d78-148">Update</span></span> | <span data-ttu-id="60d78-149">Delete</span><span class="sxs-lookup"><span data-stu-id="60d78-149">Delete</span></span> | <span data-ttu-id="60d78-150">ข้อควรพิจารณาที่สำคัญ</span><span class="sxs-lookup"><span data-stu-id="60d78-150">Important considerations</span></span> |
| --- | --- | --- | --- | --- |
<span data-ttu-id="60d78-151">งานโครงการ</span><span class="sxs-lookup"><span data-stu-id="60d78-151">Project task</span></span> | <span data-ttu-id="60d78-152">ใช่</span><span class="sxs-lookup"><span data-stu-id="60d78-152">Yes</span></span> | <span data-ttu-id="60d78-153">ใช่</span><span class="sxs-lookup"><span data-stu-id="60d78-153">Yes</span></span> | <span data-ttu-id="60d78-154">ใช่</span><span class="sxs-lookup"><span data-stu-id="60d78-154">Yes</span></span> | <span data-ttu-id="60d78-155">ไม่มี</span><span class="sxs-lookup"><span data-stu-id="60d78-155">None</span></span> |
| <span data-ttu-id="60d78-156">การขึ้นต่อกันของงานโครงการ</span><span class="sxs-lookup"><span data-stu-id="60d78-156">Project task dependency</span></span> | <span data-ttu-id="60d78-157">ใช่</span><span class="sxs-lookup"><span data-stu-id="60d78-157">Yes</span></span> | <span data-ttu-id="60d78-158">ใช่</span><span class="sxs-lookup"><span data-stu-id="60d78-158">Yes</span></span> | | <span data-ttu-id="60d78-159">ไม่ปรับปรุงเรกคอร์ดการขึ้นต่อกันของงานโครงการ</span><span class="sxs-lookup"><span data-stu-id="60d78-159">Project task dependency records aren't updated.</span></span> <span data-ttu-id="60d78-160">แต่สามารถลบเรกคอร์ดเก่าและสร้างเรกคอร์ดใหม่ได้</span><span class="sxs-lookup"><span data-stu-id="60d78-160">Instead, an old record can be deleted and a new record can be created.</span></span> |
| <span data-ttu-id="60d78-161">การกำหนดทรัพยากร</span><span class="sxs-lookup"><span data-stu-id="60d78-161">Resource assignment</span></span> | <span data-ttu-id="60d78-162">ใช่</span><span class="sxs-lookup"><span data-stu-id="60d78-162">Yes</span></span> | <span data-ttu-id="60d78-163">ใช่</span><span class="sxs-lookup"><span data-stu-id="60d78-163">Yes</span></span> | | <span data-ttu-id="60d78-164">ไม่รองรับการดำเนินการกับฟิลด์ต่อไปนี้: **BookableResourceID**, **Effort**, **EffortCompleted**, **EffortRemaining** และ **PlannedWork**</span><span class="sxs-lookup"><span data-stu-id="60d78-164">Operations with the following fields aren't supported: **BookableResourceID**, **Effort**, **EffortCompleted**, **EffortRemaining**, and **PlannedWork**.</span></span> <span data-ttu-id="60d78-165">ไม่ปรับปรุงเรกคอร์ดการกำหนดทรัพยากร</span><span class="sxs-lookup"><span data-stu-id="60d78-165">Resource assignment records aren't updated.</span></span> <span data-ttu-id="60d78-166">แต่สามารถลบเรกคอร์ดเก่าและสร้างเรกคอร์ดใหม่ได้</span><span class="sxs-lookup"><span data-stu-id="60d78-166">Instead, the old record can be deleted and a new record can be created.</span></span> |
| <span data-ttu-id="60d78-167">บักเก็ตโครงการ</span><span class="sxs-lookup"><span data-stu-id="60d78-167">Project bucket</span></span> | <span data-ttu-id="60d78-168">ไม่พร้อมใช้งาน</span><span class="sxs-lookup"><span data-stu-id="60d78-168">N/A</span></span> | <span data-ttu-id="60d78-169">ไม่พร้อมใช้งาน</span><span class="sxs-lookup"><span data-stu-id="60d78-169">N/A</span></span> | <span data-ttu-id="60d78-170">ไม่พร้อมใช้งาน</span><span class="sxs-lookup"><span data-stu-id="60d78-170">N/A</span></span> | <span data-ttu-id="60d78-171">มีการสร้างบักเก็ตโครงการเริ่มต้นโดยใช้ **CreateProjectV1** API</span><span class="sxs-lookup"><span data-stu-id="60d78-171">The default bucket is created using the **CreateProjectV1** API.</span></span> |
| <span data-ttu-id="60d78-172">สมาชิกของทีมโครงการ</span><span class="sxs-lookup"><span data-stu-id="60d78-172">Project team member</span></span> | <span data-ttu-id="60d78-173">ใช่</span><span class="sxs-lookup"><span data-stu-id="60d78-173">Yes</span></span> | <span data-ttu-id="60d78-174">ใช่</span><span class="sxs-lookup"><span data-stu-id="60d78-174">Yes</span></span> | <span data-ttu-id="60d78-175">ใช่</span><span class="sxs-lookup"><span data-stu-id="60d78-175">Yes</span></span> | <span data-ttu-id="60d78-176">สำหรับการดำเนินการสร้าง ให้ใช้ **CreateTeamMemberV1** API</span><span class="sxs-lookup"><span data-stu-id="60d78-176">For the create operation, use the **CreateTeamMemberV1** API.</span></span> |
| <span data-ttu-id="60d78-177">Project</span><span class="sxs-lookup"><span data-stu-id="60d78-177">Project</span></span> | <span data-ttu-id="60d78-178">ใช่</span><span class="sxs-lookup"><span data-stu-id="60d78-178">Yes</span></span> | <span data-ttu-id="60d78-179">ใช่</span><span class="sxs-lookup"><span data-stu-id="60d78-179">Yes</span></span> | <span data-ttu-id="60d78-180">ไม่พร้อมใช้งาน</span><span class="sxs-lookup"><span data-stu-id="60d78-180">N/A</span></span> | <span data-ttu-id="60d78-181">ไม่รองรับการดำเนินการกับฟิลด์ต่อไปนี้: **StateCode**, **BulkGenerationStatus**, **GlobalRevisionToken**, **CalendarID**, **Effort**, **EffortCompleted**, **EffortRemaining**, **Progress**, **Finish**, **TaskEarliestStart** และ **Duration**</span><span class="sxs-lookup"><span data-stu-id="60d78-181">Operations with the following fields aren't supported: **StateCode**, **BulkGenerationStatus**, **GlobalRevisionToken**, **CalendarID**, **Effort**, **EffortCompleted**, **EffortRemaining**, **Progress**, **Finish**, **TaskEarliestStart**, and **Duration**.</span></span> |

<span data-ttu-id="60d78-182">API เหล่านี้สามารถเรียกใช้กับเอนทิตีอ็อบเจ็กต์ที่มีฟิลด์แบบกำหนดเอง</span><span class="sxs-lookup"><span data-stu-id="60d78-182">These APIs can be called with entity objects that include custom fields.</span></span>

<span data-ttu-id="60d78-183">รหัสคุณสมบัติเป็นแบบระบุหรือไม่ก็ได้</span><span class="sxs-lookup"><span data-stu-id="60d78-183">The ID property is optional.</span></span> <span data-ttu-id="60d78-184">หากระบุ ระบบจะพยายามใช้และแสดงข้อยกเว้นหากไม่สามารถใช้งานได้</span><span class="sxs-lookup"><span data-stu-id="60d78-184">If it's provided, the system attempts to use it and throws an exception if it can't be used.</span></span> <span data-ttu-id="60d78-185">หากไม่ระบบ ระบบจะสร้างขึ้นเอง</span><span class="sxs-lookup"><span data-stu-id="60d78-185">If it isn't provided, the system will generate it.</span></span>

## <a name="limitations-and-known-issues"></a><span data-ttu-id="60d78-186">ข้อจำกัดและปัญหาที่ทราบ</span><span class="sxs-lookup"><span data-stu-id="60d78-186">Limitations and known issues</span></span>
<span data-ttu-id="60d78-187">ต่อไปนี้เป็นรายการข้อจำกัดและปัญหาที่ทราบ:</span><span class="sxs-lookup"><span data-stu-id="60d78-187">The following is a list of limitations and known issues:</span></span>

- <span data-ttu-id="60d78-188">API กำหนดการ สามารถใช้ได้โดย **ผู้ใช้ที่มีสิทธิ์การใช้งาน Microsoft Project**</span><span class="sxs-lookup"><span data-stu-id="60d78-188">Schedule APIs can only be used by **Users with Microsoft Project License.**</span></span> <span data-ttu-id="60d78-189">แต่ไม่สามารถใช้โดย:</span><span class="sxs-lookup"><span data-stu-id="60d78-189">They can't be used by:</span></span>
    - <span data-ttu-id="60d78-190">ผู้ใช้แอปพลิเคชัน</span><span class="sxs-lookup"><span data-stu-id="60d78-190">Application users</span></span>
    - <span data-ttu-id="60d78-191">ผู้ใช้ของระบบ</span><span class="sxs-lookup"><span data-stu-id="60d78-191">System users</span></span>
    - <span data-ttu-id="60d78-192">ผู้ใช้การบูรณาการ</span><span class="sxs-lookup"><span data-stu-id="60d78-192">Integration users</span></span>
    - <span data-ttu-id="60d78-193">ผู้ใช้รายอื่นที่ไม่มีสิทธิ์การใช้งานที่จำเป็น</span><span class="sxs-lookup"><span data-stu-id="60d78-193">Other users that don't have the required license</span></span>
- <span data-ttu-id="60d78-194">**OperationSet** แต่ละรายการสามารถดำเนินงานได้สูงสุด 100 รายการ</span><span class="sxs-lookup"><span data-stu-id="60d78-194">Each **OperationSet** can only have a maximum of 100 operations.</span></span>
- <span data-ttu-id="60d78-195">ผู้ใช้แต่ละรายสามารถมี **OperationSet** ที่เปิดอยู่ได้สูงสุด 10 รายการ</span><span class="sxs-lookup"><span data-stu-id="60d78-195">Each user can only have a maximum of 10 open **OperationSets**.</span></span>
- <span data-ttu-id="60d78-196">ปัจจุบัน Project Operations รองรับงานทั้งหมดสูงสุด 500 งานในโครงการ</span><span class="sxs-lookup"><span data-stu-id="60d78-196">Project Operations currently supports a maximum of 500 total tasks on a project.</span></span>
- <span data-ttu-id="60d78-197">ขณะนี้สถานะความล้มเหลวและบันทึกความล้มเหลวของ **OperationSet** ยังไม่พร้อมใช้งาน</span><span class="sxs-lookup"><span data-stu-id="60d78-197">**OperationSet** failure status and failure logs aren't currently available.</span></span>
- <span data-ttu-id="60d78-198">API กำหนดการอยู่ในสถานะพรีวิวสำหรับสาธารณะ</span><span class="sxs-lookup"><span data-stu-id="60d78-198">Schedule APIs are in Public preview.</span></span> <span data-ttu-id="60d78-199">Microsoft ไม่รองรับการใช้ API เหล่านี้ในสภาพแวดล้อมการทำงานจริง</span><span class="sxs-lookup"><span data-stu-id="60d78-199">Using these APIs in a Production environment isn't supported by Microsoft.</span></span>

## <a name="sample-scenario"></a><span data-ttu-id="60d78-200">สถานการณ์ตัวอย่าง</span><span class="sxs-lookup"><span data-stu-id="60d78-200">Sample scenario</span></span>

<span data-ttu-id="60d78-201">ในสถานการณ์นี้ คุณจะสร้างโครงการ สมาชิกทีม งานสี่งาน และการกำหนดทรัพยากรสองรายการ</span><span class="sxs-lookup"><span data-stu-id="60d78-201">In this scenario, you will create a project, a team member, four tasks, and two resource assignments.</span></span> <span data-ttu-id="60d78-202">จากนั้น คุณจะปรับปรุงหนึ่งงาน ปรับปรุงโครงการ ลบหนึ่งงาน ลบการกำหนดทรัพยากรหนึ่งรายการ และสร้างการขึ้นต่อกันของงาน</span><span class="sxs-lookup"><span data-stu-id="60d78-202">Next, you will update one task, update the project, delete one task, delete one resource assignment, and create a task dependency.</span></span>

```C#
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
var task4 = GetTask("4ZZ";, projectReference);

var assignment1 = GetResourceAssignment("R1", teamMember, task2, project);
var assignment2 = GetResourceAssignment"R2", teamMember, task3, project);

var task1Response = CallPssCreateAction(task1, operationSetId);
var task2Response = CallPssCreateAction(task2, operationSetId);
var task3Response = CallPssCreateAction(task3, operationSetId);
var task4Response = CallPssCreateAction(task4, operationSetId);

varassignment1Response = CallPssCreateAction(assignment1, operationSetId);
varassignment2Response = CallPssCreateAction(assignment2, operationSetId);

task2["msdyn_subject"] = "Updated Task";
var task2UpdateResponse = CallPssUpdateAction(task2, operationSetId);

project["msdyn_subject"] = $"Proj update {DateTime.Now.ToShortTimeString()}";
var projectUpdateResponse = CallPssUpdateAction(project, operationSetId);

var task4DeleteResponse = CallPssDeleteAction(task4.Id.ToString(), task4.LogicalName, operationSetId);

varassignment2DeleteResponse = CallPssDeleteAction(assignment2.Id.ToString(), assignment2.LogicalName, operationSetId);

var dependency1 = GetTaskDependency(project, task2, task3);
var dependency1Response = CallPssCreateAction(dependency1, operationSetId);

CallExecuteOperationSetAction(operationSetId);
Console.WriteLine("Done....");
```

## <a name="additional-samples"></a><span data-ttu-id="60d78-203">ตัวอย่างเพิ่มเติม</span><span class="sxs-lookup"><span data-stu-id="60d78-203">Additional samples</span></span>

```C#
#region Call actions 

///<summary>
/// Calls the action to create an operationSet
/// </summary>
/// <paramname="projectId">project id for the operations to be included in this operationSet>/param>
/// <paramname="description">description of this operationSet</param>
/// <returns>operationSet id</returns>
privatestring CallCreateOperationSetAction(Guid projectId, string description)
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
/// <paramname="entity">Task or Resource Assignment</param>
/// <paramname="operationSetId">operationSet id</param>
/// <returns>OperationSetResponse</returns>
private OperationSetResponse CallPssCreateAction(Entity entity, string operationSetId)
{
    OrganizationRequest operationSetRequest = new OrganizationRequest("msdyn_PssCreateV1");
    operationSetRequest["Entity"] = entity;
    operationSetRequest["OperationSetId"] = operationSetId;
    return GetOperationSetResponseFromOrgResponse(organizationService.Execute(operationSetRequest));
}

/// <summary<
/// Calls the action to update an entity, only Task for now
/// </summary>
/// <paramname="entity">Task or Resource Assignment</param>
/// <paramname="operationSetId">operationSet Id</param>
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
/// <summary>
/// <paramname="recordId">Id of the record to be deleted</param>
/// <paramname="entityLogicalName">Entity logical name of the record</param>
/// <paramname="operationSetId">OperationSet Id</param>
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
/// <summary>
/// <paramname="operationSetId">operationSet id</param>
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
/// <paramname="operationSetId">operationSet id</param>
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
/// <paramname="project">Project</param>
/// <returns>project Id</returns>
private Guid CallCreateProjectAction(Entity project)
{
    OrganizationRequest createProjectRequest = new OrganizationRequest("msdyn_CreateProjectV1";
    createProjectRequest["Project"] = project;
    OrganizationResponse response = organizationService.Execute(createProjectRequest);
    var projectId = Guid.Parse((string)response["ProjectId"]);

    return projectId;
}

/// <summary>
/// Calls the action to create a new project team member
/// </summary>
/// <paramname="teamMember">Project team member</param>
/// <returns>project team member Id</returns>
privatestring CallCreateTeamMemberAction(Entity teamMember)
{
    OrganizationRequest request = new OrganizationRequest("msdyn_CreateTeamMemberV1");
    request["TeamMember"] = teamMember;
    OrganizationResponse response = organizationService.Execute(request);
    return (string)response["TeamMemberId"];
}

private OperationSetResponse GetOperationSetResponseFromOrgResponse(OrganizationResponse orgResponse)
{
    return JsonConvert.DeserializeObject><OperationSetResponse>
    ((string)orgResponse.Results["OperationSetResponse";]);
}

private EntityCollection GetDefaultBucket(EntityReference projectReference)
{
    var columnsToFetch = new ColumnSet(";msdyn_project", "msdyn_name");
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
    task["msdyn_effort";] = 4d;
    task["msdyn_scheduledstart"] = DateTime.Today;
    task["msdyn_scheduledend"] = DateTime.Today.AddDays(5);
    task["msdyn_progress"] = 0.34m;
    task["msdyn_start"] = DateTime.Now.AddDays(1);
    task["msdyn_projectbucket"] = GetBucket(projectReference).ToEntityReference();
    task["msdyn_LinkStatus"] = new OptionSetValue(192350000);

    //Custom field handling
    /*
        task["new_custom1"] = "Just my test";
        task[";new_age"] = 98;
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
publicclassOperationSetResponse
{
    [DataMember(Name = "operationSetId")]
    public Guid OperationSetId { get; set; }

    [DataMember(Name = "operationSetDetailId")]
    public Guid OperationSetDetailId { get; set; }

    [DataMember(Name = "operationType")]
    publicstring OperationType { get; set; }

    [DataMember(Name = "recordId")]
    publicstring RecordId { get; set; }

    [DataMember(Name = "correlationId")]
    publicstring CorrelationId { get; set; }
}

#endregion
```
