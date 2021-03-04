---
title: กลุ่มหน่วยนับและหน่วยนับ
description: หัวข้อนี้แสดงข้อมูลเกี่ยวกับกลุ่มของหน่วยนับและหน่วยนับ
author: rumant
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 03/05/2019
ms.topic: article
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: 6620c99563394d1f3881d6bfdb72d01c1c4e8d6f
ms.sourcegitcommit: 418fa1fe9d605b8faccc2d5dee1b04b4e753f194
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 02/10/2021
ms.locfileid: "5145606"
---
# <a name="unit-groups-and-units"></a><span data-ttu-id="87d95-103">กลุ่มหน่วยนับและหน่วยนับ</span><span class="sxs-lookup"><span data-stu-id="87d95-103">Unit groups and units</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

<span data-ttu-id="87d95-104">กลุ่มของหน่วยนับและหน่วยนับเป็นเอนทิตีพื้นฐานใน Microsoft Dynamics 365</span><span class="sxs-lookup"><span data-stu-id="87d95-104">Unit groups and units are basic entities in Microsoft Dynamics 365.</span></span> <span data-ttu-id="87d95-105">หน่วยเป็นหน่วยวัดเดียวและหลายหน่วยสามารถจัดกลุ่มเป็นกลุ่มหน่วยนับ</span><span class="sxs-lookup"><span data-stu-id="87d95-105">A unit is a single unit of measure, and multiple units can be grouped into unit groups.</span></span> <span data-ttu-id="87d95-106">บางครั้งกลุ่มหน่วยจะเรียกว่าเป็นกำหนดการหน่วยในส่วนติดต่อ (UI) ผู้ใช้ Dynamics 365</span><span class="sxs-lookup"><span data-stu-id="87d95-106">A unit group is sometimes referred to as a unit schedule in the Dynamics 365 user interface (UI).</span></span> 

<span data-ttu-id="87d95-107">ต่อไปนี้เป็นตัวอย่างของหน่วยนับและกลุ่มของหน่วยนับ:</span><span class="sxs-lookup"><span data-stu-id="87d95-107">Here are some examples of units and unit groups:</span></span>
 
- <span data-ttu-id="87d95-108">**กลุ่มของหน่วยนับ**: ระยะทาง</span><span class="sxs-lookup"><span data-stu-id="87d95-108">**Unit group**: Distance</span></span> 
    - <span data-ttu-id="87d95-109">**หน่วย**: ไมล์ กิโลเมตร และอื่นๆ</span><span class="sxs-lookup"><span data-stu-id="87d95-109">**Units**: Mile, Kilometer, and so on.</span></span>
- <span data-ttu-id="87d95-110">**กลุ่มของหน่วยนับ**: เวลา</span><span class="sxs-lookup"><span data-stu-id="87d95-110">**Unit group**: Time</span></span>
    - <span data-ttu-id="87d95-111">**หน่วย**: ชั่วโมง วัน สัปดาห์ และอื่นๆ</span><span class="sxs-lookup"><span data-stu-id="87d95-111">**Units**: Hour, day, week, and so on.</span></span> 

<span data-ttu-id="87d95-112">เมื่อคุณตั้งค่าหลายหน่วยในกลุ่มของหน่วยนับ คุณจะต้องตั้งค่าปัจจัยการแปลงระหว่างหน่วยโดยการกำหนดหน่วยแรกที่คุณตั้งค่าเป็นหน่วยเริ่มต้นหรือหน่วยหลักสำหรับกลุ่มของหน่วยนับ</span><span class="sxs-lookup"><span data-stu-id="87d95-112">When you set up multiple units in a unit group, you must also set up a conversion factor between them by designating the first unit that you set up as the default or primary unit for the unit group.</span></span> 

