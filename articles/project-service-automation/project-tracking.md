---
title: ความคืบหน้าและการใช้ต้นทุนของโครงการ
description: หัวข้อนี้แสดงข้อมูลเกี่ยวกับวิธีการติดตามความคืบหน้าของโครงการและปริมาณการใช้ต้นทุน
author: ruhercul
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom:
- dyn365-projectservice
ms.date: 03/01/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.assetid: 0d742164-5469-421d-8917-63160a81f651
ms.author: ruhercul
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
ms.openlocfilehash: 8aa5814938129f30885d8161a7c86197ab013364
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 03/24/2020
ms.locfileid: "3756484"
---
# <a name="project-progress-and-cost-consumption"></a><span data-ttu-id="72da9-103">ความคืบหน้าและการใช้ต้นทุนของโครงการ</span><span class="sxs-lookup"><span data-stu-id="72da9-103">Project progress and cost consumption</span></span>

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

<span data-ttu-id="72da9-104">ความจำเป็นในการติดตามความคืบหน้ากับกำหนดการแตกต่างกันไปตามอุตสาหกรรม</span><span class="sxs-lookup"><span data-stu-id="72da9-104">The need to track progress against a schedule varies by industry.</span></span> <span data-ttu-id="72da9-105">อุตสาหกรรมบางอย่างติดตามในระดับที่ละเอียด ในขณะที่อุตสาหกรรมอื่นๆ ติดตามในระดับที่สูงขึ้น</span><span class="sxs-lookup"><span data-stu-id="72da9-105">Some industries track at a granular level, whereas other industries track at a higher level.</span></span> <span data-ttu-id="72da9-106">หัวข้อนี้แสดงให้เห็นถึงวิธีการจัดกำหนดการเพื่อให้ตรงกับข้อกำหนดขององค์กรของคุณ</span><span class="sxs-lookup"><span data-stu-id="72da9-106">This topic shows how to schedule in order to meet your organization's requirements.</span></span>

## <a name="effort-tracking-view"></a><span data-ttu-id="72da9-107">มุมมองการติดตามความพยายามที่ใช้</span><span class="sxs-lookup"><span data-stu-id="72da9-107">Effort tracking view</span></span>

<span data-ttu-id="72da9-108">มุมมอง **การติดตามความพยายามที่ใช้** ติดตามความคืบหน้าของงานในกำหนดการ</span><span class="sxs-lookup"><span data-stu-id="72da9-108">The **Effort tracking** view tracks the progress of tasks in the schedule.</span></span> <span data-ttu-id="72da9-109">ซึ่งจะเปรียบเทียบจำนวนชั่วโมงของความพยายามจริงที่ใช้กับงานกับจำนวนชั่วโมงของความพยายามที่วางแผนไว้ที่จะใช้ไปกับงาน</span><span class="sxs-lookup"><span data-stu-id="72da9-109">It compares the actual effort hours that have been spent on a task to the planned effort hours for that task.</span></span> <span data-ttu-id="72da9-110">PSA จะใช้สูตรต่อไปนี้เพื่อคำนวณเป้าหมายการติดตาม:</span><span class="sxs-lookup"><span data-stu-id="72da9-110">PSA uses the following formulas to calculate the tracking metrics:</span></span>

- <span data-ttu-id="72da9-111">เปอร์เซ็นต์ความคืบหน้า = ความพยายามจริงที่ใช้จนถึงปัจจุบัน ÷ ความพยายามที่วางแผนไว้สำหรับงาน</span><span class="sxs-lookup"><span data-stu-id="72da9-111">Progress percentage = Actual effort spent to date ÷ Planned effort for the task</span></span> 
- <span data-ttu-id="72da9-112">การประมาณการที่ต้องใช้เพื่อดำเนินงานให้เสร็จสมบูรณ์ (ETC) = ความพยายามที่วางแผนไว้ – ความพยายามที่แท้จริงจนถึงปัจจุบัน</span><span class="sxs-lookup"><span data-stu-id="72da9-112">Estimate to complete (ETC) = Planned effort – Actual effort spent to date</span></span> 
- <span data-ttu-id="72da9-113">การประมาณการที่ใช้เมื่อดำเนินงานเสร็จสมบูรณ์ (EAC) = ความพยายามที่เหลือ + ความพยายามที่แท้จริงจนถึงปัจจุบัน</span><span class="sxs-lookup"><span data-stu-id="72da9-113">Estimate at complete (EAC) = Remaining effort + Actual effort spent to date</span></span> 
- <span data-ttu-id="72da9-114">ผลต่างความพยายามที่คาดการณ์ = ความพยายามที่วางแผนไว้ – EAC</span><span class="sxs-lookup"><span data-stu-id="72da9-114">Projected effort variance = Planned effort – EAC</span></span>

