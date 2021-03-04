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
ms.openlocfilehash: 63ad6544f0ec0a893aebd8d81f3ee895e51c294e
ms.sourcegitcommit: 418fa1fe9d605b8faccc2d5dee1b04b4e753f194
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 02/10/2021
ms.locfileid: "5146146"
---
# <a name="actuals-overview"></a><span data-ttu-id="7c20e-103">ภาพรวมข้อมูลจริง</span><span class="sxs-lookup"><span data-stu-id="7c20e-103">Actuals overview</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

<span data-ttu-id="7c20e-104">ค่าจริง คือจำนวนของงานที่เสร็จสมบูรณ์แล้วในโครงการ</span><span class="sxs-lookup"><span data-stu-id="7c20e-104">Actuals are the amount of work that has been completed on a project.</span></span> <span data-ttu-id="7c20e-105">ค่าจริงของโครงการสามารถสืบย้อนกลับไปยังเอกสารต้นทางของพวกเขา</span><span class="sxs-lookup"><span data-stu-id="7c20e-105">Project actuals can be traced back to their source documents.</span></span> <span data-ttu-id="7c20e-106">เอกสารต้นทางเหล่านั้น รวมถึงเวลา ค่าใช้จ่าย และรายการสมุดรายวัน และใบแจ้งหนี้ิ่ด้วย</span><span class="sxs-lookup"><span data-stu-id="7c20e-106">Those source documents include time, expense, and journal entries, and also invoices.</span></span>

![วิธีการติดตามค่าจริงของโครงการไปยังเอกสารต้นทาง](media/basic-guide-18.png)

## <a name="submitting-a-time-entry"></a><span data-ttu-id="7c20e-108">ส่งรายการเวลา</span><span class="sxs-lookup"><span data-stu-id="7c20e-108">Submitting a time entry</span></span>

<span data-ttu-id="7c20e-109">ใน PSA เมื่อรายการเวลาถูกส่งสำหรับโครงการที่ถูกแม็ปกับรายละเอียดการให้บริการตามสัญญาในเวลาและวัสดุ จะมีการสร้างบรรทัดสมุดรายวันสองรายการ</span><span class="sxs-lookup"><span data-stu-id="7c20e-109">In PSA, when a time entry is submitted for a project that is mapped to a time-and-materials contract line, two journal lines are created.</span></span> <span data-ttu-id="7c20e-110">หนึ่งบรรทัดสำหรับต้นทุน และอีกบรรทัดสำหรับการขายที่ยังไม่ได้เรียกเก็บเงิน</span><span class="sxs-lookup"><span data-stu-id="7c20e-110">One line is for cost, and the other line is for unbilled sales.</span></span> <span data-ttu-id="7c20e-111">เมื่อรายการเวลาถูกส่งสำหรับโครงการที่ถูกแม็ปกับรายละเอียดการให้บริการตามสัญญาที่มีเวลาคงที่ จะมีการสร้างบรรทัดสมุดรายวันสำหรับต้นทุนบรรทัดเดียว</span><span class="sxs-lookup"><span data-stu-id="7c20e-111">When a time entry is submitted for a project that is mapped to a fixed-price contract line, a journal line is created only for cost.</span></span> 

<span data-ttu-id="7c20e-112">ตรรกะสำหรับการป้อนราคาเริ่มต้นอยู่บนบรรทัดสมุดรายวัน</span><span class="sxs-lookup"><span data-stu-id="7c20e-112">Logic for entering default prices resides on the journal line.</span></span> <span data-ttu-id="7c20e-113">ค่าฟิลด์ทั้งหมดจากรายการเวลาจะถูกคัดลอกไปยังบรรทัดสมุดรายวัน</span><span class="sxs-lookup"><span data-stu-id="7c20e-113">All the field values from a time entry are copied to the journal line.</span></span> <span data-ttu-id="7c20e-114">ฟิลด์เหล่านี้รวมถึงวันที่ของธุรกรรม รายละเอียดการให้บริการตามสัญญาที่โครงการถูกแม็ปด้วย และสกุลเงินที่เป็นผลในราคาตลาดที่เหมาะสม</span><span class="sxs-lookup"><span data-stu-id="7c20e-114">These fields include the date of the transaction, the contract line that the project is mapped to, and the currency result in the appropriate price list.</span></span> 

<span data-ttu-id="7c20e-115">ฟิลด์ที่มีผลต่อราคาเริ่มต้น เช่น **บทบาท** และ **หน่วยองค์กร** ทำให้เกิดราคาที่เหมาะสมที่จะป้อนโดยค่าเริ่มต้นบนบรรทัดสมุดรายวัน</span><span class="sxs-lookup"><span data-stu-id="7c20e-115">The fields that affect default prices, such as **Role** and **Org Unit**, cause an appropriate price to be entered by default on the journal line.</span></span> <span data-ttu-id="7c20e-116">หากคุณเพิ่มฟิลด์แบบกำหนดเองในรายการเวลา และคุณต้องการให้ค่าของฟิลด์ถูกเผยแพร่ไปยังที่เกิดขึ้นจริง ให้สร้างฟิลด์บนเอนทิตีที่เกิดขึ้นจริง และใช้การแม็ปฟิลด์เพื่อคัดลอกฟิลด์จากรายการเวลาไปยังที่เกิดขึ้นจริง</span><span class="sxs-lookup"><span data-stu-id="7c20e-116">If you add a custom field on the time entry, and you want the field value to be propagated to actuals, create the field on the Actuals entity, and use field mappings to copy the field from the time entry to the actual.</span></span>

## <a name="submitting-an-expense-entry"></a><span data-ttu-id="7c20e-117">การส่งรายการค่าใช้จ่าย</span><span class="sxs-lookup"><span data-stu-id="7c20e-117">Submitting an expense entry</span></span>

