---
title: โฮมเพจข้อมูลจริง
description: หัวข้อนี้ให้ข้อมูลเกี่ยวกับวิธีการทำงานกับข้อมูลจริงใน Microsoft Dynamics 365 Project Operations
author: rumant
manager: AnnBe
ms.date: 09/16/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-customerservice
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: ''
ms.search.industry: ''
ms.author: rumant
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: 75ad336a995aba3505325466433a5c5e2bb3e776
ms.sourcegitcommit: 56c42d7f5995a674426a1c2a81bae897dceb391c
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 10/01/2020
ms.locfileid: "3907341"
---
# <a name="actuals"></a><span data-ttu-id="228a0-103">ข้อมูลจริง</span><span class="sxs-lookup"><span data-stu-id="228a0-103">Actuals</span></span>

<span data-ttu-id="228a0-104">_**นำไปใช้กับ:** Project Operations สำหรับสถานการณ์ตามทรัพยากร/วัสดุที่ไม่ได้เก็บในคลัง_</span><span class="sxs-lookup"><span data-stu-id="228a0-104">_**Applies to:** Project Operations for resource/non-stocked based scenarios_</span></span>

<span data-ttu-id="228a0-105">ค่าจริง คือจำนวนของงานที่เสร็จสมบูรณ์แล้วในโครงการ</span><span class="sxs-lookup"><span data-stu-id="228a0-105">Actuals are the amount of work that has been completed on a project.</span></span> <span data-ttu-id="228a0-106">สถานการณ์ดังกล่าวสร้างขึ้นจากรายการเวลาและค่าใช้จ่าย และรายการสมุดรายวันและใบแจ้งหนี้</span><span class="sxs-lookup"><span data-stu-id="228a0-106">They are created as a result of time and expense entries, and journal entries and invoices.</span></span>

## <a name="journal-lines-and-time-submission"></a><span data-ttu-id="228a0-107">การส่งบรรทัดสมุดรายวันและเวลา</span><span class="sxs-lookup"><span data-stu-id="228a0-107">Journal lines and time submission</span></span>

<span data-ttu-id="228a0-108">สำหรับข้อมูลเพิ่มเติมเกี่ยวกับรายการเวลา โปรดดู [ภาพรวมของรายการเวลา](../time/time-entry-overview.md)</span><span class="sxs-lookup"><span data-stu-id="228a0-108">For more information about time entry, see [Time entry overview](../time/time-entry-overview.md).</span></span>

### <a name="time-and-materials"></a><span data-ttu-id="228a0-109">เวลาและวัสดุ</span><span class="sxs-lookup"><span data-stu-id="228a0-109">Time and materials</span></span>

<span data-ttu-id="228a0-110">เมื่อรายการเวลาที่ส่งมีการเชื่อมโยงกับโครงการที่แม็ปกับรายละเอียดการให้บริการตามสัญญาของเวลาและวัสดุ ระบบจะสร้างบรรทัดสมุดรายวันสองรายการ รายการหนึ่งสำหรับต้นทุนและอีกรายการสำหรับการขายที่ยังไม่เรียกเก็บเงิน</span><span class="sxs-lookup"><span data-stu-id="228a0-110">When a time entry that is submitted is linked to a project that is mapped to a time-and-materials contract line, the system creates two journal lines, one for cost and one for unbilled sales.</span></span>

### <a name="fixed-price"></a><span data-ttu-id="228a0-111">ราคาคงที่</span><span class="sxs-lookup"><span data-stu-id="228a0-111">Fixed price</span></span>

<span data-ttu-id="228a0-112">เมื่อรายการเวลาที่ส่งมีการเชื่อมโยงกับโครงการที่แม็ปกับรายละเอียดการให้บริการตามสัญญาที่มีราคาคงที่ ระบบจะสร้างบรรทัดสมุดรายวันหนึ่งรายการสำหรับต้นทุน</span><span class="sxs-lookup"><span data-stu-id="228a0-112">When a time entry that is submitted is linked to a project that is mapped to a fixed-price contract line, the system creates one journal line for cost.</span></span>

### <a name="default-pricing"></a><span data-ttu-id="228a0-113">การกำหนดราคาเริ่มต้น</span><span class="sxs-lookup"><span data-stu-id="228a0-113">Default pricing</span></span>

<span data-ttu-id="228a0-114">ตรรกะสำหรับการสร้างราคาเริ่มต้นอยู่ในบรรทัดสมุดรายวัน</span><span class="sxs-lookup"><span data-stu-id="228a0-114">The logic for creating default prices resides on the journal line.</span></span> <span data-ttu-id="228a0-115">ค่าฟิลด์จากรายการเวลาจะถูกคัดลอกไปยังบรรทัดสมุดรายวัน</span><span class="sxs-lookup"><span data-stu-id="228a0-115">The field values from the time entry are copied to the journal line.</span></span> <span data-ttu-id="228a0-116">ค่าเหล่านี้รวมถึงวันที่ของธุรกรรม รายละเอียดการให้บริการตามสัญญาที่โครงการถูกแม็ปด้วย และสกุลเงินที่เป็นผลในรายการราคาที่เหมาะสม</span><span class="sxs-lookup"><span data-stu-id="228a0-116">These values include the transaction date, the contract line that the project is mapped to, and the currency result in the appropriate price list.</span></span>

<span data-ttu-id="228a0-117">ฟิลด์ที่มีผลต่อการกำหนดราคาเริ่มต้น เช่น **บทบาท** และ **หน่วยองค์กร** ใช้ในการกำหนดราคาที่เหมาะสมในบรรทัดสมุดรายวัน</span><span class="sxs-lookup"><span data-stu-id="228a0-117">The fields that affect default pricing, such as **Role** and **Org Unit**, are used to determine the appropriate price on the journal line.</span></span> <span data-ttu-id="228a0-118">คุณสามารถเพิ่มฟิลด์ที่กำหนดเองในรายการเวลา</span><span class="sxs-lookup"><span data-stu-id="228a0-118">You can add a custom field on the time entry.</span></span> <span data-ttu-id="228a0-119">หากคุณต้องการให้ค่าของฟิลด์ถูกเผยแพร่ไปยังที่เกิดขึ้นจริง ให้สร้างฟิลด์บนเอนทิตีที่เกิดขึ้นจริง และใช้การแม็ปฟิลด์เพื่อคัดลอกฟิลด์จากรายการเวลาไปยังที่เกิดขึ้นจริง</span><span class="sxs-lookup"><span data-stu-id="228a0-119">If you want the field value to be propagated to actuals, create the field on the Actuals entity, and use field mappings to copy the field from the time entry to the actual.</span></span>

