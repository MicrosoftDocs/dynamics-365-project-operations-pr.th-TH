---
title: ข้อมูลจริง
description: หัวข้อนี้ให้ข้อมูลเกี่ยวกับวิธีการทำงานกับข้อมูลจริงใน Microsoft Dynamics 365 Project Operations
author: rumant
manager: AnnBe
ms.date: 09/16/2020
ms.topic: article
ms.prod: ''
ms.service: project-operations
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: ''
ms.search.industry: ''
ms.author: rumant
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: 13c429763fa805fae5324e4dcf1bf7669e842281
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 10/28/2020
ms.locfileid: "4126346"
---
# <a name="actuals"></a><span data-ttu-id="06d64-103">ข้อมูลจริง</span><span class="sxs-lookup"><span data-stu-id="06d64-103">Actuals</span></span> 

<span data-ttu-id="06d64-104">_**นำไปใช้กับ:** Project Operations สำหรับสถานการณ์ตามทรัพยากร/วัสดุที่ไม่ได้เก็บในคลัง_</span><span class="sxs-lookup"><span data-stu-id="06d64-104">_**Applies to:** Project Operations for resource/non-stocked based scenarios_</span></span>

<span data-ttu-id="06d64-105">ค่าจริง คือจำนวนของงานที่เสร็จสมบูรณ์แล้วในโครงการ</span><span class="sxs-lookup"><span data-stu-id="06d64-105">Actuals are the amount of work that has been completed on a project.</span></span> <span data-ttu-id="06d64-106">สถานการณ์ดังกล่าวสร้างขึ้นจากรายการเวลาและค่าใช้จ่าย และรายการสมุดรายวันและใบแจ้งหนี้</span><span class="sxs-lookup"><span data-stu-id="06d64-106">They are created as a result of time and expense entries, and journal entries and invoices.</span></span>

## <a name="journal-lines-and-time-submission"></a><span data-ttu-id="06d64-107">การส่งบรรทัดสมุดรายวันและเวลา</span><span class="sxs-lookup"><span data-stu-id="06d64-107">Journal lines and time submission</span></span>

<span data-ttu-id="06d64-108">สำหรับข้อมูลเพิ่มเติมเกี่ยวกับรายการเวลา โปรดดู [ภาพรวมของรายการเวลา](../time/time-entry-overview.md)</span><span class="sxs-lookup"><span data-stu-id="06d64-108">For more information about time entry, see [Time entry overview](../time/time-entry-overview.md).</span></span>

### <a name="time-and-materials"></a><span data-ttu-id="06d64-109">เวลาและวัสดุ</span><span class="sxs-lookup"><span data-stu-id="06d64-109">Time and materials</span></span>

<span data-ttu-id="06d64-110">เมื่อรายการเวลาที่ส่งมีการเชื่อมโยงกับโครงการที่แม็ปกับรายละเอียดการให้บริการตามสัญญาของเวลาและวัสดุ ระบบจะสร้างบรรทัดสมุดรายวันสองรายการ รายการหนึ่งสำหรับต้นทุนและอีกรายการสำหรับการขายที่ยังไม่เรียกเก็บเงิน</span><span class="sxs-lookup"><span data-stu-id="06d64-110">When a time entry that is submitted is linked to a project that is mapped to a time-and-materials contract line, the system creates two journal lines, one for cost and one for unbilled sales.</span></span>

### <a name="fixed-price"></a><span data-ttu-id="06d64-111">ราคาคงที่</span><span class="sxs-lookup"><span data-stu-id="06d64-111">Fixed price</span></span>

<span data-ttu-id="06d64-112">เมื่อรายการเวลาที่ส่งมีการเชื่อมโยงกับโครงการที่แม็ปกับรายละเอียดการให้บริการตามสัญญาที่มีราคาคงที่ ระบบจะสร้างบรรทัดสมุดรายวันหนึ่งรายการสำหรับต้นทุน</span><span class="sxs-lookup"><span data-stu-id="06d64-112">When a time entry that is submitted is linked to a project that is mapped to a fixed-price contract line, the system creates one journal line for cost.</span></span>

### <a name="default-pricing"></a><span data-ttu-id="06d64-113">การกำหนดราคาเริ่มต้น</span><span class="sxs-lookup"><span data-stu-id="06d64-113">Default pricing</span></span>

<span data-ttu-id="06d64-114">ตรรกะสำหรับการสร้างราคาเริ่มต้นอยู่ในบรรทัดสมุดรายวัน</span><span class="sxs-lookup"><span data-stu-id="06d64-114">The logic for creating default prices resides on the journal line.</span></span> <span data-ttu-id="06d64-115">ค่าฟิลด์จากรายการเวลาจะถูกคัดลอกไปยังบรรทัดสมุดรายวัน</span><span class="sxs-lookup"><span data-stu-id="06d64-115">The field values from the time entry are copied to the journal line.</span></span> <span data-ttu-id="06d64-116">ค่าเหล่านี้รวมถึงวันที่ของธุรกรรม รายละเอียดการให้บริการตามสัญญาที่โครงการถูกแม็ปด้วย และสกุลเงินที่เป็นผลในรายการราคาที่เหมาะสม</span><span class="sxs-lookup"><span data-stu-id="06d64-116">These values include the transaction date, the contract line that the project is mapped to, and the currency result in the appropriate price list.</span></span>

<span data-ttu-id="06d64-117">ฟิลด์ที่มีผลต่อการกำหนดราคาเริ่มต้น เช่น **บทบาท** และ **หน่วยองค์กร** ใช้ในการกำหนดราคาที่เหมาะสมในบรรทัดสมุดรายวัน</span><span class="sxs-lookup"><span data-stu-id="06d64-117">The fields that affect default pricing, such as **Role** and **Org Unit**, are used to determine the appropriate price on the journal line.</span></span> <span data-ttu-id="06d64-118">คุณสามารถเพิ่มฟิลด์ที่กำหนดเองในรายการเวลา</span><span class="sxs-lookup"><span data-stu-id="06d64-118">You can add a custom field on the time entry.</span></span> <span data-ttu-id="06d64-119">หากคุณต้องการให้ค่าของฟิลด์ถูกเผยแพร่ไปยังที่เกิดขึ้นจริง ให้สร้างฟิลด์บนเอนทิตีที่เกิดขึ้นจริง และใช้การแม็ปฟิลด์เพื่อคัดลอกฟิลด์จากรายการเวลาไปยังที่เกิดขึ้นจริง</span><span class="sxs-lookup"><span data-stu-id="06d64-119">If you want the field value to be propagated to actuals, create the field on the Actuals entity, and use field mappings to copy the field from the time entry to the actual.</span></span>