<span data-ttu-id="7c20e-118">ใน PSA เมื่อรายการค่าใช้จ่ายถูกส่งสำหรับโครงการที่ถูกแม็ปกับรายละเอียดการให้บริการตามสัญญาในเวลาและวัสดุ จะมีการสร้างบรรทัดสมุดรายวันสองบรรทัด</span><span class="sxs-lookup"><span data-stu-id="7c20e-118">In PSA, when an expense entry is submitted for a project that is mapped to a time-and-materials contract line, two journal lines are created.</span></span> <span data-ttu-id="7c20e-119">หนึ่งบรรทัดสำหรับต้นทุน และอีกบรรทัดสำหรับการขายที่ยังไม่ได้เรียกเก็บเงิน</span><span class="sxs-lookup"><span data-stu-id="7c20e-119">One line is for cost, and the other line is for unbilled sales.</span></span> <span data-ttu-id="7c20e-120">เมื่อรายการค่าใช้จ่ายถูกส่งสำหรับโครงการที่ถูกแม็ปกับรายละเอียดการให้บริการตามสัญญาที่มีราคาคงที่ จะมีการสร้างบรรทัดสมุดรายวันสำหรับต้นทุนบรรทัดเดียว</span><span class="sxs-lookup"><span data-stu-id="7c20e-120">When an expense entry is submitted for a project that is mapped to a fixed-price contract line, a journal line is created only for cost.</span></span>

<span data-ttu-id="7c20e-121">ตรรกะสำหรับการป้อนราคาเริ่มต้นสำหรับค่าใช้จ่าย จะขึ้นอยู่กับประเภทของค่าใช้จ่ายที่ถูกเลือก บนหน้า **รายการค่าใช้จ่าย**</span><span class="sxs-lookup"><span data-stu-id="7c20e-121">Logic for entering default prices for expenses is based on the expense category that is selected on the **Expense entry** page.</span></span> <span data-ttu-id="7c20e-122">วันที่ของธุรกรรม รายละเอียดการให้บริการตามสัญญาที่โครงการถูกแม็ปด้วย และสกุลเงิน จะถูกใช้เพื่อระบุราคาตลาดที่เหมาะสม</span><span class="sxs-lookup"><span data-stu-id="7c20e-122">The transaction date, the contract line that the project is mapped to, and the currency are all used to determine the appropriate price list.</span></span> <span data-ttu-id="7c20e-123">อย่างไรก็ตาม สำหรับราคาตัวเอง ยอดเงินป้อนโดยผู้ใช้จะถูกตั้งค่าโดยตรงบนบรรทัดสมุดรายวันค่าใช้จ่ายที่เกี่ยวข้อง สำหรับต้นทุนและยอดขายโดยค่าเริ่มต้น</span><span class="sxs-lookup"><span data-stu-id="7c20e-123">However, for the price itself, the amount that the user entered is set directly on the related expense journal lines for cost and sales by default.</span></span>

<span data-ttu-id="7c20e-124">ในเวอร์ชันปัจจุบันของ PSA รายการตามประเภทของราคาเริ่มต้นต่อหน่วย ในรายการค่าใช้จ่าย ยังไม่พร้อมใช้งาน</span><span class="sxs-lookup"><span data-stu-id="7c20e-124">In the current version of PSA, category-based entry of per-unit default prices on expense entries isn't available.</span></span>

## <a name="using-entry-journals-to-record-costs"></a><span data-ttu-id="7c20e-125">การใช้สมุดบันทึกรายการเพื่อบันทึกต้นทุน</span><span class="sxs-lookup"><span data-stu-id="7c20e-125">Using Entry journals to record costs</span></span>

<span data-ttu-id="7c20e-126">ใน PSA สมุดบันทึกรายการช่วยให้คุณสามารถบันทึกต้นทุนหรือรายได้ ในคลาสวัสดุ ค่าธรรมเนียม เวลา ค่าใช้จ่าย หรือธุรกรรมภาษีได้</span><span class="sxs-lookup"><span data-stu-id="7c20e-126">In PSA, Entry journals let you record the cost or revenue in the material, fee, time, expense, or tax transaction classes.</span></span> <span data-ttu-id="7c20e-127">สมุดรายวันมีหัวข้อ บรรทัด และการดำเนินการ **ยืนยัน**</span><span class="sxs-lookup"><span data-stu-id="7c20e-127">A journal has a header, lines, and a **Confirm** action.</span></span> <span data-ttu-id="7c20e-128">ต่อไปนี้เป็นบางสถานการณ์ที่คุณอาจใช้สมุดรายวัน:</span><span class="sxs-lookup"><span data-stu-id="7c20e-128">Here are some scenarios where you might use a journal:</span></span>

- <span data-ttu-id="7c20e-129">คุณต้องบันทึกต้นทุนที่แท้จริงของวัสดุและการขายในโครงการ</span><span class="sxs-lookup"><span data-stu-id="7c20e-129">You must record material actual costs and sales on a project.</span></span>
- <span data-ttu-id="7c20e-130">คุณต้องย้ายธุรกรรมที่เกิดขึ้นจริงจากระบบอื่นไปยัง PSA</span><span class="sxs-lookup"><span data-stu-id="7c20e-130">You must move transaction actuals from another system to PSA.</span></span>
- <span data-ttu-id="7c20e-131">คุณต้องบันทึกต้นทุนที่เกิดขึ้นในระบบอื่น เช่น ต้นทุนการจัดซื้อ หรือการรับเหมารายย่อย</span><span class="sxs-lookup"><span data-stu-id="7c20e-131">You must record costs that occurred in another system, such as procurement or subcontracting costs.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="7c20e-132">การใช้สมุดบันทึกรายการเพื่อสร้างข้อมูลจริงควรกระทำโดยผู้ใช้ที่ตระหนักดีถึงผลกระทบทางบัญชีที่เกิดขึ้นจริงต่อโครงการเท่านั้น</span><span class="sxs-lookup"><span data-stu-id="7c20e-132">Using Entry journals to create actuals should be done only by a user who is fully aware of the accounting impact the Actuals have on the project.</span></span> <span data-ttu-id="7c20e-133">เนื่องจากแอปพลิเคชันไม่ตรวจสอบความถูกต้องของประเภทรายการสมุดรายวัน หรือราคาที่เกี่ยวข้องที่ป้อนในรายการสมุดรายวัน</span><span class="sxs-lookup"><span data-stu-id="7c20e-133">This is because the application does not validate the journal line type, or the related pricing that is entered on the journal line.</span></span> <span data-ttu-id="7c20e-134">เนื่องจากผลกระทบของสมุดรายวันประเภทนี้ โปรดใช้ความระมัดระวังว่าใครจะได้รับสิทธิ์ในการสร้างสมุดบันทึกรายการ</span><span class="sxs-lookup"><span data-stu-id="7c20e-134">Because of the impact of this journal type, exercise adequate caution in who is given access to create Entry journals.</span></span>     