## <a name="journal-lines-and-basic-expense-submission"></a><span data-ttu-id="228a0-120">การส่งบรรทัดสมุดรายวันและค่าใช้จ่ายพื้นฐาน</span><span class="sxs-lookup"><span data-stu-id="228a0-120">Journal lines and basic expense submission</span></span>

<span data-ttu-id="228a0-121">สำหรับข้อมูลเพิ่มเติมเกี่ยวกับรายการค่าใช้จ่าย โปรดดู [ภาพรวมของค่าใช้จ่าย](../expense/expense-overview.md)</span><span class="sxs-lookup"><span data-stu-id="228a0-121">For more information about expense entry, see [Expense overview](../expense/expense-overview.md).</span></span>

### <a name="time-and-materials"></a><span data-ttu-id="228a0-122">เวลาและวัสดุ</span><span class="sxs-lookup"><span data-stu-id="228a0-122">Time and materials</span></span>

<span data-ttu-id="228a0-123">เมื่อรายการค่าใช้จ่ายพื้นฐานที่ส่งมีการเชื่อมโยงกับโครงการที่แม็ปกับรายละเอียดการให้บริการตามสัญญาของเวลาและวัสดุ ระบบจะสร้างบรรทัดสมุดรายวันสองรายการ รายการหนึ่งสำหรับต้นทุนและอีกรายการสำหรับการขายที่ยังไม่เรียกเก็บเงิน</span><span class="sxs-lookup"><span data-stu-id="228a0-123">When a basic expense entry that is submitted is linked to a project that is mapped to a time-and-materials contract line, the system creates two journal lines, one for cost and one for unbilled sales.</span></span>

### <a name="fixed-price"></a><span data-ttu-id="228a0-124">ราคาคงที่</span><span class="sxs-lookup"><span data-stu-id="228a0-124">Fixed price</span></span>

<span data-ttu-id="228a0-125">เมื่อรายการค่าใช้จ่ายพื้นฐานที่ส่งมีการเชื่อมโยงกับโครงการที่แม็ปกับรายละเอียดการให้บริการตามสัญญาที่มีราคาคงที่ ระบบจะสร้างบรรทัดสมุดรายวันหนึ่งรายการสำหรับต้นทุน</span><span class="sxs-lookup"><span data-stu-id="228a0-125">When a basic expense entry that is submitted is linked to a project that is mapped to a fixed-price contract line, the system creates one journal line for cost.</span></span>

### <a name="default-pricing"></a><span data-ttu-id="228a0-126">การกำหนดราคาเริ่มต้น</span><span class="sxs-lookup"><span data-stu-id="228a0-126">Default pricing</span></span>

<span data-ttu-id="228a0-127">ตรรกะสำหรับการป้อนราคาเริ่มต้นสำหรับค่าใช้จ่ายจะขึ้นอยู่กับประเภทค่าใช้จ่าย</span><span class="sxs-lookup"><span data-stu-id="228a0-127">The logic for entering default prices for expenses is based on the expense category.</span></span> <span data-ttu-id="228a0-128">วันที่ของธุรกรรม รายละเอียดการให้บริการตามสัญญาที่โครงการถูกแม็ปด้วย และสกุลเงิน จะถูกใช้เพื่อระบุราคาตลาดที่เหมาะสม</span><span class="sxs-lookup"><span data-stu-id="228a0-128">The transaction date, the contract line that the project is mapped to, and the currency are all used to determine the appropriate price list.</span></span> <span data-ttu-id="228a0-129">อย่างไรก็ตาม ตามค่าเริ่มต้น ยอดเงินที่ป้อนสำหรับราคาจะถูกตั้งค่าโดยตรงบนบรรทัดสมุดรายวันค่าใช้จ่ายที่เกี่ยวข้องสำหรับต้นทุนและยอดขาย</span><span class="sxs-lookup"><span data-stu-id="228a0-129">However, by default, the amount that is entered for the price itself is set directly on the related expense journal lines for cost and sales.</span></span>

<span data-ttu-id="228a0-130">รายการตามประเภทของราคาเริ่มต้นต่อหน่วย ในรายการค่าใช้จ่าย ยังไม่พร้อมใช้งาน</span><span class="sxs-lookup"><span data-stu-id="228a0-130">Category-based entry of per-unit default prices on expense entries isn't available.</span></span>

## <a name="use-entry-journals-to-record-costs"></a><span data-ttu-id="228a0-131">ใช้รายการสมุดรายวันเพื่อบันทึกต้นทุน</span><span class="sxs-lookup"><span data-stu-id="228a0-131">Use entry journals to record costs</span></span>

<span data-ttu-id="228a0-132">คุณสามารถใช้รายการสมุดรายวันเพื่อบันทึกต้นทุนหรือรายได้ ในคลาสวัสดุ ค่าธรรมเนียม เวลา ค่าใช้จ่าย หรือธุรกรรมภาษีได้</span><span class="sxs-lookup"><span data-stu-id="228a0-132">You can use entry journals to record the cost or revenue in the material, fee, time, expense, or tax transaction classes.</span></span> <span data-ttu-id="228a0-133">สมุดรายวันสามารถใช้เพื่อวัตถุประสงค์ดังต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="228a0-133">Journals can be used for the following purposes:</span></span>

