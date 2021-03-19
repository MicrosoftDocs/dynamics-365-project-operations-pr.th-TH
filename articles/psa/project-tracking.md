---
title: ความคืบหน้าของโครงการและการใช้ต้นทุน
description: หัวข้อนี้แสดงข้อมูลเกี่ยวกับการติดตามความคืบหน้าของโครงการและปริมาณการใช้ต้นทุน
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 08/21/2020
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
ms.openlocfilehash: 73b23aad2976c8ccbb542fc2dda1d96dd9f5714b
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 02/15/2021
ms.locfileid: "5283661"
---
# <a name="project-progress-and-cost-consumption"></a><span data-ttu-id="4eccb-103">ความคืบหน้าของโครงการและการใช้ต้นทุน</span><span class="sxs-lookup"><span data-stu-id="4eccb-103">Project progress and cost consumption</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

<span data-ttu-id="4eccb-104">ความจำเป็นในการติดตามความคืบหน้ากับกำหนดการแตกต่างกันไปตามอุตสาหกรรม</span><span class="sxs-lookup"><span data-stu-id="4eccb-104">The need to track progress against a schedule varies by industry.</span></span> <span data-ttu-id="4eccb-105">อุตสาหกรรมบางอย่างติดตามในระดับที่ละเอียด ในขณะที่อุตสาหกรรมอื่นๆ ติดตามในระดับที่สูงขึ้น</span><span class="sxs-lookup"><span data-stu-id="4eccb-105">Some industries track at a granular level, whereas other industries track at a higher level.</span></span> <span data-ttu-id="4eccb-106">หัวข้อนี้แสดงให้เห็นถึงวิธีการจัดกำหนดการเพื่อให้ตรงกับข้อกำหนดขององค์กรของคุณ</span><span class="sxs-lookup"><span data-stu-id="4eccb-106">This topic shows how to schedule in order to meet your organization's requirements.</span></span>

## <a name="effort-tracking-view"></a><span data-ttu-id="4eccb-107">มุมมองการติดตามกำลังคนที่ใช้</span><span class="sxs-lookup"><span data-stu-id="4eccb-107">Effort tracking view</span></span>

<span data-ttu-id="4eccb-108">มุมมอง **การติดตามความพยายามที่ใช้** ติดตามความคืบหน้าของงานในกำหนดการ</span><span class="sxs-lookup"><span data-stu-id="4eccb-108">The **Effort tracking** view tracks the progress of tasks in the schedule.</span></span> <span data-ttu-id="4eccb-109">ซึ่งจะเปรียบเทียบจำนวนชั่วโมงที่ใช้จริงกับงานกับจำนวนชั่วโมงที่วางแผนไว้ที่ของงาน</span><span class="sxs-lookup"><span data-stu-id="4eccb-109">It compares the actual effort hours spent on a task to the task's planned effort hours.</span></span> <span data-ttu-id="4eccb-110">Project Service Automation ใช้สูตรต่อไปนี้เพื่อคำนวณเป้าหมายการติดตาม:</span><span class="sxs-lookup"><span data-stu-id="4eccb-110">Project Service Automation uses the following formulas to calculate the tracking metrics:</span></span>

<span data-ttu-id="4eccb-111">เริ่มต้นด้วยการสร้างงาน: ต้นทุนตามแผนจะมีการกำหนดเป็นต้นทุนโดยประมาณเมื่อเสร็จสมบูรณ์</span><span class="sxs-lookup"><span data-stu-id="4eccb-111">Initially on the task creation: Planned cost will be set to the Estimated cost at complete.</span></span> <span data-ttu-id="4eccb-112">เมื่อมีการบันทึกข้อมูลตามจริงในงาน รายการต่อไปนี้จะได้รับการคำนวณในมุมมองการติดตามสำหรับกำลังคน</span><span class="sxs-lookup"><span data-stu-id="4eccb-112">Once Actuals are recorded on the task, the following will be calculation on the Tracking view for Effort</span></span>

