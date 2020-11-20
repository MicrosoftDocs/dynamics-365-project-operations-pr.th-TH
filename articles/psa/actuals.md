---
title: ภาพรวมข้อมูลจริง
description: หัวข้อนี้แสดงข้อมูลเกี่ยวกับค่าจริงของโครงการ
author: rumant
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 08/03/2020
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
ms.openlocfilehash: cf9e36c99790b77f0ed6490f49b4ebeb043bcdf6
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 10/28/2020
ms.locfileid: "4129791"
---
# <a name="actuals-overview"></a><span data-ttu-id="98abf-103">ภาพรวมข้อมูลจริง</span><span class="sxs-lookup"><span data-stu-id="98abf-103">Actuals overview</span></span>

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

<span data-ttu-id="98abf-104">ค่าจริง คือจำนวนของงานที่เสร็จสมบูรณ์แล้วในโครงการ</span><span class="sxs-lookup"><span data-stu-id="98abf-104">Actuals are the amount of work that has been completed on a project.</span></span> <span data-ttu-id="98abf-105">ค่าจริงของโครงการสามารถสืบย้อนกลับไปยังเอกสารต้นทางของพวกเขา</span><span class="sxs-lookup"><span data-stu-id="98abf-105">Project actuals can be traced back to their source documents.</span></span> <span data-ttu-id="98abf-106">เอกสารต้นทางเหล่านั้น รวมถึงเวลา ค่าใช้จ่าย และรายการสมุดรายวัน และใบแจ้งหนี้ิ่ด้วย</span><span class="sxs-lookup"><span data-stu-id="98abf-106">Those source documents include time, expense, and journal entries, and also invoices.</span></span>

![วิธีการติดตามค่าจริงของโครงการไปยังเอกสารต้นทาง](media/basic-guide-18.png)

## <a name="submitting-a-time-entry"></a><span data-ttu-id="98abf-108">ส่งรายการเวลา</span><span class="sxs-lookup"><span data-stu-id="98abf-108">Submitting a time entry</span></span>

<span data-ttu-id="98abf-109">ใน PSA เมื่อรายการเวลาถูกส่งสำหรับโครงการที่ถูกแม็ปกับรายละเอียดการให้บริการตามสัญญาในเวลาและวัสดุ จะมีการสร้างบรรทัดสมุดรายวันสองรายการ</span><span class="sxs-lookup"><span data-stu-id="98abf-109">In PSA, when a time entry is submitted for a project that is mapped to a time-and-materials contract line, two journal lines are created.</span></span> <span data-ttu-id="98abf-110">หนึ่งบรรทัดสำหรับต้นทุน และอีกบรรทัดสำหรับการขายที่ยังไม่ได้เรียกเก็บเงิน</span><span class="sxs-lookup"><span data-stu-id="98abf-110">One line is for cost, and the other line is for unbilled sales.</span></span> <span data-ttu-id="98abf-111">เมื่อรายการเวลาถูกส่งสำหรับโครงการที่ถูกแม็ปกับรายละเอียดการให้บริการตามสัญญาที่มีเวลาคงที่ จะมีการสร้างบรรทัดสมุดรายวันสำหรับต้นทุนบรรทัดเดียว</span><span class="sxs-lookup"><span data-stu-id="98abf-111">When a time entry is submitted for a project that is mapped to a fixed-price contract line, a journal line is created only for cost.</span></span> 

<span data-ttu-id="98abf-112">ตรรกะสำหรับการป้อนราคาเริ่มต้นอยู่บนบรรทัดสมุดรายวัน</span><span class="sxs-lookup"><span data-stu-id="98abf-112">Logic for entering default prices resides on the journal line.</span></span> <span data-ttu-id="98abf-113">ค่าฟิลด์ทั้งหมดจากรายการเวลาจะถูกคัดลอกไปยังบรรทัดสมุดรายวัน</span><span class="sxs-lookup"><span data-stu-id="98abf-113">All the field values from a time entry are copied to the journal line.</span></span> <span data-ttu-id="98abf-114">ฟิลด์เหล่านี้รวมถึงวันที่ของธุรกรรม รายละเอียดการให้บริการตามสัญญาที่โครงการถูกแม็ปด้วย และสกุลเงินที่เป็นผลในราคาตลาดที่เหมาะสม</span><span class="sxs-lookup"><span data-stu-id="98abf-114">These fields include the date of the transaction, the contract line that the project is mapped to, and the currency result in the appropriate price list.</span></span> 

<span data-ttu-id="98abf-115">ฟิลด์ที่มีผลต่อราคาเริ่มต้น เช่น **บทบาท** และ **หน่วยองค์กร** ทำให้เกิดราคาที่เหมาะสมที่จะป้อนโดยค่าเริ่มต้นบนบรรทัดสมุดรายวัน</span><span class="sxs-lookup"><span data-stu-id="98abf-115">The fields that affect default prices, such as **Role** and **Org Unit**, cause an appropriate price to be entered by default on the journal line.</span></span> <span data-ttu-id="98abf-116">หากคุณเพิ่มฟิลด์แบบกำหนดเองในรายการเวลา และคุณต้องการให้ค่าของฟิลด์ถูกเผยแพร่ไปยังที่เกิดขึ้นจริง ให้สร้างฟิลด์บนเอนทิตีที่เกิดขึ้นจริง และใช้การแม็ปฟิลด์เพื่อคัดลอกฟิลด์จากรายการเวลาไปยังที่เกิดขึ้นจริง</span><span class="sxs-lookup"><span data-stu-id="98abf-116">If you add a custom field on the time entry, and you want the field value to be propagated to actuals, create the field on the Actuals entity, and use field mappings to copy the field from the time entry to the actual.</span></span>

## <a name="submitting-an-expense-entry"></a><span data-ttu-id="98abf-117">การส่งรายการค่าใช้จ่าย</span><span class="sxs-lookup"><span data-stu-id="98abf-117">Submitting an expense entry</span></span>