- <span data-ttu-id="228a0-134">บันทึกต้นทุนจริงของวัสดุและยอดขายในโครงการ</span><span class="sxs-lookup"><span data-stu-id="228a0-134">Record the actual cost of materials and sales on a project.</span></span>
- <span data-ttu-id="228a0-135">ย้ายธุรกรรมที่เกิดขึ้นจริงจากระบบอื่นไปยัง Microsoft Dynamics 365 Project Operations</span><span class="sxs-lookup"><span data-stu-id="228a0-135">Move transaction actuals from another system to Microsoft Dynamics 365 Project Operations.</span></span>
- <span data-ttu-id="228a0-136">บันทึกต้นทุนที่เกิดขึ้นในระบบอื่น</span><span class="sxs-lookup"><span data-stu-id="228a0-136">Record costs that occurred in another system.</span></span> <span data-ttu-id="228a0-137">ต้นทุนเหล่านี้อาจรวมถึงต้นทุนการจัดซื้อจัดจ้างหรือการรับเหมาช่วง</span><span class="sxs-lookup"><span data-stu-id="228a0-137">These costs can include procurement or subcontracting costs.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="228a0-138">แอปพลิเคชันไม่ตรวจสอบความถูกต้องของชนิดบรรทัดสมุดรายวันหรือการกำหนดราคาที่เกี่ยวข้องซึ่งป้อนในบรรทัดสมุดรายวัน</span><span class="sxs-lookup"><span data-stu-id="228a0-138">The application doesn't validate the journal line type or the related pricing that is entered on the journal line.</span></span> <span data-ttu-id="228a0-139">ดังนั้น เฉพาะผู้ใช้ที่ทราบถึงผลกระทบทางการบัญชีที่เกิดขึ้นจริงต่อโครงการเท่านั้นที่ควรใช้รายการสมุดรายวันเพื่อสร้างข้อมูลจริง</span><span class="sxs-lookup"><span data-stu-id="228a0-139">Therefore, only a user who is fully aware of the accounting impact that actuals have on the project should use entry journals to create actuals.</span></span> <span data-ttu-id="228a0-140">เนื่องจากผลกระทบของชนิดสมุดรายวันนี้ คุณควรเลือกอย่างรอบคอบว่าใครมีสิทธิ์ในการสร้างรายการสมุดรายวัน</span><span class="sxs-lookup"><span data-stu-id="228a0-140">Because of the impact of this journal type, you should carefully choose who has access to create entry journals.</span></span>
## <a name="record-actuals-based-on-project-events"></a><span data-ttu-id="228a0-141">บันทึกข้อมูลจริงตามเหตุการณ์ของโครงการ</span><span class="sxs-lookup"><span data-stu-id="228a0-141">Record actuals based on project events</span></span>

<span data-ttu-id="228a0-142">Project Operations จะบันทึกธุรกรรมทางการเงินที่เกิดขึ้นระหว่างโครงการ</span><span class="sxs-lookup"><span data-stu-id="228a0-142">Project Operations records the financial transactions that occur during a project.</span></span> <span data-ttu-id="228a0-143">ธุรกรรมเหล่านี้จะถูกบันทึก เป็นค่าจริง</span><span class="sxs-lookup"><span data-stu-id="228a0-143">These transactions are recorded as actuals.</span></span> <span data-ttu-id="228a0-144">ตารางต่อไปนี้แสดงชนิดที่แตกต่างกันของความจริงที่ถูกสร้าง ขึ้นอยู่กับว่าโครงการเป็นแบบในเวลาและวัสดุหรือโครงการที่มีราคาคงที่ อยู่ในระยะที่กำหนดหรือเป็นโครงการภายใน</span><span class="sxs-lookup"><span data-stu-id="228a0-144">The following tables show the different types of actuals that are created, depending on whether the project is a time-and-materials or fixed-price project, is in the presales stage, or is an internal project.</span></span>

### <a name="the-resource-belongs-to-same-organizational-unit-as-the-projects-contracting-unit"></a><span data-ttu-id="228a0-145">ทรัพยากรเป็นของหน่วยองค์กรเดียวกันกับหน่วยที่ทำสัญญาของโครงการ</span><span class="sxs-lookup"><span data-stu-id="228a0-145">The resource belongs to same organizational unit as the project's contracting unit</span></span>

