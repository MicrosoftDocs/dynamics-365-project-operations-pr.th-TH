---
title: การจัดการทรัพยากรเปลี่ยนแปลง (Project Service Automation 3.x)
description: หัวข้อนี้แสดงข้อมูลเกี่ยวกับการเปลี่ยนแปลงในพื้นที่การจัดการทรัพยากร
author: makk
manager: kfend
ms.custom:
- dyn365-projectservice
ms.date: 03/18/2019
ms.topic: article
ms.prod: Project Service
ms.service: business-applications
ms.assetid: 25fafd22-fe94-4865-8d4d-3e6582c999d5
ms.author: makk
audience: admin
search.audienceType:
- admin
- customizer
search.app:
- D365PS
ms.openlocfilehash: e00ce5a9604e25764567a3f9d38ec85aec4245d4
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 03/24/2020
ms.locfileid: "3756443"
---
# <a name="resource-management-changes-project-service-automation-3x"></a><span data-ttu-id="1920c-103">การจัดการทรัพยากรเปลี่ยนแปลง (Project Service Automation 3.x)</span><span class="sxs-lookup"><span data-stu-id="1920c-103">Resource management changes (Project Service Automation 3.x)</span></span>

<span data-ttu-id="1920c-104">ส่วนของหัวข้อนี้ให้ข้อมูลเกี่ยวกับการเปลี่ยนแปลงที่ได้ทำไว้ในพื้นที่การจัดการทรัพยากรของ Dynamics 365 Project Service Automation รุ่น 3.x</span><span class="sxs-lookup"><span data-stu-id="1920c-104">The sections of this topic provide information about the changes that have been made to the Resource management area of Dynamics 365 Project Service Automation version 3.x.</span></span>

## <a name="project-estimates"></a><span data-ttu-id="1920c-105">การประมาณการโครงการ</span><span class="sxs-lookup"><span data-stu-id="1920c-105">Project estimates</span></span>

<span data-ttu-id="1920c-106">แทนที่จะขึ้นอยู่กับ **msdyn\_งานโครงการ** เอนทิตี **(งานโครงการ)**, การประเมินโครงการจะขึ้นอยู่กับ **msdyn\_การมอบหมายทรัพยากร** เอนทิตี (**การมอบหมายทรัพยากร**)</span><span class="sxs-lookup"><span data-stu-id="1920c-106">Instead of being based on the **msdyn\_projecttask** entity (**Project Task**), project estimates are based on the **msdyn\_resourceassignment** entity (**Resource Assignment**).</span></span> <span data-ttu-id="1920c-107">การมอบหมายทรัพยากรได้กลายเป็น "แหล่งที่มาของความจริง" สำหรับการจัดกำหนดการและการกำหนดราคางาน</span><span class="sxs-lookup"><span data-stu-id="1920c-107">Resource assignments have become the "source of truth" for task scheduling and pricing.</span></span>

## <a name="line-tasks"></a><span data-ttu-id="1920c-108">งานในรายการ</span><span class="sxs-lookup"><span data-stu-id="1920c-108">Line tasks</span></span>

<span data-ttu-id="1920c-109">ใน PSA 3.x, งานในรายการจะล้าสมัย (ไม่สนับสนุน)</span><span class="sxs-lookup"><span data-stu-id="1920c-109">In PSA 3.x, line tasks are obsolete (deprecated).</span></span> <span data-ttu-id="1920c-110">ตอนนี้การมอบหมายจะชี้ไปที่งานทั้งหมดแทนที่จะเป็นงานในรายการ</span><span class="sxs-lookup"><span data-stu-id="1920c-110">Assignments now point to the whole task instead of the line tasks.</span></span>

<span data-ttu-id="1920c-111">ตัวอย่างต่อไปนี้แสดงให้เห็นวิธีว่างานที่มีชื่อว่า "งานทดสอบ" ถูกมอบหมายให้กับสมาชิกในทีม A และ B ในรุ่นก่อนหน้าของ PSA และใน PSA 3.x</span><span class="sxs-lookup"><span data-stu-id="1920c-111">The following example shows how a task that is named "Test task" is assigned to team members A and B in earlier versions of PSA and in PSA 3.x.</span></span>