<span data-ttu-id="87d95-113">ตัวอย่างเช่น ในกลุ่มของหน่วยนับ **เวลา** ถ้าคุณตั้งค่า **ชั่วโมง** เป็นหน่วยแรก ระบบจะกำหนด **ชั่วโมง** เป็นหน่วยเริ่มต้น</span><span class="sxs-lookup"><span data-stu-id="87d95-113">For example, in a **Time** unit group, if you set up **Hour** as the first unit, the system designates **Hour** as the default unit.</span></span> <span data-ttu-id="87d95-114">ถ้าหน่วยถัดไปที่คุณตั้งค่าเป็น **วัน** คุณจะต้องตั้งค่าปัจจัยการแปลงสำหรับ **วัน** วัน เป็น **ชั่วโมง**</span><span class="sxs-lookup"><span data-stu-id="87d95-114">If the next unit that you set up is **Day**, you must set up a conversion factor for **Day** to **Hour**.</span></span> <span data-ttu-id="87d95-115">ถ้าคุณเพิ่ม **สัปดาห์** เป็นหน่วยที่สาม คุณต้องตั้งค่าปัจจัยการแปลงสำหรับ **สัปดาห์** เป็น **วัน** หรือ **ชั่วโมง**</span><span class="sxs-lookup"><span data-stu-id="87d95-115">If you then add **Week** as a third unit, you must set up a conversion factor for **Week** in terms of **Day** or **Hour**.</span></span> 

<span data-ttu-id="87d95-116">รูปภาพต่อไปนี้แสดงตัวอย่างการตั้งค่าสำหรับหน่วย **วัน** ที่ฟิลด์ **ปริมาณ** แสดงจำนวนชั่วโมงที่อยู่ในหนึ่งวัน และ **สัปดาห์** ที่ฟิลด์ **ปริมาณ** แสดงจำนวนวันที่อยู่ในหนึ่งสัปดาห์</span><span class="sxs-lookup"><span data-stu-id="87d95-116">The following image shows an example setup for the **Day** unit, where the **Quantity** field shows the number of hours that are in a day, and **Week**, where the **Quantity** field show the number of days that are in a week.</span></span>

> ![กลุ่มของหน่วยนับ: หน้าข้อมูล](media/advanced-2.png)

## <a name="using-units-and-unit-groups"></a><span data-ttu-id="87d95-118">การใช้หน่วยและกลุ่มของหน่วยนับ</span><span class="sxs-lookup"><span data-stu-id="87d95-118">Using units and unit groups</span></span>

<span data-ttu-id="87d95-119">Dynamics 365 Project Service Automation ใช้หน่วยและกลุ่มของหน่วยนับเพื่อประมวลผลการประเมินและรายการสำหรับทั้งค่าใช้จ่ายและเวลา</span><span class="sxs-lookup"><span data-stu-id="87d95-119">Dynamics 365 Project Service Automation uses units and unit groups to process estimates and entries for both expenses and time.</span></span> 

<span data-ttu-id="87d95-120">สำหรับค่าใช้จ่าย แต่ละประเภทค่าใช้จ่ายจะมีหน่วยและกลุ่มของหน่วยนับเริ่มต้น</span><span class="sxs-lookup"><span data-stu-id="87d95-120">For expenses, each expense category has a default unit group and unit.</span></span> <span data-ttu-id="87d95-121">ค่าเหล่านี้จะถูกป้อนเป็นค่าเริ่มต้นในรายการราคาตลาดสำหรับประเภทค่าใช้จ่าย</span><span class="sxs-lookup"><span data-stu-id="87d95-121">These values are entered as default values on price list entries for expense categories.</span></span> 

