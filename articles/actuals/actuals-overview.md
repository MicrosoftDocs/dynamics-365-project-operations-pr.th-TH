---
title: ข้อมูลจริง
description: หัวข้อนี้ให้ข้อมูลเกี่ยวกับวิธีการทำงานกับข้อมูลจริงใน Microsoft Dynamics 365 Project Operations
author: rumant
ms.date: 04/01/2021
ms.topic: article
ms.prod: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.custom: intro-internal
ms.assetid: ''
ms.search.region: ''
ms.search.industry: ''
ms.author: rumant
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: 9e046602a3005930c41ab8c50472d5b1a72303c6
ms.sourcegitcommit: 0fafe022731f0e1e8693382ff906e3f8541d34ca
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 07/07/2021
ms.locfileid: "6368634"
---
# <a name="actuals"></a><span data-ttu-id="506fb-103">ข้อมูลจริง</span><span class="sxs-lookup"><span data-stu-id="506fb-103">Actuals</span></span> 

<span data-ttu-id="506fb-104">_**นำไปใช้กับ:** Project Operations สำหรับสถานการณ์ตามทรัพยากร/สินค้าที่ไม่ได้เก็บในคลัง การปรับใช้งานแบบ Lite - จัดการกับการออกใบแจ้งหนี้ชั่วคราว_</span><span class="sxs-lookup"><span data-stu-id="506fb-104">_**Applies to:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="506fb-105">ข้อมูลจริงแสดงถึงความคืบหน้าทางการเงินที่ได้รับการตรวจสอบและอนุมัติและและจัดกำหนดการในโครงการ</span><span class="sxs-lookup"><span data-stu-id="506fb-105">Actuals represent the reviewed and approved financial and schedule progress on a project.</span></span> <span data-ttu-id="506fb-106">โดยสร้างขึ้นจากการอนุมัติเวลา ค่าใช้จ่าย รายการการใช้วัสดุ และรายการสมุดรายวันและใบแจ้งหนี้</span><span class="sxs-lookup"><span data-stu-id="506fb-106">They are created as a result of approval of time, expense, material usage entries, and journal entries and invoices.</span></span>

## <a name="journal-lines-and-time-submission"></a><span data-ttu-id="506fb-107">การส่งบรรทัดสมุดรายวันและเวลา</span><span class="sxs-lookup"><span data-stu-id="506fb-107">Journal lines and time submission</span></span>

<span data-ttu-id="506fb-108">สำหรับข้อมูลเพิ่มเติมเกี่ยวกับรายการเวลา โปรดดู [ภาพรวมของรายการเวลา](../time/time-entry-overview.md)</span><span class="sxs-lookup"><span data-stu-id="506fb-108">For more information about time entry, see [Time entry overview](../time/time-entry-overview.md).</span></span>

### <a name="time-and-materials"></a><span data-ttu-id="506fb-109">เวลาและวัสดุ</span><span class="sxs-lookup"><span data-stu-id="506fb-109">Time and materials</span></span>

<span data-ttu-id="506fb-110">เมื่อรายการเวลาที่ส่งมีการเชื่อมโยงกับโครงการที่แม็ปกับรายละเอียดการให้บริการตามสัญญาของเวลาและวัสดุ ระบบจะสร้างบรรทัดสมุดรายวันสองรายการ รายการหนึ่งสำหรับต้นทุนและอีกรายการสำหรับการขายที่ยังไม่เรียกเก็บเงิน</span><span class="sxs-lookup"><span data-stu-id="506fb-110">When a time entry that is submitted is linked to a project that is mapped to a time-and-materials contract line, the system creates two journal lines, one for cost and one for unbilled sales.</span></span>

### <a name="fixed-price"></a><span data-ttu-id="506fb-111">ราคาคงที่</span><span class="sxs-lookup"><span data-stu-id="506fb-111">Fixed price</span></span>

<span data-ttu-id="506fb-112">เมื่อรายการเวลาที่ส่งมีการเชื่อมโยงกับโครงการที่แม็ปกับรายละเอียดการให้บริการตามสัญญาที่มีราคาคงที่ ระบบจะสร้างบรรทัดสมุดรายวันหนึ่งรายการสำหรับต้นทุน</span><span class="sxs-lookup"><span data-stu-id="506fb-112">When a time entry that is submitted is linked to a project that is mapped to a fixed-price contract line, the system creates one journal line for cost.</span></span>

### <a name="default-pricing"></a><span data-ttu-id="506fb-113">การกำหนดราคาเริ่มต้น</span><span class="sxs-lookup"><span data-stu-id="506fb-113">Default pricing</span></span>

<span data-ttu-id="506fb-114">ตรรกะสำหรับการสร้างราคาเริ่มต้นอยู่ในบรรทัดสมุดรายวัน</span><span class="sxs-lookup"><span data-stu-id="506fb-114">The logic for creating default prices resides on the journal line.</span></span> <span data-ttu-id="506fb-115">ค่าฟิลด์จากรายการเวลาจะถูกคัดลอกไปยังบรรทัดสมุดรายวัน</span><span class="sxs-lookup"><span data-stu-id="506fb-115">The field values from the time entry are copied to the journal line.</span></span> <span data-ttu-id="506fb-116">ค่าเหล่านี้รวมถึงวันที่ของธุรกรรม รายละเอียดการให้บริการตามสัญญาที่โครงการถูกแม็ปด้วย และสกุลเงินที่เป็นผลในรายการราคาที่เหมาะสม</span><span class="sxs-lookup"><span data-stu-id="506fb-116">These values include the transaction date, the contract line that the project is mapped to, and the currency result in the appropriate price list.</span></span>