- <span data-ttu-id="1920c-112">**ก่อน PSA 3.x:**</span><span class="sxs-lookup"><span data-stu-id="1920c-112">**Before PSA 3.x:**</span></span>

    - <span data-ttu-id="1920c-113">งานทดสอบ</span><span class="sxs-lookup"><span data-stu-id="1920c-113">Test task</span></span>

        - <span data-ttu-id="1920c-114">งานทดสอบ – งานในรายการที่ 1</span><span class="sxs-lookup"><span data-stu-id="1920c-114">Test task – Line task 1</span></span>

            - <span data-ttu-id="1920c-115">การมอบหมายงานให้ A</span><span class="sxs-lookup"><span data-stu-id="1920c-115">Assignment to A</span></span>

        - <span data-ttu-id="1920c-116">งานทดสอบ – งานในรายการที่ 2</span><span class="sxs-lookup"><span data-stu-id="1920c-116">Test task – Line task 2</span></span>

            - <span data-ttu-id="1920c-117">การมอบหมายงานให้ B</span><span class="sxs-lookup"><span data-stu-id="1920c-117">Assignment to B</span></span>

- <span data-ttu-id="1920c-118">**PSA 3.x:**</span><span class="sxs-lookup"><span data-stu-id="1920c-118">**PSA 3.x:**</span></span>

    - <span data-ttu-id="1920c-119">งานทดสอบ</span><span class="sxs-lookup"><span data-stu-id="1920c-119">Test task</span></span>

        - <span data-ttu-id="1920c-120">การมอบหมายงานให้ A</span><span class="sxs-lookup"><span data-stu-id="1920c-120">Assignment to A</span></span>
        - <span data-ttu-id="1920c-121">การมอบหมายงานให้ B</span><span class="sxs-lookup"><span data-stu-id="1920c-121">Assignment to B</span></span>

## <a name="unassigned-assignment"></a><span data-ttu-id="1920c-122">การมอบหมายงานที่ไม่ได้มอบหมาย</span><span class="sxs-lookup"><span data-stu-id="1920c-122">Unassigned assignment</span></span>

<span data-ttu-id="1920c-123">ใน PSA 3.x, การมอบหมายงานที่ไม่ได้มอบหมายคือการมอบหมายที่มอบหมายให้กับสมาชิกในทีม **NULL** และทรัพยากร **NULL**</span><span class="sxs-lookup"><span data-stu-id="1920c-123">In PSA 3.x, an unassigned assignment is an assignment that is assigned to a **NULL** team member and a **NULL** resource.</span></span> <span data-ttu-id="1920c-124">การมอบหมายงานที่ไม่ได้มอบหมายอาจเกิดขึ้นได้ในสองสถานการณ์:</span><span class="sxs-lookup"><span data-stu-id="1920c-124">Unassigned assignments can occur in a couple of scenarios:</span></span>

- <span data-ttu-id="1920c-125">ถ้ามีการสร้างงานแต่ยังไม่ได้มอบหมายให้กับสมาชิกใดในทีม การมอบหมายงานที่ไม่ได้มอบหมายจะถูกสร้างขึ้นเสมอ</span><span class="sxs-lookup"><span data-stu-id="1920c-125">If a task has been created, but it hasn't yet been assigned to any team member, an unassigned assignment is always created.</span></span> 
- <span data-ttu-id="1920c-126">ถ้าผู้รับมอบหมายในงานทั้งหมดถูกลบออก การมอบหมายงานที่ไม่ได้มอบหมายจะถูกสร้างขึ้นอีกครั้งสำหรับงานนนั้น</span><span class="sxs-lookup"><span data-stu-id="1920c-126">If all assignees on a task are removed, an unassigned assignment is re-created for that task.</span></span>

## <a name="scheduling-fields-on-the-project-task-entity"></a><span data-ttu-id="1920c-127">ฟิลด์การจัดกำหนดการบนเอนทิตีงานโครงการ</span><span class="sxs-lookup"><span data-stu-id="1920c-127">Scheduling fields on the Project Task entity</span></span>