## <a name="journal-lines-and-basic-expense-submission"></a><span data-ttu-id="06d64-120">การส่งบรรทัดสมุดรายวันและค่าใช้จ่ายพื้นฐาน</span><span class="sxs-lookup"><span data-stu-id="06d64-120">Journal lines and basic expense submission</span></span>

<span data-ttu-id="06d64-121">สำหรับข้อมูลเพิ่มเติมเกี่ยวกับรายการค่าใช้จ่าย โปรดดู [ภาพรวมของค่าใช้จ่าย](../expense/expense-overview.md)</span><span class="sxs-lookup"><span data-stu-id="06d64-121">For more information about expense entry, see [Expense overview](../expense/expense-overview.md).</span></span>

### <a name="time-and-materials"></a><span data-ttu-id="06d64-122">เวลาและวัสดุ</span><span class="sxs-lookup"><span data-stu-id="06d64-122">Time and materials</span></span>

<span data-ttu-id="06d64-123">เมื่อรายการค่าใช้จ่ายพื้นฐานที่ส่งมีการเชื่อมโยงกับโครงการที่แม็ปกับรายละเอียดการให้บริการตามสัญญาของเวลาและวัสดุ ระบบจะสร้างบรรทัดสมุดรายวันสองรายการ รายการหนึ่งสำหรับต้นทุนและอีกรายการสำหรับการขายที่ยังไม่เรียกเก็บเงิน</span><span class="sxs-lookup"><span data-stu-id="06d64-123">When a basic expense entry that is submitted is linked to a project that is mapped to a time-and-materials contract line, the system creates two journal lines, one for cost and one for unbilled sales.</span></span>

### <a name="fixed-price"></a><span data-ttu-id="06d64-124">ราคาคงที่</span><span class="sxs-lookup"><span data-stu-id="06d64-124">Fixed price</span></span>

<span data-ttu-id="06d64-125">เมื่อรายการค่าใช้จ่ายพื้นฐานที่ส่งมีการเชื่อมโยงกับโครงการที่แม็ปกับรายละเอียดการให้บริการตามสัญญาที่มีราคาคงที่ ระบบจะสร้างบรรทัดสมุดรายวันหนึ่งรายการสำหรับต้นทุน</span><span class="sxs-lookup"><span data-stu-id="06d64-125">When a basic expense entry that is submitted is linked to a project that is mapped to a fixed-price contract line, the system creates one journal line for cost.</span></span>

### <a name="default-pricing"></a><span data-ttu-id="06d64-126">การกำหนดราคาเริ่มต้น</span><span class="sxs-lookup"><span data-stu-id="06d64-126">Default pricing</span></span>

<span data-ttu-id="06d64-127">ตรรกะสำหรับการป้อนราคาเริ่มต้นสำหรับค่าใช้จ่ายจะขึ้นอยู่กับประเภทค่าใช้จ่าย</span><span class="sxs-lookup"><span data-stu-id="06d64-127">The logic for entering default prices for expenses is based on the expense category.</span></span> <span data-ttu-id="06d64-128">วันที่ของธุรกรรม รายละเอียดการให้บริการตามสัญญาที่โครงการถูกแม็ปด้วย และสกุลเงิน จะถูกใช้เพื่อระบุราคาตลาดที่เหมาะสม</span><span class="sxs-lookup"><span data-stu-id="06d64-128">The transaction date, the contract line that the project is mapped to, and the currency are all used to determine the appropriate price list.</span></span> <span data-ttu-id="06d64-129">อย่างไรก็ตาม ตามค่าเริ่มต้น ยอดเงินที่ป้อนสำหรับราคาจะถูกตั้งค่าโดยตรงบนบรรทัดสมุดรายวันค่าใช้จ่ายที่เกี่ยวข้องสำหรับต้นทุนและยอดขาย</span><span class="sxs-lookup"><span data-stu-id="06d64-129">However, by default, the amount that is entered for the price itself is set directly on the related expense journal lines for cost and sales.</span></span>

<span data-ttu-id="06d64-130">รายการตามประเภทของราคาเริ่มต้นต่อหน่วย ในรายการค่าใช้จ่าย ยังไม่พร้อมใช้งาน</span><span class="sxs-lookup"><span data-stu-id="06d64-130">Category-based entry of per-unit default prices on expense entries isn't available.</span></span>

## <a name="use-entry-journals-to-record-costs"></a><span data-ttu-id="06d64-131">ใช้รายการสมุดรายวันเพื่อบันทึกต้นทุน</span><span class="sxs-lookup"><span data-stu-id="06d64-131">Use entry journals to record costs</span></span>

<span data-ttu-id="06d64-132">คุณสามารถใช้รายการสมุดรายวันเพื่อบันทึกต้นทุนหรือรายได้ ในคลาสวัสดุ ค่าธรรมเนียม เวลา ค่าใช้จ่าย หรือธุรกรรมภาษีได้</span><span class="sxs-lookup"><span data-stu-id="06d64-132">You can use entry journals to record the cost or revenue in the material, fee, time, expense, or tax transaction classes.</span></span> <span data-ttu-id="06d64-133">สมุดรายวันสามารถใช้เพื่อวัตถุประสงค์ดังต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="06d64-133">Journals can be used for the following purposes:</span></span>