<span data-ttu-id="87d95-122">ตัวอย่างเช่น คุณมีประเภทค่าใช้จ่ายที่ชื่อ **ระยะทางเป็นไมล์**</span><span class="sxs-lookup"><span data-stu-id="87d95-122">For example, you have an expense category that is named **Mileage**.</span></span> <span data-ttu-id="87d95-123">มีกลุ่มของหน่วยนับที่มีชื่อว่า **ระยะทาง** และหน่วยเริ่มต้นที่มีชื่อว่า **ไมล์**</span><span class="sxs-lookup"><span data-stu-id="87d95-123">It has a unit group that is named **Distance** and a default unit that is named **Mile**.</span></span> <span data-ttu-id="87d95-124">ถ้าคุณตั้งค่ากลุ่มของหน่วยนับ **ระยะทาง** เพื่อให้มีสองหน่วย (**ไมล์** และ **กิโลเมตร**) คุณสามารถตั้งค่าสองราคาสำหรับประเภท **ระยะทางเป็นไมล์** ในราคาตลาดเดียว: ราคาต่อไมล์และราคาต่อกิโลเมตร</span><span class="sxs-lookup"><span data-stu-id="87d95-124">If you set up the **Distance** unit group so that it has two units (**Mile** and **Kilometer**), you can set two prices for the **Mileage** category on one price list: price per mile and price per kilometer.</span></span>

| <span data-ttu-id="87d95-125">ประเภทค่าใช้จ่าย</span><span class="sxs-lookup"><span data-stu-id="87d95-125">Expense category</span></span>  | <span data-ttu-id="87d95-126">กลุ่มของหน่วยนับ</span><span class="sxs-lookup"><span data-stu-id="87d95-126">Unit group</span></span>  | <span data-ttu-id="87d95-127">หน่วย</span><span class="sxs-lookup"><span data-stu-id="87d95-127">Unit</span></span>      | <span data-ttu-id="87d95-128">วิธีการตั้งราคา</span><span class="sxs-lookup"><span data-stu-id="87d95-128">Pricing method</span></span>  | <span data-ttu-id="87d95-129">ราคาต่อหน่วย</span><span class="sxs-lookup"><span data-stu-id="87d95-129">Price per unit</span></span>  |
|-------------------|---------------|-----------|-------------------|-------------------|
| <span data-ttu-id="87d95-130">ระยะทางเป็นไมล์</span><span class="sxs-lookup"><span data-stu-id="87d95-130">Mileage</span></span>           | <span data-ttu-id="87d95-131">ระยะทาง</span><span class="sxs-lookup"><span data-stu-id="87d95-131">Distance</span></span>      | <span data-ttu-id="87d95-132">ไมล์</span><span class="sxs-lookup"><span data-stu-id="87d95-132">Mile</span></span>      | <span data-ttu-id="87d95-133">ราคาต่อหน่วย</span><span class="sxs-lookup"><span data-stu-id="87d95-133">Price per unit</span></span>    | <span data-ttu-id="87d95-134">10 USD</span><span class="sxs-lookup"><span data-stu-id="87d95-134">10 USD</span></span>            |
| <span data-ttu-id="87d95-135">ระยะทางเป็นไมล์</span><span class="sxs-lookup"><span data-stu-id="87d95-135">Mileage</span></span>           | <span data-ttu-id="87d95-136">ระยะทาง</span><span class="sxs-lookup"><span data-stu-id="87d95-136">Distance</span></span>      | <span data-ttu-id="87d95-137">กิโลเมตร</span><span class="sxs-lookup"><span data-stu-id="87d95-137">Kilometer</span></span> | <span data-ttu-id="87d95-138">ราคาต่อหน่วย</span><span class="sxs-lookup"><span data-stu-id="87d95-138">Price per unit</span></span>    |  <span data-ttu-id="87d95-139">6 USD</span><span class="sxs-lookup"><span data-stu-id="87d95-139">6 USD</span></span>            |

<span data-ttu-id="87d95-140">เมื่อคุณป้อนค่าใช้จ่ายในโครงการ ระบบจะกำหนดราคาโดยใช้การรวมกันของประเภทและหน่วยในค่าใช้จ่าย</span><span class="sxs-lookup"><span data-stu-id="87d95-140">When you enter an expense on a project, the system determines the price through the combination of the category and the unit on the expense.</span></span> 