<span data-ttu-id="1920c-128">ฟิล์ดในเอนทิตี **msdyn\_projecttask** ได้ถูกยกเลิกการสนับสนุนหรือย้ายไปยังเอนทิตี **msdyn\_resourceassignment** ตอนนี้มีการอ้างอิงจากเอนทิตี **msdyn\_projectteam** (**Project Team Member**)</span><span class="sxs-lookup"><span data-stu-id="1920c-128">The fields on the **msdyn\_projecttask** entity have been deprecated or moved to the **msdyn\_resourceassignment** entity, or they are now referenced from the **msdyn\_projectteam** entity (**Project Team Member**).</span></span>

| <span data-ttu-id="1920c-129">ฟิลด์ที่ไม่สนับสนุนใน msdyn\_projecttask (งานโครงการ)</span><span class="sxs-lookup"><span data-stu-id="1920c-129">Deprecated field on msdyn\_projecttask (Project Task)</span></span> | <span data-ttu-id="1920c-130">ฟิลด์ใหม่บน msdyn\_resourceassignment (การมอบหมายทรัพยากร)</span><span class="sxs-lookup"><span data-stu-id="1920c-130">New field on msdyn\_resourceassignment (Resource Assignment)</span></span> | <span data-ttu-id="1920c-131">ข้อคิดเห็น</span><span class="sxs-lookup"><span data-stu-id="1920c-131">Comment</span></span> |
|---|---|---|
| <span data-ttu-id="1920c-132">msdyn\_assignedresources</span><span class="sxs-lookup"><span data-stu-id="1920c-132">msdyn\_assignedresources</span></span> | <span data-ttu-id="1920c-133">ไม่มี</span><span class="sxs-lookup"><span data-stu-id="1920c-133">None</span></span> | |
| <span data-ttu-id="1920c-134">msdyn\_assignedteammembers</span><span class="sxs-lookup"><span data-stu-id="1920c-134">msdyn\_assignedteammembers</span></span> | <span data-ttu-id="1920c-135">ไม่มี</span><span class="sxs-lookup"><span data-stu-id="1920c-135">None</span></span> | |
| <span data-ttu-id="1920c-136">msdyn\_numberofresources</span><span class="sxs-lookup"><span data-stu-id="1920c-136">msdyn\_numberofresources</span></span> | <span data-ttu-id="1920c-137">ไม่มี</span><span class="sxs-lookup"><span data-stu-id="1920c-137">None</span></span> | |
| <span data-ttu-id="1920c-138">msdyn\_scheduledhours</span><span class="sxs-lookup"><span data-stu-id="1920c-138">msdyn\_scheduledhours</span></span> | <span data-ttu-id="1920c-139">ไม่มี</span><span class="sxs-lookup"><span data-stu-id="1920c-139">None</span></span> | |
| <span data-ttu-id="1920c-140">msdyn\_effortcontour</span><span class="sxs-lookup"><span data-stu-id="1920c-140">msdyn\_effortcontour</span></span> | <span data-ttu-id="1920c-141">msdyn\_plannedwork</span><span class="sxs-lookup"><span data-stu-id="1920c-141">msdyn\_plannedwork</span></span> | <span data-ttu-id="1920c-142">รูปแบบของโครงสร้างข้อมูล JavaScript Object Notation (JSON) ที่เก็บอยู่ในฟิล์ดมีการเปลี่ยนแปลง</span><span class="sxs-lookup"><span data-stu-id="1920c-142">The format of the JavaScript Object Notation (JSON) data structure that is stored in the field has been changed.</span></span> |

## <a name="schedule-contour"></a><span data-ttu-id="1920c-143">เส้นชั้นหมายกำหนดการให้บริการ</span><span class="sxs-lookup"><span data-stu-id="1920c-143">Schedule contour</span></span>