- <span data-ttu-id="06d64-134">บันทึกต้นทุนจริงของวัสดุและยอดขายในโครงการ</span><span class="sxs-lookup"><span data-stu-id="06d64-134">Record the actual cost of materials and sales on a project.</span></span>
- <span data-ttu-id="06d64-135">ย้ายธุรกรรมที่เกิดขึ้นจริงจากระบบอื่นไปยัง Microsoft Dynamics 365 Project Operations</span><span class="sxs-lookup"><span data-stu-id="06d64-135">Move transaction actuals from another system to Microsoft Dynamics 365 Project Operations.</span></span>
- <span data-ttu-id="06d64-136">บันทึกต้นทุนที่เกิดขึ้นในระบบอื่น</span><span class="sxs-lookup"><span data-stu-id="06d64-136">Record costs that occurred in another system.</span></span> <span data-ttu-id="06d64-137">ต้นทุนเหล่านี้อาจรวมถึงต้นทุนการจัดซื้อจัดจ้างหรือการรับเหมาช่วง</span><span class="sxs-lookup"><span data-stu-id="06d64-137">These costs can include procurement or subcontracting costs.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="06d64-138">แอปพลิเคชันไม่ตรวจสอบความถูกต้องของชนิดบรรทัดสมุดรายวันหรือการกำหนดราคาที่เกี่ยวข้องซึ่งป้อนในบรรทัดสมุดรายวัน</span><span class="sxs-lookup"><span data-stu-id="06d64-138">The application doesn't validate the journal line type or the related pricing that is entered on the journal line.</span></span> <span data-ttu-id="06d64-139">ดังนั้น เฉพาะผู้ใช้ที่ทราบถึงผลกระทบทางการบัญชีที่เกิดขึ้นจริงต่อโครงการเท่านั้นที่ควรใช้รายการสมุดรายวันเพื่อสร้างข้อมูลจริง</span><span class="sxs-lookup"><span data-stu-id="06d64-139">Therefore, only a user who is fully aware of the accounting impact that actuals have on the project should use entry journals to create actuals.</span></span> <span data-ttu-id="06d64-140">เนื่องจากผลกระทบของชนิดสมุดรายวันนี้ คุณควรเลือกอย่างรอบคอบว่าใครมีสิทธิ์ในการสร้างรายการสมุดรายวัน</span><span class="sxs-lookup"><span data-stu-id="06d64-140">Because of the impact of this journal type, you should carefully choose who has access to create entry journals.</span></span>
## <a name="record-actuals-based-on-project-events"></a><span data-ttu-id="06d64-141">บันทึกข้อมูลจริงตามเหตุการณ์ของโครงการ</span><span class="sxs-lookup"><span data-stu-id="06d64-141">Record actuals based on project events</span></span>

<span data-ttu-id="06d64-142">Project Operations จะบันทึกธุรกรรมทางการเงินที่เกิดขึ้นระหว่างโครงการ</span><span class="sxs-lookup"><span data-stu-id="06d64-142">Project Operations records the financial transactions that occur during a project.</span></span> <span data-ttu-id="06d64-143">ธุรกรรมเหล่านี้จะถูกบันทึก เป็นค่าจริง</span><span class="sxs-lookup"><span data-stu-id="06d64-143">These transactions are recorded as actuals.</span></span> <span data-ttu-id="06d64-144">ตารางต่อไปนี้แสดงชนิดที่แตกต่างกันของความจริงที่ถูกสร้าง ขึ้นอยู่กับว่าโครงการเป็นแบบในเวลาและวัสดุหรือโครงการที่มีราคาคงที่ อยู่ในระยะที่กำหนดหรือเป็นโครงการภายใน</span><span class="sxs-lookup"><span data-stu-id="06d64-144">The following tables show the different types of actuals that are created, depending on whether the project is a time-and-materials or fixed-price project, is in the presales stage, or is an internal project.</span></span>

### <a name="the-resource-belongs-to-same-organizational-unit-as-the-projects-contracting-unit"></a><span data-ttu-id="06d64-145">ทรัพยากรเป็นของหน่วยองค์กรเดียวกันกับหน่วยที่ทำสัญญาของโครงการ</span><span class="sxs-lookup"><span data-stu-id="06d64-145">The resource belongs to same organizational unit as the project's contracting unit</span></span>