- <span data-ttu-id="4eccb-113">เปอร์เซ็นต์ความคืบหน้า = กำลังคนจริงที่ใช้ไปจนถึงปัจจุบัน ÷ ประมาณการเมื่อดำเนินงานเสร็จสมบูรณ์ (EAC)</span><span class="sxs-lookup"><span data-stu-id="4eccb-113">Progress percentage = Actual effort spent to date ÷ Estimate at complete (EAC)</span></span> 
- <span data-ttu-id="4eccb-114">การประมาณการที่ต้องใช้จนเสร็จสมบูรณ์ (ETC) = ประมาณการเมื่อดำเนินงานเสร็จสมบูรณ (EAC) – กำลังคนจริงที่ใช้ไปจนถึงปัจจุบัน</span><span class="sxs-lookup"><span data-stu-id="4eccb-114">Estimate to complete (ETC) = Estimate at complete (EAC)  – Actual effort spent to date</span></span> 
- <span data-ttu-id="4eccb-115">EAC = กำลังคนที่เหลือ + กำลังคนจริงที่ใช้ไปจนถึงปัจจุบัน</span><span class="sxs-lookup"><span data-stu-id="4eccb-115">EAC = Remaining effort + Actual effort spent to date</span></span> 
- <span data-ttu-id="4eccb-116">ผลต่างความพยายามที่คาดการณ์ = ความพยายามที่วางแผนไว้ – EAC</span><span class="sxs-lookup"><span data-stu-id="4eccb-116">Projected effort variance = Planned effort – EAC</span></span>

<span data-ttu-id="4eccb-117">Project Service Automation แสดงการประมาณการของผลต่างของกำลังคนในงาน</span><span class="sxs-lookup"><span data-stu-id="4eccb-117">Project Service Automation shows a projection of the effort variance on the task.</span></span> <span data-ttu-id="4eccb-118">ถ้า EAC มากกว่าความพยายามที่วางแผนไว้ งานจะถูกคาดการณ์ให้ใช้เวลามากกว่าที่วางแผนไว้แต่เดิม</span><span class="sxs-lookup"><span data-stu-id="4eccb-118">If the EAC is more than the planned effort, the task is projected to take more time than was originally planned.</span></span> <span data-ttu-id="4eccb-119">ดังนั้น จึงล่าช้ากว่ากำหนดเวลา</span><span class="sxs-lookup"><span data-stu-id="4eccb-119">Therefore, it's behind schedule.</span></span> <span data-ttu-id="4eccb-120">ถ้า EAC น้อยกว่าความพยายามที่วางแผนไว้ งานจะถูกคาดการณ์ให้ใช้เวลาน้อยกว่าที่วางแผนไว้แต่เดิม</span><span class="sxs-lookup"><span data-stu-id="4eccb-120">If the EAC is less than the planned effort, the task is projected to take less time than was originally planned.</span></span> <span data-ttu-id="4eccb-121">ดังนั้น จึงก่อนกำหนดการ</span><span class="sxs-lookup"><span data-stu-id="4eccb-121">Therefore, it's ahead of schedule.</span></span>

## <a name="reprojecting-effort"></a><span data-ttu-id="4eccb-122">ความพยายามในการประมาณการใหม่</span><span class="sxs-lookup"><span data-stu-id="4eccb-122">Reprojecting effort</span></span>

<span data-ttu-id="4eccb-123">เป็นปกติสำหรับผู้จัดการโครงการที่จะแก้ไขการประมาณการเดิมของงาน</span><span class="sxs-lookup"><span data-stu-id="4eccb-123">It's common for a project manager to revise the original estimates on a task.</span></span> <span data-ttu-id="4eccb-124">การประมาณการโครงการใหม่เป็นการรับรู้ของผู้จัดการโครงการของการประมาณการ ที่กำหนดสถานะปัจจุบันของโครงการ</span><span class="sxs-lookup"><span data-stu-id="4eccb-124">Project reprojections are a project manager's perception of estimates, given the current state of a project.</span></span> <span data-ttu-id="4eccb-125">อย่างไรก็ตาม เราไม่แนะนำให้ผู้จัดการโครงการเปลี่ยนเลขเส้นฐาน เนื่องจากเส้นฐานของโครงการแสดงแหล่งที่มาของความจริงที่เชื่อมต่อ สำหรับหมายกำหนดการให้บริการรและการปประมาณการต้นทุนของโครงการ และผู้เกี่ยวข้องทั้งหมดในโครงการได้ตกลงกันแล้ว</span><span class="sxs-lookup"><span data-stu-id="4eccb-125">However, we don't recommend that project managers change the baseline numbers, because the project baseline represents the established source of truth for the project's schedule and cost estimate, and all project stakeholders have agreed to it.</span></span>

