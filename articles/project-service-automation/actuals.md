---
title: ตามจริง
description: หัวข้อนี้แสดงข้อมูลเกี่ยวกับค่าจริงของโครงการ
author: rumant
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom:
- dyn365-projectservice
ms.date: 03/06/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.assetid: 44c6e85f-5b21-4e24-999c-15a2f065d977
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
ms.openlocfilehash: 8291e0eb8531e8e9690368675f333c44b6e92e48
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 03/24/2020
ms.locfileid: "3756488"
---
# <a name="actuals"></a><span data-ttu-id="0ba7a-103">ตามจริง</span><span class="sxs-lookup"><span data-stu-id="0ba7a-103">Actuals</span></span>

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

<span data-ttu-id="0ba7a-104">ค่าจริง คือจำนวนของงานที่เสร็จสมบูรณ์แล้วในโครงการ</span><span class="sxs-lookup"><span data-stu-id="0ba7a-104">Actuals are the amount of work that has been completed on a project.</span></span> <span data-ttu-id="0ba7a-105">ค่าจริงของโครงการสามารถสืบย้อนกลับไปยังเอกสารต้นทางของพวกเขา</span><span class="sxs-lookup"><span data-stu-id="0ba7a-105">Project actuals can be traced back to their source documents.</span></span> <span data-ttu-id="0ba7a-106">เอกสารต้นทางเหล่านั้น รวมถึงเวลา ค่าใช้จ่าย และรายการสมุดรายวัน และใบแจ้งหนี้ิ่ด้วย</span><span class="sxs-lookup"><span data-stu-id="0ba7a-106">Those source documents include time, expense, and journal entries, and also invoices.</span></span>

![วิธีการติดตามค่าจริงของโครงการไปยังเอกสารต้นทาง](media/basic-guide-18.png)

## <a name="submitting-a-time-entry"></a><span data-ttu-id="0ba7a-108">ส่งรายการเวลา</span><span class="sxs-lookup"><span data-stu-id="0ba7a-108">Submitting a time entry</span></span>

<span data-ttu-id="0ba7a-109">ใน PSA เมื่อรายการเวลาถูกส่งสำหรับโครงการที่ถูกแม็ปกับรายละเอียดการให้บริการตามสัญญาในเวลาและวัสดุ จะมีการสร้างบรรทัดสมุดรายวันสองรายการ</span><span class="sxs-lookup"><span data-stu-id="0ba7a-109">In PSA, when a time entry is submitted for a project that is mapped to a time-and-materials contract line, two journal lines are created.</span></span> <span data-ttu-id="0ba7a-110">หนึ่งบรรทัดสำหรับต้นทุน และอีกบรรทัดสำหรับการขายที่ยังไม่ได้เรียกเก็บเงิน</span><span class="sxs-lookup"><span data-stu-id="0ba7a-110">One line is for cost, and the other line is for unbilled sales.</span></span> <span data-ttu-id="0ba7a-111">เมื่อรายการเวลาถูกส่งสำหรับโครงการที่ถูกแม็ปกับรายละเอียดการให้บริการตามสัญญาที่มีเวลาคงที่ จะมีการสร้างบรรทัดสมุดรายวันสำหรับต้นทุนบรรทัดเดียว</span><span class="sxs-lookup"><span data-stu-id="0ba7a-111">When a time entry is submitted for a project that is mapped to a fixed-price contract line, a journal line is created only for cost.</span></span> 

<span data-ttu-id="0ba7a-112">ตรรกะสำหรับการป้อนราคาเริ่มต้นอยู่บนบรรทัดสมุดรายวัน</span><span class="sxs-lookup"><span data-stu-id="0ba7a-112">Logic for entering default prices resides on the journal line.</span></span> <span data-ttu-id="0ba7a-113">ค่าฟิลด์ทั้งหมดจากรายการเวลาจะถูกคัดลอกไปยังบรรทัดสมุดรายวัน</span><span class="sxs-lookup"><span data-stu-id="0ba7a-113">All the field values from a time entry are copied to the journal line.</span></span> <span data-ttu-id="0ba7a-114">ฟิลด์เหล่านี้รวมถึงวันที่ของธุรกรรม รายละเอียดการให้บริการตามสัญญาที่โครงการถูกแม็ปด้วย และสกุลเงินที่เป็นผลในราคาตลาดที่เหมาะสม</span><span class="sxs-lookup"><span data-stu-id="0ba7a-114">These fields include the date of the transaction, the contract line that the project is mapped to, and the currency result in the appropriate price list.</span></span> 

<span data-ttu-id="0ba7a-115">ฟิลด์ที่มีผลต่อราคาเริ่มต้น เช่น **บทบาท** และ **หน่วยองค์กร** ทำให้เกิดราคาที่เหมาะสมที่จะป้อนโดยค่าเริ่มต้นบนบรรทัดสมุดรายวัน</span><span class="sxs-lookup"><span data-stu-id="0ba7a-115">The fields that affect default prices, such as **Role** and **Org Unit**, cause an appropriate price to be entered by default on the journal line.</span></span> <span data-ttu-id="0ba7a-116">หากคุณเพิ่มฟิลด์แบบกำหนดเองในรายการเวลา และคุณต้องการให้ค่าของฟิลด์ถูกเผยแพร่ไปยังที่เกิดขึ้นจริง ให้สร้างฟิลด์บนเอนทิตีที่เกิดขึ้นจริง และใช้การแม็ปฟิลด์เพื่อคัดลอกฟิลด์จากรายการเวลาไปยังที่เกิดขึ้นจริง</span><span class="sxs-lookup"><span data-stu-id="0ba7a-116">If you add a custom field on the time entry, and you want the field value to be propagated to actuals, create the field on the Actuals entity, and use field mappings to copy the field from the time entry to the actual.</span></span>

## <a name="submitting-an-expense-entry"></a><span data-ttu-id="0ba7a-117">การส่งรายการค่าใช้จ่าย</span><span class="sxs-lookup"><span data-stu-id="0ba7a-117">Submitting an expense entry</span></span>