| <span data-ttu-id="87d95-141">คำอธิบายเกี่ยวกับค่าใช้จ่าย</span><span class="sxs-lookup"><span data-stu-id="87d95-141">Expense description</span></span>        | <span data-ttu-id="87d95-142">ประเภทค่าใช้จ่าย</span><span class="sxs-lookup"><span data-stu-id="87d95-142">Expense category</span></span>  | <span data-ttu-id="87d95-143">หน่วย</span><span class="sxs-lookup"><span data-stu-id="87d95-143">Unit</span></span>  | <span data-ttu-id="87d95-144">ปริมาณ</span><span class="sxs-lookup"><span data-stu-id="87d95-144">Quantity</span></span>  | <span data-ttu-id="87d95-145">ราคาต่อหน่วย</span><span class="sxs-lookup"><span data-stu-id="87d95-145">Unit price</span></span>   |
|----------------------------|---------------------|-------|-----------|----------------|
| <span data-ttu-id="87d95-146">ผลักดันไปยังตำแหน่งที่ตั้งของไคลเอ็นต์</span><span class="sxs-lookup"><span data-stu-id="87d95-146">Drive to client location</span></span> | <span data-ttu-id="87d95-147">ระยะทางเป็นไมล์</span><span class="sxs-lookup"><span data-stu-id="87d95-147">Mileage</span></span>             | <span data-ttu-id="87d95-148">ไมล์</span><span class="sxs-lookup"><span data-stu-id="87d95-148">Mile</span></span>  | <span data-ttu-id="87d95-149">10</span><span class="sxs-lookup"><span data-stu-id="87d95-149">10</span></span>        | <span data-ttu-id="87d95-150">10 USD</span><span class="sxs-lookup"><span data-stu-id="87d95-150">10 USD</span></span>         |

<span data-ttu-id="87d95-151">สำหรับเวลา แต่ละส่วนหัวของราคาตลาดจะมีฟิลด์ **หน่วยเวลาเริ่มต้น**</span><span class="sxs-lookup"><span data-stu-id="87d95-151">For time, each price list header has a **Default Time Unit** field.</span></span> <span data-ttu-id="87d95-152">จะมีการตั้งค่าเมื่อคุณสร้างส่วนหัวของราคาตลาด</span><span class="sxs-lookup"><span data-stu-id="87d95-152">The value is set when you create the price list header.</span></span> <span data-ttu-id="87d95-153">หน่วยนี้จะถูกใช้เพื่อตั้งค่าราคาตามบทบาททั้งหมดในราคาตลาดนั้น</span><span class="sxs-lookup"><span data-stu-id="87d95-153">This unit is then used to set all role-based prices on that price list.</span></span>

<span data-ttu-id="87d95-154">บรรทัดการประเมินสำหรับฟิลด์ **เวลาในใบเสนอราคา** สามารถแสดงในหน่วยเวลาใดๆ ก็ได้</span><span class="sxs-lookup"><span data-stu-id="87d95-154">Estimate lines for the **Time on Quote** field can be expressed in any unit of time.</span></span> <span data-ttu-id="87d95-155">อย่างไรก็ตามบรรทัดการประเมินในโครงการและรายการเวลาสำหรับโครงการสามารถใช้ได้แค่หน่วยของเวลา **ชั่วโมง** เท่านั้น</span><span class="sxs-lookup"><span data-stu-id="87d95-155">However, estimate lines on projects and time entries for projects can use only the **Hour** unit of time.</span></span> <span data-ttu-id="87d95-156">ถ้าหน่วยในรายการเวลาหรือบรรทัดการประเมินไม่ตรงกับหน่วยบนบรรทัดรายการราคาสำหรับบทบาทนั้นระบบจะแปลงราคาให้กับหน่วยที่กำหนดไว้ในการประเมินโครงการหรือธุรกรรมจริงของโครงการ</span><span class="sxs-lookup"><span data-stu-id="87d95-156">If the unit on the time entry or estimate line doesn't match the unit on the price list line for that role, the system converts the price to the units that are defined in the project estimate or the project actual transaction.</span></span>