<span data-ttu-id="72da9-115">PSA แสดงการประมาณการของผลต่างความพยายามในงาน</span><span class="sxs-lookup"><span data-stu-id="72da9-115">PSA shows a projection of the effort variance on the task.</span></span> <span data-ttu-id="72da9-116">ถ้า EAC มากกว่าความพยายามที่วางแผนไว้ งานจะถูกคาดการณ์ให้ใช้เวลามากกว่าที่วางแผนไว้แต่เดิม</span><span class="sxs-lookup"><span data-stu-id="72da9-116">If the EAC is more than the planned effort, the task is projected to take more time than was originally planned.</span></span> <span data-ttu-id="72da9-117">ดังนั้น จึงล่าช้ากว่ากำหนดเวลา</span><span class="sxs-lookup"><span data-stu-id="72da9-117">Therefore, it's behind schedule.</span></span> <span data-ttu-id="72da9-118">ถ้า EAC น้อยกว่าความพยายามที่วางแผนไว้ งานจะถูกคาดการณ์ให้ใช้เวลาน้อยกว่าที่วางแผนไว้แต่เดิม</span><span class="sxs-lookup"><span data-stu-id="72da9-118">If the EAC is less than the planned effort, the task is projected to take less time than was originally planned.</span></span> <span data-ttu-id="72da9-119">ดังนั้น จึงก่อนกำหนดการ</span><span class="sxs-lookup"><span data-stu-id="72da9-119">Therefore, it's ahead of schedule.</span></span>

## <a name="re-projecting-effort"></a><span data-ttu-id="72da9-120">ความพยายามในการประมาณการใหม่</span><span class="sxs-lookup"><span data-stu-id="72da9-120">Re-projecting effort</span></span>

<span data-ttu-id="72da9-121">เป็นปกติสำหรับผู้จัดการโครงการที่จะแก้ไขการประมาณการเดิมของงาน</span><span class="sxs-lookup"><span data-stu-id="72da9-121">It's common for a project manager to revise the original estimates on a task.</span></span> <span data-ttu-id="72da9-122">การประมาณการโครงการใหม่เป็นการรับรู้ของผู้จัดการโครงการของการประมาณการ ที่กำหนดสถานะปัจจุบันของโครงการ</span><span class="sxs-lookup"><span data-stu-id="72da9-122">Project re-projections are a project manager's perception of estimates, given the current state of a project.</span></span> <span data-ttu-id="72da9-123">อย่างไรก็ตาม เราไม่แนะนำให้ผู้จัดการโครงการเปลี่ยนเลขเส้นฐาน เนื่องจากเส้นฐานของโครงการแสดงแหล่งที่มาของความจริงที่เชื่อมต่อ สำหรับหมายกำหนดการให้บริการรและการปประมาณการต้นทุนของโครงการ และผู้เกี่ยวข้องทั้งหมดในโครงการได้ตกลงกันแล้ว</span><span class="sxs-lookup"><span data-stu-id="72da9-123">However, we don't recommend that project managers change the baseline numbers, because the project baseline represents the established source of truth for the project's schedule and cost estimate, and all project stakeholders have agreed to it.</span></span>

<span data-ttu-id="72da9-124">มีสองวิธีที่ผู้จัดการโครงการสามารถประมาณการโครงการความพยายามในการทำงานใหม่:</span><span class="sxs-lookup"><span data-stu-id="72da9-124">There are two ways that a project manager can re-project effort on tasks:</span></span>

- <span data-ttu-id="72da9-125">แทนที่ ETC ค่าเริ่มต้นด้วยการประมาณการใหม่ของความพยายามที่เหลือจริงในงาน</span><span class="sxs-lookup"><span data-stu-id="72da9-125">Override the default ETC with a new estimate of the actual remaining effort on the task.</span></span> 
- <span data-ttu-id="72da9-126">แทนที่เปอร์เซ็นต์ความคืบหน้าค่าเริ่มต้นด้วยการประมาณการใหม่ของความคืบหน้าจริงในงาน</span><span class="sxs-lookup"><span data-stu-id="72da9-126">Override the default progress percentage with a new estimate of the true progress on the task.</span></span>