<span data-ttu-id="4eccb-126">มีสองวิธีที่ผู้จัดการโครงการสามารถประมาณการโครงการกำลังคนในการทำงานใหม่:</span><span class="sxs-lookup"><span data-stu-id="4eccb-126">There are two ways that a project manager can reproject effort on tasks:</span></span>

- <span data-ttu-id="4eccb-127">แทนที่ ETC ค่าเริ่มต้นด้วยการประมาณการใหม่ของกำลังคนที่เหลือจริงในงาน</span><span class="sxs-lookup"><span data-stu-id="4eccb-127">Override the default ETC with a new estimate of the actual remaining effort on the task.</span></span> 
- <span data-ttu-id="4eccb-128">แทนที่เปอร์เซ็นต์ความคืบหน้าค่าเริ่มต้นด้วยการประมาณการใหม่ของความคืบหน้าจริงในงาน</span><span class="sxs-lookup"><span data-stu-id="4eccb-128">Override the default progress percentage with a new estimate of the true progress on the task.</span></span>

<span data-ttu-id="4eccb-129">แต่ละวิธีเหล่านี้ทำให้เกิดการคำนวณใหม่ของ ETC EAC ของงาน และเปอร์เซ็นต์ความคืบหน้า และผลต่างความพยายามที่คาดการณ์ไว้ในงาน</span><span class="sxs-lookup"><span data-stu-id="4eccb-129">Each of these approaches cause a recalculation of the task's ETC, EAC, and progress percentage, and the projected effort variance on a task.</span></span> <span data-ttu-id="4eccb-130">EAC ETC, และเปอร์เซ็นต์ความคืบหน้าในงานสรุปจะถูกคำนวณอีกครั้ง และสร้างการคาดการณ์ใหม่ของผลต่างความพยายาม</span><span class="sxs-lookup"><span data-stu-id="4eccb-130">The EAC, ETC, and progress percentage on the summary tasks are also recalculated, and produce a new projection of effort variance.</span></span>

## <a name="reprojection-of-effort-on-summary-tasks"></a><span data-ttu-id="4eccb-131">การประมาณการใหม่ของความพยายามในงานสรุป</span><span class="sxs-lookup"><span data-stu-id="4eccb-131">Reprojection of effort on summary tasks</span></span>

<span data-ttu-id="4eccb-132">กำลังคนในงานสรุป หรืองานคอนเทนเนอร์สามารถประมาณการได้อีกครั้ง</span><span class="sxs-lookup"><span data-stu-id="4eccb-132">Effort on summary tasks or container tasks can be reprojected.</span></span> <span data-ttu-id="4eccb-133">โดยไม่คำนึงถึงว่าผู้ใช้ประมาณการโครงการอีกครั้งโดยใช้กำลังคนที่เหลือ หรือเปอร์เซ็นต์ความคืบหน้าในงานสรุป ชุดของการคำนวณต่อไปนี้จะเริ่มต้น:</span><span class="sxs-lookup"><span data-stu-id="4eccb-133">Regardless of whether the user reprojects by using the remaining effort or the progress percentage on the summary tasks, the following set of calculations begins:</span></span>