<span data-ttu-id="98abf-118">ใน PSA เมื่อรายการค่าใช้จ่ายถูกส่งสำหรับโครงการที่ถูกแม็ปกับรายละเอียดการให้บริการตามสัญญาในเวลาและวัสดุ จะมีการสร้างบรรทัดสมุดรายวันสองบรรทัด</span><span class="sxs-lookup"><span data-stu-id="98abf-118">In PSA, when an expense entry is submitted for a project that is mapped to a time-and-materials contract line, two journal lines are created.</span></span> <span data-ttu-id="98abf-119">หนึ่งบรรทัดสำหรับต้นทุน และอีกบรรทัดสำหรับการขายที่ยังไม่ได้เรียกเก็บเงิน</span><span class="sxs-lookup"><span data-stu-id="98abf-119">One line is for cost, and the other line is for unbilled sales.</span></span> <span data-ttu-id="98abf-120">เมื่อรายการค่าใช้จ่ายถูกส่งสำหรับโครงการที่ถูกแม็ปกับรายละเอียดการให้บริการตามสัญญาที่มีราคาคงที่ จะมีการสร้างบรรทัดสมุดรายวันสำหรับต้นทุนบรรทัดเดียว</span><span class="sxs-lookup"><span data-stu-id="98abf-120">When an expense entry is submitted for a project that is mapped to a fixed-price contract line, a journal line is created only for cost.</span></span>

<span data-ttu-id="98abf-121">ตรรกะสำหรับการป้อนราคาเริ่มต้นสำหรับค่าใช้จ่าย จะขึ้นอยู่กับประเภทของค่าใช้จ่ายที่ถูกเลือก บนหน้า **รายการค่าใช้จ่าย**</span><span class="sxs-lookup"><span data-stu-id="98abf-121">Logic for entering default prices for expenses is based on the expense category that is selected on the **Expense entry** page.</span></span> <span data-ttu-id="98abf-122">วันที่ของธุรกรรม รายละเอียดการให้บริการตามสัญญาที่โครงการถูกแม็ปด้วย และสกุลเงิน จะถูกใช้เพื่อระบุราคาตลาดที่เหมาะสม</span><span class="sxs-lookup"><span data-stu-id="98abf-122">The transaction date, the contract line that the project is mapped to, and the currency are all used to determine the appropriate price list.</span></span> <span data-ttu-id="98abf-123">อย่างไรก็ตาม สำหรับราคาตัวเอง ยอดเงินป้อนโดยผู้ใช้จะถูกตั้งค่าโดยตรงบนบรรทัดสมุดรายวันค่าใช้จ่ายที่เกี่ยวข้อง สำหรับต้นทุนและยอดขายโดยค่าเริ่มต้น</span><span class="sxs-lookup"><span data-stu-id="98abf-123">However, for the price itself, the amount that the user entered is set directly on the related expense journal lines for cost and sales by default.</span></span>

<span data-ttu-id="98abf-124">ในเวอร์ชันปัจจุบันของ PSA รายการตามประเภทของราคาเริ่มต้นต่อหน่วย ในรายการค่าใช้จ่าย ยังไม่พร้อมใช้งาน</span><span class="sxs-lookup"><span data-stu-id="98abf-124">In the current version of PSA, category-based entry of per-unit default prices on expense entries isn't available.</span></span>

## <a name="using-entry-journals-to-record-costs"></a><span data-ttu-id="98abf-125">การใช้สมุดบันทึกรายการเพื่อบันทึกต้นทุน</span><span class="sxs-lookup"><span data-stu-id="98abf-125">Using Entry journals to record costs</span></span>

<span data-ttu-id="98abf-126">ใน PSA สมุดบันทึกรายการช่วยให้คุณสามารถบันทึกต้นทุนหรือรายได้ ในคลาสวัสดุ ค่าธรรมเนียม เวลา ค่าใช้จ่าย หรือธุรกรรมภาษีได้</span><span class="sxs-lookup"><span data-stu-id="98abf-126">In PSA, Entry journals let you record the cost or revenue in the material, fee, time, expense, or tax transaction classes.</span></span> <span data-ttu-id="98abf-127">สมุดรายวันมีหัวข้อ บรรทัด และการดำเนินการ **ยืนยัน**</span><span class="sxs-lookup"><span data-stu-id="98abf-127">A journal has a header, lines, and a **Confirm** action.</span></span> <span data-ttu-id="98abf-128">ต่อไปนี้เป็นบางสถานการณ์ที่คุณอาจใช้สมุดรายวัน:</span><span class="sxs-lookup"><span data-stu-id="98abf-128">Here are some scenarios where you might use a journal:</span></span>

- <span data-ttu-id="98abf-129">คุณต้องบันทึกต้นทุนที่แท้จริงของวัสดุและการขายในโครงการ</span><span class="sxs-lookup"><span data-stu-id="98abf-129">You must record material actual costs and sales on a project.</span></span>
- <span data-ttu-id="98abf-130">คุณต้องย้ายธุรกรรมที่เกิดขึ้นจริงจากระบบอื่นไปยัง PSA</span><span class="sxs-lookup"><span data-stu-id="98abf-130">You must move transaction actuals from another system to PSA.</span></span>
- <span data-ttu-id="98abf-131">คุณต้องบันทึกต้นทุนที่เกิดขึ้นในระบบอื่น เช่น ต้นทุนการจัดซื้อ หรือการรับเหมารายย่อย</span><span class="sxs-lookup"><span data-stu-id="98abf-131">You must record costs that occurred in another system, such as procurement or subcontracting costs.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="98abf-132">การใช้สมุดบันทึกรายการเพื่อสร้างข้อมูลจริงควรกระทำโดยผู้ใช้ที่ตระหนักดีถึงผลกระทบทางบัญชีที่เกิดขึ้นจริงต่อโครงการเท่านั้น</span><span class="sxs-lookup"><span data-stu-id="98abf-132">Using Entry journals to create actuals should be done only by a user who is fully aware of the accounting impact the Actuals have on the project.</span></span> <span data-ttu-id="98abf-133">เนื่องจากแอปพลิเคชันไม่ตรวจสอบความถูกต้องของประเภทรายการสมุดรายวัน หรือราคาที่เกี่ยวข้องที่ป้อนในรายการสมุดรายวัน</span><span class="sxs-lookup"><span data-stu-id="98abf-133">This is because the application does not validate the journal line type, or the related pricing that is entered on the journal line.</span></span> <span data-ttu-id="98abf-134">เนื่องจากผลกระทบของสมุดรายวันประเภทนี้ โปรดใช้ความระมัดระวังว่าใครจะได้รับสิทธิ์ในการสร้างสมุดบันทึกรายการ</span><span class="sxs-lookup"><span data-stu-id="98abf-134">Because of the impact of this journal type, exercise adequate caution in who is given access to create Entry journals.</span></span>     