## <a name="recording-actuals-based-on-project-events"></a><span data-ttu-id="7c20e-135">บันทึกจริงตามเหตุการณ์ของโครงการ</span><span class="sxs-lookup"><span data-stu-id="7c20e-135">Recording actuals based on project events</span></span>

<span data-ttu-id="7c20e-136">PSA จะบันทึกธุรกรรมทางการเงินที่เกิดขึ้นระหว่างโครงการ</span><span class="sxs-lookup"><span data-stu-id="7c20e-136">PSA records the financial transactions that occur during a project.</span></span> <span data-ttu-id="7c20e-137">ธุรกรรมเหล่านี้จะถูกบันทึก เป็น **ค่าจริง**</span><span class="sxs-lookup"><span data-stu-id="7c20e-137">These transactions are recorded as **actuals**.</span></span> <span data-ttu-id="7c20e-138">ตารางต่อไปนี้แสดงชนิดที่แตกต่างกันของความจริงที่ถูกสร้าง ขึ้นอยู่กับว่าโครงการเป็นแบบในเวลาและวัสดุหรือโครงการที่มีราคาคงที่ อยู่ในระยะที่กำหนดหรือเป็นโครงการภายใน</span><span class="sxs-lookup"><span data-stu-id="7c20e-138">The following tables show the different types of actuals that are created, depending on whether the project is a time-and-materials or fixed-price project, is in the presales stage, or is an internal project.</span></span>

<span data-ttu-id="7c20e-139">**ทรัพยากรเป็นของหน่วยองค์กรเดียวกันกับหน่วยที่ทำสัญญาของโครงการ**</span><span class="sxs-lookup"><span data-stu-id="7c20e-139">**The resource belongs to same organizational unit as the project's contracting unit**</span></span>