<table>
<thead>
<tr>
<th rowspan="3"><span data-ttu-id="228a0-146">เหตุการณ์</span><span class="sxs-lookup"><span data-stu-id="228a0-146">Event</span></span></th>
<th colspan="4"><span data-ttu-id="228a0-147">โครงการที่เรียกเก็บเงินได้หรือขายแล้ว</span><span class="sxs-lookup"><span data-stu-id="228a0-147">Billable or sold project</span></span></th>
<th rowspan="3"><span data-ttu-id="228a0-148">โครงการในระยะที่ำกำหนด</span><span class="sxs-lookup"><span data-stu-id="228a0-148">Project in the presales stage</span></span></th>
<th rowspan="3"><span data-ttu-id="228a0-149">โครงการภายใน</span><span class="sxs-lookup"><span data-stu-id="228a0-149">Internal project</span></span></th>
</tr>
<tr>
<th colspan="2"><span data-ttu-id="228a0-150">เวลาและวัสดุ</span><span class="sxs-lookup"><span data-stu-id="228a0-150">Time and materials</span></span></th>
<th colspan="2"><span data-ttu-id="228a0-151">ราคาคงที่</span><span class="sxs-lookup"><span data-stu-id="228a0-151">Fixed price</span></span></th>
</tr>
<tr>
<th><span data-ttu-id="228a0-152">ตามจริง</span><span class="sxs-lookup"><span data-stu-id="228a0-152">Actuals</span></span></th>
<th><span data-ttu-id="228a0-153">สกุลเงินในธุรกรรม</span><span class="sxs-lookup"><span data-stu-id="228a0-153">Transaction currency</span></span></th>
<th><span data-ttu-id="228a0-154">ราคาคงที่</span><span class="sxs-lookup"><span data-stu-id="228a0-154">Fixed price</span></span></th>
<th><span data-ttu-id="228a0-155">สกุลเงินในธุรกรรม</span><span class="sxs-lookup"><span data-stu-id="228a0-155">Transaction currency</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="228a0-156">รายการเวลาถูกสร้างขึ้น</span><span class="sxs-lookup"><span data-stu-id="228a0-156">A time entry is created.</span></span></td>
<td colspan="6"><span data-ttu-id="228a0-157">ไม่มีกิจกรรมในเอนทิตีที่เกิดขึ้นจริง</span><span class="sxs-lookup"><span data-stu-id="228a0-157">No activity in the Actuals entity</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="228a0-158">รายการเวลาถูกส่ง</span><span class="sxs-lookup"><span data-stu-id="228a0-158">A time entry is submitted.</span></span></td>
<td colspan="6"><span data-ttu-id="228a0-159">ไม่มีกิจกรรมในเอนทิตีที่เกิดขึ้นจริง</span><span class="sxs-lookup"><span data-stu-id="228a0-159">No activity in the Actuals entity</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="228a0-160">เวลาได้รับการอนุมัติ และไม่มีการเปลี่ยนแปลงหรือเพิ่มขึ้นของชั่วโมงที่เรียกเก็บเงินได้เกิดขึ้น ในระหว่างการอนุมัติ</span><span class="sxs-lookup"><span data-stu-id="228a0-160">Time is approved, and no change to or increase in billable hours occurs during approval.</span></span></td>
<td><span data-ttu-id="228a0-161">จำนวนจริงของต้นทุน</span><span class="sxs-lookup"><span data-stu-id="228a0-161">Cost actual</span></span></td>
<td><span data-ttu-id="228a0-162">สกุลเงินของหน่วยตามสัญญา</span><span class="sxs-lookup"><span data-stu-id="228a0-162">Contracting unit currency</span></span></td>
<td rowspan="2"><span data-ttu-id="228a0-163">จำนวนจริงของต้นทุน</span><span class="sxs-lookup"><span data-stu-id="228a0-163">Cost actual</span></span></td>
<td rowspan="2"><span data-ttu-id="228a0-164">สกุลเงินของหน่วยตามสัญญา</span><span class="sxs-lookup"><span data-stu-id="228a0-164">Contracting unit currency</span></span>
<td rowspan="2"><span data-ttu-id="228a0-165">จำนวนจริงของต้นทุน</span><span class="sxs-lookup"><span data-stu-id="228a0-165">Cost actual</span></span></td>
<td rowspan="2"><span data-ttu-id="228a0-166">จำนวนจริงของต้นทุน</span><span class="sxs-lookup"><span data-stu-id="228a0-166">Cost actual</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="228a0-167">การขายที่เกิดขึ้นจริงที่ยังไม่ได้เรียกเก็บและคิดค่าธรรมเนียมได้</span><span class="sxs-lookup"><span data-stu-id="228a0-167">Unbilled sales actual – Chargeable</span></span></td>
<td><span data-ttu-id="228a0-168">สกุลเงินตามสัญญาโครงการ</span><span class="sxs-lookup"><span data-stu-id="228a0-168">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="228a0-169">เวลาได้รับการอนุมัติ และการลดลงของชั่วโมงที่เรียกเก็บเงินได้เกิดขึ้น ในระหว่างการอนุมัติ</span><span class="sxs-lookup"><span data-stu-id="228a0-169">Time is approved, and a decrease in billable hours occurs during approval.</span></span></td>
<td><span data-ttu-id="228a0-170">จำนวนจริงของต้นทุน</span><span class="sxs-lookup"><span data-stu-id="228a0-170">Cost actual</span></span></td>
<td><span data-ttu-id="228a0-171">สกุลเงินของหน่วยตามสัญญา</span><span class="sxs-lookup"><span data-stu-id="228a0-171">Contracting unit currency</span></span></td>
<td rowspan="3"><span data-ttu-id="228a0-172">จำนวนจริงของต้นทุน</span><span class="sxs-lookup"><span data-stu-id="228a0-172">Cost actual</span></span></td>
<td rowspan="3"><span data-ttu-id="228a0-173">สกุลเงินของหน่วยตามสัญญา</span><span class="sxs-lookup"><span data-stu-id="228a0-173">Contracting unit currency</span></span></td>
<td rowspan="3"><span data-ttu-id="228a0-174">จำนวนจริงของต้นทุน</span><span class="sxs-lookup"><span data-stu-id="228a0-174">Cost actual</span></span></td>
<td rowspan="3"><span data-ttu-id="228a0-175">จำนวนจริงของต้นทุน</span><span class="sxs-lookup"><span data-stu-id="228a0-175">Cost actual</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="228a0-176">การขายที่ยังไม่ได้เรียกเก็บและคิดค่าธรรมเนียมได้ตามจริง สำหรับปริมาณใหม่</span><span class="sxs-lookup"><span data-stu-id="228a0-176">Unbilled sales actual – Chargeable for the new quantity</span></span></td>
<td><span data-ttu-id="228a0-177">สกุลเงินตามสัญญาโครงการ</span><span class="sxs-lookup"><span data-stu-id="228a0-177">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="228a0-178">การขายที่ยังไม่ได้เรียกเก็บและคิดค่าธรรมเนียมไม่ได้ตามจริง สำหรับความแตกต่าง</span><span class="sxs-lookup"><span data-stu-id="228a0-178">Unbilled sales actual – Non-chargeable for the difference</span></span></td>
<td><span data-ttu-id="228a0-179">สกุลเงินตามสัญญาโครงการ</span><span class="sxs-lookup"><span data-stu-id="228a0-179">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="228a0-180">ใบแจ้งหนี้ได้รับการยืนยัน และไม่มีการเปลี่ยนแปลงหรือเพิ่มขึ้นของชั่วโมงที่เรียกเก็บเงินได้เกิดขึ้น</span><span class="sxs-lookup"><span data-stu-id="228a0-180">An invoice is confirmed, and no change to or increase in billable hours occurs.</span></span></td>
<td><span data-ttu-id="228a0-181">การกลับการขายที่ยังไม่ได้เรียกเก็บเงิน</span><span class="sxs-lookup"><span data-stu-id="228a0-181">Unbilled sales reversal</span></span></td>
<td><span data-ttu-id="228a0-182">สกุลเงินตามสัญญาโครงการ</span><span class="sxs-lookup"><span data-stu-id="228a0-182">Project contract currency</span></span></td>
<td rowspan="2"><span data-ttu-id="228a0-183">การขายที่เรียกเก็บเงินสำหรับไมล์สโตน</span><span class="sxs-lookup"><span data-stu-id="228a0-183">Billed sales for milestone</span></span></td>
<td rowspan="2"><span data-ttu-id="228a0-184">สกุลเงินตามสัญญาโครงการ</span><span class="sxs-lookup"><span data-stu-id="228a0-184">Project contract currency</span></span></td>
<td rowspan="2"><span data-ttu-id="228a0-185">ไม่สามารถใช้งานได้</span><span class="sxs-lookup"><span data-stu-id="228a0-185">Not applicable</span></span></td>
<td rowspan="2"><span data-ttu-id="228a0-186">ไม่สามารถใช้งานได้</span><span class="sxs-lookup"><span data-stu-id="228a0-186">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="228a0-187">การขายที่เรียกเก็บเงินแล้ว</span><span class="sxs-lookup"><span data-stu-id="228a0-187">Billed sales</span></span></td>
<td><span data-ttu-id="228a0-188">สกุลเงินตามสัญญาโครงการ</span><span class="sxs-lookup"><span data-stu-id="228a0-188">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="228a0-189">ใบแจ้งหนี้ได้รับการยืนยัน และการลดลงของชั่วโมงที่เรียกเก็บเงินได้เกิดขึ้น</span><span class="sxs-lookup"><span data-stu-id="228a0-189">An invoice is confirmed, and a decrease in billable hours occurs.</span></span></td>
<td><span data-ttu-id="228a0-190">การกลับการขายที่ยังไม่ได้เรียกเก็บเงิน</span><span class="sxs-lookup"><span data-stu-id="228a0-190">Unbilled sales reversal</span></span></td>
<td><span data-ttu-id="228a0-191">สกุลเงินตามสัญญาโครงการ</span><span class="sxs-lookup"><span data-stu-id="228a0-191">Project contract currency</span></span></td>
<td rowspan="3"><span data-ttu-id="228a0-192">ไม่สามารถใช้งานได้</span><span class="sxs-lookup"><span data-stu-id="228a0-192">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="228a0-193">ไม่สามารถใช้งานได้</span><span class="sxs-lookup"><span data-stu-id="228a0-193">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="228a0-194">ไม่สามารถใช้งานได้</span><span class="sxs-lookup"><span data-stu-id="228a0-194">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="228a0-195">ไม่สามารถใช้งานได้</span><span class="sxs-lookup"><span data-stu-id="228a0-195">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="228a0-196">การขายที่เรียกเก็บแล้วและคิดค่าธรรมเนียมได้ สำหรับปริมาณใหม่</span><span class="sxs-lookup"><span data-stu-id="228a0-196">Billed sales – Chargeable for the new quantity</span></span></td>
<td><span data-ttu-id="228a0-197">สกุลเงินตามสัญญาโครงการ</span><span class="sxs-lookup"><span data-stu-id="228a0-197">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="228a0-198">การขายที่เรียกเก็บเงินแล้วและคิดค่าธรรมเนียมไม่ได้ สำหรับความแตกต่าง</span><span class="sxs-lookup"><span data-stu-id="228a0-198">Billed sales – Non-chargeable for the difference</span></span></td>
<td><span data-ttu-id="228a0-199">สกุลเงินตามสัญญาโครงการ</span><span class="sxs-lookup"><span data-stu-id="228a0-199">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="228a0-200">ใบแจ้งหนี้จะถูกแก้ไขเพื่อเพิ่มปริมาณที่คิดค่าธรรมเนียมได้</span><span class="sxs-lookup"><span data-stu-id="228a0-200">An invoice is corrected to increase the chargeable quantity.</span></span></td>
<td><span data-ttu-id="228a0-201">การขายที่เรียกเก็บเงินแล้ว ย้อนกลับ</span><span class="sxs-lookup"><span data-stu-id="228a0-201">Billed sales – Reversal</span></span></td>
<td><span data-ttu-id="228a0-202">สกุลเงินตามสัญญาโครงการ</span><span class="sxs-lookup"><span data-stu-id="228a0-202">Project contract currency</span></span></td>
<td rowspan="5">
<ul>
<li><span data-ttu-id="228a0-203">การย้อนกลับการขายที่เรียกเก็บเงินแล้วสำหรับไมล์สโตน</span><span class="sxs-lookup"><span data-stu-id="228a0-203">Billed sales reversal for milestone</span></span></li>
<li><span data-ttu-id="228a0-204">เปลี่ยนสถานะไมล์สโตน จาก <strong>ออกใบหนี้</strong> เป็น <strong>พร้อมสำหรับใบแจ้งหนี้</strong></span><span class="sxs-lookup"><span data-stu-id="228a0-204">Change in milestone status from <strong>Invoiced</strong> to <strong>Ready for invoice</strong></span></span></li>
</ul>
</td>
<td rowspan="5"><span data-ttu-id="228a0-205">สกุลเงินตามสัญญาโครงการ</span><span class="sxs-lookup"><span data-stu-id="228a0-205">Project contract currency</span></span></td>
<td rowspan="5"><span data-ttu-id="228a0-206">ไม่สามารถใช้งานได้</span><span class="sxs-lookup"><span data-stu-id="228a0-206">Not applicable</span></span></td>
<td rowspan="5"><span data-ttu-id="228a0-207">ไม่สามารถใช้งานได้</span><span class="sxs-lookup"><span data-stu-id="228a0-207">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="228a0-208">การขายที่เรียกเก็บเงินแล้ว</span><span class="sxs-lookup"><span data-stu-id="228a0-208">Billed sales</span></span></td>
<td><span data-ttu-id="228a0-209">สกุลเงินตามสัญญาโครงการ</span><span class="sxs-lookup"><span data-stu-id="228a0-209">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="228a0-210">ใบแจ้งหนี้จะถูกแก้ไขเพื่อลดปริมาณที่คิดค่าธรรมเนียมได้</span><span class="sxs-lookup"><span data-stu-id="228a0-210">An invoice is corrected to decrease the chargeable quantity.</span></span></td>
<td><span data-ttu-id="228a0-211">การขายที่เรียกเก็บเงินแล้ว ย้อนกลับ</span><span class="sxs-lookup"><span data-stu-id="228a0-211">Billed sales – Reversal</span></span></td>
<td><span data-ttu-id="228a0-212">สกุลเงินตามสัญญาโครงการ</span><span class="sxs-lookup"><span data-stu-id="228a0-212">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="228a0-213">การขายที่เรียกเก็บเงินแล้วสำหรับปริมาณใหม่</span><span class="sxs-lookup"><span data-stu-id="228a0-213">Billed sales for the new quantity</span></span></td>
<td><span data-ttu-id="228a0-214">สกุลเงินตามสัญญาโครงการ</span><span class="sxs-lookup"><span data-stu-id="228a0-214">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="228a0-215">การขายที่ยังไม่เรียกเก็บเงินและคิดค่าธรรมเนียมได้ สำหรับความแตกต่าง</span><span class="sxs-lookup"><span data-stu-id="228a0-215">Unbilled sales – Chargeable for the difference</span></span></td>
<td><span data-ttu-id="228a0-216">สกุลเงินตามสัญญาโครงการ</span><span class="sxs-lookup"><span data-stu-id="228a0-216">Project contract currency</span></span></td>
</tr>
</tbody>
</table>