<span data-ttu-id="72da9-127">แต่ละวิธีเหล่านี้ทำให้เกิดการคำนวณใหม่ของ ETC EAC ของงาน และเปอร์เซ็นต์ความคืบหน้า และผลต่างความพยายามที่คาดการณ์ไว้ในงาน</span><span class="sxs-lookup"><span data-stu-id="72da9-127">Each of these approaches cause a recalculation of the task's ETC, EAC, and progress percentage, and the projected effort variance on a task.</span></span> <span data-ttu-id="72da9-128">EAC ETC, และเปอร์เซ็นต์ความคืบหน้าในงานสรุปจะถูกคำนวณอีกครั้ง และสร้างการคาดการณ์ใหม่ของผลต่างความพยายาม</span><span class="sxs-lookup"><span data-stu-id="72da9-128">The EAC, ETC, and progress percentage on the summary tasks are also recalculated, and produce a new projection of effort variance.</span></span>

## <a name="re-projection-of-effort-on-summary-tasks"></a><span data-ttu-id="72da9-129">การประมาณการใหม่ของความพยายามในงานสรุป</span><span class="sxs-lookup"><span data-stu-id="72da9-129">Re-projection of effort on summary tasks</span></span>

<span data-ttu-id="72da9-130">ความพยายามในงานสรุป หรืองานคอนเทนเนอร์สามารถประมาณการได้อีกครั้ง</span><span class="sxs-lookup"><span data-stu-id="72da9-130">Effort on summary tasks or container tasks can be re-projected.</span></span> <span data-ttu-id="72da9-131">โดยไม่คำนึงถึงว่าผู้ใช้ประมาณการโครงการอีกครั้งโดยใช้ความพยายามที่เหลือ หรือเปอร์เซ็นต์ความคืบหน้าในงานสรุป ชุดของการคำนวณต่อไปนี้จะเริ่มต้น:</span><span class="sxs-lookup"><span data-stu-id="72da9-131">Regardless of whether the user re-projects by using the remaining effort or the progress percentage on the summary tasks, the following set of calculations begins:</span></span>

- <span data-ttu-id="72da9-132">EAC ETC และเปอร์เซ็นต์ความคืบหน้าของงานจะถูกคำนวณ</span><span class="sxs-lookup"><span data-stu-id="72da9-132">The EAC, ETC, and progress percentage on the task are calculated.</span></span>
- <span data-ttu-id="72da9-133">EAC ใหม่จะถูกกระจายลงไปยังงานย่อยในสัดส่วนเดียวกันกับ EAC เดิมที่อยู่ในงาน</span><span class="sxs-lookup"><span data-stu-id="72da9-133">The new EAC is distributed down to the child tasks in the same proportion as the original EAC was on the task.</span></span>
- <span data-ttu-id="72da9-134">EAC ใหม่ในแต่ละงานที่อยู่ในงานโหนดปลายสุดจะถูกคำนวณ</span><span class="sxs-lookup"><span data-stu-id="72da9-134">The new EAC on each of the individualt tasks down to the leaf node tasks is calculated.</span></span> 
- <span data-ttu-id="72da9-135">งานย่อยที่ได้รับผลกระทบไปยังโหนดปลายสุดมีการคำนวณ ETC และเปอร์เซ็นต์ความคืบหน้าของพวกเขาใหม่ตามค่า EAC</span><span class="sxs-lookup"><span data-stu-id="72da9-135">The affected child tasks down to the leaf nodes have their ETC and progress percentage recalculated based on the EAC value.</span></span> <span data-ttu-id="72da9-136">ซึ่งส่งผลให้เกิดการคาดการณ์ใหม่สำหรับผลต่างความพยายามของงาน</span><span class="sxs-lookup"><span data-stu-id="72da9-136">This results in a new projection for the effort variance of the task.</span></span> 
- <span data-ttu-id="72da9-137">EAC ของงานสรุปรวมถึงโหนดรากจะถูกคำนวณใหม่</span><span class="sxs-lookup"><span data-stu-id="72da9-137">The EACs of the summary tasks all the way to the root node are recalculated.</span></span>

### <a name="cost-tracking-view"></a><span data-ttu-id="72da9-138">มุมมองการติดตามต้นทุน</span><span class="sxs-lookup"><span data-stu-id="72da9-138">Cost tracking view</span></span> 