<table>
<thead>
<tr>
<th rowspan="3"><span data-ttu-id="7c20e-140">เหตุการณ์</span><span class="sxs-lookup"><span data-stu-id="7c20e-140">Event</span></span></th>
<th colspan="4"><span data-ttu-id="7c20e-141">โครงการที่เรียกเก็บเงินได้หรือขายแล้ว</span><span class="sxs-lookup"><span data-stu-id="7c20e-141">Billable or sold project</span></span></th>
<th rowspan="3"><span data-ttu-id="7c20e-142">โครงการในระยะที่ำกำหนด</span><span class="sxs-lookup"><span data-stu-id="7c20e-142">Project in the presales stage</span></span></th>
<th rowspan="3"><span data-ttu-id="7c20e-143">โครงการภายใน</span><span class="sxs-lookup"><span data-stu-id="7c20e-143">Internal project</span></span></th>
</tr>
<tr>
<th colspan="2"><span data-ttu-id="7c20e-144">เวลาและวัสดุ</span><span class="sxs-lookup"><span data-stu-id="7c20e-144">Time and materials</span></span></th>
<th colspan="2"><span data-ttu-id="7c20e-145">ราคาคงที่</span><span class="sxs-lookup"><span data-stu-id="7c20e-145">Fixed price</span></span></th>
</tr>
<tr>
<th><span data-ttu-id="7c20e-146">ตามจริง</span><span class="sxs-lookup"><span data-stu-id="7c20e-146">Actuals</span></span></th>
<th><span data-ttu-id="7c20e-147">สกุลเงินในธุรกรรม</span><span class="sxs-lookup"><span data-stu-id="7c20e-147">Transaction currency</span></span></th>
<th><span data-ttu-id="7c20e-148">ราคาคงที่</span><span class="sxs-lookup"><span data-stu-id="7c20e-148">Fixed price</span></span></th>
<th><span data-ttu-id="7c20e-149">สกุลเงินในธุรกรรม</span><span class="sxs-lookup"><span data-stu-id="7c20e-149">Transaction currency</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="7c20e-150">รายการเวลาถูกสร้างขึ้น</span><span class="sxs-lookup"><span data-stu-id="7c20e-150">A time entry is created.</span></span></td>
<td colspan="6"><span data-ttu-id="7c20e-151">ไม่มีกิจกรรมในเอนทิตีที่เกิดขึ้นจริง</span><span class="sxs-lookup"><span data-stu-id="7c20e-151">No activity in the Actuals entity</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="7c20e-152">รายการเวลาถูกส่ง</span><span class="sxs-lookup"><span data-stu-id="7c20e-152">A time entry is submitted.</span></span></td>
<td colspan="6"><span data-ttu-id="7c20e-153">ไม่มีกิจกรรมในเอนทิตีที่เกิดขึ้นจริง</span><span class="sxs-lookup"><span data-stu-id="7c20e-153">No activity in the Actuals entity</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="7c20e-154">เวลาได้รับการอนุมัติ และไม่มีการเปลี่ยนแปลงหรือเพิ่มขึ้นของชั่วโมงที่เรียกเก็บเงินได้เกิดขึ้น ในระหว่างการอนุมัติ</span><span class="sxs-lookup"><span data-stu-id="7c20e-154">Time is approved, and no change to or increase in billable hours occurs during approval.</span></span></td>
<td><span data-ttu-id="7c20e-155">จำนวนจริงของต้นทุน</span><span class="sxs-lookup"><span data-stu-id="7c20e-155">Cost actual</span></span></td>
<td><span data-ttu-id="7c20e-156">สกุลเงินของหน่วยตามสัญญา</span><span class="sxs-lookup"><span data-stu-id="7c20e-156">Contracting unit currency</span></span></td>
<td rowspan="2"><span data-ttu-id="7c20e-157">จำนวนจริงของต้นทุน</span><span class="sxs-lookup"><span data-stu-id="7c20e-157">Cost actual</span></span></td>
<td rowspan="2"><span data-ttu-id="7c20e-158">สกุลเงินของหน่วยตามสัญญา</span><span class="sxs-lookup"><span data-stu-id="7c20e-158">Contracting unit currency</span></span>
<td rowspan="2"><span data-ttu-id="7c20e-159">จำนวนจริงของต้นทุน</span><span class="sxs-lookup"><span data-stu-id="7c20e-159">Cost actual</span></span></td>
<td rowspan="2"><span data-ttu-id="7c20e-160">จำนวนจริงของต้นทุน</span><span class="sxs-lookup"><span data-stu-id="7c20e-160">Cost actual</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="7c20e-161">การขายที่เกิดขึ้นจริงที่ยังไม่ได้เรียกเก็บและคิดค่าธรรมเนียมได้</span><span class="sxs-lookup"><span data-stu-id="7c20e-161">Unbilled sales actual – Chargeable</span></span></td>
<td><span data-ttu-id="7c20e-162">สกุลเงินตามสัญญาโครงการ</span><span class="sxs-lookup"><span data-stu-id="7c20e-162">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="7c20e-163">เวลาได้รับการอนุมัติ และการลดลงของชั่วโมงที่เรียกเก็บเงินได้เกิดขึ้น ในระหว่างการอนุมัติ</span><span class="sxs-lookup"><span data-stu-id="7c20e-163">Time is approved, and a decrease in billable hours occurs during approval.</span></span></td>
<td><span data-ttu-id="7c20e-164">จำนวนจริงของต้นทุน</span><span class="sxs-lookup"><span data-stu-id="7c20e-164">Cost actual</span></span></td>
<td><span data-ttu-id="7c20e-165">สกุลเงินของหน่วยตามสัญญา</span><span class="sxs-lookup"><span data-stu-id="7c20e-165">Contracting unit currency</span></span></td>
<td rowspan="3"><span data-ttu-id="7c20e-166">จำนวนจริงของต้นทุน</span><span class="sxs-lookup"><span data-stu-id="7c20e-166">Cost actual</span></span></td>
<td rowspan="3"><span data-ttu-id="7c20e-167">สกุลเงินของหน่วยตามสัญญา</span><span class="sxs-lookup"><span data-stu-id="7c20e-167">Contracting unit currency</span></span></td>
<td rowspan="3"><span data-ttu-id="7c20e-168">จำนวนจริงของต้นทุน</span><span class="sxs-lookup"><span data-stu-id="7c20e-168">Cost actual</span></span></td>
<td rowspan="3"><span data-ttu-id="7c20e-169">จำนวนจริงของต้นทุน</span><span class="sxs-lookup"><span data-stu-id="7c20e-169">Cost actual</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="7c20e-170">การขายที่ยังไม่ได้เรียกเก็บและคิดค่าธรรมเนียมได้ตามจริง สำหรับปริมาณใหม่</span><span class="sxs-lookup"><span data-stu-id="7c20e-170">Unbilled sales actual – Chargeable for the new quantity</span></span></td>
<td><span data-ttu-id="7c20e-171">สกุลเงินตามสัญญาโครงการ</span><span class="sxs-lookup"><span data-stu-id="7c20e-171">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="7c20e-172">การขายที่ยังไม่ได้เรียกเก็บและคิดค่าธรรมเนียมไม่ได้ตามจริง สำหรับความแตกต่าง</span><span class="sxs-lookup"><span data-stu-id="7c20e-172">Unbilled sales actual – Non-chargeable for the difference</span></span></td>
<td><span data-ttu-id="7c20e-173">สกุลเงินตามสัญญาโครงการ</span><span class="sxs-lookup"><span data-stu-id="7c20e-173">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="7c20e-174">ใบแจ้งหนี้ได้รับการยืนยัน และไม่มีการเปลี่ยนแปลงหรือเพิ่มขึ้นของชั่วโมงที่เรียกเก็บเงินได้เกิดขึ้น</span><span class="sxs-lookup"><span data-stu-id="7c20e-174">An invoice is confirmed, and no change to or increase in billable hours occurs.</span></span></td>
<td><span data-ttu-id="7c20e-175">การกลับการขายที่ยังไม่ได้เรียกเก็บเงิน</span><span class="sxs-lookup"><span data-stu-id="7c20e-175">Unbilled sales reversal</span></span></td>
<td><span data-ttu-id="7c20e-176">สกุลเงินตามสัญญาโครงการ</span><span class="sxs-lookup"><span data-stu-id="7c20e-176">Project contract currency</span></span></td>
<td rowspan="2"><span data-ttu-id="7c20e-177">การขายที่เรียกเก็บเงินสำหรับไมล์สโตน</span><span class="sxs-lookup"><span data-stu-id="7c20e-177">Billed sales for milestone</span></span></td>
<td rowspan="2"><span data-ttu-id="7c20e-178">สกุลเงินตามสัญญาโครงการ</span><span class="sxs-lookup"><span data-stu-id="7c20e-178">Project contract currency</span></span></td>
<td rowspan="2"><span data-ttu-id="7c20e-179">ไม่สามารถใช้งานได้</span><span class="sxs-lookup"><span data-stu-id="7c20e-179">Not applicable</span></span></td>
<td rowspan="2"><span data-ttu-id="7c20e-180">ไม่สามารถใช้งานได้</span><span class="sxs-lookup"><span data-stu-id="7c20e-180">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="7c20e-181">การขายที่เรียกเก็บเงินแล้ว</span><span class="sxs-lookup"><span data-stu-id="7c20e-181">Billed sales</span></span></td>
<td><span data-ttu-id="7c20e-182">สกุลเงินตามสัญญาโครงการ</span><span class="sxs-lookup"><span data-stu-id="7c20e-182">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="7c20e-183">ใบแจ้งหนี้ได้รับการยืนยัน และการลดลงของชั่วโมงที่เรียกเก็บเงินได้เกิดขึ้น</span><span class="sxs-lookup"><span data-stu-id="7c20e-183">An invoice is confirmed, and a decrease in billable hours occurs.</span></span></td>
<td><span data-ttu-id="7c20e-184">การกลับการขายที่ยังไม่ได้เรียกเก็บเงิน</span><span class="sxs-lookup"><span data-stu-id="7c20e-184">Unbilled sales reversal</span></span></td>
<td><span data-ttu-id="7c20e-185">สกุลเงินตามสัญญาโครงการ</span><span class="sxs-lookup"><span data-stu-id="7c20e-185">Project contract currency</span></span></td>
<td rowspan="3"><span data-ttu-id="7c20e-186">ไม่สามารถใช้งานได้</span><span class="sxs-lookup"><span data-stu-id="7c20e-186">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="7c20e-187">ไม่สามารถใช้งานได้</span><span class="sxs-lookup"><span data-stu-id="7c20e-187">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="7c20e-188">ไม่สามารถใช้งานได้</span><span class="sxs-lookup"><span data-stu-id="7c20e-188">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="7c20e-189">ไม่สามารถใช้งานได้</span><span class="sxs-lookup"><span data-stu-id="7c20e-189">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="7c20e-190">การขายที่เรียกเก็บแล้วและคิดค่าธรรมเนียมได้ สำหรับปริมาณใหม่</span><span class="sxs-lookup"><span data-stu-id="7c20e-190">Billed sales – Chargeable for the new quantity</span></span></td>
<td><span data-ttu-id="7c20e-191">สกุลเงินตามสัญญาโครงการ</span><span class="sxs-lookup"><span data-stu-id="7c20e-191">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="7c20e-192">การขายที่เรียกเก็บเงินแล้วและคิดค่าธรรมเนียมไม่ได้ สำหรับความแตกต่าง</span><span class="sxs-lookup"><span data-stu-id="7c20e-192">Billed sales – Non-chargeable for the difference</span></span></td>
<td><span data-ttu-id="7c20e-193">สกุลเงินตามสัญญาโครงการ</span><span class="sxs-lookup"><span data-stu-id="7c20e-193">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="7c20e-194">ใบแจ้งหนี้จะถูกแก้ไขเพื่อเพิ่มปริมาณที่คิดค่าธรรมเนียมได้</span><span class="sxs-lookup"><span data-stu-id="7c20e-194">An invoice is corrected to increase the chargeable quantity.</span></span></td>
<td><span data-ttu-id="7c20e-195">การขายที่เรียกเก็บเงินแล้ว ย้อนกลับ</span><span class="sxs-lookup"><span data-stu-id="7c20e-195">Billed sales – Reversal</span></span></td>
<td><span data-ttu-id="7c20e-196">สกุลเงินตามสัญญาโครงการ</span><span class="sxs-lookup"><span data-stu-id="7c20e-196">Project contract currency</span></span></td>
<td rowspan="5">
<ul>
<li><span data-ttu-id="7c20e-197">การย้อนกลับการขายที่เรียกเก็บเงินแล้วสำหรับไมล์สโตน</span><span class="sxs-lookup"><span data-stu-id="7c20e-197">Billed sales reversal for milestone</span></span></li>
<li><span data-ttu-id="7c20e-198">เปลี่ยนสถานะไมล์สโตน จาก <strong>ออกใบหนี้</strong> เป็น <strong>พร้อมสำหรับใบแจ้งหนี้</strong></span><span class="sxs-lookup"><span data-stu-id="7c20e-198">Change in milestone status from <strong>Invoiced</strong> to <strong>Ready for invoice</strong></span></span></li>
</ul>
</td>
<td rowspan="5"><span data-ttu-id="7c20e-199">สกุลเงินตามสัญญาโครงการ</span><span class="sxs-lookup"><span data-stu-id="7c20e-199">Project contract currency</span></span></td>
<td rowspan="5"><span data-ttu-id="7c20e-200">ไม่สามารถใช้งานได้</span><span class="sxs-lookup"><span data-stu-id="7c20e-200">Not applicable</span></span></td>
<td rowspan="5"><span data-ttu-id="7c20e-201">ไม่สามารถใช้งานได้</span><span class="sxs-lookup"><span data-stu-id="7c20e-201">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="7c20e-202">การขายที่เรียกเก็บเงินแล้ว</span><span class="sxs-lookup"><span data-stu-id="7c20e-202">Billed sales</span></span></td>
<td><span data-ttu-id="7c20e-203">สกุลเงินตามสัญญาโครงการ</span><span class="sxs-lookup"><span data-stu-id="7c20e-203">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="7c20e-204">ใบแจ้งหนี้จะถูกแก้ไขเพื่อลดปริมาณที่คิดค่าธรรมเนียมได้</span><span class="sxs-lookup"><span data-stu-id="7c20e-204">An invoice is corrected to decrease the chargeable quantity.</span></span></td>
<td><span data-ttu-id="7c20e-205">การขายที่เรียกเก็บเงินแล้ว ย้อนกลับ</span><span class="sxs-lookup"><span data-stu-id="7c20e-205">Billed sales – Reversal</span></span></td>
<td><span data-ttu-id="7c20e-206">สกุลเงินตามสัญญาโครงการ</span><span class="sxs-lookup"><span data-stu-id="7c20e-206">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="7c20e-207">การขายที่เรียกเก็บเงินแล้วสำหรับปริมาณใหม่</span><span class="sxs-lookup"><span data-stu-id="7c20e-207">Billed sales for the new quantity</span></span></td>
<td><span data-ttu-id="7c20e-208">สกุลเงินตามสัญญาโครงการ</span><span class="sxs-lookup"><span data-stu-id="7c20e-208">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="7c20e-209">การขายที่ยังไม่เรียกเก็บเงินและคิดค่าธรรมเนียมได้ สำหรับความแตกต่าง</span><span class="sxs-lookup"><span data-stu-id="7c20e-209">Unbilled sales – Chargeable for the difference</span></span></td>
<td><span data-ttu-id="7c20e-210">สกุลเงินตามสัญญาโครงการ</span><span class="sxs-lookup"><span data-stu-id="7c20e-210">Project contract currency</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="7c20e-211">**ทรัพยากรเป็นของหน่วยองค์กรที่แตกต่างจากหน่วยที่ทำสัญญาของโครงการ**</span><span class="sxs-lookup"><span data-stu-id="7c20e-211">**The resource belongs to an organizational unit that differs from the project's contracting unit**</span></span>