### <a name="the-resource-belongs-to-an-organizational-unit-that-differs-from-the-projects-contracting-unit"></a><span data-ttu-id="228a0-217">ทรัพยากรเป็นของหน่วยองค์กรที่แตกต่างจากหน่วยที่ทำสัญญาของโครงการ</span><span class="sxs-lookup"><span data-stu-id="228a0-217">The resource belongs to an organizational unit that differs from the project's contracting unit</span></span>

<table>
<thead>
<tr>
<th rowspan="3"><span data-ttu-id="228a0-218">เหตุการณ์</span><span class="sxs-lookup"><span data-stu-id="228a0-218">Event</span></span></th>
<th colspan="4"><span data-ttu-id="228a0-219">โครงการที่เรียกเก็บเงินได้หรือขายแล้ว</span><span class="sxs-lookup"><span data-stu-id="228a0-219">Billable or sold project</span></span></th>
<th rowspan="3"><span data-ttu-id="228a0-220">โครงการในระยะที่ำกำหนด</span><span class="sxs-lookup"><span data-stu-id="228a0-220">Project in the presales stage</span></span></th>
<th rowspan="3"><span data-ttu-id="228a0-221">โครงการภายใน</span><span class="sxs-lookup"><span data-stu-id="228a0-221">Internal project</span></span></th>
</tr>
<tr>
<th colspan="2"><span data-ttu-id="228a0-222">เวลาและวัสดุ</span><span class="sxs-lookup"><span data-stu-id="228a0-222">Time and materials</span></span></th>
<th colspan="2"><span data-ttu-id="228a0-223">ราคาคงที่</span><span class="sxs-lookup"><span data-stu-id="228a0-223">Fixed price</span></span></th>
</tr>
<tr>
<th><span data-ttu-id="228a0-224">ตามจริง</span><span class="sxs-lookup"><span data-stu-id="228a0-224">Actuals</span></span></th>
<th><span data-ttu-id="228a0-225">สกุลเงินในธุรกรรม</span><span class="sxs-lookup"><span data-stu-id="228a0-225">Transaction currency</span></span></th>
<th><span data-ttu-id="228a0-226">ราคาคงที่</span><span class="sxs-lookup"><span data-stu-id="228a0-226">Fixed price</span></span></th>
<th><span data-ttu-id="228a0-227">สกุลเงินในธุรกรรม</span><span class="sxs-lookup"><span data-stu-id="228a0-227">Transaction currency</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="228a0-228">รายการเวลาถูกสร้างขึ้น</span><span class="sxs-lookup"><span data-stu-id="228a0-228">A time entry is created.</span></span></td>
<td colspan="6"><span data-ttu-id="228a0-229">ไม่มีกิจกรรมในเอนทิตีที่เกิดขึ้นจริง</span><span class="sxs-lookup"><span data-stu-id="228a0-229">No activity in the Actuals entity</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="228a0-230">รายการเวลาถูกส่ง</span><span class="sxs-lookup"><span data-stu-id="228a0-230">A time entry is submitted.</span></span></td>
<td colspan="6"><span data-ttu-id="228a0-231">ไม่มีกิจกรรมในเอนทิตีที่เกิดขึ้นจริง</span><span class="sxs-lookup"><span data-stu-id="228a0-231">No activity in the Actuals entity</span></span></td>
</tr>
<tr>
<td rowspan="4"><span data-ttu-id="228a0-232">เวลาได้รับการอนุมัติ และไม่มีการเปลี่ยนแปลงหรือเพิ่มขึ้นของชั่วโมงที่เรียกเก็บเงินได้เกิดขึ้น ในระหว่างการอนุมัติ</span><span class="sxs-lookup"><span data-stu-id="228a0-232">Time is approved, and no change to or increase in billable hours occurs during approval.</span></span></td>
<td><span data-ttu-id="228a0-233">จำนวนจริงของต้นทุน</span><span class="sxs-lookup"><span data-stu-id="228a0-233">Cost actual</span></span></td>
<td><span data-ttu-id="228a0-234">สกุลเงินของหน่วยตามสัญญา</span><span class="sxs-lookup"><span data-stu-id="228a0-234">Contracting unit currency</span></span></td>
<td rowspan="4"><span data-ttu-id="228a0-235">จำนวนจริงของต้นทุน</span><span class="sxs-lookup"><span data-stu-id="228a0-235">Cost actual</span></span></td>
<td rowspan="4"><span data-ttu-id="228a0-236">สกุลเงินของหน่วยตามสัญญา</span><span class="sxs-lookup"><span data-stu-id="228a0-236">Contracting unit currency</span></span></td>
<td rowspan="4"><span data-ttu-id="228a0-237">จำนวนจริงของต้นทุน</span><span class="sxs-lookup"><span data-stu-id="228a0-237">Cost actual</span></span></td>
<td rowspan="4"><span data-ttu-id="228a0-238">จำนวนจริงของต้นทุน</span><span class="sxs-lookup"><span data-stu-id="228a0-238">Cost actual</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="228a0-239">การขายที่เกิดขึ้นจริงที่ยังไม่ได้เรียกเก็บและคิดค่าธรรมเนียมได้</span><span class="sxs-lookup"><span data-stu-id="228a0-239">Unbilled sales actual – Chargeable</span></span></td>
<td><span data-ttu-id="228a0-240">สกุลเงินตามสัญญาโครงการ</span><span class="sxs-lookup"><span data-stu-id="228a0-240">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="228a0-241">ต้นทุนต่อหน่วยการจัดเตรียมทรัพยากร</span><span class="sxs-lookup"><span data-stu-id="228a0-241">Resourcing unit cost</span></span></td>
<td><span data-ttu-id="228a0-242">สกุลเงินต่อหน่วยการจัดเตรียมทรัพยากร</span><span class="sxs-lookup"><span data-stu-id="228a0-242">Resourcing unit currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="228a0-243">การขายระหว่างองค์กร</span><span class="sxs-lookup"><span data-stu-id="228a0-243">Interorganizational sales</span></span></td>
<td><span data-ttu-id="228a0-244">สกุลเงินของหน่วยตามสัญญา</span><span class="sxs-lookup"><span data-stu-id="228a0-244">Contracting unit currency</span></span></td>
</tr>
<tr>
<td rowspan="5"><span data-ttu-id="228a0-245">เวลาได้รับการอนุมัติ และการลดลงของชั่วโมงที่เรียกเก็บเงินได้เกิดขึ้น ในระหว่างการอนุมัติ</span><span class="sxs-lookup"><span data-stu-id="228a0-245">Time is approved, and a decrease in billable hours occurs during approval.</span></span></td>
<td><span data-ttu-id="228a0-246">จำนวนจริงของต้นทุน</span><span class="sxs-lookup"><span data-stu-id="228a0-246">Cost actual</span></span></td>
<td><span data-ttu-id="228a0-247">สกุลเงินของหน่วยตามสัญญา</span><span class="sxs-lookup"><span data-stu-id="228a0-247">Contracting unit currency</span></span></td>
<td rowspan="5"><span data-ttu-id="228a0-248">จำนวนจริงของต้นทุน</span><span class="sxs-lookup"><span data-stu-id="228a0-248">Cost actual</span></span></td>
<td rowspan="5"><span data-ttu-id="228a0-249">สกุลเงินของหน่วยตามสัญญา</span><span class="sxs-lookup"><span data-stu-id="228a0-249">Contracting unit currency</span></span></td>
<td rowspan="5"><span data-ttu-id="228a0-250">จำนวนจริงของต้นทุน</span><span class="sxs-lookup"><span data-stu-id="228a0-250">Cost actual</span></span></td>
<td rowspan="5"><span data-ttu-id="228a0-251">จำนวนจริงของต้นทุน</span><span class="sxs-lookup"><span data-stu-id="228a0-251">Cost actual</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="228a0-252">ต้นทุนต่อหน่วยการจัดเตรียมทรัพยากร</span><span class="sxs-lookup"><span data-stu-id="228a0-252">Resourcing unit cost</span></span></td>
<td><span data-ttu-id="228a0-253">สกุลเงินต่อหน่วยการจัดเตรียมทรัพยากร</span><span class="sxs-lookup"><span data-stu-id="228a0-253">Resourcing unit currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="228a0-254">การขายระหว่างองค์กร</span><span class="sxs-lookup"><span data-stu-id="228a0-254">Interorganizational sales</span></span></td>
<td><span data-ttu-id="228a0-255">สกุลเงินของหน่วยตามสัญญา</span><span class="sxs-lookup"><span data-stu-id="228a0-255">Contracting unit currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="228a0-256">การขายที่ยังไม่ได้เรียกเก็บและคิดค่าธรรมเนียมได้ตามจริง สำหรับปริมาณใหม่</span><span class="sxs-lookup"><span data-stu-id="228a0-256">Unbilled sales actual – Chargeable for the new quantity</span></span></td>
<td><span data-ttu-id="228a0-257">สกุลเงินตามสัญญาโครงการ</span><span class="sxs-lookup"><span data-stu-id="228a0-257">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="228a0-258">การขายที่ยังไม่ได้เรียกเก็บและคิดค่าธรรมเนียมไม่ได้ตามจริง สำหรับความแตกต่าง</span><span class="sxs-lookup"><span data-stu-id="228a0-258">Unbilled sales actual – Non-chargeable for the difference</span></span></td>
<td><span data-ttu-id="228a0-259">สกุลเงินตามสัญญาโครงการ</span><span class="sxs-lookup"><span data-stu-id="228a0-259">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="228a0-260">ใบแจ้งหนี้ได้รับการยืนยัน และไม่มีการเปลี่ยนแปลงหรือเพิ่มขึ้นของชั่วโมงที่เรียกเก็บเงินได้เกิดขึ้น</span><span class="sxs-lookup"><span data-stu-id="228a0-260">An invoice is confirmed, and no change to or increase in billable hours occurs.</span></span></td>
<td><span data-ttu-id="228a0-261">การกลับการขายที่ยังไม่ได้เรียกเก็บเงิน</span><span class="sxs-lookup"><span data-stu-id="228a0-261">Unbilled sales reversal</span></span></td>
<td><span data-ttu-id="228a0-262">สกุลเงินตามสัญญาโครงการ</span><span class="sxs-lookup"><span data-stu-id="228a0-262">Project contract currency</span></span></td>
<td rowspan="2"><span data-ttu-id="228a0-263">การขายที่เรียกเก็บเงินสำหรับไมล์สโตน</span><span class="sxs-lookup"><span data-stu-id="228a0-263">Billed sales for milestone</span></span></td>
<td rowspan="2"><span data-ttu-id="228a0-264">สกุลเงินตามสัญญาโครงการ</span><span class="sxs-lookup"><span data-stu-id="228a0-264">Project contract currency</span></span></td>
<td rowspan="2"><span data-ttu-id="228a0-265">ไม่สามารถใช้งานได้</span><span class="sxs-lookup"><span data-stu-id="228a0-265">Not applicable</span></span></td>
<td rowspan="2"><span data-ttu-id="228a0-266">ไม่สามารถใช้งานได้</span><span class="sxs-lookup"><span data-stu-id="228a0-266">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="228a0-267">การขายที่เรียกเก็บเงินแล้ว</span><span class="sxs-lookup"><span data-stu-id="228a0-267">Billed sales</span></span></td>
<td><span data-ttu-id="228a0-268">สกุลเงินตามสัญญาโครงการ</span><span class="sxs-lookup"><span data-stu-id="228a0-268">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="228a0-269">ใบแจ้งหนี้ได้รับการยืนยัน และการลดลงของชั่วโมงที่เรียกเก็บเงินได้เกิดขึ้น</span><span class="sxs-lookup"><span data-stu-id="228a0-269">An invoice is confirmed, and a decrease in billable hours occurs.</span></span></td>
<td><span data-ttu-id="228a0-270">การกลับการขายที่ยังไม่ได้เรียกเก็บเงิน</span><span class="sxs-lookup"><span data-stu-id="228a0-270">Unbilled sales reversal</span></span></td>
<td><span data-ttu-id="228a0-271">สกุลเงินตามสัญญาโครงการ</span><span class="sxs-lookup"><span data-stu-id="228a0-271">Project contract currency</span></span></td>
<td rowspan="3"><span data-ttu-id="228a0-272">ไม่สามารถใช้งานได้</span><span class="sxs-lookup"><span data-stu-id="228a0-272">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="228a0-273">ไม่สามารถใช้งานได้</span><span class="sxs-lookup"><span data-stu-id="228a0-273">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="228a0-274">ไม่สามารถใช้งานได้</span><span class="sxs-lookup"><span data-stu-id="228a0-274">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="228a0-275">ไม่สามารถใช้งานได้</span><span class="sxs-lookup"><span data-stu-id="228a0-275">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="228a0-276">การขายที่เรียกเก็บแล้วและคิดค่าธรรมเนียมได้ สำหรับปริมาณใหม่</span><span class="sxs-lookup"><span data-stu-id="228a0-276">Billed sales – Chargeable for the new quantity</span></span></td>
<td><span data-ttu-id="228a0-277">สกุลเงินตามสัญญาโครงการ</span><span class="sxs-lookup"><span data-stu-id="228a0-277">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="228a0-278">การขายที่เรียกเก็บเงินแล้วและคิดค่าธรรมเนียมไม่ได้ สำหรับความแตกต่าง</span><span class="sxs-lookup"><span data-stu-id="228a0-278">Billed sales – Non-chargeable for the difference</span></span></td>
<td><span data-ttu-id="228a0-279">สกุลเงินตามสัญญาโครงการ</span><span class="sxs-lookup"><span data-stu-id="228a0-279">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="228a0-280">ใบแจ้งหนี้จะถูกแก้ไขเพื่อเพิ่มปริมาณที่คิดค่าธรรมเนียมได้</span><span class="sxs-lookup"><span data-stu-id="228a0-280">An invoice is corrected to increase the chargeable quantity.</span></span></td>
<td><span data-ttu-id="228a0-281">การขายที่เรียกเก็บเงินแล้ว ย้อนกลับ</span><span class="sxs-lookup"><span data-stu-id="228a0-281">Billed sales – Reversal</span></span></td>
<td><span data-ttu-id="228a0-282">สกุลเงินตามสัญญาโครงการ</span><span class="sxs-lookup"><span data-stu-id="228a0-282">Project contract currency</span></span></td>
<td rowspan="5">
<ul>
<li><span data-ttu-id="228a0-283">การย้อนกลับการขายที่เรียกเก็บเงินแล้วสำหรับไมล์สโตน</span><span class="sxs-lookup"><span data-stu-id="228a0-283">Billed sales reversal for milestone</span></span></li>
<li><span data-ttu-id="228a0-284">เปลี่ยนสถานะไมล์สโตน จาก <strong>ออกใบหนี้</strong> เป็น <strong>พร้อมสำหรับใบแจ้งหนี้</strong></span><span class="sxs-lookup"><span data-stu-id="228a0-284">Change in milestone status from <strong>Invoiced</strong> to <strong>Ready for invoice</strong></span></span></li>
</ul>
</td>
<td rowspan="5"><span data-ttu-id="228a0-285">สกุลเงินตามสัญญาโครงการ</span><span class="sxs-lookup"><span data-stu-id="228a0-285">Project contract currency</span></span></td>
<td rowspan="5"><span data-ttu-id="228a0-286">ไม่สามารถใช้งานได้</span><span class="sxs-lookup"><span data-stu-id="228a0-286">Not applicable</span></span></td>
<td rowspan="5"><span data-ttu-id="228a0-287">ไม่สามารถใช้งานได้</span><span class="sxs-lookup"><span data-stu-id="228a0-287">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="228a0-288">การขายที่เรียกเก็บเงินแล้ว</span><span class="sxs-lookup"><span data-stu-id="228a0-288">Billed sales</span></span></td>
<td><span data-ttu-id="228a0-289">สกุลเงินตามสัญญาโครงการ</span><span class="sxs-lookup"><span data-stu-id="228a0-289">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="228a0-290">ใบแจ้งหนี้จะถูกแก้ไขเพื่อลดปริมาณที่คิดค่าธรรมเนียมได้</span><span class="sxs-lookup"><span data-stu-id="228a0-290">An invoice is corrected to decrease the chargeable quantity.</span></span></td>
<td><span data-ttu-id="228a0-291">การขายที่เรียกเก็บเงินแล้ว ย้อนกลับ</span><span class="sxs-lookup"><span data-stu-id="228a0-291">Billed sales – Reversal</span></span></td>
<td><span data-ttu-id="228a0-292">สกุลเงินตามสัญญาโครงการ</span><span class="sxs-lookup"><span data-stu-id="228a0-292">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="228a0-293">การขายที่เรียกเก็บเงินแล้วสำหรับปริมาณใหม่</span><span class="sxs-lookup"><span data-stu-id="228a0-293">Billed sales for the new quantity</span></span></td>
<td><span data-ttu-id="228a0-294">สกุลเงินตามสัญญาโครงการ</span><span class="sxs-lookup"><span data-stu-id="228a0-294">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="228a0-295">การขายที่ยังไม่เรียกเก็บเงินและคิดค่าธรรมเนียมได้ สำหรับความแตกต่าง</span><span class="sxs-lookup"><span data-stu-id="228a0-295">Unbilled sales – Chargeable for the difference</span></span></td>
<td><span data-ttu-id="228a0-296">สกุลเงินตามสัญญาโครงการ</span><span class="sxs-lookup"><span data-stu-id="228a0-296">Project contract currency</span></span></td>
</tr>
</tbody>
</table>