<span data-ttu-id="1920c-144">เส้นชั้นหมายกำหนดการให้บริการจะถูกจัดเก็บไว้ในฟิลด์ **งานที่วางแผน** (**msdyn\_plannedwork**) ของแต่ละเอนทิตี **การมอบหมายทรัพยากร** (**msdyn\_resourceassignment**)</span><span class="sxs-lookup"><span data-stu-id="1920c-144">The schedule contour is stored in the **Planned Work** field (**msdyn\_plannedwork**) of each **Resource Assignment** entity (**msdyn\_resourceassignment**).</span></span>

### <a name="structure"></a><span data-ttu-id="1920c-145">โครงสร้าง</span><span class="sxs-lookup"><span data-stu-id="1920c-145">Structure</span></span>

<span data-ttu-id="1920c-146">โครงสร้างใหม่ของเส้นชั้นหมายกำหนดการให้บริการประกอบด้วยชิ้นเวลาที่ยืดหยุ่นที่กำหนดไว้สำหรับแต่ละวันของหมายกำหนดการให้บริการ</span><span class="sxs-lookup"><span data-stu-id="1920c-146">The new structure of the schedule contour consists of flexible time slices that are defined for each day of the schedule.</span></span> <span data-ttu-id="1920c-147">แต่ละส่วนของเวลามีคุณสมบัติดังต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="1920c-147">Each time slice has the following properties:</span></span>

- <span data-ttu-id="1920c-148">**เริ่มต้น** – จุดเริ่มต้นของชั่วโมงการทำงานสำหรับวันตามปฏิทินโครงการ</span><span class="sxs-lookup"><span data-stu-id="1920c-148">**Start** – The start of the working hours for the day, according to the project calendar.</span></span>
- <span data-ttu-id="1920c-149">**สิ้นสุด** – จุดสิ้นสุดของชั่วโมงการทำงานสำหรับวันตามปฏิทินโครงการ</span><span class="sxs-lookup"><span data-stu-id="1920c-149">**End** – The end of the working hours for the day, according to the project calendar.</span></span>
- <span data-ttu-id="1920c-150">**ชั่วโมง** – จำนวนชั่วโมงที่มอบหมายในวัน</span><span class="sxs-lookup"><span data-stu-id="1920c-150">**Hours** – The number of hours that are assigned on the day.</span></span>

<span data-ttu-id="1920c-151">**ตัวอย่าง**</span><span class="sxs-lookup"><span data-stu-id="1920c-151">**Example**</span></span>

<span data-ttu-id="1920c-152">ตัวอย่างนี้ใช้ปฏิทินโครงการที่วันทำงานตั้งแต่ 9.00-17.00 น. ในโซนเวลา UTC-8</span><span class="sxs-lookup"><span data-stu-id="1920c-152">This example uses a project calendar where the workday is from 9 AM to 5 PM in the UTC-8 time zone.</span></span>

```json
[{"End":"\/Date(1543885200000)\/","Start":"\/Date(1543856400000)\/","Hours":8},{"End":"\/Date(1543971600000)\/","Start":"\/Date(1543942800000)\/","Hours":8},{"End":"\/Date(1544058000000)\/","Start":"\/Date(1544029200000)\/","Hours":2}]
```

### <a name="auto-scheduling-and-manual-scheduling"></a><span data-ttu-id="1920c-153">การจัดกำหนดการแบบอัตโนมัติและการจัดกำหนดการด้วยตนเอง</span><span class="sxs-lookup"><span data-stu-id="1920c-153">Auto-scheduling and manual scheduling</span></span>

<span data-ttu-id="1920c-154">ถ้างานมีการจัดกำหนดการแบบอัตโนมัติ ชั่วโมงจะถูกโหลดด้านหน้าและระยะเวลาของงานอาจจะลดลง</span><span class="sxs-lookup"><span data-stu-id="1920c-154">If a task is auto-scheduled, the hours are front-loaded, and the task duration might be reduced.</span></span>

<span data-ttu-id="1920c-155">**ตัวอย่าง**</span><span class="sxs-lookup"><span data-stu-id="1920c-155">**Example**</span></span>