<span data-ttu-id="87d95-157">ตัวอย่างต่อไปนี้แสดงให้เห็นว่า PSA ใช้กลุ่มของหน่วยนับ หน่วย และปัจจัยการแปลง</span><span class="sxs-lookup"><span data-stu-id="87d95-157">The following example shows how PSA uses the unit group, units, and conversion factors.</span></span>
- <span data-ttu-id="87d95-158">หน่วย</span><span class="sxs-lookup"><span data-stu-id="87d95-158">Units</span></span>

   - <span data-ttu-id="87d95-159">**กลุ่มของหน่วยนับ**: เวลา</span><span class="sxs-lookup"><span data-stu-id="87d95-159">**Unit group**: Time</span></span> 
   - <span data-ttu-id="87d95-160">**หน่วย**: ชั่วโมง</span><span class="sxs-lookup"><span data-stu-id="87d95-160">**Units**: Hour</span></span> 
    
    - <span data-ttu-id="87d95-161">**วัน** - ปัจจัยการแปลง: 8 ชั่วโมง</span><span class="sxs-lookup"><span data-stu-id="87d95-161">**Day** - Conversion factor: 8 hours</span></span>       
    - <span data-ttu-id="87d95-162">**สัปดาห์** - ปัจจัยการแปลง: 40 ชั่วโมง</span><span class="sxs-lookup"><span data-stu-id="87d95-162">**Week** - Conversion factor: 40 hours</span></span>  
        
- <span data-ttu-id="87d95-163">การตั้งค่าราคาตลาดในโครงการ A:</span><span class="sxs-lookup"><span data-stu-id="87d95-163">Price list setup on Project A:</span></span>

    - <span data-ttu-id="87d95-164">**ชื่อ**: ราคาขาย UK 2016</span><span class="sxs-lookup"><span data-stu-id="87d95-164">**Name**: UK sales prices 2016</span></span> 
    - <span data-ttu-id="87d95-165">**หน่วยเวลาเริ่มต้น**: วัน</span><span class="sxs-lookup"><span data-stu-id="87d95-165">**Default time unit**: Day</span></span> 
    - <span data-ttu-id="87d95-166">**สกุลเงิน**: GBP</span><span class="sxs-lookup"><span data-stu-id="87d95-166">**Currency**: GBP</span></span>

| <span data-ttu-id="87d95-167">บทบาท</span><span class="sxs-lookup"><span data-stu-id="87d95-167">Role</span></span>      | <span data-ttu-id="87d95-168">กลุ่มของหน่วยนับ</span><span class="sxs-lookup"><span data-stu-id="87d95-168">Unit group</span></span> | <span data-ttu-id="87d95-169">หน่วย</span><span class="sxs-lookup"><span data-stu-id="87d95-169">Unit</span></span> | <span data-ttu-id="87d95-170">หน่วยองค์กร</span><span class="sxs-lookup"><span data-stu-id="87d95-170">Organizational unit</span></span> | <span data-ttu-id="87d95-171">ราคา</span><span class="sxs-lookup"><span data-stu-id="87d95-171">Price</span></span>   |
|-----------|------------|------|---------------------|---------|
| <span data-ttu-id="87d95-172">นักพัฒนา</span><span class="sxs-lookup"><span data-stu-id="87d95-172">Developer</span></span> | <span data-ttu-id="87d95-173">Time</span><span class="sxs-lookup"><span data-stu-id="87d95-173">Time</span></span>       | <span data-ttu-id="87d95-174">Day</span><span class="sxs-lookup"><span data-stu-id="87d95-174">Day</span></span>  | <span data-ttu-id="87d95-175">Contoso UK</span><span class="sxs-lookup"><span data-stu-id="87d95-175">Contoso UK</span></span>          | <span data-ttu-id="87d95-176">800 GBP</span><span class="sxs-lookup"><span data-stu-id="87d95-176">800 GBP</span></span> |

### <a name="time-entry"></a><span data-ttu-id="87d95-177">รายการเวลา</span><span class="sxs-lookup"><span data-stu-id="87d95-177">Time entry</span></span>

<span data-ttu-id="87d95-178">ตารางต่อไปนี้แสดงธุรกรรมด้านการขายที่เป็นผลลัพธ์ซึ่งสร้างโดย PSA สำหรับโครงการสามชั่วโมง</span><span class="sxs-lookup"><span data-stu-id="87d95-178">The following table shows the resulting sales-side transaction created by PSA for a three hour project.</span></span>