<span data-ttu-id="0ba7a-118">ใน PSA เมื่อรายการค่าใช้จ่ายถูกส่งสำหรับโครงการที่ถูกแม็ปกับรายละเอียดการให้บริการตามสัญญาในเวลาและวัสดุ จะมีการสร้างบรรทัดสมุดรายวันสองบรรทัด</span><span class="sxs-lookup"><span data-stu-id="0ba7a-118">In PSA, when an expense entry is submitted for a project that is mapped to a time-and-materials contract line, two journal lines are created.</span></span> <span data-ttu-id="0ba7a-119">หนึ่งบรรทัดสำหรับต้นทุน และอีกบรรทัดสำหรับการขายที่ยังไม่ได้เรียกเก็บเงิน</span><span class="sxs-lookup"><span data-stu-id="0ba7a-119">One line is for cost, and the other line is for unbilled sales.</span></span> <span data-ttu-id="0ba7a-120">เมื่อรายการค่าใช้จ่ายถูกส่งสำหรับโครงการที่ถูกแม็ปกับรายละเอียดการให้บริการตามสัญญาที่มีราคาคงที่ จะมีการสร้างบรรทัดสมุดรายวันสำหรับต้นทุนบรรทัดเดียว</span><span class="sxs-lookup"><span data-stu-id="0ba7a-120">When an expense entry is submitted for a project that is mapped to a fixed-price contract line, a journal line is created only for cost.</span></span>

<span data-ttu-id="0ba7a-121">ตรรกะสำหรับการป้อนราคาเริ่มต้นสำหรับค่าใช้จ่าย จะขึ้นอยู่กับประเภทของค่าใช้จ่ายที่ถูกเลือก บนหน้า **รายการค่าใช้จ่าย**</span><span class="sxs-lookup"><span data-stu-id="0ba7a-121">Logic for entering default prices for expenses is based on the expense category that is selected on the **Expense entry** page.</span></span> <span data-ttu-id="0ba7a-122">วันที่ของธุรกรรม รายละเอียดการให้บริการตามสัญญาที่โครงการถูกแม็ปด้วย และสกุลเงิน จะถูกใช้เพื่อระบุราคาตลาดที่เหมาะสม</span><span class="sxs-lookup"><span data-stu-id="0ba7a-122">The transaction date, the contract line that the project is mapped to, and the currency are all used to determine the appropriate price list.</span></span> <span data-ttu-id="0ba7a-123">อย่างไรก็ตาม สำหรับราคาตัวเอง ยอดเงินป้อนโดยผู้ใช้จะถูกตั้งค่าโดยตรงบนบรรทัดสมุดรายวันค่าใช้จ่ายที่เกี่ยวข้อง สำหรับต้นทุนและยอดขายโดยค่าเริ่มต้น</span><span class="sxs-lookup"><span data-stu-id="0ba7a-123">However, for the price itself, the amount that the user entered is set directly on the related expense journal lines for cost and sales by default.</span></span>

<span data-ttu-id="0ba7a-124">ในเวอร์ชันปัจจุบันของ PSA รายการตามประเภทของราคาเริ่มต้นต่อหน่วย ในรายการค่าใช้จ่าย ยังไม่พร้อมใช้งาน</span><span class="sxs-lookup"><span data-stu-id="0ba7a-124">In the current version of PSA, category-based entry of per-unit default prices on expense entries isn't available.</span></span>

## <a name="using-journals-to-record-costs"></a><span data-ttu-id="0ba7a-125">การใช้สมุดรายวันเพื่อบันทึกต้นทุน</span><span class="sxs-lookup"><span data-stu-id="0ba7a-125">Using journals to record costs</span></span>

<span data-ttu-id="0ba7a-126">ใน PSA สมุดรายวันช่วยให้คุณสามารถบันทึกต้นทุนหรือรายได้ ในคลาสวัสดุ ค่าธรรมเนียม เวลา ค่าใช้จ่าย หรือธุรกรรมภาษีได้</span><span class="sxs-lookup"><span data-stu-id="0ba7a-126">In PSA, journals let you record cost or revenue in the material, fee, time, expense, or tax transaction classes.</span></span> <span data-ttu-id="0ba7a-127">สมุดรายวันมีหัวข้อ บรรทัด และการดำเนินการ **ยืนยัน**</span><span class="sxs-lookup"><span data-stu-id="0ba7a-127">A journal has a header, lines, and a **Confirm** action.</span></span> <span data-ttu-id="0ba7a-128">ต่อไปนี้เป็นบางสถานการณ์ที่คุณอาจใช้สมุดรายวัน:</span><span class="sxs-lookup"><span data-stu-id="0ba7a-128">Here are some scenarios where you might use a journal:</span></span>

- <span data-ttu-id="0ba7a-129">คุณต้องบันทึกต้นทุนที่แท้จริงของวัสดุและการขายในโครงการ</span><span class="sxs-lookup"><span data-stu-id="0ba7a-129">You must record material actual costs and sales on a project.</span></span>
- <span data-ttu-id="0ba7a-130">คุณต้องย้ายธุรกรรมที่เกิดขึ้นจริงจากระบบอื่นไปยัง PSA</span><span class="sxs-lookup"><span data-stu-id="0ba7a-130">You must move transaction actuals from another system to PSA.</span></span>
- <span data-ttu-id="0ba7a-131">คุณต้องบันทึกต้นทุนที่เกิดขึ้นในระบบอื่น เช่น ต้นทุนการจัดซื้อ หรือการรับเหมารายย่อย</span><span class="sxs-lookup"><span data-stu-id="0ba7a-131">You must record costs that occurred in another system, such as procurement or subcontracting costs.</span></span>

## <a name="recording-actuals-based-on-project-events"></a><span data-ttu-id="0ba7a-132">บันทึกจริงตามเหตุการณ์ของโครงการ</span><span class="sxs-lookup"><span data-stu-id="0ba7a-132">Recording actuals based on project events</span></span>