<span data-ttu-id="1920c-156">งานต่อไปนี้จะถูกจัดกำหนดการโดยอัตโนมัติเป็นเวลา18ชั่วโมงตลอดสามวัน (3 ธันวาคม 2018 ถึง 5 ธันวาคม 2018)</span><span class="sxs-lookup"><span data-stu-id="1920c-156">The following task is auto-scheduled for 18 hours over three days (December 3, 2018, to December 5, 2018).</span></span>

```json
[{"End":"\/Date(1543885200000)\/","Start":"\/Date(1543856400000)\/","Hours":8},{"End":"\/Date(1543971600000)\/","Start":"\/Date(1543942800000)\/","Hours":8},{"End":"\/Date(1544058000000)\/","Start":"\/Date(1544029200000)\/","Hours":2}]
```

<span data-ttu-id="1920c-157">ถ้างานถูกจัดกำหนดการด้วยตนเอง ชั่วโมงจะมีการกระจายอย่างสม่ำเสมอไปที่วันที่ทั้งหมด</span><span class="sxs-lookup"><span data-stu-id="1920c-157">If a task is manually scheduled, the hours are evenly distributed to all the dates.</span></span>

<span data-ttu-id="1920c-158">**ตัวอย่าง**</span><span class="sxs-lookup"><span data-stu-id="1920c-158">**Example**</span></span>

<span data-ttu-id="1920c-159">งานต่อไปนี้จะถูกจัดกำหนดการด้วยตนเองเป็นเวลา18ชั่วโมงตลอดสามวัน (3 ธันวาคม 2018 ถึง 5 ธันวาคม 2018)</span><span class="sxs-lookup"><span data-stu-id="1920c-159">The following task is manually scheduled for 18 hours over three days (December 3, 2018, to December 5, 2018).</span></span>

```json
[{"End":"\/Date(1543885200000)\/","Start":"\/Date(1543856400000)\/","Hours":6},{"End":"\/Date(1543971600000)\/","Start":"\/Date(1543942800000)\/","Hours":6},{"End":"\/Date(1544058000000)\/","Start":"\/Date(1544029200000)\/","Hours":6}]
```

### <a name="assignment-unit"></a><span data-ttu-id="1920c-160">หน่วยการมอบหมาย</span><span class="sxs-lookup"><span data-stu-id="1920c-160">Assignment unit</span></span>

<span data-ttu-id="1920c-161">หน่วยการมอบหมายได้ถูกยกเลิกการสนับสนุนใน PSA 3.x</span><span class="sxs-lookup"><span data-stu-id="1920c-161">The assignment unit has been deprecated in PSA 3.x.</span></span> <span data-ttu-id="1920c-162">ขณะนี้ชั่วโมงความพยายามงานจะถูกแบ่งเท่าๆกันต่อวันท่ามกลางทรัพยากรที่มอบหมายทั้งหมด.</span><span class="sxs-lookup"><span data-stu-id="1920c-162">The task effort hours are now equally divided, per day, among all the assigned resources.</span></span>

<span data-ttu-id="1920c-163">**ตัวอย่าง**</span><span class="sxs-lookup"><span data-stu-id="1920c-163">**Example**</span></span>

<span data-ttu-id="1920c-164">ในตัวอย่างนี้ งานจะถูกมอบหมายให้กับสองทรัพยากรและมีการจัดกำหนดการแบบอัตโนมัติสำหรับ 36 ชั่วโมงในสามวัน (3 ธันวาคม 2018 ถึง 5 ธันวาคม 2018)</span><span class="sxs-lookup"><span data-stu-id="1920c-164">In this example, the task is is assigned to two resources and is auto-scheduled for 36 hours over three days (December 3, 2018, to December 5, 2018).</span></span>

- <span data-ttu-id="1920c-165">การมอบหมายที่ 1:</span><span class="sxs-lookup"><span data-stu-id="1920c-165">Assignment 1:</span></span>

    ```json
    [{"End":"\/Date(1543885200000)\/","Start":"\/Date(1543856400000)\/","Hours":8},{"End":"\/Date(1543971600000)\/","Start":"\/Date(1543942800000)\/","Hours":8},{"End":"\/Date(1544058000000)\/","Start":"\/Date(1544029200000)\/","Hours":2}]
    ```