| <span data-ttu-id="87d95-179">โครงการ</span><span class="sxs-lookup"><span data-stu-id="87d95-179">Project</span></span>   | <span data-ttu-id="87d95-180">งาน</span><span class="sxs-lookup"><span data-stu-id="87d95-180">Task</span></span>    | <span data-ttu-id="87d95-181">บทบาท</span><span class="sxs-lookup"><span data-stu-id="87d95-181">Role</span></span>      | <span data-ttu-id="87d95-182">ปริมาณ</span><span class="sxs-lookup"><span data-stu-id="87d95-182">Quantity</span></span> | <span data-ttu-id="87d95-183">หน่วย</span><span class="sxs-lookup"><span data-stu-id="87d95-183">Unit</span></span>  | <span data-ttu-id="87d95-184">ราคาต่อหน่วย</span><span class="sxs-lookup"><span data-stu-id="87d95-184">Unit price</span></span> | <span data-ttu-id="87d95-185">จำนวนเงินยอดขายที่ยังไม่ได้เรียกเก็บ</span><span class="sxs-lookup"><span data-stu-id="87d95-185">Unbilled sales amount</span></span> |
|-----------|---------|-----------|----------|-------|------------|-----------------------|
| <span data-ttu-id="87d95-186">Project A</span><span class="sxs-lookup"><span data-stu-id="87d95-186">Project A</span></span> | <span data-ttu-id="87d95-187">ออกแบบ</span><span class="sxs-lookup"><span data-stu-id="87d95-187">Design</span></span>  | <span data-ttu-id="87d95-188">นักพัฒนา</span><span class="sxs-lookup"><span data-stu-id="87d95-188">Developer</span></span> | <span data-ttu-id="87d95-189">3</span><span class="sxs-lookup"><span data-stu-id="87d95-189">3</span></span>        | <span data-ttu-id="87d95-190">Hour</span><span class="sxs-lookup"><span data-stu-id="87d95-190">Hour</span></span>  | <span data-ttu-id="87d95-191">100 GBP</span><span class="sxs-lookup"><span data-stu-id="87d95-191">100 GBP</span></span>    | <span data-ttu-id="87d95-192">300 GBP</span><span class="sxs-lookup"><span data-stu-id="87d95-192">300 GBP</span></span>               |

## <a name="time-unit-faq"></a><span data-ttu-id="87d95-193">คำถามที่ถามบ่อยของหน่วยเวลา</span><span class="sxs-lookup"><span data-stu-id="87d95-193">Time unit FAQ</span></span>

### <a name="does-psa-convert-to-different-units-in-the-case-of-expenses"></a><span data-ttu-id="87d95-194">PSA แปลงเป็นหน่วยที่แตกต่างกันในกรณีที่มีค่าใช้จ่ายหรือไม่?</span><span class="sxs-lookup"><span data-stu-id="87d95-194">Does PSA convert to different units in the case of expenses?</span></span>
<span data-ttu-id="87d95-195">ไม่</span><span class="sxs-lookup"><span data-stu-id="87d95-195">No.</span></span> <span data-ttu-id="87d95-196">การแปลงหน่วยจะทำงานสำหรับเวลาเท่านั้น</span><span class="sxs-lookup"><span data-stu-id="87d95-196">Unit conversion works only for time.</span></span> <span data-ttu-id="87d95-197">สำหรับค่าใช้จ่าย ถ้าระบบไม่พบราคาสำหรับการรวมของประเภทค่าใช้จ่ายและหน่วย ราคาจะถูกตั้งค่าเป็น 0.00 โดยค่าเริ่มต้น</span><span class="sxs-lookup"><span data-stu-id="87d95-197">For expenses, if the system can't find a price for the combination of the expense category and unit, the price is set to 0.00 by default.</span></span>