<span data-ttu-id="506fb-117">ฟิลด์ที่มีผลต่อการกำหนดราคาเริ่มต้น เช่น **บทบาท** และ **หน่วยการจัดเตรียมทรัพยากร** มีการใช้เพื่อกำหนดราคาที่เหมาะสมในบรรทัดสมุดรายวัน</span><span class="sxs-lookup"><span data-stu-id="506fb-117">The fields that affect default pricing, such as **Role** and **Resourcing Unit**, are used to determine the appropriate price on the journal line.</span></span> <span data-ttu-id="506fb-118">คุณสามารถเพิ่มฟิลด์ที่กำหนดเองในรายการเวลา</span><span class="sxs-lookup"><span data-stu-id="506fb-118">You can add a custom field on the time entry.</span></span> <span data-ttu-id="506fb-119">หากคุณต้องการให้ค่าฟิลด์กระจายเป็นข้อมูลจริง ให้สร้างฟิลด์ในตาราง **ข้อมูลจริง** และ **บรรทัดสมุดรายวัน**</span><span class="sxs-lookup"><span data-stu-id="506fb-119">If you want the field value to be propagated to actuals, create the field in the **Actuals** and **Journal Line** tables.</span></span> <span data-ttu-id="506fb-120">ใช้โค้ดแบบกำหนดเองเพื่อเผยแพร่ค่าฟิลด์ที่เลือกจากรายการเวลาไปยังข้อมูลจริงผ่านบรรทัดสมุดรายวันโดยใช้ที่มาของธุรกรรม</span><span class="sxs-lookup"><span data-stu-id="506fb-120">Use custom code to propagate the selected field value from Time Entry to Actuals through the journal line using transaction origins.</span></span> <span data-ttu-id="506fb-121">สำหรับข้อมูลเพิ่มเติมเกี่ยวกับที่มาของธุรกรรมและการเชื่อมต่อ โปรดดู [การเชื่อมโยงข้อมูลจริงกับเรกคอร์ดเดิม](linkingactuals.md#example-how-transaction-origin-works-with-transaction-connection)</span><span class="sxs-lookup"><span data-stu-id="506fb-121">For more information about transaction origins and connections, see [Linking Actuals to original records](linkingactuals.md#example-how-transaction-origin-works-with-transaction-connection).</span></span>

## <a name="journal-lines-and-basic-expense-submission"></a><span data-ttu-id="506fb-122">การส่งบรรทัดสมุดรายวันและค่าใช้จ่ายพื้นฐาน</span><span class="sxs-lookup"><span data-stu-id="506fb-122">Journal lines and basic expense submission</span></span>

<span data-ttu-id="506fb-123">สำหรับข้อมูลเพิ่มเติมเกี่ยวกับรายการค่าใช้จ่าย โปรดดู [ภาพรวมของค่าใช้จ่าย](../expense/expense-overview.md)</span><span class="sxs-lookup"><span data-stu-id="506fb-123">For more information about expense entry, see [Expense overview](../expense/expense-overview.md).</span></span>

### <a name="time-and-materials"></a><span data-ttu-id="506fb-124">เวลาและวัสดุ</span><span class="sxs-lookup"><span data-stu-id="506fb-124">Time and materials</span></span>

<span data-ttu-id="506fb-125">เมื่อรายการค่าใช้จ่ายพื้นฐานที่ส่งมีการเชื่อมโยงกับโครงการที่แม็ปกับรายละเอียดการให้บริการตามสัญญาของเวลาและวัสดุ ระบบจะสร้างบรรทัดสมุดรายวันสองรายการ รายการหนึ่งสำหรับต้นทุนและอีกรายการสำหรับการขายที่ยังไม่เรียกเก็บเงิน</span><span class="sxs-lookup"><span data-stu-id="506fb-125">When a basic expense entry that is submitted is linked to a project that is mapped to a time-and-materials contract line, the system creates two journal lines, one for cost and one for unbilled sales.</span></span>

### <a name="fixed-price"></a><span data-ttu-id="506fb-126">ราคาคงที่</span><span class="sxs-lookup"><span data-stu-id="506fb-126">Fixed price</span></span>

<span data-ttu-id="506fb-127">เมื่อรายการค่าใช้จ่ายพื้นฐานที่ส่งเชื่อมโยงกับโครงการที่ถูกแม็ปกับรายละเอียดการให้บริการตามสัญญาที่มีราคาคงที่ ระบบจะสร้างบรรทัดสมุดรายวันเดียวสำหรับต้นทุน</span><span class="sxs-lookup"><span data-stu-id="506fb-127">When a submitted basic expense entry is linked to a project that's mapped to a fixed-price contract line, the system creates one journal line for cost.</span></span>

### <a name="default-pricing"></a><span data-ttu-id="506fb-128">การกำหนดราคาเริ่มต้น</span><span class="sxs-lookup"><span data-stu-id="506fb-128">Default pricing</span></span>

<span data-ttu-id="506fb-129">ตรรกะสำหรับการป้อนราคาเริ่มต้นสำหรับค่าใช้จ่ายจะขึ้นอยู่กับประเภทค่าใช้จ่าย</span><span class="sxs-lookup"><span data-stu-id="506fb-129">The logic for entering default prices for expenses is based on the expense category.</span></span> <span data-ttu-id="506fb-130">วันที่ของธุรกรรม รายละเอียดการให้บริการตามสัญญาที่โครงการถูกแม็ปด้วย และสกุลเงิน จะถูกใช้เพื่อระบุรายการราคาที่เหมาะสม</span><span class="sxs-lookup"><span data-stu-id="506fb-130">The transaction date, the contract line that the project is mapped to, and the currency, are all used to determine the appropriate price list.</span></span> <span data-ttu-id="506fb-131">ฟิลด์ที่มีผลต่อราคาเริ่มต้น เช่น **ประเภทธุรกรรม** และ **หน่วย** มีการใช้เพื่อกำหนดราคาที่เหมาะสมในบรรทัดสมุดรายวัน</span><span class="sxs-lookup"><span data-stu-id="506fb-131">The fields that affect default pricing, such as **Transaction Category** and **Unit**, are used to determine the appropriate price on the journal line.</span></span> <span data-ttu-id="506fb-132">อย่างไรก็ตาม วิธีนี้ใช้ได้เฉพาะเมื่อวิธีการกำหนดราคาในรายการราคาเป็น **ราคาต่อหน่วย**</span><span class="sxs-lookup"><span data-stu-id="506fb-132">However, this only works when the pricing method in the price list is **Price per unit**.</span></span> <span data-ttu-id="506fb-133">หากวิธีการกำหนดราคาเป็น **ตามต้นทุน** หรือ **คิดส่วนเพิ่มราคากับต้นทุน** ราคาที่ป้อนเมื่อสร้างรายการค่าใช้จ่ายจะใช้สำหรับต้นทุน และราคาในรายการสมุดรายวันการขายจะคำนวณตามวิธีการกำหนดราคา</span><span class="sxs-lookup"><span data-stu-id="506fb-133">If pricing method is **At cost** or **Markup over cost**, the price entered when the expense entry is created is used for cost and the price on the sales journal line is calculated based on the pricing method.</span></span> 

<span data-ttu-id="506fb-134">คุณสามารถเพิ่มฟิลด์แบบกำหนดเองในรายการค่าใช้จ่ายได้</span><span class="sxs-lookup"><span data-stu-id="506fb-134">You can add a custom field on the expense entry.</span></span> <span data-ttu-id="506fb-135">หากคุณต้องการให้ค่าฟิลด์กระจายเป็นข้อมูลจริง ให้สร้างฟิลด์ในตาราง **ข้อมูลจริง** และ **บรรทัดสมุดรายวัน**</span><span class="sxs-lookup"><span data-stu-id="506fb-135">If you want the field value to be propagated to actuals, create the field in the **Actuals** and **Journal Line** tables.</span></span> <span data-ttu-id="506fb-136">ใช้โค้ดแบบกำหนดเองเพื่อเผยแพร่ค่าฟิลด์ที่เลือกจากรายการเวลาไปยังข้อมูลจริงผ่านบรรทัดสมุดรายวันโดยใช้ที่มาของธุรกรรม</span><span class="sxs-lookup"><span data-stu-id="506fb-136">Use custom code to propagate the selected field value from Time Entry to Actuals through the journal line using transaction origins.</span></span> <span data-ttu-id="506fb-137">สำหรับข้อมูลเพิ่มเติมเกี่ยวกับที่มาของธุรกรรมและการเชื่อมต่อ โปรดดู [การเชื่อมโยงข้อมูลจริงกับเรกคอร์ดเดิม](linkingactuals.md#example-how-transaction-origin-works-with-transaction-connection)</span><span class="sxs-lookup"><span data-stu-id="506fb-137">For more information about transaction origins and connections, see [Linking Actuals to original records](linkingactuals.md#example-how-transaction-origin-works-with-transaction-connection).</span></span>

## <a name="journal-lines-and-material-usage-log-submission"></a><span data-ttu-id="506fb-138">บรรทัดสมุดรายวันและการส่งบันทึกการใช้วัสดุ</span><span class="sxs-lookup"><span data-stu-id="506fb-138">Journal lines and material usage log submission</span></span>

<span data-ttu-id="506fb-139">สำหรับข้อมูลเพิ่มเติมเกี่ยวกับรายการค่าใช้จ่าย โปรดดู [บันทึกการใช้วัสดุ](../material/material-usage-log.md)</span><span class="sxs-lookup"><span data-stu-id="506fb-139">For more information about expense entry, see [Material Usage Log](../material/material-usage-log.md).</span></span>

### <a name="time-and-materials"></a><span data-ttu-id="506fb-140">เวลาและวัสดุ</span><span class="sxs-lookup"><span data-stu-id="506fb-140">Time and materials</span></span>

<span data-ttu-id="506fb-141">เมื่อรายการบันทึกการใช้วัสดุที่ส่งเชื่อมโยงกับโครงการที่แม็ปกับรายละเอียดการให้บริการตามสัญญาสำหรับเวลาและวัสดุ ระบบจะสร้างบรรทัดสมุดรายวันสองรายการ รายการหนึ่งสำหรับต้นทุน และอีกรายการสำหรับการขายที่ยังไม่เรียกเก็บเงิน</span><span class="sxs-lookup"><span data-stu-id="506fb-141">When a submitted material usage log entry is linked to a project that is mapped to a time and materials contract line, the system creates two journal lines, one for cost and one for unbilled sales.</span></span>

### <a name="fixed-price"></a><span data-ttu-id="506fb-142">ราคาคงที่</span><span class="sxs-lookup"><span data-stu-id="506fb-142">Fixed price</span></span>

<span data-ttu-id="506fb-143">เมื่อรายการบันทึกการใช้วัสุดที่ส่งเชื่อมโยงกับโครงการที่ถูกแม็ปกับรายละเอียดการให้บริการตามสัญญาที่มีราคาคงที่ ระบบจะสร้างบรรทัดสมุดรายวันเดียวสำหรับต้นทุน</span><span class="sxs-lookup"><span data-stu-id="506fb-143">When a submitted material usage log entry is linked to a project that is mapped to a fixed-price contract line, the system creates one journal line for cost.</span></span>

### <a name="default-pricing"></a><span data-ttu-id="506fb-144">การกำหนดราคาเริ่มต้น</span><span class="sxs-lookup"><span data-stu-id="506fb-144">Default pricing</span></span>

<span data-ttu-id="506fb-145">ตรรกะในการป้อนราคาเริ่มต้นสำหรับวัสดุจะอิงตามชุดผสมของผลิตภัณฑ์และหน่วย</span><span class="sxs-lookup"><span data-stu-id="506fb-145">The logic for entering default prices for material is based on the product and unit combination.</span></span> <span data-ttu-id="506fb-146">วันที่ของธุรกรรม รายละเอียดการให้บริการตามสัญญาที่โครงการถูกแม็ปด้วย และสกุลเงิน จะถูกใช้เพื่อระบุรายการราคาที่เหมาะสม</span><span class="sxs-lookup"><span data-stu-id="506fb-146">The transaction date, the contract line that the project is mapped to, and the currency, are all used to determine the appropriate price list.</span></span> <span data-ttu-id="506fb-147">ฟิลด์ที่มีผลต่อราคาเริ่มต้น เช่น **รหัสผลิตภัณฑ์** และ **หน่วย** มีการใช้เพื่อกำหนดราคาที่เหมาะสมในบรรทัดสมุดรายวัน</span><span class="sxs-lookup"><span data-stu-id="506fb-147">The fields that affect default pricing, such as **Product ID** and **Unit**, are used to determine the appropriate price on the journal line.</span></span> <span data-ttu-id="506fb-148">อย่างไรก็ตาม วิธีนี้ใช้ได้กับผลิตภัณฑ์ในแคตตาล็อกเท่านั้น</span><span class="sxs-lookup"><span data-stu-id="506fb-148">However, this only works for catalog products.</span></span> <span data-ttu-id="506fb-149">สำหรับผลิตภัณฑ์ที่เขียนเพิ่ม ราคาที่ป้อนเมื่อสร้างรายการบันทึกการใช้วัสดุจะใช้สำหรับต้นทุนและราคาขายในบรรทัดสมุดรายวัน</span><span class="sxs-lookup"><span data-stu-id="506fb-149">For write-in products, the price entered when the material usage log entry is created is used for cost and sales price on the journal lines.</span></span> 

<span data-ttu-id="506fb-150">คุณสามารถเพิ่มฟิลด์แบบกำหนดเองในรายการ **บันทึกการใช้วัสดุ** ได้</span><span class="sxs-lookup"><span data-stu-id="506fb-150">You can add a custom field on the **Material Usage Log** entry.</span></span> <span data-ttu-id="506fb-151">หากคุณต้องการให้ค่าฟิลด์กระจายเป็นข้อมูลจริง ให้สร้างฟิลด์ในตาราง **ข้อมูลจริง** และ **บรรทัดสมุดรายวัน**</span><span class="sxs-lookup"><span data-stu-id="506fb-151">If you want the field value to be propagated to actuals, create the field in the **Actuals** and **Journal Line** tables.</span></span> <span data-ttu-id="506fb-152">ใช้โค้ดแบบกำหนดเองเพื่อเผยแพร่ค่าฟิลด์ที่เลือกจากรายการเวลาไปยังข้อมูลจริงผ่านบรรทัดสมุดรายวันโดยใช้ที่มาของธุรกรรม</span><span class="sxs-lookup"><span data-stu-id="506fb-152">Use custom code to propagate the selected field value from Time Entry to Actuals through the journal line using transaction origins.</span></span> <span data-ttu-id="506fb-153">สำหรับข้อมูลเพิ่มเติมเกี่ยวกับที่มาของธุรกรรมและการเชื่อมต่อ โปรดดู [การเชื่อมโยงข้อมูลจริงกับเรกคอร์ดเดิม](linkingactuals.md#example-how-transaction-origin-works-with-transaction-connection)</span><span class="sxs-lookup"><span data-stu-id="506fb-153">For more information about transaction origins and connections, see [Linking Actuals to original records](linkingactuals.md#example-how-transaction-origin-works-with-transaction-connection).</span></span>

## <a name="use-entry-journals-to-record-costs"></a><span data-ttu-id="506fb-154">ใช้รายการสมุดรายวันเพื่อบันทึกต้นทุน</span><span class="sxs-lookup"><span data-stu-id="506fb-154">Use entry journals to record costs</span></span>

<span data-ttu-id="506fb-155">คุณสามารถใช้รายการสมุดรายวันเพื่อบันทึกต้นทุนหรือรายได้ ในคลาสวัสดุ ค่าธรรมเนียม เวลา ค่าใช้จ่าย หรือธุรกรรมภาษีได้</span><span class="sxs-lookup"><span data-stu-id="506fb-155">You can use entry journals to record the cost or revenue in the material, fee, time, expense, or tax transaction classes.</span></span> <span data-ttu-id="506fb-156">สมุดรายวันสามารถใช้เพื่อวัตถุประสงค์ดังต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="506fb-156">Journals can be used for the following purposes:</span></span>

- <span data-ttu-id="506fb-157">ย้ายข้อมูลจริงของธุรกรรมจากระบบอื่นไปยัง Microsoft Dynamics 365 Project Operations</span><span class="sxs-lookup"><span data-stu-id="506fb-157">Move transaction actuals from another system to Microsoft Dynamics 365 Project Operations.</span></span>
- <span data-ttu-id="506fb-158">บันทึกต้นทุนที่เกิดขึ้นในระบบอื่น</span><span class="sxs-lookup"><span data-stu-id="506fb-158">Record costs that occurred in another system.</span></span> <span data-ttu-id="506fb-159">ต้นทุนเหล่านี้อาจรวมถึงต้นทุนการจัดซื้อจัดจ้างหรือการรับเหมาช่วง</span><span class="sxs-lookup"><span data-stu-id="506fb-159">These costs can include procurement or subcontracting costs.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="506fb-160">แอปพลิเคชันไม่ตรวจสอบความถูกต้องของชนิดบรรทัดสมุดรายวันหรือการกำหนดราคาที่เกี่ยวข้องซึ่งป้อนในบรรทัดสมุดรายวัน</span><span class="sxs-lookup"><span data-stu-id="506fb-160">The application doesn't validate the journal line type or the related pricing that is entered on the journal line.</span></span> <span data-ttu-id="506fb-161">ดังนั้น เฉพาะผู้ใช้ที่ทราบถึงผลกระทบทางการบัญชีที่เกิดขึ้นจริงต่อโครงการเท่านั้นที่ควรใช้รายการสมุดรายวันเพื่อสร้างข้อมูลจริง</span><span class="sxs-lookup"><span data-stu-id="506fb-161">Therefore, only a user who is fully aware of the accounting impact that actuals have on the project should use entry journals to create actuals.</span></span> <span data-ttu-id="506fb-162">เนื่องจากผลกระทบของชนิดสมุดรายวันนี้ คุณควรเลือกอย่างรอบคอบว่าใครมีสิทธิ์ในการสร้างรายการสมุดรายวัน</span><span class="sxs-lookup"><span data-stu-id="506fb-162">Because of the impact of this journal type, you should carefully choose who has access to create entry journals.</span></span>

## <a name="record-actuals-based-on-project-events"></a><span data-ttu-id="506fb-163">บันทึกข้อมูลจริงตามเหตุการณ์ของโครงการ</span><span class="sxs-lookup"><span data-stu-id="506fb-163">Record actuals based on project events</span></span>

<span data-ttu-id="506fb-164">Project Operations จะบันทึกธุรกรรมทางการเงินที่เกิดขึ้นระหว่างโครงการ</span><span class="sxs-lookup"><span data-stu-id="506fb-164">Project Operations records the financial transactions that occur during a project.</span></span> <span data-ttu-id="506fb-165">ธุรกรรมเหล่านี้จะถูกบันทึก เป็นค่าจริง</span><span class="sxs-lookup"><span data-stu-id="506fb-165">These transactions are recorded as actuals.</span></span> <span data-ttu-id="506fb-166">ตารางต่อไปนี้แสดงชนิดที่แตกต่างกันของความจริงที่ถูกสร้าง ขึ้นอยู่กับว่าโครงการเป็นแบบในเวลาและวัสดุหรือโครงการที่มีราคาคงที่ อยู่ในระยะที่กำหนดหรือเป็นโครงการภายใน</span><span class="sxs-lookup"><span data-stu-id="506fb-166">The following tables show the different types of actuals that are created, depending on whether the project is a time-and-materials or fixed-price project, is in the presales stage, or is an internal project.</span></span>

### <a name="the-resource-belongs-to-same-organizational-unit-as-the-projects-contracting-unit"></a><span data-ttu-id="506fb-167">ทรัพยากรเป็นของหน่วยองค์กรเดียวกันกับหน่วยที่ทำสัญญาของโครงการ</span><span class="sxs-lookup"><span data-stu-id="506fb-167">The resource belongs to same organizational unit as the project's contracting unit</span></span>

<table>
<thead>
<tr>
<th rowspan="3"><span data-ttu-id="506fb-168">เหตุการณ์</span><span class="sxs-lookup"><span data-stu-id="506fb-168">Event</span></span></th>
<th colspan="4"><span data-ttu-id="506fb-169">โครงการที่เรียกเก็บเงินได้หรือขายแล้ว</span><span class="sxs-lookup"><span data-stu-id="506fb-169">Billable or sold project</span></span></th>
<th rowspan="3"><span data-ttu-id="506fb-170">โครงการในระยะที่ำกำหนด</span><span class="sxs-lookup"><span data-stu-id="506fb-170">Project in the presales stage</span></span></th>
<th rowspan="3"><span data-ttu-id="506fb-171">โครงการภายใน</span><span class="sxs-lookup"><span data-stu-id="506fb-171">Internal project</span></span></th>
</tr>
<tr>
<th colspan="2"><span data-ttu-id="506fb-172">เวลาและวัสดุ</span><span class="sxs-lookup"><span data-stu-id="506fb-172">Time and materials</span></span></th>
<th colspan="2"><span data-ttu-id="506fb-173">ราคาคงที่</span><span class="sxs-lookup"><span data-stu-id="506fb-173">Fixed price</span></span></th>
</tr>
<tr>
<th><span data-ttu-id="506fb-174">ตามจริง</span><span class="sxs-lookup"><span data-stu-id="506fb-174">Actuals</span></span></th>
<th><span data-ttu-id="506fb-175">สกุลเงินในธุรกรรม</span><span class="sxs-lookup"><span data-stu-id="506fb-175">Transaction currency</span></span></th>
<th><span data-ttu-id="506fb-176">ราคาคงที่</span><span class="sxs-lookup"><span data-stu-id="506fb-176">Fixed price</span></span></th>
<th><span data-ttu-id="506fb-177">สกุลเงินในธุรกรรม</span><span class="sxs-lookup"><span data-stu-id="506fb-177">Transaction currency</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="506fb-178">รายการเวลาถูกสร้างขึ้น</span><span class="sxs-lookup"><span data-stu-id="506fb-178">A time entry is created.</span></span></td>
<td colspan="6"><span data-ttu-id="506fb-179">ไม่มีกิจกรรมในเอนทิตีที่เกิดขึ้นจริง</span><span class="sxs-lookup"><span data-stu-id="506fb-179">No activity in the Actuals entity</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="506fb-180">รายการเวลาถูกส่ง</span><span class="sxs-lookup"><span data-stu-id="506fb-180">A time entry is submitted.</span></span></td>
<td colspan="6"><span data-ttu-id="506fb-181">ไม่มีกิจกรรมในเอนทิตีที่เกิดขึ้นจริง</span><span class="sxs-lookup"><span data-stu-id="506fb-181">No activity in the Actuals entity</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="506fb-182">เวลาได้รับการอนุมัติ และไม่มีการเปลี่ยนแปลงหรือเพิ่มขึ้นของชั่วโมงที่เรียกเก็บเงินได้เกิดขึ้น ในระหว่างการอนุมัติ</span><span class="sxs-lookup"><span data-stu-id="506fb-182">Time is approved, and no change to or increase in billable hours occurs during approval.</span></span></td>
<td><span data-ttu-id="506fb-183">จำนวนจริงของต้นทุน</span><span class="sxs-lookup"><span data-stu-id="506fb-183">Cost actual</span></span></td>
<td><span data-ttu-id="506fb-184">สกุลเงินของหน่วยที่ทำสัญญา</span><span class="sxs-lookup"><span data-stu-id="506fb-184">Contracting unit currency</span></span></td>
<td rowspan="2"><span data-ttu-id="506fb-185">จำนวนจริงของต้นทุน</span><span class="sxs-lookup"><span data-stu-id="506fb-185">Cost actual</span></span></td>
<td rowspan="2"><span data-ttu-id="506fb-186">สกุลเงินของหน่วยที่ทำสัญญา</span><span class="sxs-lookup"><span data-stu-id="506fb-186">Contracting unit currency</span></span>
<td rowspan="2"><span data-ttu-id="506fb-187">จำนวนจริงของต้นทุน</span><span class="sxs-lookup"><span data-stu-id="506fb-187">Cost actual</span></span></td>
<td rowspan="2"><span data-ttu-id="506fb-188">จำนวนจริงของต้นทุน</span><span class="sxs-lookup"><span data-stu-id="506fb-188">Cost actual</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="506fb-189">การขายที่เกิดขึ้นจริงที่ยังไม่ได้เรียกเก็บและคิดค่าธรรมเนียมได้</span><span class="sxs-lookup"><span data-stu-id="506fb-189">Unbilled sales actual – Chargeable</span></span></td>
<td><span data-ttu-id="506fb-190">สกุลเงินตามสัญญาโครงการ</span><span class="sxs-lookup"><span data-stu-id="506fb-190">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="506fb-191">เวลาได้รับการอนุมัติ และการลดลงของชั่วโมงที่เรียกเก็บเงินได้เกิดขึ้น ในระหว่างการอนุมัติ</span><span class="sxs-lookup"><span data-stu-id="506fb-191">Time is approved, and a decrease in billable hours occurs during approval.</span></span></td>
<td><span data-ttu-id="506fb-192">จำนวนจริงของต้นทุน</span><span class="sxs-lookup"><span data-stu-id="506fb-192">Cost actual</span></span></td>
<td><span data-ttu-id="506fb-193">สกุลเงินของหน่วยที่ทำสัญญา</span><span class="sxs-lookup"><span data-stu-id="506fb-193">Contracting unit currency</span></span></td>
<td rowspan="3"><span data-ttu-id="506fb-194">จำนวนจริงของต้นทุน</span><span class="sxs-lookup"><span data-stu-id="506fb-194">Cost actual</span></span></td>
<td rowspan="3"><span data-ttu-id="506fb-195">สกุลเงินของหน่วยที่ทำสัญญา</span><span class="sxs-lookup"><span data-stu-id="506fb-195">Contracting unit currency</span></span></td>
<td rowspan="3"><span data-ttu-id="506fb-196">จำนวนจริงของต้นทุน</span><span class="sxs-lookup"><span data-stu-id="506fb-196">Cost actual</span></span></td>
<td rowspan="3"><span data-ttu-id="506fb-197">จำนวนจริงของต้นทุน</span><span class="sxs-lookup"><span data-stu-id="506fb-197">Cost actual</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="506fb-198">การขายที่ยังไม่ได้เรียกเก็บและคิดค่าธรรมเนียมได้ตามจริง สำหรับปริมาณใหม่</span><span class="sxs-lookup"><span data-stu-id="506fb-198">Unbilled sales actual – Chargeable for the new quantity</span></span></td>
<td><span data-ttu-id="506fb-199">สกุลเงินตามสัญญาโครงการ</span><span class="sxs-lookup"><span data-stu-id="506fb-199">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="506fb-200">การขายที่ยังไม่ได้เรียกเก็บและคิดค่าธรรมเนียมไม่ได้ตามจริง สำหรับความแตกต่าง</span><span class="sxs-lookup"><span data-stu-id="506fb-200">Unbilled sales actual – Non-chargeable for the difference</span></span></td>
<td><span data-ttu-id="506fb-201">สกุลเงินตามสัญญาโครงการ</span><span class="sxs-lookup"><span data-stu-id="506fb-201">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="506fb-202">ใบแจ้งหนี้ได้รับการยืนยัน และไม่มีการเปลี่ยนแปลงหรือเพิ่มขึ้นของชั่วโมงที่เรียกเก็บเงินได้เกิดขึ้น</span><span class="sxs-lookup"><span data-stu-id="506fb-202">An invoice is confirmed, and no change to or increase in billable hours occurs.</span></span></td>
<td><span data-ttu-id="506fb-203">การกลับการขายที่ยังไม่ได้เรียกเก็บเงิน</span><span class="sxs-lookup"><span data-stu-id="506fb-203">Unbilled sales reversal</span></span></td>
<td><span data-ttu-id="506fb-204">สกุลเงินตามสัญญาโครงการ</span><span class="sxs-lookup"><span data-stu-id="506fb-204">Project contract currency</span></span></td>
<td rowspan="2"><span data-ttu-id="506fb-205">การขายที่เรียกเก็บเงินสำหรับหลักเป้าหมาย</span><span class="sxs-lookup"><span data-stu-id="506fb-205">Billed sales for milestone</span></span></td>
<td rowspan="2"><span data-ttu-id="506fb-206">สกุลเงินตามสัญญาโครงการ</span><span class="sxs-lookup"><span data-stu-id="506fb-206">Project contract currency</span></span></td>
<td rowspan="2"><span data-ttu-id="506fb-207">ไม่สามารถใช้งานได้</span><span class="sxs-lookup"><span data-stu-id="506fb-207">Not applicable</span></span></td>
<td rowspan="2"><span data-ttu-id="506fb-208">ไม่สามารถใช้งานได้</span><span class="sxs-lookup"><span data-stu-id="506fb-208">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="506fb-209">การขายที่เรียกเก็บเงินแล้ว</span><span class="sxs-lookup"><span data-stu-id="506fb-209">Billed sales</span></span></td>
<td><span data-ttu-id="506fb-210">สกุลเงินตามสัญญาโครงการ</span><span class="sxs-lookup"><span data-stu-id="506fb-210">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="506fb-211">ใบแจ้งหนี้ได้รับการยืนยัน และการลดลงของชั่วโมงที่เรียกเก็บเงินได้เกิดขึ้น</span><span class="sxs-lookup"><span data-stu-id="506fb-211">An invoice is confirmed, and a decrease in billable hours occurs.</span></span></td>
<td><span data-ttu-id="506fb-212">การกลับการขายที่ยังไม่ได้เรียกเก็บเงิน</span><span class="sxs-lookup"><span data-stu-id="506fb-212">Unbilled sales reversal</span></span></td>
<td><span data-ttu-id="506fb-213">สกุลเงินตามสัญญาโครงการ</span><span class="sxs-lookup"><span data-stu-id="506fb-213">Project contract currency</span></span></td>
<td rowspan="3"><span data-ttu-id="506fb-214">ไม่สามารถใช้งานได้</span><span class="sxs-lookup"><span data-stu-id="506fb-214">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="506fb-215">ไม่สามารถใช้งานได้</span><span class="sxs-lookup"><span data-stu-id="506fb-215">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="506fb-216">ไม่สามารถใช้งานได้</span><span class="sxs-lookup"><span data-stu-id="506fb-216">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="506fb-217">ไม่สามารถใช้งานได้</span><span class="sxs-lookup"><span data-stu-id="506fb-217">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="506fb-218">การขายที่เรียกเก็บแล้วและคิดค่าธรรมเนียมได้ สำหรับปริมาณใหม่</span><span class="sxs-lookup"><span data-stu-id="506fb-218">Billed sales – Chargeable for the new quantity</span></span></td>
<td><span data-ttu-id="506fb-219">สกุลเงินตามสัญญาโครงการ</span><span class="sxs-lookup"><span data-stu-id="506fb-219">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="506fb-220">การขายที่เรียกเก็บเงินแล้วและคิดค่าธรรมเนียมไม่ได้ สำหรับความแตกต่าง</span><span class="sxs-lookup"><span data-stu-id="506fb-220">Billed sales – Non-chargeable for the difference</span></span></td>
<td><span data-ttu-id="506fb-221">สกุลเงินตามสัญญาโครงการ</span><span class="sxs-lookup"><span data-stu-id="506fb-221">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="506fb-222">ใบแจ้งหนี้จะถูกแก้ไขเพื่อเพิ่มปริมาณที่คิดค่าธรรมเนียมได้</span><span class="sxs-lookup"><span data-stu-id="506fb-222">An invoice is corrected to increase the chargeable quantity.</span></span></td>
<td><span data-ttu-id="506fb-223">การขายที่เรียกเก็บเงินแล้ว ย้อนกลับ</span><span class="sxs-lookup"><span data-stu-id="506fb-223">Billed sales – Reversal</span></span></td>
<td><span data-ttu-id="506fb-224">สกุลเงินตามสัญญาโครงการ</span><span class="sxs-lookup"><span data-stu-id="506fb-224">Project contract currency</span></span></td>
<td rowspan="5">
<ul>
<li><span data-ttu-id="506fb-225">การย้อนกลับการขายที่เรียกเก็บเงินแล้วสำหรับหลักเป้าหมาย</span><span class="sxs-lookup"><span data-stu-id="506fb-225">Billed sales reversal for milestone</span></span></li>
<li><span data-ttu-id="506fb-226">เปลี่ยนสถานะหลักเป้าหมาย จาก <strong>ออกใบหนี้</strong> เป็น <strong>พร้อมสำหรับใบแจ้งหนี้</strong></span><span class="sxs-lookup"><span data-stu-id="506fb-226">Change in milestone status from <strong>Invoiced</strong> to <strong>Ready for invoice</strong></span></span></li>
</ul>
</td>
<td rowspan="5"><span data-ttu-id="506fb-227">สกุลเงินตามสัญญาโครงการ</span><span class="sxs-lookup"><span data-stu-id="506fb-227">Project contract currency</span></span></td>
<td rowspan="5"><span data-ttu-id="506fb-228">ไม่สามารถใช้งานได้</span><span class="sxs-lookup"><span data-stu-id="506fb-228">Not applicable</span></span></td>
<td rowspan="5"><span data-ttu-id="506fb-229">ไม่สามารถใช้งานได้</span><span class="sxs-lookup"><span data-stu-id="506fb-229">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="506fb-230">การขายที่เรียกเก็บเงินแล้ว</span><span class="sxs-lookup"><span data-stu-id="506fb-230">Billed sales</span></span></td>
<td><span data-ttu-id="506fb-231">สกุลเงินตามสัญญาโครงการ</span><span class="sxs-lookup"><span data-stu-id="506fb-231">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="506fb-232">ใบแจ้งหนี้จะถูกแก้ไขเพื่อลดปริมาณที่คิดค่าธรรมเนียมได้</span><span class="sxs-lookup"><span data-stu-id="506fb-232">An invoice is corrected to decrease the chargeable quantity.</span></span></td>
<td><span data-ttu-id="506fb-233">การขายที่เรียกเก็บเงินแล้ว ย้อนกลับ</span><span class="sxs-lookup"><span data-stu-id="506fb-233">Billed sales – Reversal</span></span></td>
<td><span data-ttu-id="506fb-234">สกุลเงินตามสัญญาโครงการ</span><span class="sxs-lookup"><span data-stu-id="506fb-234">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="506fb-235">การขายที่เรียกเก็บเงินแล้วสำหรับปริมาณใหม่</span><span class="sxs-lookup"><span data-stu-id="506fb-235">Billed sales for the new quantity</span></span></td>
<td><span data-ttu-id="506fb-236">สกุลเงินตามสัญญาโครงการ</span><span class="sxs-lookup"><span data-stu-id="506fb-236">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="506fb-237">การขายที่ยังไม่เรียกเก็บเงินและคิดค่าธรรมเนียมได้ สำหรับความแตกต่าง</span><span class="sxs-lookup"><span data-stu-id="506fb-237">Unbilled sales – Chargeable for the difference</span></span></td>
<td><span data-ttu-id="506fb-238">สกุลเงินตามสัญญาโครงการ</span><span class="sxs-lookup"><span data-stu-id="506fb-238">Project contract currency</span></span></td>
</tr>
</tbody>
</table>

### <a name="the-resource-belongs-to-an-organizational-unit-that-differs-from-the-projects-contracting-unit"></a><span data-ttu-id="506fb-239">ทรัพยากรเป็นของหน่วยองค์กรที่แตกต่างจากหน่วยที่ทำสัญญาของโครงการ</span><span class="sxs-lookup"><span data-stu-id="506fb-239">The resource belongs to an organizational unit that differs from the project's contracting unit</span></span>

<table>
<thead>
<tr>
<th rowspan="3"><span data-ttu-id="506fb-240">เหตุการณ์</span><span class="sxs-lookup"><span data-stu-id="506fb-240">Event</span></span></th>
<th colspan="4"><span data-ttu-id="506fb-241">โครงการที่เรียกเก็บเงินได้หรือขายแล้ว</span><span class="sxs-lookup"><span data-stu-id="506fb-241">Billable or sold project</span></span></th>
<th rowspan="3"><span data-ttu-id="506fb-242">โครงการในระยะที่ำกำหนด</span><span class="sxs-lookup"><span data-stu-id="506fb-242">Project in the presales stage</span></span></th>
<th rowspan="3"><span data-ttu-id="506fb-243">โครงการภายใน</span><span class="sxs-lookup"><span data-stu-id="506fb-243">Internal project</span></span></th>
</tr>
<tr>
<th colspan="2"><span data-ttu-id="506fb-244">เวลาและวัสดุ</span><span class="sxs-lookup"><span data-stu-id="506fb-244">Time and materials</span></span></th>
<th colspan="2"><span data-ttu-id="506fb-245">ราคาคงที่</span><span class="sxs-lookup"><span data-stu-id="506fb-245">Fixed price</span></span></th>
</tr>
<tr>
<th><span data-ttu-id="506fb-246">ตามจริง</span><span class="sxs-lookup"><span data-stu-id="506fb-246">Actuals</span></span></th>
<th><span data-ttu-id="506fb-247">สกุลเงินในธุรกรรม</span><span class="sxs-lookup"><span data-stu-id="506fb-247">Transaction currency</span></span></th>
<th><span data-ttu-id="506fb-248">ราคาคงที่</span><span class="sxs-lookup"><span data-stu-id="506fb-248">Fixed price</span></span></th>
<th><span data-ttu-id="506fb-249">สกุลเงินในธุรกรรม</span><span class="sxs-lookup"><span data-stu-id="506fb-249">Transaction currency</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="506fb-250">รายการเวลาถูกสร้างขึ้น</span><span class="sxs-lookup"><span data-stu-id="506fb-250">A time entry is created.</span></span></td>
<td colspan="6"><span data-ttu-id="506fb-251">ไม่มีกิจกรรมในเอนทิตีที่เกิดขึ้นจริง</span><span class="sxs-lookup"><span data-stu-id="506fb-251">No activity in the Actuals entity</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="506fb-252">รายการเวลาถูกส่ง</span><span class="sxs-lookup"><span data-stu-id="506fb-252">A time entry is submitted.</span></span></td>
<td colspan="6"><span data-ttu-id="506fb-253">ไม่มีกิจกรรมในเอนทิตีที่เกิดขึ้นจริง</span><span class="sxs-lookup"><span data-stu-id="506fb-253">No activity in the Actuals entity</span></span></td>
</tr>
<tr>
<td rowspan="4"><span data-ttu-id="506fb-254">เวลาได้รับการอนุมัติ และไม่มีการเปลี่ยนแปลงหรือเพิ่มขึ้นของชั่วโมงที่เรียกเก็บเงินได้เกิดขึ้น ในระหว่างการอนุมัติ</span><span class="sxs-lookup"><span data-stu-id="506fb-254">Time is approved, and no change to or increase in billable hours occurs during approval.</span></span></td>
<td><span data-ttu-id="506fb-255">จำนวนจริงของต้นทุน</span><span class="sxs-lookup"><span data-stu-id="506fb-255">Cost actual</span></span></td>
<td><span data-ttu-id="506fb-256">สกุลเงินของหน่วยที่ทำสัญญา</span><span class="sxs-lookup"><span data-stu-id="506fb-256">Contracting unit currency</span></span></td>
<td rowspan="4"><span data-ttu-id="506fb-257">จำนวนจริงของต้นทุน</span><span class="sxs-lookup"><span data-stu-id="506fb-257">Cost actual</span></span></td>
<td rowspan="4"><span data-ttu-id="506fb-258">สกุลเงินของหน่วยที่ทำสัญญา</span><span class="sxs-lookup"><span data-stu-id="506fb-258">Contracting unit currency</span></span></td>
<td rowspan="4"><span data-ttu-id="506fb-259">จำนวนจริงของต้นทุน</span><span class="sxs-lookup"><span data-stu-id="506fb-259">Cost actual</span></span></td>
<td rowspan="4"><span data-ttu-id="506fb-260">จำนวนจริงของต้นทุน</span><span class="sxs-lookup"><span data-stu-id="506fb-260">Cost actual</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="506fb-261">การขายที่เกิดขึ้นจริงที่ยังไม่ได้เรียกเก็บและคิดค่าธรรมเนียมได้</span><span class="sxs-lookup"><span data-stu-id="506fb-261">Unbilled sales actual – Chargeable</span></span></td>
<td><span data-ttu-id="506fb-262">สกุลเงินตามสัญญาโครงการ</span><span class="sxs-lookup"><span data-stu-id="506fb-262">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="506fb-263">ต้นทุนต่อหน่วยการจัดเตรียมทรัพยากร</span><span class="sxs-lookup"><span data-stu-id="506fb-263">Resourcing unit cost</span></span></td>
<td><span data-ttu-id="506fb-264">สกุลเงินต่อหน่วยการจัดเตรียมทรัพยากร</span><span class="sxs-lookup"><span data-stu-id="506fb-264">Resourcing unit currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="506fb-265">การขายระหว่างองค์กร</span><span class="sxs-lookup"><span data-stu-id="506fb-265">Interorganizational sales</span></span></td>
<td><span data-ttu-id="506fb-266">สกุลเงินของหน่วยที่ทำสัญญา</span><span class="sxs-lookup"><span data-stu-id="506fb-266">Contracting unit currency</span></span></td>
</tr>
<tr>
<td rowspan="5"><span data-ttu-id="506fb-267">เวลาได้รับการอนุมัติ และการลดลงของชั่วโมงที่เรียกเก็บเงินได้เกิดขึ้น ในระหว่างการอนุมัติ</span><span class="sxs-lookup"><span data-stu-id="506fb-267">Time is approved, and a decrease in billable hours occurs during approval.</span></span></td>
<td><span data-ttu-id="506fb-268">จำนวนจริงของต้นทุน</span><span class="sxs-lookup"><span data-stu-id="506fb-268">Cost actual</span></span></td>
<td><span data-ttu-id="506fb-269">สกุลเงินของหน่วยที่ทำสัญญา</span><span class="sxs-lookup"><span data-stu-id="506fb-269">Contracting unit currency</span></span></td>
<td rowspan="5"><span data-ttu-id="506fb-270">จำนวนจริงของต้นทุน</span><span class="sxs-lookup"><span data-stu-id="506fb-270">Cost actual</span></span></td>
<td rowspan="5"><span data-ttu-id="506fb-271">สกุลเงินของหน่วยที่ทำสัญญา</span><span class="sxs-lookup"><span data-stu-id="506fb-271">Contracting unit currency</span></span></td>
<td rowspan="5"><span data-ttu-id="506fb-272">จำนวนจริงของต้นทุน</span><span class="sxs-lookup"><span data-stu-id="506fb-272">Cost actual</span></span></td>
<td rowspan="5"><span data-ttu-id="506fb-273">จำนวนจริงของต้นทุน</span><span class="sxs-lookup"><span data-stu-id="506fb-273">Cost actual</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="506fb-274">ต้นทุนต่อหน่วยการจัดเตรียมทรัพยากร</span><span class="sxs-lookup"><span data-stu-id="506fb-274">Resourcing unit cost</span></span></td>
<td><span data-ttu-id="506fb-275">สกุลเงินต่อหน่วยการจัดเตรียมทรัพยากร</span><span class="sxs-lookup"><span data-stu-id="506fb-275">Resourcing unit currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="506fb-276">การขายระหว่างองค์กร</span><span class="sxs-lookup"><span data-stu-id="506fb-276">Interorganizational sales</span></span></td>
<td><span data-ttu-id="506fb-277">สกุลเงินของหน่วยที่ทำสัญญา</span><span class="sxs-lookup"><span data-stu-id="506fb-277">Contracting unit currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="506fb-278">การขายที่ยังไม่ได้เรียกเก็บและคิดค่าธรรมเนียมได้ตามจริง สำหรับปริมาณใหม่</span><span class="sxs-lookup"><span data-stu-id="506fb-278">Unbilled sales actual – Chargeable for the new quantity</span></span></td>
<td><span data-ttu-id="506fb-279">สกุลเงินตามสัญญาโครงการ</span><span class="sxs-lookup"><span data-stu-id="506fb-279">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="506fb-280">การขายที่ยังไม่ได้เรียกเก็บและคิดค่าธรรมเนียมไม่ได้ตามจริง สำหรับความแตกต่าง</span><span class="sxs-lookup"><span data-stu-id="506fb-280">Unbilled sales actual – Non-chargeable for the difference</span></span></td>
<td><span data-ttu-id="506fb-281">สกุลเงินตามสัญญาโครงการ</span><span class="sxs-lookup"><span data-stu-id="506fb-281">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="506fb-282">ใบแจ้งหนี้ได้รับการยืนยัน และไม่มีการเปลี่ยนแปลงหรือเพิ่มขึ้นของชั่วโมงที่เรียกเก็บเงินได้เกิดขึ้น</span><span class="sxs-lookup"><span data-stu-id="506fb-282">An invoice is confirmed, and no change to or increase in billable hours occurs.</span></span></td>
<td><span data-ttu-id="506fb-283">การกลับการขายที่ยังไม่ได้เรียกเก็บเงิน</span><span class="sxs-lookup"><span data-stu-id="506fb-283">Unbilled sales reversal</span></span></td>
<td><span data-ttu-id="506fb-284">สกุลเงินตามสัญญาโครงการ</span><span class="sxs-lookup"><span data-stu-id="506fb-284">Project contract currency</span></span></td>
<td rowspan="2"><span data-ttu-id="506fb-285">การขายที่เรียกเก็บเงินสำหรับหลักเป้าหมาย</span><span class="sxs-lookup"><span data-stu-id="506fb-285">Billed sales for milestone</span></span></td>
<td rowspan="2"><span data-ttu-id="506fb-286">สกุลเงินตามสัญญาโครงการ</span><span class="sxs-lookup"><span data-stu-id="506fb-286">Project contract currency</span></span></td>
<td rowspan="2"><span data-ttu-id="506fb-287">ไม่สามารถใช้งานได้</span><span class="sxs-lookup"><span data-stu-id="506fb-287">Not applicable</span></span></td>
<td rowspan="2"><span data-ttu-id="506fb-288">ไม่สามารถใช้งานได้</span><span class="sxs-lookup"><span data-stu-id="506fb-288">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="506fb-289">การขายที่เรียกเก็บเงินแล้ว</span><span class="sxs-lookup"><span data-stu-id="506fb-289">Billed sales</span></span></td>
<td><span data-ttu-id="506fb-290">สกุลเงินตามสัญญาโครงการ</span><span class="sxs-lookup"><span data-stu-id="506fb-290">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="506fb-291">ใบแจ้งหนี้ได้รับการยืนยัน และการลดลงของชั่วโมงที่เรียกเก็บเงินได้เกิดขึ้น</span><span class="sxs-lookup"><span data-stu-id="506fb-291">An invoice is confirmed, and a decrease in billable hours occurs.</span></span></td>
<td><span data-ttu-id="506fb-292">การกลับการขายที่ยังไม่ได้เรียกเก็บเงิน</span><span class="sxs-lookup"><span data-stu-id="506fb-292">Unbilled sales reversal</span></span></td>
<td><span data-ttu-id="506fb-293">สกุลเงินตามสัญญาโครงการ</span><span class="sxs-lookup"><span data-stu-id="506fb-293">Project contract currency</span></span></td>
<td rowspan="3"><span data-ttu-id="506fb-294">ไม่สามารถใช้งานได้</span><span class="sxs-lookup"><span data-stu-id="506fb-294">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="506fb-295">ไม่สามารถใช้งานได้</span><span class="sxs-lookup"><span data-stu-id="506fb-295">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="506fb-296">ไม่สามารถใช้งานได้</span><span class="sxs-lookup"><span data-stu-id="506fb-296">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="506fb-297">ไม่สามารถใช้งานได้</span><span class="sxs-lookup"><span data-stu-id="506fb-297">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="506fb-298">การขายที่เรียกเก็บแล้วและคิดค่าธรรมเนียมได้ สำหรับปริมาณใหม่</span><span class="sxs-lookup"><span data-stu-id="506fb-298">Billed sales – Chargeable for the new quantity</span></span></td>
<td><span data-ttu-id="506fb-299">สกุลเงินตามสัญญาโครงการ</span><span class="sxs-lookup"><span data-stu-id="506fb-299">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="506fb-300">การขายที่เรียกเก็บเงินแล้วและคิดค่าธรรมเนียมไม่ได้ สำหรับความแตกต่าง</span><span class="sxs-lookup"><span data-stu-id="506fb-300">Billed sales – Non-chargeable for the difference</span></span></td>
<td><span data-ttu-id="506fb-301">สกุลเงินตามสัญญาโครงการ</span><span class="sxs-lookup"><span data-stu-id="506fb-301">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="506fb-302">ใบแจ้งหนี้จะถูกแก้ไขเพื่อเพิ่มปริมาณที่คิดค่าธรรมเนียมได้</span><span class="sxs-lookup"><span data-stu-id="506fb-302">An invoice is corrected to increase the chargeable quantity.</span></span></td>
<td><span data-ttu-id="506fb-303">การขายที่เรียกเก็บเงินแล้ว ย้อนกลับ</span><span class="sxs-lookup"><span data-stu-id="506fb-303">Billed sales – Reversal</span></span></td>
<td><span data-ttu-id="506fb-304">สกุลเงินตามสัญญาโครงการ</span><span class="sxs-lookup"><span data-stu-id="506fb-304">Project contract currency</span></span></td>
<td rowspan="5">
<ul>
<li><span data-ttu-id="506fb-305">การย้อนกลับการขายที่เรียกเก็บเงินแล้วสำหรับหลักเป้าหมาย</span><span class="sxs-lookup"><span data-stu-id="506fb-305">Billed sales reversal for milestone</span></span></li>
<li><span data-ttu-id="506fb-306">เปลี่ยนสถานะหลักเป้าหมาย จาก <strong>ออกใบหนี้</strong> เป็น <strong>พร้อมสำหรับใบแจ้งหนี้</strong></span><span class="sxs-lookup"><span data-stu-id="506fb-306">Change in milestone status from <strong>Invoiced</strong> to <strong>Ready for invoice</strong></span></span></li>
</ul>
</td>
<td rowspan="5"><span data-ttu-id="506fb-307">สกุลเงินตามสัญญาโครงการ</span><span class="sxs-lookup"><span data-stu-id="506fb-307">Project contract currency</span></span></td>
<td rowspan="5"><span data-ttu-id="506fb-308">ไม่สามารถใช้งานได้</span><span class="sxs-lookup"><span data-stu-id="506fb-308">Not applicable</span></span></td>
<td rowspan="5"><span data-ttu-id="506fb-309">ไม่สามารถใช้งานได้</span><span class="sxs-lookup"><span data-stu-id="506fb-309">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="506fb-310">การขายที่เรียกเก็บเงินแล้ว</span><span class="sxs-lookup"><span data-stu-id="506fb-310">Billed sales</span></span></td>
<td><span data-ttu-id="506fb-311">สกุลเงินตามสัญญาโครงการ</span><span class="sxs-lookup"><span data-stu-id="506fb-311">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="506fb-312">ใบแจ้งหนี้จะถูกแก้ไขเพื่อลดปริมาณที่คิดค่าธรรมเนียมได้</span><span class="sxs-lookup"><span data-stu-id="506fb-312">An invoice is corrected to decrease the chargeable quantity.</span></span></td>
<td><span data-ttu-id="506fb-313">การขายที่เรียกเก็บเงินแล้ว ย้อนกลับ</span><span class="sxs-lookup"><span data-stu-id="506fb-313">Billed sales – Reversal</span></span></td>
<td><span data-ttu-id="506fb-314">สกุลเงินตามสัญญาโครงการ</span><span class="sxs-lookup"><span data-stu-id="506fb-314">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="506fb-315">การขายที่เรียกเก็บเงินแล้วสำหรับปริมาณใหม่</span><span class="sxs-lookup"><span data-stu-id="506fb-315">Billed sales for the new quantity</span></span></td>
<td><span data-ttu-id="506fb-316">สกุลเงินตามสัญญาโครงการ</span><span class="sxs-lookup"><span data-stu-id="506fb-316">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="506fb-317">การขายที่ยังไม่เรียกเก็บเงินและคิดค่าธรรมเนียมได้ สำหรับความแตกต่าง</span><span class="sxs-lookup"><span data-stu-id="506fb-317">Unbilled sales – Chargeable for the difference</span></span></td>
<td><span data-ttu-id="506fb-318">สกุลเงินตามสัญญาโครงการ</span><span class="sxs-lookup"><span data-stu-id="506fb-318">Project contract currency</span></span></td>
</tr>
</tbody>
</table>


[!INCLUDE[footer-include](../includes/footer-banner.md)]