<table>
<thead>
<tr>
<th rowspan="3"><span data-ttu-id="06d64-146">เหตุการณ์</span><span class="sxs-lookup"><span data-stu-id="06d64-146">Event</span></span></th>
<th colspan="4"><span data-ttu-id="06d64-147">โครงการที่เรียกเก็บเงินได้หรือขายแล้ว</span><span class="sxs-lookup"><span data-stu-id="06d64-147">Billable or sold project</span></span></th>
<th rowspan="3"><span data-ttu-id="06d64-148">โครงการในระยะที่ำกำหนด</span><span class="sxs-lookup"><span data-stu-id="06d64-148">Project in the presales stage</span></span></th>
<th rowspan="3"><span data-ttu-id="06d64-149">โครงการภายใน</span><span class="sxs-lookup"><span data-stu-id="06d64-149">Internal project</span></span></th>
</tr>
<tr>
<th colspan="2"><span data-ttu-id="06d64-150">เวลาและวัสดุ</span><span class="sxs-lookup"><span data-stu-id="06d64-150">Time and materials</span></span></th>
<th colspan="2"><span data-ttu-id="06d64-151">ราคาคงที่</span><span class="sxs-lookup"><span data-stu-id="06d64-151">Fixed price</span></span></th>
</tr>
<tr>
<th><span data-ttu-id="06d64-152">ตามจริง</span><span class="sxs-lookup"><span data-stu-id="06d64-152">Actuals</span></span></th>
<th><span data-ttu-id="06d64-153">สกุลเงินในธุรกรรม</span><span class="sxs-lookup"><span data-stu-id="06d64-153">Transaction currency</span></span></th>
<th><span data-ttu-id="06d64-154">ราคาคงที่</span><span class="sxs-lookup"><span data-stu-id="06d64-154">Fixed price</span></span></th>
<th><span data-ttu-id="06d64-155">สกุลเงินในธุรกรรม</span><span class="sxs-lookup"><span data-stu-id="06d64-155">Transaction currency</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="06d64-156">รายการเวลาถูกสร้างขึ้น</span><span class="sxs-lookup"><span data-stu-id="06d64-156">A time entry is created.</span></span></td>
<td colspan="6"><span data-ttu-id="06d64-157">ไม่มีกิจกรรมในเอนทิตีที่เกิดขึ้นจริง</span><span class="sxs-lookup"><span data-stu-id="06d64-157">No activity in the Actuals entity</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="06d64-158">รายการเวลาถูกส่ง</span><span class="sxs-lookup"><span data-stu-id="06d64-158">A time entry is submitted.</span></span></td>
<td colspan="6"><span data-ttu-id="06d64-159">ไม่มีกิจกรรมในเอนทิตีที่เกิดขึ้นจริง</span><span class="sxs-lookup"><span data-stu-id="06d64-159">No activity in the Actuals entity</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="06d64-160">เวลาได้รับการอนุมัติ และไม่มีการเปลี่ยนแปลงหรือเพิ่มขึ้นของชั่วโมงที่เรียกเก็บเงินได้เกิดขึ้น ในระหว่างการอนุมัติ</span><span class="sxs-lookup"><span data-stu-id="06d64-160">Time is approved, and no change to or increase in billable hours occurs during approval.</span></span></td>
<td><span data-ttu-id="06d64-161">จำนวนจริงของต้นทุน</span><span class="sxs-lookup"><span data-stu-id="06d64-161">Cost actual</span></span></td>
<td><span data-ttu-id="06d64-162">สกุลเงินของหน่วยตามสัญญา</span><span class="sxs-lookup"><span data-stu-id="06d64-162">Contracting unit currency</span></span></td>
<td rowspan="2"><span data-ttu-id="06d64-163">จำนวนจริงของต้นทุน</span><span class="sxs-lookup"><span data-stu-id="06d64-163">Cost actual</span></span></td>
<td rowspan="2"><span data-ttu-id="06d64-164">สกุลเงินของหน่วยตามสัญญา</span><span class="sxs-lookup"><span data-stu-id="06d64-164">Contracting unit currency</span></span>
<td rowspan="2"><span data-ttu-id="06d64-165">จำนวนจริงของต้นทุน</span><span class="sxs-lookup"><span data-stu-id="06d64-165">Cost actual</span></span></td>
<td rowspan="2"><span data-ttu-id="06d64-166">จำนวนจริงของต้นทุน</span><span class="sxs-lookup"><span data-stu-id="06d64-166">Cost actual</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="06d64-167">การขายที่เกิดขึ้นจริงที่ยังไม่ได้เรียกเก็บและคิดค่าธรรมเนียมได้</span><span class="sxs-lookup"><span data-stu-id="06d64-167">Unbilled sales actual – Chargeable</span></span></td>
<td><span data-ttu-id="06d64-168">สกุลเงินตามสัญญาโครงการ</span><span class="sxs-lookup"><span data-stu-id="06d64-168">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="06d64-169">เวลาได้รับการอนุมัติ และการลดลงของชั่วโมงที่เรียกเก็บเงินได้เกิดขึ้น ในระหว่างการอนุมัติ</span><span class="sxs-lookup"><span data-stu-id="06d64-169">Time is approved, and a decrease in billable hours occurs during approval.</span></span></td>
<td><span data-ttu-id="06d64-170">จำนวนจริงของต้นทุน</span><span class="sxs-lookup"><span data-stu-id="06d64-170">Cost actual</span></span></td>
<td><span data-ttu-id="06d64-171">สกุลเงินของหน่วยตามสัญญา</span><span class="sxs-lookup"><span data-stu-id="06d64-171">Contracting unit currency</span></span></td>
<td rowspan="3"><span data-ttu-id="06d64-172">จำนวนจริงของต้นทุน</span><span class="sxs-lookup"><span data-stu-id="06d64-172">Cost actual</span></span></td>
<td rowspan="3"><span data-ttu-id="06d64-173">สกุลเงินของหน่วยตามสัญญา</span><span class="sxs-lookup"><span data-stu-id="06d64-173">Contracting unit currency</span></span></td>
<td rowspan="3"><span data-ttu-id="06d64-174">จำนวนจริงของต้นทุน</span><span class="sxs-lookup"><span data-stu-id="06d64-174">Cost actual</span></span></td>
<td rowspan="3"><span data-ttu-id="06d64-175">จำนวนจริงของต้นทุน</span><span class="sxs-lookup"><span data-stu-id="06d64-175">Cost actual</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="06d64-176">การขายที่ยังไม่ได้เรียกเก็บและคิดค่าธรรมเนียมได้ตามจริง สำหรับปริมาณใหม่</span><span class="sxs-lookup"><span data-stu-id="06d64-176">Unbilled sales actual – Chargeable for the new quantity</span></span></td>
<td><span data-ttu-id="06d64-177">สกุลเงินตามสัญญาโครงการ</span><span class="sxs-lookup"><span data-stu-id="06d64-177">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="06d64-178">การขายที่ยังไม่ได้เรียกเก็บและคิดค่าธรรมเนียมไม่ได้ตามจริง สำหรับความแตกต่าง</span><span class="sxs-lookup"><span data-stu-id="06d64-178">Unbilled sales actual – Non-chargeable for the difference</span></span></td>
<td><span data-ttu-id="06d64-179">สกุลเงินตามสัญญาโครงการ</span><span class="sxs-lookup"><span data-stu-id="06d64-179">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="06d64-180">ใบแจ้งหนี้ได้รับการยืนยัน และไม่มีการเปลี่ยนแปลงหรือเพิ่มขึ้นของชั่วโมงที่เรียกเก็บเงินได้เกิดขึ้น</span><span class="sxs-lookup"><span data-stu-id="06d64-180">An invoice is confirmed, and no change to or increase in billable hours occurs.</span></span></td>
<td><span data-ttu-id="06d64-181">การกลับการขายที่ยังไม่ได้เรียกเก็บเงิน</span><span class="sxs-lookup"><span data-stu-id="06d64-181">Unbilled sales reversal</span></span></td>
<td><span data-ttu-id="06d64-182">สกุลเงินตามสัญญาโครงการ</span><span class="sxs-lookup"><span data-stu-id="06d64-182">Project contract currency</span></span></td>
<td rowspan="2"><span data-ttu-id="06d64-183">การขายที่เรียกเก็บเงินสำหรับไมล์สโตน</span><span class="sxs-lookup"><span data-stu-id="06d64-183">Billed sales for milestone</span></span></td>
<td rowspan="2"><span data-ttu-id="06d64-184">สกุลเงินตามสัญญาโครงการ</span><span class="sxs-lookup"><span data-stu-id="06d64-184">Project contract currency</span></span></td>
<td rowspan="2"><span data-ttu-id="06d64-185">ไม่สามารถใช้งานได้</span><span class="sxs-lookup"><span data-stu-id="06d64-185">Not applicable</span></span></td>
<td rowspan="2"><span data-ttu-id="06d64-186">ไม่สามารถใช้งานได้</span><span class="sxs-lookup"><span data-stu-id="06d64-186">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="06d64-187">การขายที่เรียกเก็บเงินแล้ว</span><span class="sxs-lookup"><span data-stu-id="06d64-187">Billed sales</span></span></td>
<td><span data-ttu-id="06d64-188">สกุลเงินตามสัญญาโครงการ</span><span class="sxs-lookup"><span data-stu-id="06d64-188">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="06d64-189">ใบแจ้งหนี้ได้รับการยืนยัน และการลดลงของชั่วโมงที่เรียกเก็บเงินได้เกิดขึ้น</span><span class="sxs-lookup"><span data-stu-id="06d64-189">An invoice is confirmed, and a decrease in billable hours occurs.</span></span></td>
<td><span data-ttu-id="06d64-190">การกลับการขายที่ยังไม่ได้เรียกเก็บเงิน</span><span class="sxs-lookup"><span data-stu-id="06d64-190">Unbilled sales reversal</span></span></td>
<td><span data-ttu-id="06d64-191">สกุลเงินตามสัญญาโครงการ</span><span class="sxs-lookup"><span data-stu-id="06d64-191">Project contract currency</span></span></td>
<td rowspan="3"><span data-ttu-id="06d64-192">ไม่สามารถใช้งานได้</span><span class="sxs-lookup"><span data-stu-id="06d64-192">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="06d64-193">ไม่สามารถใช้งานได้</span><span class="sxs-lookup"><span data-stu-id="06d64-193">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="06d64-194">ไม่สามารถใช้งานได้</span><span class="sxs-lookup"><span data-stu-id="06d64-194">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="06d64-195">ไม่สามารถใช้งานได้</span><span class="sxs-lookup"><span data-stu-id="06d64-195">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="06d64-196">การขายที่เรียกเก็บแล้วและคิดค่าธรรมเนียมได้ สำหรับปริมาณใหม่</span><span class="sxs-lookup"><span data-stu-id="06d64-196">Billed sales – Chargeable for the new quantity</span></span></td>
<td><span data-ttu-id="06d64-197">สกุลเงินตามสัญญาโครงการ</span><span class="sxs-lookup"><span data-stu-id="06d64-197">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="06d64-198">การขายที่เรียกเก็บเงินแล้วและคิดค่าธรรมเนียมไม่ได้ สำหรับความแตกต่าง</span><span class="sxs-lookup"><span data-stu-id="06d64-198">Billed sales – Non-chargeable for the difference</span></span></td>
<td><span data-ttu-id="06d64-199">สกุลเงินตามสัญญาโครงการ</span><span class="sxs-lookup"><span data-stu-id="06d64-199">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="06d64-200">ใบแจ้งหนี้จะถูกแก้ไขเพื่อเพิ่มปริมาณที่คิดค่าธรรมเนียมได้</span><span class="sxs-lookup"><span data-stu-id="06d64-200">An invoice is corrected to increase the chargeable quantity.</span></span></td>
<td><span data-ttu-id="06d64-201">การขายที่เรียกเก็บเงินแล้ว ย้อนกลับ</span><span class="sxs-lookup"><span data-stu-id="06d64-201">Billed sales – Reversal</span></span></td>
<td><span data-ttu-id="06d64-202">สกุลเงินตามสัญญาโครงการ</span><span class="sxs-lookup"><span data-stu-id="06d64-202">Project contract currency</span></span></td>
<td rowspan="5">
<ul>
<li><span data-ttu-id="06d64-203">การย้อนกลับการขายที่เรียกเก็บเงินแล้วสำหรับไมล์สโตน</span><span class="sxs-lookup"><span data-stu-id="06d64-203">Billed sales reversal for milestone</span></span></li>
<li><span data-ttu-id="06d64-204">เปลี่ยนสถานะไมล์สโตน จาก <strong>ออกใบหนี้</strong> เป็น <strong>พร้อมสำหรับใบแจ้งหนี้</strong></span><span class="sxs-lookup"><span data-stu-id="06d64-204">Change in milestone status from <strong>Invoiced</strong> to <strong>Ready for invoice</strong></span></span></li>
</ul>
</td>
<td rowspan="5"><span data-ttu-id="06d64-205">สกุลเงินตามสัญญาโครงการ</span><span class="sxs-lookup"><span data-stu-id="06d64-205">Project contract currency</span></span></td>
<td rowspan="5"><span data-ttu-id="06d64-206">ไม่สามารถใช้งานได้</span><span class="sxs-lookup"><span data-stu-id="06d64-206">Not applicable</span></span></td>
<td rowspan="5"><span data-ttu-id="06d64-207">ไม่สามารถใช้งานได้</span><span class="sxs-lookup"><span data-stu-id="06d64-207">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="06d64-208">การขายที่เรียกเก็บเงินแล้ว</span><span class="sxs-lookup"><span data-stu-id="06d64-208">Billed sales</span></span></td>
<td><span data-ttu-id="06d64-209">สกุลเงินตามสัญญาโครงการ</span><span class="sxs-lookup"><span data-stu-id="06d64-209">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="06d64-210">ใบแจ้งหนี้จะถูกแก้ไขเพื่อลดปริมาณที่คิดค่าธรรมเนียมได้</span><span class="sxs-lookup"><span data-stu-id="06d64-210">An invoice is corrected to decrease the chargeable quantity.</span></span></td>
<td><span data-ttu-id="06d64-211">การขายที่เรียกเก็บเงินแล้ว ย้อนกลับ</span><span class="sxs-lookup"><span data-stu-id="06d64-211">Billed sales – Reversal</span></span></td>
<td><span data-ttu-id="06d64-212">สกุลเงินตามสัญญาโครงการ</span><span class="sxs-lookup"><span data-stu-id="06d64-212">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="06d64-213">การขายที่เรียกเก็บเงินแล้วสำหรับปริมาณใหม่</span><span class="sxs-lookup"><span data-stu-id="06d64-213">Billed sales for the new quantity</span></span></td>
<td><span data-ttu-id="06d64-214">สกุลเงินตามสัญญาโครงการ</span><span class="sxs-lookup"><span data-stu-id="06d64-214">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="06d64-215">การขายที่ยังไม่เรียกเก็บเงินและคิดค่าธรรมเนียมได้ สำหรับความแตกต่าง</span><span class="sxs-lookup"><span data-stu-id="06d64-215">Unbilled sales – Chargeable for the difference</span></span></td>
<td><span data-ttu-id="06d64-216">สกุลเงินตามสัญญาโครงการ</span><span class="sxs-lookup"><span data-stu-id="06d64-216">Project contract currency</span></span></td>
</tr>
</tbody>
</table>