<span data-ttu-id="72da9-139">มุมมอง **การติดตามต้นทุน** จะเปรียบเทียบต้นทุนจริงที่ใช้ไปกับงานกับต้นทุนที่วางแผนไว้ของงาน</span><span class="sxs-lookup"><span data-stu-id="72da9-139">The **Cost tracking** view compares the actual cost that was spent on a task to the planned cost on a task.</span></span> 

> [!NOTE]
> <span data-ttu-id="72da9-140">มุมมองนี้แสดงเฉพาะต้นทุนแรงงาน และไม่รวมต้นทุนจากการประเมินค่าใช้จ่าย</span><span class="sxs-lookup"><span data-stu-id="72da9-140">This view shows only labor costs and doesn’t include costs from the expense estimates.</span></span> 

<span data-ttu-id="72da9-141">PSA จะใช้สูตรต่อไปนี้เพื่อคำนวณเป้าหมายการติดตาม:</span><span class="sxs-lookup"><span data-stu-id="72da9-141">PSA uses the following formulas to calculate the tracking metrics:</span></span>

- <span data-ttu-id="72da9-142">เปอร์เซ็นต์ของต้นทุนที่ใช้ไป = ต้นทุนจริงที่ใช้ไปจนถึงปัจจุบัน ÷ ต้นทุนที่วางแผนไว้สำหรับงาน</span><span class="sxs-lookup"><span data-stu-id="72da9-142">Percentage of cost consumed = Actual cost spent to date ÷ Planned cost for the task</span></span>
- <span data-ttu-id="72da9-143">ต้นทุนที่ต้องใช้ดำเนินงานให้เสร็จสมบูรณ์ (CTC) = ต้นทุนที่วางแผนไว้ – ต้นทุนที่แท้จริงจนถึงปัจจุบัน</span><span class="sxs-lookup"><span data-stu-id="72da9-143">Cost to complete (CTC) = Planned cost – Actual cost spent to date</span></span>
- <span data-ttu-id="72da9-144">EAC = CTC + ต้นทุนจริงที่ใช้จ่ายถึงปัจจุบัน</span><span class="sxs-lookup"><span data-stu-id="72da9-144">EAC = CTC + Actual cost spent to date</span></span>
- <span data-ttu-id="72da9-145">ผลต่างต้นทุนที่คาดการณ์ = ต้นทุนที่วางแผนไว้ – EAC</span><span class="sxs-lookup"><span data-stu-id="72da9-145">Projected cost variance = Planned cost – EAC</span></span>

<span data-ttu-id="72da9-146">การประมาณการของผลต่างต้นทุนแสดงอยู่ในงาน</span><span class="sxs-lookup"><span data-stu-id="72da9-146">A projection of the cost variance is shown on the task.</span></span> <span data-ttu-id="72da9-147">ถ้า EAC มากกว่าต้นทุนที่วางแผนไว้ งานจะถูกคาดการณ์ให้ใช้ต้นทุนมากกว่าที่วางแผนไว้แต่เดิม</span><span class="sxs-lookup"><span data-stu-id="72da9-147">If the EAC is more than the planned cost, the task is projected to cost more than was originally planned.</span></span> <span data-ttu-id="72da9-148">ดังนั้นจึงมีแนวโน้มที่จะเกินงบประมาณ</span><span class="sxs-lookup"><span data-stu-id="72da9-148">Therefore, it's trending over budget.</span></span> <span data-ttu-id="72da9-149">ถ้า EAC น้อยกว่าต้นทุนที่วางแผนไว้ งานจะถูกคาดการณ์ให้ใช้ต้นทุนน้อยกว่าที่วางแผนไว้แต่เดิม</span><span class="sxs-lookup"><span data-stu-id="72da9-149">If the EAC is less than the planned cost, the task is projected to cost less than was originally planned.</span></span> <span data-ttu-id="72da9-150">ดังนั้นจึงมีแนวโน้มที่จะต่ำกว่างบประมาณ</span><span class="sxs-lookup"><span data-stu-id="72da9-150">Therefore, it's trending under budget.</span></span>

## <a name="project-managers-re-projection-of-cost"></a><span data-ttu-id="72da9-151">การประมาณการต้นทุนอีกครั้งของผู้จัดการโครงการ</span><span class="sxs-lookup"><span data-stu-id="72da9-151">Project manager’s re-projection of cost</span></span>

<span data-ttu-id="72da9-152">เมื่อความพยายามถูกประมาณการใหม่ CTC EAC เปอร์เซ็นต์ของต้นทุนที่ใช้ และผลต่างต้นทุนที่คาดการณ์จะถูกคำนวณใหม่ทั้งหมดในมุมมอง **การติดตามต้นทุน**</span><span class="sxs-lookup"><span data-stu-id="72da9-152">When effort is re-projected, the CTC, EAC, percentage of cost consumed, and projected cost variance are all recalculated in the **Cost tracking** view.</span></span>