- <span data-ttu-id="4eccb-134">EAC ETC และเปอร์เซ็นต์ความคืบหน้าของงานจะถูกคำนวณ</span><span class="sxs-lookup"><span data-stu-id="4eccb-134">The EAC, ETC, and progress percentage on the task are calculated.</span></span>
- <span data-ttu-id="4eccb-135">EAC ใหม่จะถูกกระจายลงไปยังงานย่อยในสัดส่วนเดียวกันกับ EAC เดิมที่อยู่ในงาน</span><span class="sxs-lookup"><span data-stu-id="4eccb-135">The new EAC is distributed down to the child tasks in the same proportion as the original EAC was on the task.</span></span>
- <span data-ttu-id="4eccb-136">EAC ใหม่ในแต่ละงานที่อยู่ในงานโหนดปลายสุดจะถูกคำนวณ</span><span class="sxs-lookup"><span data-stu-id="4eccb-136">The new EAC on each of the individual tasks down to the leaf node tasks is calculated.</span></span> 
- <span data-ttu-id="4eccb-137">งานย่อยที่ได้รับผลกระทบไปยังโหนดปลายสุดมีการคำนวณ ETC และเปอร์เซ็นต์ความคืบหน้าของพวกเขาใหม่ตามค่า EAC</span><span class="sxs-lookup"><span data-stu-id="4eccb-137">The affected child tasks down to the leaf nodes have their ETC and progress percentage recalculated based on the EAC value.</span></span> <span data-ttu-id="4eccb-138">ซึ่งส่งผลให้เกิดการคาดการณ์ใหม่สำหรับผลต่างกำลังคนของงาน</span><span class="sxs-lookup"><span data-stu-id="4eccb-138">This results in a new projection for the effort variance of the task.</span></span> 
- <span data-ttu-id="4eccb-139">EAC ของงานสรุปรวมถึงโหนดรากจะถูกคำนวณใหม่</span><span class="sxs-lookup"><span data-stu-id="4eccb-139">The EACs of the summary tasks all the way to the root node are recalculated.</span></span>

### <a name="cost-tracking-view"></a><span data-ttu-id="4eccb-140">มุมมองการติดตามต้นทุน</span><span class="sxs-lookup"><span data-stu-id="4eccb-140">Cost tracking view</span></span> 

<span data-ttu-id="4eccb-141">มุมมอง **การติดตามต้นทุน** จะเปรียบเทียบต้นทุนจริงที่ใช้ไปกับงานกับต้นทุนที่วางแผนไว้</span><span class="sxs-lookup"><span data-stu-id="4eccb-141">The **Cost tracking** view compares the actual cost that was spent on a task to the planned cost.</span></span> 

> [!NOTE]
> <span data-ttu-id="4eccb-142">มุมมองนี้แสดงเฉพาะต้นทุนแรงงาน และไม่รวมต้นทุนจากการประเมินค่าใช้จ่าย</span><span class="sxs-lookup"><span data-stu-id="4eccb-142">This view shows only labor costs and doesn’t include costs from the expense estimates.</span></span> 

<span data-ttu-id="4eccb-143">Project Service Automation ใช้สูตรต่อไปนี้เพื่อคำนวณเป้าหมายการติดตาม:</span><span class="sxs-lookup"><span data-stu-id="4eccb-143">Project Service Automation uses the following formulas to calculate the tracking metrics:</span></span>