<span data-ttu-id="0ba7a-133">PSA จะบันทึกธุรกรรมทางการเงินที่เกิดขึ้นระหว่างโครงการ</span><span class="sxs-lookup"><span data-stu-id="0ba7a-133">PSA records the financial transactions that occur during a project.</span></span> <span data-ttu-id="0ba7a-134">ธุรกรรมเหล่านี้จะถูกบันทึก เป็น**ค่าจริง**</span><span class="sxs-lookup"><span data-stu-id="0ba7a-134">These transactions are recorded as **actuals**.</span></span> <span data-ttu-id="0ba7a-135">ตารางต่อไปนี้แสดงชนิดที่แตกต่างกันของความจริงที่ถูกสร้าง ขึ้นอยู่กับว่าโครงการเป็นแบบในเวลาและวัสดุหรือโครงการที่มีราคาคงที่ อยู่ในระยะที่กำหนดหรือเป็นโครงการภายใน</span><span class="sxs-lookup"><span data-stu-id="0ba7a-135">The following tables show the different types of actuals that are created, depending on whether the project is a time-and-materials or fixed-price project, is in the presales stage, or is an internal project.</span></span>

<span data-ttu-id="0ba7a-136">**ทรัพยากรเป็นของหน่วยองค์กรเดียวกันกับหน่วยที่ทำสัญญาของโครงการ**</span><span class="sxs-lookup"><span data-stu-id="0ba7a-136">**The resource belongs to same organizational unit as the project's contracting unit**</span></span>