- <span data-ttu-id="1920c-166">การมอบหมายที่ 2:</span><span class="sxs-lookup"><span data-stu-id="1920c-166">Assignment 2:</span></span>

    ```json
    [{"End":"\/Date(1543885200000)\/","Start":"\/Date(1543856400000)\/","Hours":8},{"End":"\/Date(1543971600000)\/","Start":"\/Date(1543942800000)\/","Hours":8},{"End":"\/Date(1544058000000)\/","Start":"\/Date(1544029200000)\/","Hours":2}]
    ```

## <a name="pricing-dimensions"></a><span data-ttu-id="1920c-167">มิติการกำหนดราคา</span><span class="sxs-lookup"><span data-stu-id="1920c-167">Pricing dimensions</span></span>

<span data-ttu-id="1920c-168">ใน PSA 3.x, ฟิลด์มิติการกำหนดราคาเฉพาะทรัพยากร (เช่น**บทบาท** และ **หน่วยองค์กร**) ถูกลบออกจากเอนทิตี **msdyn\_projecttask**</span><span class="sxs-lookup"><span data-stu-id="1920c-168">In PSA 3.x, resource-specific pricing dimension fields (such as **Role** and **Organizational Unit**) have been removed from the **msdyn\_projecttask** entity.</span></span> <span data-ttu-id="1920c-169">ฟิลด์เหล่านี้สามารถดึงข้อมูลจากสมาชิกทีมโครงการที่เกี่ยวข้อง (**msdyn\_projectteam**) ของการมอบหมายทรัพยากร (**msdyn\_resourceassignment**) เมื่อการประเมินโครงการมีการสร้างขึ้น</span><span class="sxs-lookup"><span data-stu-id="1920c-169">These fields can now be retrieved from the corresponding project team member (**msdyn\_projectteam**) of the resource assignment (**msdyn\_resourceassignment**) when project estimates are generated.</span></span> <span data-ttu-id="1920c-170">ฟิลด์ใหม่ **msdyn\_organizationalunit** ได้ถูกเพิ่มลงในเอนทิตีของ **msdyn\_projectteam**</span><span class="sxs-lookup"><span data-stu-id="1920c-170">A new field, **msdyn\_organizationalunit**, has been added to the **msdyn\_projectteam** entity.</span></span>

| <span data-ttu-id="1920c-171">ฟิลด์ที่ไม่สนับสนุนใน msdyn\_projecttask (งานโครงการ)</span><span class="sxs-lookup"><span data-stu-id="1920c-171">Deprecated field on msdyn\_projecttask (Project Task)</span></span> | <span data-ttu-id="1920c-172">ฟิลด์จาก msdyn\_projectteam (สมาชิกทีมโครงการ) ที่ใช้แทน</span><span class="sxs-lookup"><span data-stu-id="1920c-172">Field from msdyn\_projectteam (Project Team Member) that is used instead</span></span> |
|---|---|
| <span data-ttu-id="1920c-173">msdyn\_resourcecategory</span><span class="sxs-lookup"><span data-stu-id="1920c-173">msdyn\_resourcecategory</span></span> | <span data-ttu-id="1920c-174">msdyn\_resourcecategory</span><span class="sxs-lookup"><span data-stu-id="1920c-174">msdyn\_resourcecategory</span></span> |
| <span data-ttu-id="1920c-175">msdyn\_organizationalunit</span><span class="sxs-lookup"><span data-stu-id="1920c-175">msdyn\_organizationalunit</span></span> | <span data-ttu-id="1920c-176">msdyn\_organizationalunit</span><span class="sxs-lookup"><span data-stu-id="1920c-176">msdyn\_organizationalunit</span></span> |

## <a name="contours"></a><span data-ttu-id="1920c-177">เส้นชั้น</span><span class="sxs-lookup"><span data-stu-id="1920c-177">Contours</span></span>