<table>
<thead>
<tr>
<th rowspan="3"><span data-ttu-id="7c20e-212">เหตุการณ์</span><span class="sxs-lookup"><span data-stu-id="7c20e-212">Event</span></span></th>
<th colspan="4"><span data-ttu-id="7c20e-213">โครงการที่เรียกเก็บเงินได้หรือขายแล้ว</span><span class="sxs-lookup"><span data-stu-id="7c20e-213">Billable or sold project</span></span></th>
<th rowspan="3"><span data-ttu-id="7c20e-214">โครงการในระยะที่ำกำหนด</span><span class="sxs-lookup"><span data-stu-id="7c20e-214">Project in the presales stage</span></span></th>
<th rowspan="3"><span data-ttu-id="7c20e-215">โครงการภายใน</span><span class="sxs-lookup"><span data-stu-id="7c20e-215">Internal project</span></span></th>
</tr>
<tr>
<th colspan="2"><span data-ttu-id="7c20e-216">เวลาและวัสดุ</span><span class="sxs-lookup"><span data-stu-id="7c20e-216">Time and materials</span></span></th>
<th colspan="2"><span data-ttu-id="7c20e-217">ราคาคงที่</span><span class="sxs-lookup"><span data-stu-id="7c20e-217">Fixed price</span></span></th>
</tr>
<tr>
<th><span data-ttu-id="7c20e-218">ตามจริง</span><span class="sxs-lookup"><span data-stu-id="7c20e-218">Actuals</span></span></th>
<th><span data-ttu-id="7c20e-219">สกุลเงินในธุรกรรม</span><span class="sxs-lookup"><span data-stu-id="7c20e-219">Transaction currency</span></span></th>
<th><span data-ttu-id="7c20e-220">ราคาคงที่</span><span class="sxs-lookup"><span data-stu-id="7c20e-220">Fixed price</span></span></th>
<th><span data-ttu-id="7c20e-221">สกุลเงินในธุรกรรม</span><span class="sxs-lookup"><span data-stu-id="7c20e-221">Transaction currency</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="7c20e-222">รายการเวลาถูกสร้างขึ้น</span><span class="sxs-lookup"><span data-stu-id="7c20e-222">A time entry is created.</span></span></td>
<td colspan="6"><span data-ttu-id="7c20e-223">ไม่มีกิจกรรมในเอนทิตีที่เกิดขึ้นจริง</span><span class="sxs-lookup"><span data-stu-id="7c20e-223">No activity in the Actuals entity</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="7c20e-224">รายการเวลาถูกส่ง</span><span class="sxs-lookup"><span data-stu-id="7c20e-224">A time entry is submitted.</span></span></td>
<td colspan="6"><span data-ttu-id="7c20e-225">ไม่มีกิจกรรมในเอนทิตีที่เกิดขึ้นจริง</span><span class="sxs-lookup"><span data-stu-id="7c20e-225">No activity in the Actuals entity</span></span></td>
</tr>
<tr>
<td rowspan="4"><span data-ttu-id="7c20e-226">เวลาได้รับการอนุมัติ และไม่มีการเปลี่ยนแปลงหรือเพิ่มขึ้นของชั่วโมงที่เรียกเก็บเงินได้เกิดขึ้น ในระหว่างการอนุมัติ</span><span class="sxs-lookup"><span data-stu-id="7c20e-226">Time is approved, and no change to or increase in billable hours occurs during approval.</span></span></td>
<td><span data-ttu-id="7c20e-227">จำนวนจริงของต้นทุน</span><span class="sxs-lookup"><span data-stu-id="7c20e-227">Cost actual</span></span></td>
<td><span data-ttu-id="7c20e-228">สกุลเงินของหน่วยตามสัญญา</span><span class="sxs-lookup"><span data-stu-id="7c20e-228">Contracting unit currency</span></span></td>
<td rowspan="4"><span data-ttu-id="7c20e-229">จำนวนจริงของต้นทุน</span><span class="sxs-lookup"><span data-stu-id="7c20e-229">Cost actual</span></span></td>
<td rowspan="4"><span data-ttu-id="7c20e-230">สกุลเงินของหน่วยตามสัญญา</span><span class="sxs-lookup"><span data-stu-id="7c20e-230">Contracting unit currency</span></span></td>
<td rowspan="4"><span data-ttu-id="7c20e-231">จำนวนจริงของต้นทุน</span><span class="sxs-lookup"><span data-stu-id="7c20e-231">Cost actual</span></span></td>
<td rowspan="4"><span data-ttu-id="7c20e-232">จำนวนจริงของต้นทุน</span><span class="sxs-lookup"><span data-stu-id="7c20e-232">Cost actual</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="7c20e-233">การขายที่เกิดขึ้นจริงที่ยังไม่ได้เรียกเก็บและคิดค่าธรรมเนียมได้</span><span class="sxs-lookup"><span data-stu-id="7c20e-233">Unbilled sales actual – Chargeable</span></span></td>
<td><span data-ttu-id="7c20e-234">สกุลเงินตามสัญญาโครงการ</span><span class="sxs-lookup"><span data-stu-id="7c20e-234">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="7c20e-235">ต้นทุนต่อหน่วยการจัดเตรียมทรัพยากร</span><span class="sxs-lookup"><span data-stu-id="7c20e-235">Resourcing unit cost</span></span></td>
<td><span data-ttu-id="7c20e-236">สกุลเงินต่อหน่วยการจัดเตรียมทรัพยากร</span><span class="sxs-lookup"><span data-stu-id="7c20e-236">Resourcing unit currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="7c20e-237">การขายระหว่างองค์กร</span><span class="sxs-lookup"><span data-stu-id="7c20e-237">Interorganizational sales</span></span></td>
<td><span data-ttu-id="7c20e-238">สกุลเงินของหน่วยตามสัญญา</span><span class="sxs-lookup"><span data-stu-id="7c20e-238">Contracting unit currency</span></span></td>
</tr>
<tr>
<td rowspan="5"><span data-ttu-id="7c20e-239">เวลาได้รับการอนุมัติ และการลดลงของชั่วโมงที่เรียกเก็บเงินได้เกิดขึ้น ในระหว่างการอนุมัติ</span><span class="sxs-lookup"><span data-stu-id="7c20e-239">Time is approved, and a decrease in billable hours occurs during approval.</span></span></td>
<td><span data-ttu-id="7c20e-240">จำนวนจริงของต้นทุน</span><span class="sxs-lookup"><span data-stu-id="7c20e-240">Cost actual</span></span></td>
<td><span data-ttu-id="7c20e-241">สกุลเงินของหน่วยตามสัญญา</span><span class="sxs-lookup"><span data-stu-id="7c20e-241">Contracting unit currency</span></span></td>
<td rowspan="5"><span data-ttu-id="7c20e-242">จำนวนจริงของต้นทุน</span><span class="sxs-lookup"><span data-stu-id="7c20e-242">Cost actual</span></span></td>
<td rowspan="5"><span data-ttu-id="7c20e-243">สกุลเงินของหน่วยตามสัญญา</span><span class="sxs-lookup"><span data-stu-id="7c20e-243">Contracting unit currency</span></span></td>
<td rowspan="5"><span data-ttu-id="7c20e-244">จำนวนจริงของต้นทุน</span><span class="sxs-lookup"><span data-stu-id="7c20e-244">Cost actual</span></span></td>
<td rowspan="5"><span data-ttu-id="7c20e-245">จำนวนจริงของต้นทุน</span><span class="sxs-lookup"><span data-stu-id="7c20e-245">Cost actual</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="7c20e-246">ต้นทุนต่อหน่วยการจัดเตรียมทรัพยากร</span><span class="sxs-lookup"><span data-stu-id="7c20e-246">Resourcing unit cost</span></span></td>
<td><span data-ttu-id="7c20e-247">สกุลเงินต่อหน่วยการจัดเตรียมทรัพยากร</span><span class="sxs-lookup"><span data-stu-id="7c20e-247">Resourcing unit currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="7c20e-248">การขายระหว่างองค์กร</span><span class="sxs-lookup"><span data-stu-id="7c20e-248">Interorganizational sales</span></span></td>
<td><span data-ttu-id="7c20e-249">สกุลเงินของหน่วยตามสัญญา</span><span class="sxs-lookup"><span data-stu-id="7c20e-249">Contracting unit currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="7c20e-250">การขายที่ยังไม่ได้เรียกเก็บและคิดค่าธรรมเนียมได้ตามจริง สำหรับปริมาณใหม่</span><span class="sxs-lookup"><span data-stu-id="7c20e-250">Unbilled sales actual – Chargeable for the new quantity</span></span></td>
<td><span data-ttu-id="7c20e-251">สกุลเงินตามสัญญาโครงการ</span><span class="sxs-lookup"><span data-stu-id="7c20e-251">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="7c20e-252">การขายที่ยังไม่ได้เรียกเก็บและคิดค่าธรรมเนียมไม่ได้ตามจริง สำหรับความแตกต่าง</span><span class="sxs-lookup"><span data-stu-id="7c20e-252">Unbilled sales actual – Non-chargeable for the difference</span></span></td>
<td><span data-ttu-id="7c20e-253">สกุลเงินตามสัญญาโครงการ</span><span class="sxs-lookup"><span data-stu-id="7c20e-253">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="7c20e-254">ใบแจ้งหนี้ได้รับการยืนยัน และไม่มีการเปลี่ยนแปลงหรือเพิ่มขึ้นของชั่วโมงที่เรียกเก็บเงินได้เกิดขึ้น</span><span class="sxs-lookup"><span data-stu-id="7c20e-254">An invoice is confirmed, and no change to or increase in billable hours occurs.</span></span></td>
<td><span data-ttu-id="7c20e-255">การกลับการขายที่ยังไม่ได้เรียกเก็บเงิน</span><span class="sxs-lookup"><span data-stu-id="7c20e-255">Unbilled sales reversal</span></span></td>
<td><span data-ttu-id="7c20e-256">สกุลเงินตามสัญญาโครงการ</span><span class="sxs-lookup"><span data-stu-id="7c20e-256">Project contract currency</span></span></td>
<td rowspan="2"><span data-ttu-id="7c20e-257">การขายที่เรียกเก็บเงินสำหรับไมล์สโตน</span><span class="sxs-lookup"><span data-stu-id="7c20e-257">Billed sales for milestone</span></span></td>
<td rowspan="2"><span data-ttu-id="7c20e-258">สกุลเงินตามสัญญาโครงการ</span><span class="sxs-lookup"><span data-stu-id="7c20e-258">Project contract currency</span></span></td>
<td rowspan="2"><span data-ttu-id="7c20e-259">ไม่สามารถใช้งานได้</span><span class="sxs-lookup"><span data-stu-id="7c20e-259">Not applicable</span></span></td>
<td rowspan="2"><span data-ttu-id="7c20e-260">ไม่สามารถใช้งานได้</span><span class="sxs-lookup"><span data-stu-id="7c20e-260">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="7c20e-261">การขายที่เรียกเก็บเงินแล้ว</span><span class="sxs-lookup"><span data-stu-id="7c20e-261">Billed sales</span></span></td>
<td><span data-ttu-id="7c20e-262">สกุลเงินตามสัญญาโครงการ</span><span class="sxs-lookup"><span data-stu-id="7c20e-262">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="7c20e-263">ใบแจ้งหนี้ได้รับการยืนยัน และการลดลงของชั่วโมงที่เรียกเก็บเงินได้เกิดขึ้น</span><span class="sxs-lookup"><span data-stu-id="7c20e-263">An invoice is confirmed, and a decrease in billable hours occurs.</span></span></td>
<td><span data-ttu-id="7c20e-264">การกลับการขายที่ยังไม่ได้เรียกเก็บเงิน</span><span class="sxs-lookup"><span data-stu-id="7c20e-264">Unbilled sales reversal</span></span></td>
<td><span data-ttu-id="7c20e-265">สกุลเงินตามสัญญาโครงการ</span><span class="sxs-lookup"><span data-stu-id="7c20e-265">Project contract currency</span></span></td>
<td rowspan="3"><span data-ttu-id="7c20e-266">ไม่สามารถใช้งานได้</span><span class="sxs-lookup"><span data-stu-id="7c20e-266">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="7c20e-267">ไม่สามารถใช้งานได้</span><span class="sxs-lookup"><span data-stu-id="7c20e-267">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="7c20e-268">ไม่สามารถใช้งานได้</span><span class="sxs-lookup"><span data-stu-id="7c20e-268">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="7c20e-269">ไม่สามารถใช้งานได้</span><span class="sxs-lookup"><span data-stu-id="7c20e-269">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="7c20e-270">การขายที่เรียกเก็บแล้วและคิดค่าธรรมเนียมได้ สำหรับปริมาณใหม่</span><span class="sxs-lookup"><span data-stu-id="7c20e-270">Billed sales – Chargeable for the new quantity</span></span></td>
<td><span data-ttu-id="7c20e-271">สกุลเงินตามสัญญาโครงการ</span><span class="sxs-lookup"><span data-stu-id="7c20e-271">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="7c20e-272">การขายที่เรียกเก็บเงินแล้วและคิดค่าธรรมเนียมไม่ได้ สำหรับความแตกต่าง</span><span class="sxs-lookup"><span data-stu-id="7c20e-272">Billed sales – Non-chargeable for the difference</span></span></td>
<td><span data-ttu-id="7c20e-273">สกุลเงินตามสัญญาโครงการ</span><span class="sxs-lookup"><span data-stu-id="7c20e-273">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="7c20e-274">ใบแจ้งหนี้จะถูกแก้ไขเพื่อเพิ่มปริมาณที่คิดค่าธรรมเนียมได้</span><span class="sxs-lookup"><span data-stu-id="7c20e-274">An invoice is corrected to increase the chargeable quantity.</span></span></td>
<td><span data-ttu-id="7c20e-275">การขายที่เรียกเก็บเงินแล้ว ย้อนกลับ</span><span class="sxs-lookup"><span data-stu-id="7c20e-275">Billed sales – Reversal</span></span></td>
<td><span data-ttu-id="7c20e-276">สกุลเงินตามสัญญาโครงการ</span><span class="sxs-lookup"><span data-stu-id="7c20e-276">Project contract currency</span></span></td>
<td rowspan="5">
<ul>
<li><span data-ttu-id="7c20e-277">การย้อนกลับการขายที่เรียกเก็บเงินแล้วสำหรับไมล์สโตน</span><span class="sxs-lookup"><span data-stu-id="7c20e-277">Billed sales reversal for milestone</span></span></li>
<li><span data-ttu-id="7c20e-278">เปลี่ยนสถานะไมล์สโตน จาก <strong>ออกใบหนี้</strong> เป็น <strong>พร้อมสำหรับใบแจ้งหนี้</strong></span><span class="sxs-lookup"><span data-stu-id="7c20e-278">Change in milestone status from <strong>Invoiced</strong> to <strong>Ready for invoice</strong></span></span></li>
</ul>
</td>
<td rowspan="5"><span data-ttu-id="7c20e-279">สกุลเงินตามสัญญาโครงการ</span><span class="sxs-lookup"><span data-stu-id="7c20e-279">Project contract currency</span></span></td>
<td rowspan="5"><span data-ttu-id="7c20e-280">ไม่สามารถใช้งานได้</span><span class="sxs-lookup"><span data-stu-id="7c20e-280">Not applicable</span></span></td>
<td rowspan="5"><span data-ttu-id="7c20e-281">ไม่สามารถใช้งานได้</span><span class="sxs-lookup"><span data-stu-id="7c20e-281">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="7c20e-282">การขายที่เรียกเก็บเงินแล้ว</span><span class="sxs-lookup"><span data-stu-id="7c20e-282">Billed sales</span></span></td>
<td><span data-ttu-id="7c20e-283">สกุลเงินตามสัญญาโครงการ</span><span class="sxs-lookup"><span data-stu-id="7c20e-283">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="7c20e-284">ใบแจ้งหนี้จะถูกแก้ไขเพื่อลดปริมาณที่คิดค่าธรรมเนียมได้</span><span class="sxs-lookup"><span data-stu-id="7c20e-284">An invoice is corrected to decrease the chargeable quantity.</span></span></td>
<td><span data-ttu-id="7c20e-285">การขายที่เรียกเก็บเงินแล้ว ย้อนกลับ</span><span class="sxs-lookup"><span data-stu-id="7c20e-285">Billed sales – Reversal</span></span></td>
<td><span data-ttu-id="7c20e-286">สกุลเงินตามสัญญาโครงการ</span><span class="sxs-lookup"><span data-stu-id="7c20e-286">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="7c20e-287">การขายที่เรียกเก็บเงินแล้วสำหรับปริมาณใหม่</span><span class="sxs-lookup"><span data-stu-id="7c20e-287">Billed sales for the new quantity</span></span></td>
<td><span data-ttu-id="7c20e-288">สกุลเงินตามสัญญาโครงการ</span><span class="sxs-lookup"><span data-stu-id="7c20e-288">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="7c20e-289">การขายที่ยังไม่เรียกเก็บเงินและคิดค่าธรรมเนียมได้ สำหรับความแตกต่าง</span><span class="sxs-lookup"><span data-stu-id="7c20e-289">Unbilled sales – Chargeable for the difference</span></span></td>
<td><span data-ttu-id="7c20e-290">สกุลเงินตามสัญญาโครงการ</span><span class="sxs-lookup"><span data-stu-id="7c20e-290">Project contract currency</span></span></td>
</tr>
</tbody>
</table>