## <a name="recording-actuals-based-on-project-events"></a><span data-ttu-id="98abf-135">บันทึกจริงตามเหตุการณ์ของโครงการ</span><span class="sxs-lookup"><span data-stu-id="98abf-135">Recording actuals based on project events</span></span>

<span data-ttu-id="98abf-136">PSA จะบันทึกธุรกรรมทางการเงินที่เกิดขึ้นระหว่างโครงการ</span><span class="sxs-lookup"><span data-stu-id="98abf-136">PSA records the financial transactions that occur during a project.</span></span> <span data-ttu-id="98abf-137">ธุรกรรมเหล่านี้จะถูกบันทึก เป็น **ค่าจริง**</span><span class="sxs-lookup"><span data-stu-id="98abf-137">These transactions are recorded as **actuals**.</span></span> <span data-ttu-id="98abf-138">ตารางต่อไปนี้แสดงชนิดที่แตกต่างกันของความจริงที่ถูกสร้าง ขึ้นอยู่กับว่าโครงการเป็นแบบในเวลาและวัสดุหรือโครงการที่มีราคาคงที่ อยู่ในระยะที่กำหนดหรือเป็นโครงการภายใน</span><span class="sxs-lookup"><span data-stu-id="98abf-138">The following tables show the different types of actuals that are created, depending on whether the project is a time-and-materials or fixed-price project, is in the presales stage, or is an internal project.</span></span>

<span data-ttu-id="98abf-139">**ทรัพยากรเป็นของหน่วยองค์กรเดียวกันกับหน่วยที่ทำสัญญาของโครงการ**</span><span class="sxs-lookup"><span data-stu-id="98abf-139">**The resource belongs to same organizational unit as the project's contracting unit**</span></span>