<span data-ttu-id="1920c-178">ฟิล์ดการกำหนดราคาและการประเมินเส้นชั้นได้ถูกยกเลิกการสนับสนุนในเอนทิตี **msdyn\_projecttask**</span><span class="sxs-lookup"><span data-stu-id="1920c-178">The pricing and estimation contour fields have been deprecated on the **msdyn\_projecttask** entity.</span></span> <span data-ttu-id="1920c-179">พวกเขาถูกย้ายไปยังเอนทิตี **msdyn\_resourceassignment**</span><span class="sxs-lookup"><span data-stu-id="1920c-179">They have been moved to the **msdyn\_resourceassignment** entity.</span></span>

| <span data-ttu-id="1920c-180">ฟิลด์ที่ไม่สนับสนุนใน msdyn\_projecttask (งานโครงการ)</span><span class="sxs-lookup"><span data-stu-id="1920c-180">Deprecated field on msdyn\_projecttask (Project Task)</span></span> | <span data-ttu-id="1920c-181">ฟิลด์ใหม่บน msdyn\_resourceassignment (การมอบหมายทรัพยากร)</span><span class="sxs-lookup"><span data-stu-id="1920c-181">New field on msdyn\_resourceassignment (Resource Assignment)</span></span> |
|---|---|
| <span data-ttu-id="1920c-182">msdyn\_costestimatecontour</span><span class="sxs-lookup"><span data-stu-id="1920c-182">msdyn\_costestimatecontour</span></span> | <span data-ttu-id="1920c-183">msdyn\_plannedcostcontour</span><span class="sxs-lookup"><span data-stu-id="1920c-183">msdyn\_plannedcostcontour</span></span> |
| <span data-ttu-id="1920c-184">msdyn\_salesestimatecontour</span><span class="sxs-lookup"><span data-stu-id="1920c-184">msdyn\_salesestimatecontour</span></span> | <span data-ttu-id="1920c-185">msdyn\_plannedcostcontour</span><span class="sxs-lookup"><span data-stu-id="1920c-185">msdyn\_plannedsalescontour</span></span> |

<span data-ttu-id="1920c-186">ฟิล์ดต่อไปนี้ถูกเพิ่มไปยังเอนทิตี **msdyn\_resourceassignment**:</span><span class="sxs-lookup"><span data-stu-id="1920c-186">The following fields have been added to the **msdyn\_resourceassignment** entity:</span></span>

* <span data-ttu-id="1920c-187">msdyn\_plannedcost</span><span class="sxs-lookup"><span data-stu-id="1920c-187">msdyn\_plannedcost</span></span>
* <span data-ttu-id="1920c-188">msdyn\_plannedsales</span><span class="sxs-lookup"><span data-stu-id="1920c-188">msdyn\_plannedsales</span></span>

<span data-ttu-id="1920c-189">ฟิลด์ต่อไปนี้สำหรับต้นทุนและการขายที่วางแผน, จริง, และที่คงเหลือจะไม่มีการเปลี่ยนแปลงในเอนทิตี **msdyn\_projecttask**:</span><span class="sxs-lookup"><span data-stu-id="1920c-189">The following fields for planned, actual, and remaining cost and sales are unchanged on the **msdyn\_projecttask** entity:</span></span>

* <span data-ttu-id="1920c-190">msdyn\_plannedcost</span><span class="sxs-lookup"><span data-stu-id="1920c-190">msdyn\_plannedcost</span></span>
* <span data-ttu-id="1920c-191">msdyn\_plannedsales</span><span class="sxs-lookup"><span data-stu-id="1920c-191">msdyn\_plannedsales</span></span>
* <span data-ttu-id="1920c-192">msdyn\_actualcost</span><span class="sxs-lookup"><span data-stu-id="1920c-192">msdyn\_actualcost</span></span>
* <span data-ttu-id="1920c-193">msdyn\_actualsales</span><span class="sxs-lookup"><span data-stu-id="1920c-193">msdyn\_actualsales</span></span>
* <span data-ttu-id="1920c-194">msdyn\_remainingcost</span><span class="sxs-lookup"><span data-stu-id="1920c-194">msdyn\_remainingcost</span></span>
* <span data-ttu-id="1920c-195">msdyn\_remainingsales</span><span class="sxs-lookup"><span data-stu-id="1920c-195">msdyn\_remainingsales</span></span>