## <a name="project-status-summary"></a><span data-ttu-id="72da9-153">สรุปสถานะโครงการ</span><span class="sxs-lookup"><span data-stu-id="72da9-153">Project status summary</span></span>

<span data-ttu-id="72da9-154">การติดตามข้อมูลในมุมมอง **การติดตามความพยายาม** และ **การติดตามต้นทุน** แสดงความคืบหน้าและปริมาณการใช้ต้นทุนที่ระดับโหนดรากของโครงการ งานสรุป และงานโหนดปลายสุด</span><span class="sxs-lookup"><span data-stu-id="72da9-154">Tracking data in the **Effort tracking** and **Cost tracking** views shows the progress and cost consumption at the project root node, summary tasks, and leaf node tasks levels.</span></span> <span data-ttu-id="72da9-155">ส่วน **สถานะ** บนหน้า **เอนทิตีโครงการ** แสดงสรุปของสถานะระดับโครงการ</span><span class="sxs-lookup"><span data-stu-id="72da9-155">The **Status** section on the **Project entity** page shows a summary of project-level status.</span></span>

## <a name="status-summary-fields"></a><span data-ttu-id="72da9-156">ฟิลด์สรุปสถานะ</span><span class="sxs-lookup"><span data-stu-id="72da9-156">Status summary fields</span></span>

<span data-ttu-id="72da9-157">ฟิลด์ **สถานะโครงการโดยรวม** เป็นฟิลด์ที่สามารถแก้ไขได้ ซึ่งแสดงสถานะโดยรวมของโครงการ</span><span class="sxs-lookup"><span data-stu-id="72da9-157">The **Overall project status** field is an editable field that shows the overall status of the project.</span></span> <span data-ttu-id="72da9-158">ใช้การกำหนดรหัสแบบสี เช่น สีเขียว สีเหลือง และสีแดง เพื่อระบุความเสี่ยงที่เพิ่มขึ้น</span><span class="sxs-lookup"><span data-stu-id="72da9-158">It uses color-coding, such as green, yellow, and red, to indicate increasing risk.</span></span> <span data-ttu-id="72da9-159">ฟิลด์ **ข้อคิดเห็น** ช่วยให้ผู้จัดการโครงการป้อนข้อคิดเห็นเฉพาะเกี่ยวกับสถานะ</span><span class="sxs-lookup"><span data-stu-id="72da9-159">The **Comments** field lets the project manager enter specific comments about the status.</span></span> <span data-ttu-id="72da9-160">**สถานะที่ปรับปรุงบน** ฟิลด์ไม่สามารถแก้ไขได้ และค่าเป็นการประทับเวลาที่บ่งชี้ว่าสถานะถูกปรับปรุงครั้งล่าสุดเมื่อใด</span><span class="sxs-lookup"><span data-stu-id="72da9-160">The **Status updated on** field is not editable and the value is a timestamp that indicates when the status was last updated.</span></span>

<span data-ttu-id="72da9-161">ฟิลด์ **ประสิทธิภาพกำหนดการ** และ **ประสิทธิภาพต้นทุน** ถูกตั้งค่าจากวันที่ติดตาม</span><span class="sxs-lookup"><span data-stu-id="72da9-161">The **Schedule performance** and **Cost performance** fields are set from the tracking date.</span></span> <span data-ttu-id="72da9-162">เมื่อผลต่างหมายกำหนดการให้บริการและต้นทุนสำหรับโหนดรากในมุมมอง **การติดตามความพยายาม** เป็นค่าบวก คุณสามารถตั้งค่าฟิลด์เหล่านี้เป็น **ก่อนเวลา** ได้</span><span class="sxs-lookup"><span data-stu-id="72da9-162">When the schedule and cost variance for the root node in the **Effort tracking** view are positive, you can set these fields to **Ahead**.</span></span> <span data-ttu-id="72da9-163">เมื่อผลต่างหมายกำหนดการให้บริการและต้นทุนสำหรับโหนดรากเป็นค่าลบ คุณสามารถตั้งค่าให้เป็น **หลังกำหนด** ได้</span><span class="sxs-lookup"><span data-stu-id="72da9-163">When the schedule and cost variance for the root node are negative, you can set them to **Behind**.</span></span>