<span data-ttu-id="4eccb-144">เมื่อสร้างงาน ต้นทุนที่วางแผนไว้จะเท่ากับต้นทุนโดยประมาณเมื่อเสร็จสมบูรณ์</span><span class="sxs-lookup"><span data-stu-id="4eccb-144">When a task is created, the planned cost is equal to the estimated cost at complete.</span></span> <span data-ttu-id="4eccb-145">หลังจากมีการบันทึกข้อมูลตามจริงในงาน รายการต่อไปนี้จะได้รับการคำนวณในมุมมอง **การติดตาม** สำหรับต้นทุน:</span><span class="sxs-lookup"><span data-stu-id="4eccb-145">After actuals are recorded on the task, the following is calculated on the **Tracking** view for cost:</span></span>

 - <span data-ttu-id="4eccb-146">เปอร์เซ็นต์ของต้นทุนที่ใช้ไป = ต้นทุนจริงที่ใช้ไปจนถึงปัจจุบัน ÷ ต้นทุนโดยประมาณเมื่อดำเนินงานเสร็จสมบูรณ์สำหรับงาน</span><span class="sxs-lookup"><span data-stu-id="4eccb-146">Percentage of cost consumed = Actual cost spent to date ÷ Estimated cost at complete for the task</span></span>
 - <span data-ttu-id="4eccb-147">ต้นทุนที่ต้องใช้จนเสร็จสมบูรณ์ (CTC) = ต้นทุนโดยประมาณเมื่อดำเนินงานเสร็จสมบูรณ์ – ต้นทุนจริงจนถึงปัจจุบัน</span><span class="sxs-lookup"><span data-stu-id="4eccb-147">Cost to complete (CTC) = Estimated cost at complete – Actual cost spent to date</span></span>
 - <span data-ttu-id="4eccb-148">ต้นทุนโดยประมาณเมื่อดำเนินงานเสร็จสมบูรณ = CTC + ต้นทุนจริงที่ใช้ไปจนถึงปัจจุบัน</span><span class="sxs-lookup"><span data-stu-id="4eccb-148">Estimated cost at complete = CTC + Actual cost spent to date</span></span>
 - <span data-ttu-id="4eccb-149">ผลต่างต้นทุนที่คาดการณ์ไว้ = ต้นทุนตามแผน - ต้นทุนโดยประมาณเมื่อดำเนินงานเสร็จสมบูรณ์</span><span class="sxs-lookup"><span data-stu-id="4eccb-149">Projected cost variance = Planned cost – Estimated cost at complete</span></span>

<span data-ttu-id="4eccb-150">การประมาณการของผลต่างต้นทุนแสดงอยู่ในงาน</span><span class="sxs-lookup"><span data-stu-id="4eccb-150">A projection of the cost variance is shown on the task.</span></span> <span data-ttu-id="4eccb-151">ถ้าต้นทุนโดยประมาณเมื่อดำเนินงานเสร็จสมบูรณ์มากกว่าต้นทุนที่วางแผนไว้ งานจะถูกคาดการณ์ให้ใช้ต้นทุนมากกว่าที่วางแผนไว้แต่เดิม</span><span class="sxs-lookup"><span data-stu-id="4eccb-151">If the estimated cost at complete is more than the planned cost, the task is projected to cost more than was originally planned.</span></span> <span data-ttu-id="4eccb-152">ดังนั้นจึงมีแนวโน้มที่จะเกินงบประมาณ</span><span class="sxs-lookup"><span data-stu-id="4eccb-152">Therefore, it's trending over budget.</span></span> <span data-ttu-id="4eccb-153">ถ้าต้นทุนโดยประมาณเมื่อดำเนินงานเสร็จสมบูรณ์น้อยกว่าต้นทุนที่วางแผนไว้ งานจะถูกคาดการณ์ให้ใช้ต้นทุนน้อยกว่าที่วางแผนไว้แต่เดิมและมีแนวโน้มที่จะอยู่ในงบประมาณ</span><span class="sxs-lookup"><span data-stu-id="4eccb-153">If the Estimated cost at complete is less than the planned cost, the task is projected to cost less than was originally planned and is trending under budget.</span></span>

## <a name="project-managers-reprojection-of-cost"></a><span data-ttu-id="4eccb-154">การประมาณการต้นทุนอีกครั้งของผู้จัดการโครงการ</span><span class="sxs-lookup"><span data-stu-id="4eccb-154">Project manager’s reprojection of cost</span></span>

<span data-ttu-id="4eccb-155">เมื่อกำลังคนถูกประมาณการใหม่ CTC, ต้นทุนโดยประมาณเมื่อดำเนินงานเสร็จสมบูรณ์ เปอร์เซ็นต์ของต้นทุนที่ใช้ และผลต่างต้นทุนที่คาดการณ์จะถูกคำนวณใหม่ทั้งหมดในมุมมอง **การติดตามต้นทุน**</span><span class="sxs-lookup"><span data-stu-id="4eccb-155">When effort is reprojected, the CTC, Estimated cost at complete, percentage of cost consumed, and projected cost variance are all recalculated in the **Cost tracking** view.</span></span>

## <a name="project-status-summary"></a><span data-ttu-id="4eccb-156">สรุปสถานะโครงการ</span><span class="sxs-lookup"><span data-stu-id="4eccb-156">Project status summary</span></span>