### <a name="the-resource-belongs-to-an-organizational-unit-that-differs-from-the-projects-contracting-unit"></a><span data-ttu-id="06d64-217">ทรัพยากรเป็นของหน่วยองค์กรที่แตกต่างจากหน่วยที่ทำสัญญาของโครงการ</span><span class="sxs-lookup"><span data-stu-id="06d64-217">The resource belongs to an organizational unit that differs from the project's contracting unit</span></span>

<table>
<thead>
<tr>
<th rowspan="3"><span data-ttu-id="06d64-218">เหตุการณ์</span><span class="sxs-lookup"><span data-stu-id="06d64-218">Event</span></span></th>
<th colspan="4"><span data-ttu-id="06d64-219">โครงการที่เรียกเก็บเงินได้หรือขายแล้ว</span><span class="sxs-lookup"><span data-stu-id="06d64-219">Billable or sold project</span></span></th>
<th rowspan="3"><span data-ttu-id="06d64-220">โครงการในระยะที่ำกำหนด</span><span class="sxs-lookup"><span data-stu-id="06d64-220">Project in the presales stage</span></span></th>
<th rowspan="3"><span data-ttu-id="06d64-221">โครงการภายใน</span><span class="sxs-lookup"><span data-stu-id="06d64-221">Internal project</span></span></th>
</tr>
<tr>
<th colspan="2"><span data-ttu-id="06d64-222">เวลาและวัสดุ</span><span class="sxs-lookup"><span data-stu-id="06d64-222">Time and materials</span></span></th>
<th colspan="2"><span data-ttu-id="06d64-223">ราคาคงที่</span><span class="sxs-lookup"><span data-stu-id="06d64-223">Fixed price</span></span></th>
</tr>
<tr>
<th><span data-ttu-id="06d64-224">ตามจริง</span><span class="sxs-lookup"><span data-stu-id="06d64-224">Actuals</span></span></th>
<th><span data-ttu-id="06d64-225">สกุลเงินในธุรกรรม</span><span class="sxs-lookup"><span data-stu-id="06d64-225">Transaction currency</span></span></th>
<th><span data-ttu-id="06d64-226">ราคาคงที่</span><span class="sxs-lookup"><span data-stu-id="06d64-226">Fixed price</span></span></th>
<th><span data-ttu-id="06d64-227">สกุลเงินในธุรกรรม</span><span class="sxs-lookup"><span data-stu-id="06d64-227">Transaction currency</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="06d64-228">รายการเวลาถูกสร้างขึ้น</span><span class="sxs-lookup"><span data-stu-id="06d64-228">A time entry is created.</span></span></td>
<td colspan="6"><span data-ttu-id="06d64-229">ไม่มีกิจกรรมในเอนทิตีที่เกิดขึ้นจริง</span><span class="sxs-lookup"><span data-stu-id="06d64-229">No activity in the Actuals entity</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="06d64-230">รายการเวลาถูกส่ง</span><span class="sxs-lookup"><span data-stu-id="06d64-230">A time entry is submitted.</span></span></td>
<td colspan="6"><span data-ttu-id="06d64-231">ไม่มีกิจกรรมในเอนทิตีที่เกิดขึ้นจริง</span><span class="sxs-lookup"><span data-stu-id="06d64-231">No activity in the Actuals entity</span></span></td>
</tr>
<tr>
<td rowspan="4"><span data-ttu-id="06d64-232">เวลาได้รับการอนุมัติ และไม่มีการเปลี่ยนแปลงหรือเพิ่มขึ้นของชั่วโมงที่เรียกเก็บเงินได้เกิดขึ้น ในระหว่างการอนุมัติ</span><span class="sxs-lookup"><span data-stu-id="06d64-232">Time is approved, and no change to or increase in billable hours occurs during approval.</span></span></td>
<td><span data-ttu-id="06d64-233">จำนวนจริงของต้นทุน</span><span class="sxs-lookup"><span data-stu-id="06d64-233">Cost actual</span></span></td>
<td><span data-ttu-id="06d64-234">สกุลเงินของหน่วยตามสัญญา</span><span class="sxs-lookup"><span data-stu-id="06d64-234">Contracting unit currency</span></span></td>
<td rowspan="4"><span data-ttu-id="06d64-235">จำนวนจริงของต้นทุน</span><span class="sxs-lookup"><span data-stu-id="06d64-235">Cost actual</span></span></td>
<td rowspan="4"><span data-ttu-id="06d64-236">สกุลเงินของหน่วยตามสัญญา</span><span class="sxs-lookup"><span data-stu-id="06d64-236">Contracting unit currency</span></span></td>
<td rowspan="4"><span data-ttu-id="06d64-237">จำนวนจริงของต้นทุน</span><span class="sxs-lookup"><span data-stu-id="06d64-237">Cost actual</span></span></td>
<td rowspan="4"><span data-ttu-id="06d64-238">จำนวนจริงของต้นทุน</span><span class="sxs-lookup"><span data-stu-id="06d64-238">Cost actual</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="06d64-239">การขายที่เกิดขึ้นจริงที่ยังไม่ได้เรียกเก็บและคิดค่าธรรมเนียมได้</span><span class="sxs-lookup"><span data-stu-id="06d64-239">Unbilled sales actual – Chargeable</span></span></td>
<td><span data-ttu-id="06d64-240">สกุลเงินตามสัญญาโครงการ</span><span class="sxs-lookup"><span data-stu-id="06d64-240">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="06d64-241">ต้นทุนต่อหน่วยการจัดเตรียมทรัพยากร</span><span class="sxs-lookup"><span data-stu-id="06d64-241">Resourcing unit cost</span></span></td>
<td><span data-ttu-id="06d64-242">สกุลเงินต่อหน่วยการจัดเตรียมทรัพยากร</span><span class="sxs-lookup"><span data-stu-id="06d64-242">Resourcing unit currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="06d64-243">การขายระหว่างองค์กร</span><span class="sxs-lookup"><span data-stu-id="06d64-243">Interorganizational sales</span></span></td>
<td><span data-ttu-id="06d64-244">สกุลเงินของหน่วยตามสัญญา</span><span class="sxs-lookup"><span data-stu-id="06d64-244">Contracting unit currency</span></span></td>
</tr>
<tr>
<td rowspan="5"><span data-ttu-id="06d64-245">เวลาได้รับการอนุมัติ และการลดลงของชั่วโมงที่เรียกเก็บเงินได้เกิดขึ้น ในระหว่างการอนุมัติ</span><span class="sxs-lookup"><span data-stu-id="06d64-245">Time is approved, and a decrease in billable hours occurs during approval.</span></span></td>
<td><span data-ttu-id="06d64-246">จำนวนจริงของต้นทุน</span><span class="sxs-lookup"><span data-stu-id="06d64-246">Cost actual</span></span></td>
<td><span data-ttu-id="06d64-247">สกุลเงินของหน่วยตามสัญญา</span><span class="sxs-lookup"><span data-stu-id="06d64-247">Contracting unit currency</span></span></td>
<td rowspan="5"><span data-ttu-id="06d64-248">จำนวนจริงของต้นทุน</span><span class="sxs-lookup"><span data-stu-id="06d64-248">Cost actual</span></span></td>
<td rowspan="5"><span data-ttu-id="06d64-249">สกุลเงินของหน่วยตามสัญญา</span><span class="sxs-lookup"><span data-stu-id="06d64-249">Contracting unit currency</span></span></td>
<td rowspan="5"><span data-ttu-id="06d64-250">จำนวนจริงของต้นทุน</span><span class="sxs-lookup"><span data-stu-id="06d64-250">Cost actual</span></span></td>
<td rowspan="5"><span data-ttu-id="06d64-251">จำนวนจริงของต้นทุน</span><span class="sxs-lookup"><span data-stu-id="06d64-251">Cost actual</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="06d64-252">ต้นทุนต่อหน่วยการจัดเตรียมทรัพยากร</span><span class="sxs-lookup"><span data-stu-id="06d64-252">Resourcing unit cost</span></span></td>
<td><span data-ttu-id="06d64-253">สกุลเงินต่อหน่วยการจัดเตรียมทรัพยากร</span><span class="sxs-lookup"><span data-stu-id="06d64-253">Resourcing unit currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="06d64-254">การขายระหว่างองค์กร</span><span class="sxs-lookup"><span data-stu-id="06d64-254">Interorganizational sales</span></span></td>
<td><span data-ttu-id="06d64-255">สกุลเงินของหน่วยตามสัญญา</span><span class="sxs-lookup"><span data-stu-id="06d64-255">Contracting unit currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="06d64-256">การขายที่ยังไม่ได้เรียกเก็บและคิดค่าธรรมเนียมได้ตามจริง สำหรับปริมาณใหม่</span><span class="sxs-lookup"><span data-stu-id="06d64-256">Unbilled sales actual – Chargeable for the new quantity</span></span></td>
<td><span data-ttu-id="06d64-257">สกุลเงินตามสัญญาโครงการ</span><span class="sxs-lookup"><span data-stu-id="06d64-257">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="06d64-258">การขายที่ยังไม่ได้เรียกเก็บและคิดค่าธรรมเนียมไม่ได้ตามจริง สำหรับความแตกต่าง</span><span class="sxs-lookup"><span data-stu-id="06d64-258">Unbilled sales actual – Non-chargeable for the difference</span></span></td>
<td><span data-ttu-id="06d64-259">สกุลเงินตามสัญญาโครงการ</span><span class="sxs-lookup"><span data-stu-id="06d64-259">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="06d64-260">ใบแจ้งหนี้ได้รับการยืนยัน และไม่มีการเปลี่ยนแปลงหรือเพิ่มขึ้นของชั่วโมงที่เรียกเก็บเงินได้เกิดขึ้น</span><span class="sxs-lookup"><span data-stu-id="06d64-260">An invoice is confirmed, and no change to or increase in billable hours occurs.</span></span></td>
<td><span data-ttu-id="06d64-261">การกลับการขายที่ยังไม่ได้เรียกเก็บเงิน</span><span class="sxs-lookup"><span data-stu-id="06d64-261">Unbilled sales reversal</span></span></td>
<td><span data-ttu-id="06d64-262">สกุลเงินตามสัญญาโครงการ</span><span class="sxs-lookup"><span data-stu-id="06d64-262">Project contract currency</span></span></td>
<td rowspan="2"><span data-ttu-id="06d64-263">การขายที่เรียกเก็บเงินสำหรับไมล์สโตน</span><span class="sxs-lookup"><span data-stu-id="06d64-263">Billed sales for milestone</span></span></td>
<td rowspan="2"><span data-ttu-id="06d64-264">สกุลเงินตามสัญญาโครงการ</span><span class="sxs-lookup"><span data-stu-id="06d64-264">Project contract currency</span></span></td>
<td rowspan="2"><span data-ttu-id="06d64-265">ไม่สามารถใช้งานได้</span><span class="sxs-lookup"><span data-stu-id="06d64-265">Not applicable</span></span></td>
<td rowspan="2"><span data-ttu-id="06d64-266">ไม่สามารถใช้งานได้</span><span class="sxs-lookup"><span data-stu-id="06d64-266">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="06d64-267">การขายที่เรียกเก็บเงินแล้ว</span><span class="sxs-lookup"><span data-stu-id="06d64-267">Billed sales</span></span></td>
<td><span data-ttu-id="06d64-268">สกุลเงินตามสัญญาโครงการ</span><span class="sxs-lookup"><span data-stu-id="06d64-268">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="06d64-269">ใบแจ้งหนี้ได้รับการยืนยัน และการลดลงของชั่วโมงที่เรียกเก็บเงินได้เกิดขึ้น</span><span class="sxs-lookup"><span data-stu-id="06d64-269">An invoice is confirmed, and a decrease in billable hours occurs.</span></span></td>
<td><span data-ttu-id="06d64-270">การกลับการขายที่ยังไม่ได้เรียกเก็บเงิน</span><span class="sxs-lookup"><span data-stu-id="06d64-270">Unbilled sales reversal</span></span></td>
<td><span data-ttu-id="06d64-271">สกุลเงินตามสัญญาโครงการ</span><span class="sxs-lookup"><span data-stu-id="06d64-271">Project contract currency</span></span></td>
<td rowspan="3"><span data-ttu-id="06d64-272">ไม่สามารถใช้งานได้</span><span class="sxs-lookup"><span data-stu-id="06d64-272">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="06d64-273">ไม่สามารถใช้งานได้</span><span class="sxs-lookup"><span data-stu-id="06d64-273">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="06d64-274">ไม่สามารถใช้งานได้</span><span class="sxs-lookup"><span data-stu-id="06d64-274">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="06d64-275">ไม่สามารถใช้งานได้</span><span class="sxs-lookup"><span data-stu-id="06d64-275">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="06d64-276">การขายที่เรียกเก็บแล้วและคิดค่าธรรมเนียมได้ สำหรับปริมาณใหม่</span><span class="sxs-lookup"><span data-stu-id="06d64-276">Billed sales – Chargeable for the new quantity</span></span></td>
<td><span data-ttu-id="06d64-277">สกุลเงินตามสัญญาโครงการ</span><span class="sxs-lookup"><span data-stu-id="06d64-277">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="06d64-278">การขายที่เรียกเก็บเงินแล้วและคิดค่าธรรมเนียมไม่ได้ สำหรับความแตกต่าง</span><span class="sxs-lookup"><span data-stu-id="06d64-278">Billed sales – Non-chargeable for the difference</span></span></td>
<td><span data-ttu-id="06d64-279">สกุลเงินตามสัญญาโครงการ</span><span class="sxs-lookup"><span data-stu-id="06d64-279">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="06d64-280">ใบแจ้งหนี้จะถูกแก้ไขเพื่อเพิ่มปริมาณที่คิดค่าธรรมเนียมได้</span><span class="sxs-lookup"><span data-stu-id="06d64-280">An invoice is corrected to increase the chargeable quantity.</span></span></td>
<td><span data-ttu-id="06d64-281">การขายที่เรียกเก็บเงินแล้ว ย้อนกลับ</span><span class="sxs-lookup"><span data-stu-id="06d64-281">Billed sales – Reversal</span></span></td>
<td><span data-ttu-id="06d64-282">สกุลเงินตามสัญญาโครงการ</span><span class="sxs-lookup"><span data-stu-id="06d64-282">Project contract currency</span></span></td>
<td rowspan="5">
<ul>
<li><span data-ttu-id="06d64-283">การย้อนกลับการขายที่เรียกเก็บเงินแล้วสำหรับไมล์สโตน</span><span class="sxs-lookup"><span data-stu-id="06d64-283">Billed sales reversal for milestone</span></span></li>
<li><span data-ttu-id="06d64-284">เปลี่ยนสถานะไมล์สโตน จาก <strong>ออกใบหนี้</strong> เป็น <strong>พร้อมสำหรับใบแจ้งหนี้</strong></span><span class="sxs-lookup"><span data-stu-id="06d64-284">Change in milestone status from <strong>Invoiced</strong> to <strong>Ready for invoice</strong></span></span></li>
</ul>
</td>
<td rowspan="5"><span data-ttu-id="06d64-285">สกุลเงินตามสัญญาโครงการ</span><span class="sxs-lookup"><span data-stu-id="06d64-285">Project contract currency</span></span></td>
<td rowspan="5"><span data-ttu-id="06d64-286">ไม่สามารถใช้งานได้</span><span class="sxs-lookup"><span data-stu-id="06d64-286">Not applicable</span></span></td>
<td rowspan="5"><span data-ttu-id="06d64-287">ไม่สามารถใช้งานได้</span><span class="sxs-lookup"><span data-stu-id="06d64-287">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="06d64-288">การขายที่เรียกเก็บเงินแล้ว</span><span class="sxs-lookup"><span data-stu-id="06d64-288">Billed sales</span></span></td>
<td><span data-ttu-id="06d64-289">สกุลเงินตามสัญญาโครงการ</span><span class="sxs-lookup"><span data-stu-id="06d64-289">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="06d64-290">ใบแจ้งหนี้จะถูกแก้ไขเพื่อลดปริมาณที่คิดค่าธรรมเนียมได้</span><span class="sxs-lookup"><span data-stu-id="06d64-290">An invoice is corrected to decrease the chargeable quantity.</span></span></td>
<td><span data-ttu-id="06d64-291">การขายที่เรียกเก็บเงินแล้ว ย้อนกลับ</span><span class="sxs-lookup"><span data-stu-id="06d64-291">Billed sales – Reversal</span></span></td>
<td><span data-ttu-id="06d64-292">สกุลเงินตามสัญญาโครงการ</span><span class="sxs-lookup"><span data-stu-id="06d64-292">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="06d64-293">การขายที่เรียกเก็บเงินแล้วสำหรับปริมาณใหม่</span><span class="sxs-lookup"><span data-stu-id="06d64-293">Billed sales for the new quantity</span></span></td>
<td><span data-ttu-id="06d64-294">สกุลเงินตามสัญญาโครงการ</span><span class="sxs-lookup"><span data-stu-id="06d64-294">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="06d64-295">การขายที่ยังไม่เรียกเก็บเงินและคิดค่าธรรมเนียมได้ สำหรับความแตกต่าง</span><span class="sxs-lookup"><span data-stu-id="06d64-295">Unbilled sales – Chargeable for the difference</span></span></td>
<td><span data-ttu-id="06d64-296">สกุลเงินตามสัญญาโครงการ</span><span class="sxs-lookup"><span data-stu-id="06d64-296">Project contract currency</span></span></td>
</tr>
</tbody>
</table>