<table>
<thead>
<tr>
<th rowspan="3"><span data-ttu-id="0ba7a-137">เหตุการณ์</span><span class="sxs-lookup"><span data-stu-id="0ba7a-137">Event</span></span></th>
<th colspan="4"><span data-ttu-id="0ba7a-138">โครงการที่เรียกเก็บเงินได้หรือขายแล้ว</span><span class="sxs-lookup"><span data-stu-id="0ba7a-138">Billable or sold project</span></span></th>
<th rowspan="3"><span data-ttu-id="0ba7a-139">โครงการในระยะที่ำกำหนด</span><span class="sxs-lookup"><span data-stu-id="0ba7a-139">Project in the presales stage</span></span></th>
<th rowspan="3"><span data-ttu-id="0ba7a-140">โครงการภายใน</span><span class="sxs-lookup"><span data-stu-id="0ba7a-140">Internal project</span></span></th>
</tr>
<tr>
<th colspan="2"><span data-ttu-id="0ba7a-141">เวลาและวัสดุ</span><span class="sxs-lookup"><span data-stu-id="0ba7a-141">Time and materials</span></span></th>
<th colspan="2"><span data-ttu-id="0ba7a-142">ราคาคงที่</span><span class="sxs-lookup"><span data-stu-id="0ba7a-142">Fixed price</span></span></th>
</tr>
<tr>
<th><span data-ttu-id="0ba7a-143">ตามจริง</span><span class="sxs-lookup"><span data-stu-id="0ba7a-143">Actuals</span></span></th>
<th><span data-ttu-id="0ba7a-144">สกุลเงินในธุรกรรม</span><span class="sxs-lookup"><span data-stu-id="0ba7a-144">Transaction currency</span></span></th>
<th><span data-ttu-id="0ba7a-145">ราคาคงที่</span><span class="sxs-lookup"><span data-stu-id="0ba7a-145">Fixed price</span></span></th>
<th><span data-ttu-id="0ba7a-146">สกุลเงินในธุรกรรม</span><span class="sxs-lookup"><span data-stu-id="0ba7a-146">Transaction currency</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="0ba7a-147">รายการเวลาถูกสร้างขึ้น</span><span class="sxs-lookup"><span data-stu-id="0ba7a-147">A time entry is created.</span></span></td>
<td colspan="6"><span data-ttu-id="0ba7a-148">ไม่มีกิจกรรมในเอนทิตีที่เกิดขึ้นจริง</span><span class="sxs-lookup"><span data-stu-id="0ba7a-148">No activity in the Actuals entity</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="0ba7a-149">รายการเวลาถูกส่ง</span><span class="sxs-lookup"><span data-stu-id="0ba7a-149">A time entry is submitted.</span></span></td>
<td colspan="6"><span data-ttu-id="0ba7a-150">ไม่มีกิจกรรมในเอนทิตีที่เกิดขึ้นจริง</span><span class="sxs-lookup"><span data-stu-id="0ba7a-150">No activity in the Actuals entity</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="0ba7a-151">เวลาได้รับการอนุมัติ และไม่มีการเปลี่ยนแปลงหรือเพิ่มขึ้นของชั่วโมงที่เรียกเก็บเงินได้เกิดขึ้น ในระหว่างการอนุมัติ</span><span class="sxs-lookup"><span data-stu-id="0ba7a-151">Time is approved, and no change to or increase in billable hours occurs during approval.</span></span></td>
<td><span data-ttu-id="0ba7a-152">จำนวนจริงของต้นทุน</span><span class="sxs-lookup"><span data-stu-id="0ba7a-152">Cost actual</span></span></td>
<td><span data-ttu-id="0ba7a-153">สกุลเงินของหน่วยตามสัญญา</span><span class="sxs-lookup"><span data-stu-id="0ba7a-153">Contracting unit currency</span></span></td>
<td rowspan="2"><span data-ttu-id="0ba7a-154">จำนวนจริงของต้นทุน</span><span class="sxs-lookup"><span data-stu-id="0ba7a-154">Cost actual</span></span></td>
<td rowspan="2"><span data-ttu-id="0ba7a-155">สกุลเงินของหน่วยตามสัญญา</span><span class="sxs-lookup"><span data-stu-id="0ba7a-155">Contracting unit currency</span></span>
<td rowspan="2"><span data-ttu-id="0ba7a-156">จำนวนจริงของต้นทุน</span><span class="sxs-lookup"><span data-stu-id="0ba7a-156">Cost actual</span></span></td>
<td rowspan="2"><span data-ttu-id="0ba7a-157">จำนวนจริงของต้นทุน</span><span class="sxs-lookup"><span data-stu-id="0ba7a-157">Cost actual</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="0ba7a-158">การขายที่เกิดขึ้นจริงที่ยังไม่ได้เรียกเก็บและคิดค่าธรรมเนียมได้</span><span class="sxs-lookup"><span data-stu-id="0ba7a-158">Unbilled sales actual – Chargeable</span></span></td>
<td><span data-ttu-id="0ba7a-159">สกุลเงินตามสัญญาโครงการ</span><span class="sxs-lookup"><span data-stu-id="0ba7a-159">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="0ba7a-160">เวลาได้รับการอนุมัติ และการลดลงของชั่วโมงที่เรียกเก็บเงินได้เกิดขึ้น ในระหว่างการอนุมัติ</span><span class="sxs-lookup"><span data-stu-id="0ba7a-160">Time is approved, and a decrease in billable hours occurs during approval.</span></span></td>
<td><span data-ttu-id="0ba7a-161">จำนวนจริงของต้นทุน</span><span class="sxs-lookup"><span data-stu-id="0ba7a-161">Cost actual</span></span></td>
<td><span data-ttu-id="0ba7a-162">สกุลเงินของหน่วยตามสัญญา</span><span class="sxs-lookup"><span data-stu-id="0ba7a-162">Contracting unit currency</span></span></td>
<td rowspan="3"><span data-ttu-id="0ba7a-163">จำนวนจริงของต้นทุน</span><span class="sxs-lookup"><span data-stu-id="0ba7a-163">Cost actual</span></span></td>
<td rowspan="3"><span data-ttu-id="0ba7a-164">สกุลเงินของหน่วยตามสัญญา</span><span class="sxs-lookup"><span data-stu-id="0ba7a-164">Contracting unit currency</span></span></td>
<td rowspan="3"><span data-ttu-id="0ba7a-165">จำนวนจริงของต้นทุน</span><span class="sxs-lookup"><span data-stu-id="0ba7a-165">Cost actual</span></span></td>
<td rowspan="3"><span data-ttu-id="0ba7a-166">จำนวนจริงของต้นทุน</span><span class="sxs-lookup"><span data-stu-id="0ba7a-166">Cost actual</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="0ba7a-167">การขายที่ยังไม่ได้เรียกเก็บและคิดค่าธรรมเนียมได้ตามจริง สำหรับปริมาณใหม่</span><span class="sxs-lookup"><span data-stu-id="0ba7a-167">Unbilled sales actual – Chargeable for the new quantity</span></span></td>
<td><span data-ttu-id="0ba7a-168">สกุลเงินตามสัญญาโครงการ</span><span class="sxs-lookup"><span data-stu-id="0ba7a-168">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="0ba7a-169">การขายที่ยังไม่ได้เรียกเก็บและคิดค่าธรรมเนียมไม่ได้ตามจริง สำหรับความแตกต่าง</span><span class="sxs-lookup"><span data-stu-id="0ba7a-169">Unbilled sales actual – Non-chargeable for the difference</span></span></td>
<td><span data-ttu-id="0ba7a-170">สกุลเงินตามสัญญาโครงการ</span><span class="sxs-lookup"><span data-stu-id="0ba7a-170">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="0ba7a-171">ใบแจ้งหนี้ได้รับการยืนยัน และไม่มีการเปลี่ยนแปลงหรือเพิ่มขึ้นของชั่วโมงที่เรียกเก็บเงินได้เกิดขึ้น</span><span class="sxs-lookup"><span data-stu-id="0ba7a-171">An invoice is confirmed, and no change to or increase in billable hours occurs.</span></span></td>
<td><span data-ttu-id="0ba7a-172">การกลับการขายที่ยังไม่ได้เรียกเก็บเงิน</span><span class="sxs-lookup"><span data-stu-id="0ba7a-172">Unbilled sales reversal</span></span></td>
<td><span data-ttu-id="0ba7a-173">สกุลเงินตามสัญญาโครงการ</span><span class="sxs-lookup"><span data-stu-id="0ba7a-173">Project contract currency</span></span></td>
<td rowspan="2"><span data-ttu-id="0ba7a-174">การขายที่เรียกเก็บเงินสำหรับไมล์สโตน</span><span class="sxs-lookup"><span data-stu-id="0ba7a-174">Billed sales for milestone</span></span></td>
<td rowspan="2"><span data-ttu-id="0ba7a-175">สกุลเงินตามสัญญาโครงการ</span><span class="sxs-lookup"><span data-stu-id="0ba7a-175">Project contract currency</span></span></td>
<td rowspan="2"><span data-ttu-id="0ba7a-176">ไม่สามารถใช้งานได้</span><span class="sxs-lookup"><span data-stu-id="0ba7a-176">Not applicable</span></span></td>
<td rowspan="2"><span data-ttu-id="0ba7a-177">ไม่สามารถใช้งานได้</span><span class="sxs-lookup"><span data-stu-id="0ba7a-177">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="0ba7a-178">การขายที่เรียกเก็บเงินแล้ว</span><span class="sxs-lookup"><span data-stu-id="0ba7a-178">Billed sales</span></span></td>
<td><span data-ttu-id="0ba7a-179">สกุลเงินตามสัญญาโครงการ</span><span class="sxs-lookup"><span data-stu-id="0ba7a-179">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="0ba7a-180">ใบแจ้งหนี้ได้รับการยืนยัน และการลดลงของชั่วโมงที่เรียกเก็บเงินได้เกิดขึ้น</span><span class="sxs-lookup"><span data-stu-id="0ba7a-180">An invoice is confirmed, and a decrease in billable hours occurs.</span></span></td>
<td><span data-ttu-id="0ba7a-181">การกลับการขายที่ยังไม่ได้เรียกเก็บเงิน</span><span class="sxs-lookup"><span data-stu-id="0ba7a-181">Unbilled sales reversal</span></span></td>
<td><span data-ttu-id="0ba7a-182">สกุลเงินตามสัญญาโครงการ</span><span class="sxs-lookup"><span data-stu-id="0ba7a-182">Project contract currency</span></span></td>
<td rowspan="3"><span data-ttu-id="0ba7a-183">ไม่สามารถใช้งานได้</span><span class="sxs-lookup"><span data-stu-id="0ba7a-183">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="0ba7a-184">ไม่สามารถใช้งานได้</span><span class="sxs-lookup"><span data-stu-id="0ba7a-184">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="0ba7a-185">ไม่สามารถใช้งานได้</span><span class="sxs-lookup"><span data-stu-id="0ba7a-185">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="0ba7a-186">ไม่สามารถใช้งานได้</span><span class="sxs-lookup"><span data-stu-id="0ba7a-186">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="0ba7a-187">การขายที่เรียกเก็บแล้วและคิดค่าธรรมเนียมได้ สำหรับปริมาณใหม่</span><span class="sxs-lookup"><span data-stu-id="0ba7a-187">Billed sales – Chargeable for the new quantity</span></span></td>
<td><span data-ttu-id="0ba7a-188">สกุลเงินตามสัญญาโครงการ</span><span class="sxs-lookup"><span data-stu-id="0ba7a-188">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="0ba7a-189">การขายที่เรียกเก็บเงินแล้วและคิดค่าธรรมเนียมไม่ได้ สำหรับความแตกต่าง</span><span class="sxs-lookup"><span data-stu-id="0ba7a-189">Billed sales – Non-chargeable for the difference</span></span></td>
<td><span data-ttu-id="0ba7a-190">สกุลเงินตามสัญญาโครงการ</span><span class="sxs-lookup"><span data-stu-id="0ba7a-190">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="0ba7a-191">ใบแจ้งหนี้จะถูกแก้ไขเพื่อเพิ่มปริมาณที่คิดค่าธรรมเนียมได้</span><span class="sxs-lookup"><span data-stu-id="0ba7a-191">An invoice is corrected to increase the chargeable quantity.</span></span></td>
<td><span data-ttu-id="0ba7a-192">การขายที่เรียกเก็บเงินแล้ว ย้อนกลับ</span><span class="sxs-lookup"><span data-stu-id="0ba7a-192">Billed sales – Reversal</span></span></td>
<td><span data-ttu-id="0ba7a-193">สกุลเงินตามสัญญาโครงการ</span><span class="sxs-lookup"><span data-stu-id="0ba7a-193">Project contract currency</span></span></td>
<td rowspan="5">
<ul>
<li><span data-ttu-id="0ba7a-194">การย้อนกลับการขายที่เรียกเก็บเงินแล้วสำหรับไมล์สโตน</span><span class="sxs-lookup"><span data-stu-id="0ba7a-194">Billed sales reversal for milestone</span></span></li>
<li><span data-ttu-id="0ba7a-195">เปลี่ยนสถานะไมล์สโตน จาก <strong>ออกใบหนี้</strong> เป็น <strong>พร้อมสำหรับใบแจ้งหนี้</strong></span><span class="sxs-lookup"><span data-stu-id="0ba7a-195">Change in milestone status from <strong>Invoiced</strong> to <strong>Ready for invoice</strong></span></span></li>
</ul>
</td>
<td rowspan="5"><span data-ttu-id="0ba7a-196">สกุลเงินตามสัญญาโครงการ</span><span class="sxs-lookup"><span data-stu-id="0ba7a-196">Project contract currency</span></span></td>
<td rowspan="5"><span data-ttu-id="0ba7a-197">ไม่สามารถใช้งานได้</span><span class="sxs-lookup"><span data-stu-id="0ba7a-197">Not applicable</span></span></td>
<td rowspan="5"><span data-ttu-id="0ba7a-198">ไม่สามารถใช้งานได้</span><span class="sxs-lookup"><span data-stu-id="0ba7a-198">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="0ba7a-199">การขายที่เรียกเก็บเงินแล้ว</span><span class="sxs-lookup"><span data-stu-id="0ba7a-199">Billed sales</span></span></td>
<td><span data-ttu-id="0ba7a-200">สกุลเงินตามสัญญาโครงการ</span><span class="sxs-lookup"><span data-stu-id="0ba7a-200">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="0ba7a-201">ใบแจ้งหนี้จะถูกแก้ไขเพื่อลดปริมาณที่คิดค่าธรรมเนียมได้</span><span class="sxs-lookup"><span data-stu-id="0ba7a-201">An invoice is corrected to decrease the chargeable quantity.</span></span></td>
<td><span data-ttu-id="0ba7a-202">การขายที่เรียกเก็บเงินแล้ว ย้อนกลับ</span><span class="sxs-lookup"><span data-stu-id="0ba7a-202">Billed sales – Reversal</span></span></td>
<td><span data-ttu-id="0ba7a-203">สกุลเงินตามสัญญาโครงการ</span><span class="sxs-lookup"><span data-stu-id="0ba7a-203">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="0ba7a-204">การขายที่เรียกเก็บเงินแล้วสำหรับปริมาณใหม่</span><span class="sxs-lookup"><span data-stu-id="0ba7a-204">Billed sales for the new quantity</span></span></td>
<td><span data-ttu-id="0ba7a-205">สกุลเงินตามสัญญาโครงการ</span><span class="sxs-lookup"><span data-stu-id="0ba7a-205">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="0ba7a-206">การขายที่ยังไม่เรียกเก็บเงินและคิดค่าธรรมเนียมได้ สำหรับความแตกต่าง</span><span class="sxs-lookup"><span data-stu-id="0ba7a-206">Unbilled sales – Chargeable for the difference</span></span></td>
<td><span data-ttu-id="0ba7a-207">สกุลเงินตามสัญญาโครงการ</span><span class="sxs-lookup"><span data-stu-id="0ba7a-207">Project contract currency</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="0ba7a-208">**ทรัพยากรเป็นของหน่วยองค์กรที่แตกต่างจากหน่วยที่ทำสัญญาของโครงการ**</span><span class="sxs-lookup"><span data-stu-id="0ba7a-208">**The resource belongs to an organizational unit that differs from the project's contracting unit**</span></span>