<span data-ttu-id="4eccb-157">การติดตามข้อมูลในมุมมอง **การติดตามกำลังคน** และ **การติดตามต้นทุน** แสดงความคืบหน้าและปริมาณการใช้ต้นทุนที่ระดับโหนดรากของโครงการ งานสรุป และงานโหนดปลายสุด</span><span class="sxs-lookup"><span data-stu-id="4eccb-157">Tracking data in the **Effort tracking** and **Cost tracking** views shows the progress and cost consumption at the project root node, summary tasks, and leaf node tasks levels.</span></span> <span data-ttu-id="4eccb-158">ส่วน **สถานะ** บนหน้า **เอนทิตีโครงการ** แสดงสรุปของสถานะระดับโครงการ</span><span class="sxs-lookup"><span data-stu-id="4eccb-158">The **Status** section on the **Project entity** page shows a summary of project-level status.</span></span>

## <a name="status-summary-fields"></a><span data-ttu-id="4eccb-159">ฟิลด์สรุปสถานะ</span><span class="sxs-lookup"><span data-stu-id="4eccb-159">Status summary fields</span></span>

<span data-ttu-id="4eccb-160">ฟิลด์ **สถานะโครงการโดยรวม** เป็นฟิลด์ที่สามารถแก้ไขได้ ซึ่งแสดงสถานะโดยรวมของโครงการ</span><span class="sxs-lookup"><span data-stu-id="4eccb-160">The **Overall project status** field is an editable field that shows the overall status of the project.</span></span> <span data-ttu-id="4eccb-161">ใช้การกำหนดรหัสแบบสี เช่น สีเขียว สีเหลือง และสีแดง เพื่อระบุความเสี่ยงที่เพิ่มขึ้น</span><span class="sxs-lookup"><span data-stu-id="4eccb-161">It uses color-coding, such as green, yellow, and red, to indicate increasing risk.</span></span> <span data-ttu-id="4eccb-162">ฟิลด์ **ข้อคิดเห็น** ช่วยให้ผู้จัดการโครงการป้อนข้อคิดเห็นเฉพาะเกี่ยวกับสถานะ</span><span class="sxs-lookup"><span data-stu-id="4eccb-162">The **Comments** field lets the project manager enter specific comments about the status.</span></span> <span data-ttu-id="4eccb-163">**สถานะที่ปรับปรุงบน** ฟิลด์ไม่สามารถแก้ไขได้ และค่าเป็นการประทับเวลาที่บ่งชี้ว่าสถานะถูกปรับปรุงครั้งล่าสุดเมื่อใด</span><span class="sxs-lookup"><span data-stu-id="4eccb-163">The **Status updated on** field is not editable and the value is a timestamp that indicates when the status was last updated.</span></span>

<span data-ttu-id="4eccb-164">ฟิลด์ **ประสิทธิภาพกำหนดการ** และ **ประสิทธิภาพต้นทุน** ถูกตั้งค่าจากวันที่ติดตาม</span><span class="sxs-lookup"><span data-stu-id="4eccb-164">The **Schedule performance** and **Cost performance** fields are set from the tracking date.</span></span> <span data-ttu-id="4eccb-165">เมื่อผลต่างหมายกำหนดการให้บริการและต้นทุนสำหรับโหนดรากในมุมมอง **การติดตามกำลังคน** เป็นค่าบวก คุณสามารถตั้งค่าฟิลด์เหล่านี้เป็น **ก่อนเวลา** ได้</span><span class="sxs-lookup"><span data-stu-id="4eccb-165">When the schedule and cost variance for the root node in the **Effort tracking** view are positive, you can set these fields to **Ahead**.</span></span> <span data-ttu-id="4eccb-166">เมื่อผลต่างหมายกำหนดการให้บริการและต้นทุนสำหรับโหนดรากเป็นค่าลบ คุณสามารถตั้งค่าให้เป็น **หลังกำหนด** ได้</span><span class="sxs-lookup"><span data-stu-id="4eccb-166">When the schedule and cost variance for the root node are negative, you can set them to **Behind**.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]