<table>
<thead>
<tr>
<th rowspan="3"><span data-ttu-id="98abf-140">เหตุการณ์</span><span class="sxs-lookup"><span data-stu-id="98abf-140">Event</span></span></th>
<th colspan="4"><span data-ttu-id="98abf-141">โครงการที่เรียกเก็บเงินได้หรือขายแล้ว</span><span class="sxs-lookup"><span data-stu-id="98abf-141">Billable or sold project</span></span></th>
<th rowspan="3"><span data-ttu-id="98abf-142">โครงการในระยะที่ำกำหนด</span><span class="sxs-lookup"><span data-stu-id="98abf-142">Project in the presales stage</span></span></th>
<th rowspan="3"><span data-ttu-id="98abf-143">โครงการภายใน</span><span class="sxs-lookup"><span data-stu-id="98abf-143">Internal project</span></span></th>
</tr>
<tr>
<th colspan="2"><span data-ttu-id="98abf-144">เวลาและวัสดุ</span><span class="sxs-lookup"><span data-stu-id="98abf-144">Time and materials</span></span></th>
<th colspan="2"><span data-ttu-id="98abf-145">ราคาคงที่</span><span class="sxs-lookup"><span data-stu-id="98abf-145">Fixed price</span></span></th>
</tr>
<tr>
<th><span data-ttu-id="98abf-146">ตามจริง</span><span class="sxs-lookup"><span data-stu-id="98abf-146">Actuals</span></span></th>
<th><span data-ttu-id="98abf-147">สกุลเงินในธุรกรรม</span><span class="sxs-lookup"><span data-stu-id="98abf-147">Transaction currency</span></span></th>
<th><span data-ttu-id="98abf-148">ราคาคงที่</span><span class="sxs-lookup"><span data-stu-id="98abf-148">Fixed price</span></span></th>
<th><span data-ttu-id="98abf-149">สกุลเงินในธุรกรรม</span><span class="sxs-lookup"><span data-stu-id="98abf-149">Transaction currency</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="98abf-150">รายการเวลาถูกสร้างขึ้น</span><span class="sxs-lookup"><span data-stu-id="98abf-150">A time entry is created.</span></span></td>
<td colspan="6"><span data-ttu-id="98abf-151">ไม่มีกิจกรรมในเอนทิตีที่เกิดขึ้นจริง</span><span class="sxs-lookup"><span data-stu-id="98abf-151">No activity in the Actuals entity</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="98abf-152">รายการเวลาถูกส่ง</span><span class="sxs-lookup"><span data-stu-id="98abf-152">A time entry is submitted.</span></span></td>
<td colspan="6"><span data-ttu-id="98abf-153">ไม่มีกิจกรรมในเอนทิตีที่เกิดขึ้นจริง</span><span class="sxs-lookup"><span data-stu-id="98abf-153">No activity in the Actuals entity</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="98abf-154">เวลาได้รับการอนุมัติ และไม่มีการเปลี่ยนแปลงหรือเพิ่มขึ้นของชั่วโมงที่เรียกเก็บเงินได้เกิดขึ้น ในระหว่างการอนุมัติ</span><span class="sxs-lookup"><span data-stu-id="98abf-154">Time is approved, and no change to or increase in billable hours occurs during approval.</span></span></td>
<td><span data-ttu-id="98abf-155">จำนวนจริงของต้นทุน</span><span class="sxs-lookup"><span data-stu-id="98abf-155">Cost actual</span></span></td>
<td><span data-ttu-id="98abf-156">สกุลเงินของหน่วยตามสัญญา</span><span class="sxs-lookup"><span data-stu-id="98abf-156">Contracting unit currency</span></span></td>
<td rowspan="2"><span data-ttu-id="98abf-157">จำนวนจริงของต้นทุน</span><span class="sxs-lookup"><span data-stu-id="98abf-157">Cost actual</span></span></td>
<td rowspan="2"><span data-ttu-id="98abf-158">สกุลเงินของหน่วยตามสัญญา</span><span class="sxs-lookup"><span data-stu-id="98abf-158">Contracting unit currency</span></span>
<td rowspan="2"><span data-ttu-id="98abf-159">จำนวนจริงของต้นทุน</span><span class="sxs-lookup"><span data-stu-id="98abf-159">Cost actual</span></span></td>
<td rowspan="2"><span data-ttu-id="98abf-160">จำนวนจริงของต้นทุน</span><span class="sxs-lookup"><span data-stu-id="98abf-160">Cost actual</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="98abf-161">การขายที่เกิดขึ้นจริงที่ยังไม่ได้เรียกเก็บและคิดค่าธรรมเนียมได้</span><span class="sxs-lookup"><span data-stu-id="98abf-161">Unbilled sales actual – Chargeable</span></span></td>
<td><span data-ttu-id="98abf-162">สกุลเงินตามสัญญาโครงการ</span><span class="sxs-lookup"><span data-stu-id="98abf-162">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="98abf-163">เวลาได้รับการอนุมัติ และการลดลงของชั่วโมงที่เรียกเก็บเงินได้เกิดขึ้น ในระหว่างการอนุมัติ</span><span class="sxs-lookup"><span data-stu-id="98abf-163">Time is approved, and a decrease in billable hours occurs during approval.</span></span></td>
<td><span data-ttu-id="98abf-164">จำนวนจริงของต้นทุน</span><span class="sxs-lookup"><span data-stu-id="98abf-164">Cost actual</span></span></td>
<td><span data-ttu-id="98abf-165">สกุลเงินของหน่วยตามสัญญา</span><span class="sxs-lookup"><span data-stu-id="98abf-165">Contracting unit currency</span></span></td>
<td rowspan="3"><span data-ttu-id="98abf-166">จำนวนจริงของต้นทุน</span><span class="sxs-lookup"><span data-stu-id="98abf-166">Cost actual</span></span></td>
<td rowspan="3"><span data-ttu-id="98abf-167">สกุลเงินของหน่วยตามสัญญา</span><span class="sxs-lookup"><span data-stu-id="98abf-167">Contracting unit currency</span></span></td>
<td rowspan="3"><span data-ttu-id="98abf-168">จำนวนจริงของต้นทุน</span><span class="sxs-lookup"><span data-stu-id="98abf-168">Cost actual</span></span></td>
<td rowspan="3"><span data-ttu-id="98abf-169">จำนวนจริงของต้นทุน</span><span class="sxs-lookup"><span data-stu-id="98abf-169">Cost actual</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="98abf-170">การขายที่ยังไม่ได้เรียกเก็บและคิดค่าธรรมเนียมได้ตามจริง สำหรับปริมาณใหม่</span><span class="sxs-lookup"><span data-stu-id="98abf-170">Unbilled sales actual – Chargeable for the new quantity</span></span></td>
<td><span data-ttu-id="98abf-171">สกุลเงินตามสัญญาโครงการ</span><span class="sxs-lookup"><span data-stu-id="98abf-171">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="98abf-172">การขายที่ยังไม่ได้เรียกเก็บและคิดค่าธรรมเนียมไม่ได้ตามจริง สำหรับความแตกต่าง</span><span class="sxs-lookup"><span data-stu-id="98abf-172">Unbilled sales actual – Non-chargeable for the difference</span></span></td>
<td><span data-ttu-id="98abf-173">สกุลเงินตามสัญญาโครงการ</span><span class="sxs-lookup"><span data-stu-id="98abf-173">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="98abf-174">ใบแจ้งหนี้ได้รับการยืนยัน และไม่มีการเปลี่ยนแปลงหรือเพิ่มขึ้นของชั่วโมงที่เรียกเก็บเงินได้เกิดขึ้น</span><span class="sxs-lookup"><span data-stu-id="98abf-174">An invoice is confirmed, and no change to or increase in billable hours occurs.</span></span></td>
<td><span data-ttu-id="98abf-175">การกลับการขายที่ยังไม่ได้เรียกเก็บเงิน</span><span class="sxs-lookup"><span data-stu-id="98abf-175">Unbilled sales reversal</span></span></td>
<td><span data-ttu-id="98abf-176">สกุลเงินตามสัญญาโครงการ</span><span class="sxs-lookup"><span data-stu-id="98abf-176">Project contract currency</span></span></td>
<td rowspan="2"><span data-ttu-id="98abf-177">การขายที่เรียกเก็บเงินสำหรับไมล์สโตน</span><span class="sxs-lookup"><span data-stu-id="98abf-177">Billed sales for milestone</span></span></td>
<td rowspan="2"><span data-ttu-id="98abf-178">สกุลเงินตามสัญญาโครงการ</span><span class="sxs-lookup"><span data-stu-id="98abf-178">Project contract currency</span></span></td>
<td rowspan="2"><span data-ttu-id="98abf-179">ไม่สามารถใช้งานได้</span><span class="sxs-lookup"><span data-stu-id="98abf-179">Not applicable</span></span></td>
<td rowspan="2"><span data-ttu-id="98abf-180">ไม่สามารถใช้งานได้</span><span class="sxs-lookup"><span data-stu-id="98abf-180">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="98abf-181">การขายที่เรียกเก็บเงินแล้ว</span><span class="sxs-lookup"><span data-stu-id="98abf-181">Billed sales</span></span></td>
<td><span data-ttu-id="98abf-182">สกุลเงินตามสัญญาโครงการ</span><span class="sxs-lookup"><span data-stu-id="98abf-182">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="98abf-183">ใบแจ้งหนี้ได้รับการยืนยัน และการลดลงของชั่วโมงที่เรียกเก็บเงินได้เกิดขึ้น</span><span class="sxs-lookup"><span data-stu-id="98abf-183">An invoice is confirmed, and a decrease in billable hours occurs.</span></span></td>
<td><span data-ttu-id="98abf-184">การกลับการขายที่ยังไม่ได้เรียกเก็บเงิน</span><span class="sxs-lookup"><span data-stu-id="98abf-184">Unbilled sales reversal</span></span></td>
<td><span data-ttu-id="98abf-185">สกุลเงินตามสัญญาโครงการ</span><span class="sxs-lookup"><span data-stu-id="98abf-185">Project contract currency</span></span></td>
<td rowspan="3"><span data-ttu-id="98abf-186">ไม่สามารถใช้งานได้</span><span class="sxs-lookup"><span data-stu-id="98abf-186">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="98abf-187">ไม่สามารถใช้งานได้</span><span class="sxs-lookup"><span data-stu-id="98abf-187">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="98abf-188">ไม่สามารถใช้งานได้</span><span class="sxs-lookup"><span data-stu-id="98abf-188">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="98abf-189">ไม่สามารถใช้งานได้</span><span class="sxs-lookup"><span data-stu-id="98abf-189">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="98abf-190">การขายที่เรียกเก็บแล้วและคิดค่าธรรมเนียมได้ สำหรับปริมาณใหม่</span><span class="sxs-lookup"><span data-stu-id="98abf-190">Billed sales – Chargeable for the new quantity</span></span></td>
<td><span data-ttu-id="98abf-191">สกุลเงินตามสัญญาโครงการ</span><span class="sxs-lookup"><span data-stu-id="98abf-191">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="98abf-192">การขายที่เรียกเก็บเงินแล้วและคิดค่าธรรมเนียมไม่ได้ สำหรับความแตกต่าง</span><span class="sxs-lookup"><span data-stu-id="98abf-192">Billed sales – Non-chargeable for the difference</span></span></td>
<td><span data-ttu-id="98abf-193">สกุลเงินตามสัญญาโครงการ</span><span class="sxs-lookup"><span data-stu-id="98abf-193">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="98abf-194">ใบแจ้งหนี้จะถูกแก้ไขเพื่อเพิ่มปริมาณที่คิดค่าธรรมเนียมได้</span><span class="sxs-lookup"><span data-stu-id="98abf-194">An invoice is corrected to increase the chargeable quantity.</span></span></td>
<td><span data-ttu-id="98abf-195">การขายที่เรียกเก็บเงินแล้ว ย้อนกลับ</span><span class="sxs-lookup"><span data-stu-id="98abf-195">Billed sales – Reversal</span></span></td>
<td><span data-ttu-id="98abf-196">สกุลเงินตามสัญญาโครงการ</span><span class="sxs-lookup"><span data-stu-id="98abf-196">Project contract currency</span></span></td>
<td rowspan="5">
<ul>
<li><span data-ttu-id="98abf-197">การย้อนกลับการขายที่เรียกเก็บเงินแล้วสำหรับไมล์สโตน</span><span class="sxs-lookup"><span data-stu-id="98abf-197">Billed sales reversal for milestone</span></span></li>
<li><span data-ttu-id="98abf-198">เปลี่ยนสถานะไมล์สโตน จาก <strong>ออกใบหนี้</strong> เป็น <strong>พร้อมสำหรับใบแจ้งหนี้</strong></span><span class="sxs-lookup"><span data-stu-id="98abf-198">Change in milestone status from <strong>Invoiced</strong> to <strong>Ready for invoice</strong></span></span></li>
</ul>
</td>
<td rowspan="5"><span data-ttu-id="98abf-199">สกุลเงินตามสัญญาโครงการ</span><span class="sxs-lookup"><span data-stu-id="98abf-199">Project contract currency</span></span></td>
<td rowspan="5"><span data-ttu-id="98abf-200">ไม่สามารถใช้งานได้</span><span class="sxs-lookup"><span data-stu-id="98abf-200">Not applicable</span></span></td>
<td rowspan="5"><span data-ttu-id="98abf-201">ไม่สามารถใช้งานได้</span><span class="sxs-lookup"><span data-stu-id="98abf-201">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="98abf-202">การขายที่เรียกเก็บเงินแล้ว</span><span class="sxs-lookup"><span data-stu-id="98abf-202">Billed sales</span></span></td>
<td><span data-ttu-id="98abf-203">สกุลเงินตามสัญญาโครงการ</span><span class="sxs-lookup"><span data-stu-id="98abf-203">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="98abf-204">ใบแจ้งหนี้จะถูกแก้ไขเพื่อลดปริมาณที่คิดค่าธรรมเนียมได้</span><span class="sxs-lookup"><span data-stu-id="98abf-204">An invoice is corrected to decrease the chargeable quantity.</span></span></td>
<td><span data-ttu-id="98abf-205">การขายที่เรียกเก็บเงินแล้ว ย้อนกลับ</span><span class="sxs-lookup"><span data-stu-id="98abf-205">Billed sales – Reversal</span></span></td>
<td><span data-ttu-id="98abf-206">สกุลเงินตามสัญญาโครงการ</span><span class="sxs-lookup"><span data-stu-id="98abf-206">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="98abf-207">การขายที่เรียกเก็บเงินแล้วสำหรับปริมาณใหม่</span><span class="sxs-lookup"><span data-stu-id="98abf-207">Billed sales for the new quantity</span></span></td>
<td><span data-ttu-id="98abf-208">สกุลเงินตามสัญญาโครงการ</span><span class="sxs-lookup"><span data-stu-id="98abf-208">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="98abf-209">การขายที่ยังไม่เรียกเก็บเงินและคิดค่าธรรมเนียมได้ สำหรับความแตกต่าง</span><span class="sxs-lookup"><span data-stu-id="98abf-209">Unbilled sales – Chargeable for the difference</span></span></td>
<td><span data-ttu-id="98abf-210">สกุลเงินตามสัญญาโครงการ</span><span class="sxs-lookup"><span data-stu-id="98abf-210">Project contract currency</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="98abf-211">**ทรัพยากรเป็นของหน่วยองค์กรที่แตกต่างจากหน่วยที่ทำสัญญาของโครงการ**</span><span class="sxs-lookup"><span data-stu-id="98abf-211">**The resource belongs to an organizational unit that differs from the project's contracting unit**</span></span>