### <a name="why-does-psa-convert-time-units"></a><span data-ttu-id="87d95-198">ทำไม PSA ถึงแปลงหน่วยเวลา?</span><span class="sxs-lookup"><span data-stu-id="87d95-198">Why does PSA convert time units?</span></span>
<span data-ttu-id="87d95-199">ในบางประเทศหรือบางภูมิภาค มีข้อกำหนดทางกฎหมายที่มีการตั้งค่าอัตราเรียกเก็บเงินในหน่วยวัน</span><span class="sxs-lookup"><span data-stu-id="87d95-199">In some countries or regions, there is a legal requirement that bill rates be set up in days.</span></span> <span data-ttu-id="87d95-200">การเจรจาราคาและการให้ส่วนลดในระหว่างรอบใบเสนอราคาจะทำโดยใช้อัตราวันสำหรับแต่ละบทบาทที่เรียกเก็บเงินได้</span><span class="sxs-lookup"><span data-stu-id="87d95-200">Price negotiation and discounting during the quote cycle is done by using day rates for each billable role.</span></span> <span data-ttu-id="87d95-201">การประเมินกำหนดการและการป้อนข้อมูลเวลาจะทำในหน่วยชั่วโมง</span><span class="sxs-lookup"><span data-stu-id="87d95-201">Schedule estimation and time entry are done in hours.</span></span> <span data-ttu-id="87d95-202">ในการสนับสนุนความแตกต่างนี้ในหน่วยเวลา PSA จะแปลงหน่วยเวลา</span><span class="sxs-lookup"><span data-stu-id="87d95-202">To support this difference in time units, PSA converts time units.</span></span>

### <a name="can-time-units-be-changed-on-project-estimates"></a><span data-ttu-id="87d95-203">หน่วยเวลาสามารถเปลี่ยนไปในการประเมินโครงการได้หรือไม่?</span><span class="sxs-lookup"><span data-stu-id="87d95-203">Can time units be changed on project estimates?</span></span>
<span data-ttu-id="87d95-204">ไม่</span><span class="sxs-lookup"><span data-stu-id="87d95-204">No.</span></span> <span data-ttu-id="87d95-205">ขณะนี้การประเมินกำหนดการถูกจำกัดเป็นชั่วโมงและไม่สามารถเปลี่ยนแปลงได้</span><span class="sxs-lookup"><span data-stu-id="87d95-205">Schedule estimation is currently restricted to hours and can’t be changed.</span></span>

### <a name="can-units-and-unit-groups-be-edited-deleted-and-added"></a><span data-ttu-id="87d95-206">สามารถแก้ไข ลบ และเพิ่มหน่วยและกลุ่มของหน่วยได้หรือไม่?</span><span class="sxs-lookup"><span data-stu-id="87d95-206">Can units and unit groups be edited, deleted, and added?</span></span>
<span data-ttu-id="87d95-207">ได้</span><span class="sxs-lookup"><span data-stu-id="87d95-207">Yes.</span></span> <span data-ttu-id="87d95-208">ด้วยข้อยกเว้นของกลุ่มหน่วย **เวลา** และหน่วย **ชั่วโมง** หน่วยทั้งหมดสามารถถูกลบหรือแก้ไข และสามารถเพิ่มหน่วยใหม่ได้</span><span class="sxs-lookup"><span data-stu-id="87d95-208">With exception of the **Time** unit group and the **Hour** unit, all units can be deleted or edited, and new units can be added.</span></span> <span data-ttu-id="87d95-209">ใน PSA กลุ่มของหน่วย **เวลา** และหน่วย **ชั่วโมง** ไม่สามารถลบได้</span><span class="sxs-lookup"><span data-stu-id="87d95-209">In PSA, the **Time** unit group and the **Hour** unit can't be deleted.</span></span> <span data-ttu-id="87d95-210">อย่างไรก็ตามคุณสามารถปรับปรุงด้วยข้อความที่แปลสำหรับฟิลด์ **ชื่อ**</span><span class="sxs-lookup"><span data-stu-id="87d95-210">However, they can be updated with a translated text for the **Name** field.</span></span>