<table>
<thead>
<tr>
<th rowspan="3"><span data-ttu-id="0ba7a-209">เหตุการณ์</span><span class="sxs-lookup"><span data-stu-id="0ba7a-209">Event</span></span></th>
<th colspan="4"><span data-ttu-id="0ba7a-210">โครงการที่เรียกเก็บเงินได้หรือขายแล้ว</span><span class="sxs-lookup"><span data-stu-id="0ba7a-210">Billable or sold project</span></span></th>
<th rowspan="3"><span data-ttu-id="0ba7a-211">โครงการในระยะที่ำกำหนด</span><span class="sxs-lookup"><span data-stu-id="0ba7a-211">Project in the presales stage</span></span></th>
<th rowspan="3"><span data-ttu-id="0ba7a-212">โครงการภายใน</span><span class="sxs-lookup"><span data-stu-id="0ba7a-212">Internal project</span></span></th>
</tr>
<tr>
<th colspan="2"><span data-ttu-id="0ba7a-213">เวลาและวัสดุ</span><span class="sxs-lookup"><span data-stu-id="0ba7a-213">Time and materials</span></span></th>
<th colspan="2"><span data-ttu-id="0ba7a-214">ราคาคงที่</span><span class="sxs-lookup"><span data-stu-id="0ba7a-214">Fixed price</span></span></th>
</tr>
<tr>
<th><span data-ttu-id="0ba7a-215">ตามจริง</span><span class="sxs-lookup"><span data-stu-id="0ba7a-215">Actuals</span></span></th>
<th><span data-ttu-id="0ba7a-216">สกุลเงินในธุรกรรม</span><span class="sxs-lookup"><span data-stu-id="0ba7a-216">Transaction currency</span></span></th>
<th><span data-ttu-id="0ba7a-217">ราคาคงที่</span><span class="sxs-lookup"><span data-stu-id="0ba7a-217">Fixed price</span></span></th>
<th><span data-ttu-id="0ba7a-218">สกุลเงินในธุรกรรม</span><span class="sxs-lookup"><span data-stu-id="0ba7a-218">Transaction currency</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="0ba7a-219">รายการเวลาถูกสร้างขึ้น</span><span class="sxs-lookup"><span data-stu-id="0ba7a-219">A time entry is created.</span></span></td>
<td colspan="6"><span data-ttu-id="0ba7a-220">ไม่มีกิจกรรมในเอนทิตีที่เกิดขึ้นจริง</span><span class="sxs-lookup"><span data-stu-id="0ba7a-220">No activity in the Actuals entity</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="0ba7a-221">รายการเวลาถูกส่ง</span><span class="sxs-lookup"><span data-stu-id="0ba7a-221">A time entry is submitted.</span></span></td>
<td colspan="6"><span data-ttu-id="0ba7a-222">ไม่มีกิจกรรมในเอนทิตีที่เกิดขึ้นจริง</span><span class="sxs-lookup"><span data-stu-id="0ba7a-222">No activity in the Actuals entity</span></span></td>
</tr>
<tr>
<td rowspan="4"><span data-ttu-id="0ba7a-223">เวลาได้รับการอนุมัติ และไม่มีการเปลี่ยนแปลงหรือเพิ่มขึ้นของชั่วโมงที่เรียกเก็บเงินได้เกิดขึ้น ในระหว่างการอนุมัติ</span><span class="sxs-lookup"><span data-stu-id="0ba7a-223">Time is approved, and no change to or increase in billable hours occurs during approval.</span></span></td>
<td><span data-ttu-id="0ba7a-224">จำนวนจริงของต้นทุน</span><span class="sxs-lookup"><span data-stu-id="0ba7a-224">Cost actual</span></span></td>
<td><span data-ttu-id="0ba7a-225">สกุลเงินของหน่วยตามสัญญา</span><span class="sxs-lookup"><span data-stu-id="0ba7a-225">Contracting unit currency</span></span></td>
<td rowspan="4"><span data-ttu-id="0ba7a-226">จำนวนจริงของต้นทุน</span><span class="sxs-lookup"><span data-stu-id="0ba7a-226">Cost actual</span></span></td>
<td rowspan="4"><span data-ttu-id="0ba7a-227">สกุลเงินของหน่วยตามสัญญา</span><span class="sxs-lookup"><span data-stu-id="0ba7a-227">Contracting unit currency</span></span></td>
<td rowspan="4"><span data-ttu-id="0ba7a-228">จำนวนจริงของต้นทุน</span><span class="sxs-lookup"><span data-stu-id="0ba7a-228">Cost actual</span></span></td>
<td rowspan="4"><span data-ttu-id="0ba7a-229">จำนวนจริงของต้นทุน</span><span class="sxs-lookup"><span data-stu-id="0ba7a-229">Cost actual</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="0ba7a-230">การขายที่เกิดขึ้นจริงที่ยังไม่ได้เรียกเก็บและคิดค่าธรรมเนียมได้</span><span class="sxs-lookup"><span data-stu-id="0ba7a-230">Unbilled sales actual – Chargeable</span></span></td>
<td><span data-ttu-id="0ba7a-231">สกุลเงินตามสัญญาโครงการ</span><span class="sxs-lookup"><span data-stu-id="0ba7a-231">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="0ba7a-232">ต้นทุนต่อหน่วยการจัดเตรียมทรัพยากร</span><span class="sxs-lookup"><span data-stu-id="0ba7a-232">Resourcing unit cost</span></span></td>
<td><span data-ttu-id="0ba7a-233">สกุลเงินต่อหน่วยการจัดเตรียมทรัพยากร</span><span class="sxs-lookup"><span data-stu-id="0ba7a-233">Resourcing unit currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="0ba7a-234">การขายระหว่างองค์กร</span><span class="sxs-lookup"><span data-stu-id="0ba7a-234">Interorganizational sales</span></span></td>
<td><span data-ttu-id="0ba7a-235">สกุลเงินของหน่วยตามสัญญา</span><span class="sxs-lookup"><span data-stu-id="0ba7a-235">Contracting unit currency</span></span></td>
</tr>
<tr>
<td rowspan="5"><span data-ttu-id="0ba7a-236">เวลาได้รับการอนุมัติ และการลดลงของชั่วโมงที่เรียกเก็บเงินได้เกิดขึ้น ในระหว่างการอนุมัติ</span><span class="sxs-lookup"><span data-stu-id="0ba7a-236">Time is approved, and a decrease in billable hours occurs during approval.</span></span></td>
<td><span data-ttu-id="0ba7a-237">จำนวนจริงของต้นทุน</span><span class="sxs-lookup"><span data-stu-id="0ba7a-237">Cost actual</span></span></td>
<td><span data-ttu-id="0ba7a-238">สกุลเงินของหน่วยตามสัญญา</span><span class="sxs-lookup"><span data-stu-id="0ba7a-238">Contracting unit currency</span></span></td>
<td rowspan="5"><span data-ttu-id="0ba7a-239">จำนวนจริงของต้นทุน</span><span class="sxs-lookup"><span data-stu-id="0ba7a-239">Cost actual</span></span></td>
<td rowspan="5"><span data-ttu-id="0ba7a-240">สกุลเงินของหน่วยตามสัญญา</span><span class="sxs-lookup"><span data-stu-id="0ba7a-240">Contracting unit currency</span></span></td>
<td rowspan="5"><span data-ttu-id="0ba7a-241">จำนวนจริงของต้นทุน</span><span class="sxs-lookup"><span data-stu-id="0ba7a-241">Cost actual</span></span></td>
<td rowspan="5"><span data-ttu-id="0ba7a-242">จำนวนจริงของต้นทุน</span><span class="sxs-lookup"><span data-stu-id="0ba7a-242">Cost actual</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="0ba7a-243">ต้นทุนต่อหน่วยการจัดเตรียมทรัพยากร</span><span class="sxs-lookup"><span data-stu-id="0ba7a-243">Resourcing unit cost</span></span></td>
<td><span data-ttu-id="0ba7a-244">สกุลเงินต่อหน่วยการจัดเตรียมทรัพยากร</span><span class="sxs-lookup"><span data-stu-id="0ba7a-244">Resourcing unit currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="0ba7a-245">การขายระหว่างองค์กร</span><span class="sxs-lookup"><span data-stu-id="0ba7a-245">Interorganizational sales</span></span></td>
<td><span data-ttu-id="0ba7a-246">สกุลเงินของหน่วยตามสัญญา</span><span class="sxs-lookup"><span data-stu-id="0ba7a-246">Contracting unit currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="0ba7a-247">การขายที่ยังไม่ได้เรียกเก็บและคิดค่าธรรมเนียมได้ตามจริง สำหรับปริมาณใหม่</span><span class="sxs-lookup"><span data-stu-id="0ba7a-247">Unbilled sales actual – Chargeable for the new quantity</span></span></td>
<td><span data-ttu-id="0ba7a-248">สกุลเงินตามสัญญาโครงการ</span><span class="sxs-lookup"><span data-stu-id="0ba7a-248">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="0ba7a-249">การขายที่ยังไม่ได้เรียกเก็บและคิดค่าธรรมเนียมไม่ได้ตามจริง สำหรับความแตกต่าง</span><span class="sxs-lookup"><span data-stu-id="0ba7a-249">Unbilled sales actual – Non-chargeable for the difference</span></span></td>
<td><span data-ttu-id="0ba7a-250">สกุลเงินตามสัญญาโครงการ</span><span class="sxs-lookup"><span data-stu-id="0ba7a-250">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="0ba7a-251">ใบแจ้งหนี้ได้รับการยืนยัน และไม่มีการเปลี่ยนแปลงหรือเพิ่มขึ้นของชั่วโมงที่เรียกเก็บเงินได้เกิดขึ้น</span><span class="sxs-lookup"><span data-stu-id="0ba7a-251">An invoice is confirmed, and no change to or increase in billable hours occurs.</span></span></td>
<td><span data-ttu-id="0ba7a-252">การกลับการขายที่ยังไม่ได้เรียกเก็บเงิน</span><span class="sxs-lookup"><span data-stu-id="0ba7a-252">Unbilled sales reversal</span></span></td>
<td><span data-ttu-id="0ba7a-253">สกุลเงินตามสัญญาโครงการ</span><span class="sxs-lookup"><span data-stu-id="0ba7a-253">Project contract currency</span></span></td>
<td rowspan="2"><span data-ttu-id="0ba7a-254">การขายที่เรียกเก็บเงินสำหรับไมล์สโตน</span><span class="sxs-lookup"><span data-stu-id="0ba7a-254">Billed sales for milestone</span></span></td>
<td rowspan="2"><span data-ttu-id="0ba7a-255">สกุลเงินตามสัญญาโครงการ</span><span class="sxs-lookup"><span data-stu-id="0ba7a-255">Project contract currency</span></span></td>
<td rowspan="2"><span data-ttu-id="0ba7a-256">ไม่สามารถใช้งานได้</span><span class="sxs-lookup"><span data-stu-id="0ba7a-256">Not applicable</span></span></td>
<td rowspan="2"><span data-ttu-id="0ba7a-257">ไม่สามารถใช้งานได้</span><span class="sxs-lookup"><span data-stu-id="0ba7a-257">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="0ba7a-258">การขายที่เรียกเก็บเงินแล้ว</span><span class="sxs-lookup"><span data-stu-id="0ba7a-258">Billed sales</span></span></td>
<td><span data-ttu-id="0ba7a-259">สกุลเงินตามสัญญาโครงการ</span><span class="sxs-lookup"><span data-stu-id="0ba7a-259">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="0ba7a-260">ใบแจ้งหนี้ได้รับการยืนยัน และการลดลงของชั่วโมงที่เรียกเก็บเงินได้เกิดขึ้น</span><span class="sxs-lookup"><span data-stu-id="0ba7a-260">An invoice is confirmed, and a decrease in billable hours occurs.</span></span></td>
<td><span data-ttu-id="0ba7a-261">การกลับการขายที่ยังไม่ได้เรียกเก็บเงิน</span><span class="sxs-lookup"><span data-stu-id="0ba7a-261">Unbilled sales reversal</span></span></td>
<td><span data-ttu-id="0ba7a-262">สกุลเงินตามสัญญาโครงการ</span><span class="sxs-lookup"><span data-stu-id="0ba7a-262">Project contract currency</span></span></td>
<td rowspan="3"><span data-ttu-id="0ba7a-263">ไม่สามารถใช้งานได้</span><span class="sxs-lookup"><span data-stu-id="0ba7a-263">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="0ba7a-264">ไม่สามารถใช้งานได้</span><span class="sxs-lookup"><span data-stu-id="0ba7a-264">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="0ba7a-265">ไม่สามารถใช้งานได้</span><span class="sxs-lookup"><span data-stu-id="0ba7a-265">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="0ba7a-266">ไม่สามารถใช้งานได้</span><span class="sxs-lookup"><span data-stu-id="0ba7a-266">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="0ba7a-267">การขายที่เรียกเก็บแล้วและคิดค่าธรรมเนียมได้ สำหรับปริมาณใหม่</span><span class="sxs-lookup"><span data-stu-id="0ba7a-267">Billed sales – Chargeable for the new quantity</span></span></td>
<td><span data-ttu-id="0ba7a-268">สกุลเงินตามสัญญาโครงการ</span><span class="sxs-lookup"><span data-stu-id="0ba7a-268">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="0ba7a-269">การขายที่เรียกเก็บเงินแล้วและคิดค่าธรรมเนียมไม่ได้ สำหรับความแตกต่าง</span><span class="sxs-lookup"><span data-stu-id="0ba7a-269">Billed sales – Non-chargeable for the difference</span></span></td>
<td><span data-ttu-id="0ba7a-270">สกุลเงินตามสัญญาโครงการ</span><span class="sxs-lookup"><span data-stu-id="0ba7a-270">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="0ba7a-271">ใบแจ้งหนี้จะถูกแก้ไขเพื่อเพิ่มปริมาณที่คิดค่าธรรมเนียมได้</span><span class="sxs-lookup"><span data-stu-id="0ba7a-271">An invoice is corrected to increase the chargeable quantity.</span></span></td>
<td><span data-ttu-id="0ba7a-272">การขายที่เรียกเก็บเงินแล้ว ย้อนกลับ</span><span class="sxs-lookup"><span data-stu-id="0ba7a-272">Billed sales – Reversal</span></span></td>
<td><span data-ttu-id="0ba7a-273">สกุลเงินตามสัญญาโครงการ</span><span class="sxs-lookup"><span data-stu-id="0ba7a-273">Project contract currency</span></span></td>
<td rowspan="5">
<ul>
<li><span data-ttu-id="0ba7a-274">การย้อนกลับการขายที่เรียกเก็บเงินแล้วสำหรับไมล์สโตน</span><span class="sxs-lookup"><span data-stu-id="0ba7a-274">Billed sales reversal for milestone</span></span></li>
<li><span data-ttu-id="0ba7a-275">เปลี่ยนสถานะไมล์สโตน จาก <strong>ออกใบหนี้</strong> เป็น <strong>พร้อมสำหรับใบแจ้งหนี้</strong></span><span class="sxs-lookup"><span data-stu-id="0ba7a-275">Change in milestone status from <strong>Invoiced</strong> to <strong>Ready for invoice</strong></span></span></li>
</ul>
</td>
<td rowspan="5"><span data-ttu-id="0ba7a-276">สกุลเงินตามสัญญาโครงการ</span><span class="sxs-lookup"><span data-stu-id="0ba7a-276">Project contract currency</span></span></td>
<td rowspan="5"><span data-ttu-id="0ba7a-277">ไม่สามารถใช้งานได้</span><span class="sxs-lookup"><span data-stu-id="0ba7a-277">Not applicable</span></span></td>
<td rowspan="5"><span data-ttu-id="0ba7a-278">ไม่สามารถใช้งานได้</span><span class="sxs-lookup"><span data-stu-id="0ba7a-278">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="0ba7a-279">การขายที่เรียกเก็บเงินแล้ว</span><span class="sxs-lookup"><span data-stu-id="0ba7a-279">Billed sales</span></span></td>
<td><span data-ttu-id="0ba7a-280">สกุลเงินตามสัญญาโครงการ</span><span class="sxs-lookup"><span data-stu-id="0ba7a-280">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="0ba7a-281">ใบแจ้งหนี้จะถูกแก้ไขเพื่อลดปริมาณที่คิดค่าธรรมเนียมได้</span><span class="sxs-lookup"><span data-stu-id="0ba7a-281">An invoice is corrected to decrease the chargeable quantity.</span></span></td>
<td><span data-ttu-id="0ba7a-282">การขายที่เรียกเก็บเงินแล้ว ย้อนกลับ</span><span class="sxs-lookup"><span data-stu-id="0ba7a-282">Billed sales – Reversal</span></span></td>
<td><span data-ttu-id="0ba7a-283">สกุลเงินตามสัญญาโครงการ</span><span class="sxs-lookup"><span data-stu-id="0ba7a-283">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="0ba7a-284">การขายที่เรียกเก็บเงินแล้วสำหรับปริมาณใหม่</span><span class="sxs-lookup"><span data-stu-id="0ba7a-284">Billed sales for the new quantity</span></span></td>
<td><span data-ttu-id="0ba7a-285">สกุลเงินตามสัญญาโครงการ</span><span class="sxs-lookup"><span data-stu-id="0ba7a-285">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="0ba7a-286">การขายที่ยังไม่เรียกเก็บเงินและคิดค่าธรรมเนียมได้ สำหรับความแตกต่าง</span><span class="sxs-lookup"><span data-stu-id="0ba7a-286">Unbilled sales – Chargeable for the difference</span></span></td>
<td><span data-ttu-id="0ba7a-287">สกุลเงินตามสัญญาโครงการ</span><span class="sxs-lookup"><span data-stu-id="0ba7a-287">Project contract currency</span></span></td>
</tr>
</tbody>
</table>