<table>
<thead>
<tr>
<th rowspan="3"><span data-ttu-id="98abf-212">เหตุการณ์</span><span class="sxs-lookup"><span data-stu-id="98abf-212">Event</span></span></th>
<th colspan="4"><span data-ttu-id="98abf-213">โครงการที่เรียกเก็บเงินได้หรือขายแล้ว</span><span class="sxs-lookup"><span data-stu-id="98abf-213">Billable or sold project</span></span></th>
<th rowspan="3"><span data-ttu-id="98abf-214">โครงการในระยะที่ำกำหนด</span><span class="sxs-lookup"><span data-stu-id="98abf-214">Project in the presales stage</span></span></th>
<th rowspan="3"><span data-ttu-id="98abf-215">โครงการภายใน</span><span class="sxs-lookup"><span data-stu-id="98abf-215">Internal project</span></span></th>
</tr>
<tr>
<th colspan="2"><span data-ttu-id="98abf-216">เวลาและวัสดุ</span><span class="sxs-lookup"><span data-stu-id="98abf-216">Time and materials</span></span></th>
<th colspan="2"><span data-ttu-id="98abf-217">ราคาคงที่</span><span class="sxs-lookup"><span data-stu-id="98abf-217">Fixed price</span></span></th>
</tr>
<tr>
<th><span data-ttu-id="98abf-218">ตามจริง</span><span class="sxs-lookup"><span data-stu-id="98abf-218">Actuals</span></span></th>
<th><span data-ttu-id="98abf-219">สกุลเงินในธุรกรรม</span><span class="sxs-lookup"><span data-stu-id="98abf-219">Transaction currency</span></span></th>
<th><span data-ttu-id="98abf-220">ราคาคงที่</span><span class="sxs-lookup"><span data-stu-id="98abf-220">Fixed price</span></span></th>
<th><span data-ttu-id="98abf-221">สกุลเงินในธุรกรรม</span><span class="sxs-lookup"><span data-stu-id="98abf-221">Transaction currency</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="98abf-222">รายการเวลาถูกสร้างขึ้น</span><span class="sxs-lookup"><span data-stu-id="98abf-222">A time entry is created.</span></span></td>
<td colspan="6"><span data-ttu-id="98abf-223">ไม่มีกิจกรรมในเอนทิตีที่เกิดขึ้นจริง</span><span class="sxs-lookup"><span data-stu-id="98abf-223">No activity in the Actuals entity</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="98abf-224">รายการเวลาถูกส่ง</span><span class="sxs-lookup"><span data-stu-id="98abf-224">A time entry is submitted.</span></span></td>
<td colspan="6"><span data-ttu-id="98abf-225">ไม่มีกิจกรรมในเอนทิตีที่เกิดขึ้นจริง</span><span class="sxs-lookup"><span data-stu-id="98abf-225">No activity in the Actuals entity</span></span></td>
</tr>
<tr>
<td rowspan="4"><span data-ttu-id="98abf-226">เวลาได้รับการอนุมัติ และไม่มีการเปลี่ยนแปลงหรือเพิ่มขึ้นของชั่วโมงที่เรียกเก็บเงินได้เกิดขึ้น ในระหว่างการอนุมัติ</span><span class="sxs-lookup"><span data-stu-id="98abf-226">Time is approved, and no change to or increase in billable hours occurs during approval.</span></span></td>
<td><span data-ttu-id="98abf-227">จำนวนจริงของต้นทุน</span><span class="sxs-lookup"><span data-stu-id="98abf-227">Cost actual</span></span></td>
<td><span data-ttu-id="98abf-228">สกุลเงินของหน่วยตามสัญญา</span><span class="sxs-lookup"><span data-stu-id="98abf-228">Contracting unit currency</span></span></td>
<td rowspan="4"><span data-ttu-id="98abf-229">จำนวนจริงของต้นทุน</span><span class="sxs-lookup"><span data-stu-id="98abf-229">Cost actual</span></span></td>
<td rowspan="4"><span data-ttu-id="98abf-230">สกุลเงินของหน่วยตามสัญญา</span><span class="sxs-lookup"><span data-stu-id="98abf-230">Contracting unit currency</span></span></td>
<td rowspan="4"><span data-ttu-id="98abf-231">จำนวนจริงของต้นทุน</span><span class="sxs-lookup"><span data-stu-id="98abf-231">Cost actual</span></span></td>
<td rowspan="4"><span data-ttu-id="98abf-232">จำนวนจริงของต้นทุน</span><span class="sxs-lookup"><span data-stu-id="98abf-232">Cost actual</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="98abf-233">การขายที่เกิดขึ้นจริงที่ยังไม่ได้เรียกเก็บและคิดค่าธรรมเนียมได้</span><span class="sxs-lookup"><span data-stu-id="98abf-233">Unbilled sales actual – Chargeable</span></span></td>
<td><span data-ttu-id="98abf-234">สกุลเงินตามสัญญาโครงการ</span><span class="sxs-lookup"><span data-stu-id="98abf-234">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="98abf-235">ต้นทุนต่อหน่วยการจัดเตรียมทรัพยากร</span><span class="sxs-lookup"><span data-stu-id="98abf-235">Resourcing unit cost</span></span></td>
<td><span data-ttu-id="98abf-236">สกุลเงินต่อหน่วยการจัดเตรียมทรัพยากร</span><span class="sxs-lookup"><span data-stu-id="98abf-236">Resourcing unit currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="98abf-237">การขายระหว่างองค์กร</span><span class="sxs-lookup"><span data-stu-id="98abf-237">Interorganizational sales</span></span></td>
<td><span data-ttu-id="98abf-238">สกุลเงินของหน่วยตามสัญญา</span><span class="sxs-lookup"><span data-stu-id="98abf-238">Contracting unit currency</span></span></td>
</tr>
<tr>
<td rowspan="5"><span data-ttu-id="98abf-239">เวลาได้รับการอนุมัติ และการลดลงของชั่วโมงที่เรียกเก็บเงินได้เกิดขึ้น ในระหว่างการอนุมัติ</span><span class="sxs-lookup"><span data-stu-id="98abf-239">Time is approved, and a decrease in billable hours occurs during approval.</span></span></td>
<td><span data-ttu-id="98abf-240">จำนวนจริงของต้นทุน</span><span class="sxs-lookup"><span data-stu-id="98abf-240">Cost actual</span></span></td>
<td><span data-ttu-id="98abf-241">สกุลเงินของหน่วยตามสัญญา</span><span class="sxs-lookup"><span data-stu-id="98abf-241">Contracting unit currency</span></span></td>
<td rowspan="5"><span data-ttu-id="98abf-242">จำนวนจริงของต้นทุน</span><span class="sxs-lookup"><span data-stu-id="98abf-242">Cost actual</span></span></td>
<td rowspan="5"><span data-ttu-id="98abf-243">สกุลเงินของหน่วยตามสัญญา</span><span class="sxs-lookup"><span data-stu-id="98abf-243">Contracting unit currency</span></span></td>
<td rowspan="5"><span data-ttu-id="98abf-244">จำนวนจริงของต้นทุน</span><span class="sxs-lookup"><span data-stu-id="98abf-244">Cost actual</span></span></td>
<td rowspan="5"><span data-ttu-id="98abf-245">จำนวนจริงของต้นทุน</span><span class="sxs-lookup"><span data-stu-id="98abf-245">Cost actual</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="98abf-246">ต้นทุนต่อหน่วยการจัดเตรียมทรัพยากร</span><span class="sxs-lookup"><span data-stu-id="98abf-246">Resourcing unit cost</span></span></td>
<td><span data-ttu-id="98abf-247">สกุลเงินต่อหน่วยการจัดเตรียมทรัพยากร</span><span class="sxs-lookup"><span data-stu-id="98abf-247">Resourcing unit currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="98abf-248">การขายระหว่างองค์กร</span><span class="sxs-lookup"><span data-stu-id="98abf-248">Interorganizational sales</span></span></td>
<td><span data-ttu-id="98abf-249">สกุลเงินของหน่วยตามสัญญา</span><span class="sxs-lookup"><span data-stu-id="98abf-249">Contracting unit currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="98abf-250">การขายที่ยังไม่ได้เรียกเก็บและคิดค่าธรรมเนียมได้ตามจริง สำหรับปริมาณใหม่</span><span class="sxs-lookup"><span data-stu-id="98abf-250">Unbilled sales actual – Chargeable for the new quantity</span></span></td>
<td><span data-ttu-id="98abf-251">สกุลเงินตามสัญญาโครงการ</span><span class="sxs-lookup"><span data-stu-id="98abf-251">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="98abf-252">การขายที่ยังไม่ได้เรียกเก็บและคิดค่าธรรมเนียมไม่ได้ตามจริง สำหรับความแตกต่าง</span><span class="sxs-lookup"><span data-stu-id="98abf-252">Unbilled sales actual – Non-chargeable for the difference</span></span></td>
<td><span data-ttu-id="98abf-253">สกุลเงินตามสัญญาโครงการ</span><span class="sxs-lookup"><span data-stu-id="98abf-253">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="98abf-254">ใบแจ้งหนี้ได้รับการยืนยัน และไม่มีการเปลี่ยนแปลงหรือเพิ่มขึ้นของชั่วโมงที่เรียกเก็บเงินได้เกิดขึ้น</span><span class="sxs-lookup"><span data-stu-id="98abf-254">An invoice is confirmed, and no change to or increase in billable hours occurs.</span></span></td>
<td><span data-ttu-id="98abf-255">การกลับการขายที่ยังไม่ได้เรียกเก็บเงิน</span><span class="sxs-lookup"><span data-stu-id="98abf-255">Unbilled sales reversal</span></span></td>
<td><span data-ttu-id="98abf-256">สกุลเงินตามสัญญาโครงการ</span><span class="sxs-lookup"><span data-stu-id="98abf-256">Project contract currency</span></span></td>
<td rowspan="2"><span data-ttu-id="98abf-257">การขายที่เรียกเก็บเงินสำหรับไมล์สโตน</span><span class="sxs-lookup"><span data-stu-id="98abf-257">Billed sales for milestone</span></span></td>
<td rowspan="2"><span data-ttu-id="98abf-258">สกุลเงินตามสัญญาโครงการ</span><span class="sxs-lookup"><span data-stu-id="98abf-258">Project contract currency</span></span></td>
<td rowspan="2"><span data-ttu-id="98abf-259">ไม่สามารถใช้งานได้</span><span class="sxs-lookup"><span data-stu-id="98abf-259">Not applicable</span></span></td>
<td rowspan="2"><span data-ttu-id="98abf-260">ไม่สามารถใช้งานได้</span><span class="sxs-lookup"><span data-stu-id="98abf-260">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="98abf-261">การขายที่เรียกเก็บเงินแล้ว</span><span class="sxs-lookup"><span data-stu-id="98abf-261">Billed sales</span></span></td>
<td><span data-ttu-id="98abf-262">สกุลเงินตามสัญญาโครงการ</span><span class="sxs-lookup"><span data-stu-id="98abf-262">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="98abf-263">ใบแจ้งหนี้ได้รับการยืนยัน และการลดลงของชั่วโมงที่เรียกเก็บเงินได้เกิดขึ้น</span><span class="sxs-lookup"><span data-stu-id="98abf-263">An invoice is confirmed, and a decrease in billable hours occurs.</span></span></td>
<td><span data-ttu-id="98abf-264">การกลับการขายที่ยังไม่ได้เรียกเก็บเงิน</span><span class="sxs-lookup"><span data-stu-id="98abf-264">Unbilled sales reversal</span></span></td>
<td><span data-ttu-id="98abf-265">สกุลเงินตามสัญญาโครงการ</span><span class="sxs-lookup"><span data-stu-id="98abf-265">Project contract currency</span></span></td>
<td rowspan="3"><span data-ttu-id="98abf-266">ไม่สามารถใช้งานได้</span><span class="sxs-lookup"><span data-stu-id="98abf-266">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="98abf-267">ไม่สามารถใช้งานได้</span><span class="sxs-lookup"><span data-stu-id="98abf-267">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="98abf-268">ไม่สามารถใช้งานได้</span><span class="sxs-lookup"><span data-stu-id="98abf-268">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="98abf-269">ไม่สามารถใช้งานได้</span><span class="sxs-lookup"><span data-stu-id="98abf-269">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="98abf-270">การขายที่เรียกเก็บแล้วและคิดค่าธรรมเนียมได้ สำหรับปริมาณใหม่</span><span class="sxs-lookup"><span data-stu-id="98abf-270">Billed sales – Chargeable for the new quantity</span></span></td>
<td><span data-ttu-id="98abf-271">สกุลเงินตามสัญญาโครงการ</span><span class="sxs-lookup"><span data-stu-id="98abf-271">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="98abf-272">การขายที่เรียกเก็บเงินแล้วและคิดค่าธรรมเนียมไม่ได้ สำหรับความแตกต่าง</span><span class="sxs-lookup"><span data-stu-id="98abf-272">Billed sales – Non-chargeable for the difference</span></span></td>
<td><span data-ttu-id="98abf-273">สกุลเงินตามสัญญาโครงการ</span><span class="sxs-lookup"><span data-stu-id="98abf-273">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="98abf-274">ใบแจ้งหนี้จะถูกแก้ไขเพื่อเพิ่มปริมาณที่คิดค่าธรรมเนียมได้</span><span class="sxs-lookup"><span data-stu-id="98abf-274">An invoice is corrected to increase the chargeable quantity.</span></span></td>
<td><span data-ttu-id="98abf-275">การขายที่เรียกเก็บเงินแล้ว ย้อนกลับ</span><span class="sxs-lookup"><span data-stu-id="98abf-275">Billed sales – Reversal</span></span></td>
<td><span data-ttu-id="98abf-276">สกุลเงินตามสัญญาโครงการ</span><span class="sxs-lookup"><span data-stu-id="98abf-276">Project contract currency</span></span></td>
<td rowspan="5">
<ul>
<li><span data-ttu-id="98abf-277">การย้อนกลับการขายที่เรียกเก็บเงินแล้วสำหรับไมล์สโตน</span><span class="sxs-lookup"><span data-stu-id="98abf-277">Billed sales reversal for milestone</span></span></li>
<li><span data-ttu-id="98abf-278">เปลี่ยนสถานะไมล์สโตน จาก <strong>ออกใบหนี้</strong> เป็น <strong>พร้อมสำหรับใบแจ้งหนี้</strong></span><span class="sxs-lookup"><span data-stu-id="98abf-278">Change in milestone status from <strong>Invoiced</strong> to <strong>Ready for invoice</strong></span></span></li>
</ul>
</td>
<td rowspan="5"><span data-ttu-id="98abf-279">สกุลเงินตามสัญญาโครงการ</span><span class="sxs-lookup"><span data-stu-id="98abf-279">Project contract currency</span></span></td>
<td rowspan="5"><span data-ttu-id="98abf-280">ไม่สามารถใช้งานได้</span><span class="sxs-lookup"><span data-stu-id="98abf-280">Not applicable</span></span></td>
<td rowspan="5"><span data-ttu-id="98abf-281">ไม่สามารถใช้งานได้</span><span class="sxs-lookup"><span data-stu-id="98abf-281">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="98abf-282">การขายที่เรียกเก็บเงินแล้ว</span><span class="sxs-lookup"><span data-stu-id="98abf-282">Billed sales</span></span></td>
<td><span data-ttu-id="98abf-283">สกุลเงินตามสัญญาโครงการ</span><span class="sxs-lookup"><span data-stu-id="98abf-283">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="98abf-284">ใบแจ้งหนี้จะถูกแก้ไขเพื่อลดปริมาณที่คิดค่าธรรมเนียมได้</span><span class="sxs-lookup"><span data-stu-id="98abf-284">An invoice is corrected to decrease the chargeable quantity.</span></span></td>
<td><span data-ttu-id="98abf-285">การขายที่เรียกเก็บเงินแล้ว ย้อนกลับ</span><span class="sxs-lookup"><span data-stu-id="98abf-285">Billed sales – Reversal</span></span></td>
<td><span data-ttu-id="98abf-286">สกุลเงินตามสัญญาโครงการ</span><span class="sxs-lookup"><span data-stu-id="98abf-286">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="98abf-287">การขายที่เรียกเก็บเงินแล้วสำหรับปริมาณใหม่</span><span class="sxs-lookup"><span data-stu-id="98abf-287">Billed sales for the new quantity</span></span></td>
<td><span data-ttu-id="98abf-288">สกุลเงินตามสัญญาโครงการ</span><span class="sxs-lookup"><span data-stu-id="98abf-288">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="98abf-289">การขายที่ยังไม่เรียกเก็บเงินและคิดค่าธรรมเนียมได้ สำหรับความแตกต่าง</span><span class="sxs-lookup"><span data-stu-id="98abf-289">Unbilled sales – Chargeable for the difference</span></span></td>
<td><span data-ttu-id="98abf-290">สกุลเงินตามสัญญาโครงการ</span><span class="sxs-lookup"><span data-stu-id="98abf-290">Project contract currency</span></span></td>
</tr>
</tbody>
</table>
