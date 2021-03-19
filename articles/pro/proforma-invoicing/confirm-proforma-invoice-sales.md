---
title: ยืนยันใบแจ้งหนี้ชั่วคราว - Lite
description: หัวข้อนี้ให้ข้อมูลเกี่ยวกับการยืนยันใบแจ้งหนี้ Proforma ใน Project Operations
author: rumant
manager: Annbe
ms.date: 10/13/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 3b1818f20a0d54848939b689f87986154943c57a
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 02/15/2021
ms.locfileid: "5274301"
---
# <a name="confirm-a-proforma-invoice---lite"></a><span data-ttu-id="9a8dd-103">ยืนยันใบแจ้งหนี้ชั่วคราว - Lite</span><span class="sxs-lookup"><span data-stu-id="9a8dd-103">Confirm a proforma invoice - lite</span></span>

<span data-ttu-id="9a8dd-104">_**นำไปใช้กับ:** การปรับใช้งานแบบ Lite - จัดการกับการออกใบแจ้งหนี้ชั่วคราว_</span><span class="sxs-lookup"><span data-stu-id="9a8dd-104">_**Applies To:** Lite deployment - deal to proforma invoicing_</span></span>


<span data-ttu-id="9a8dd-105">หลังจากยืนยันใบแจ้งหนี้ Proforma แล้วสถานะของใบแจ้งหนี้โครงการจะอัปเดตเป็น **ได้รับการยืนยัน**</span><span class="sxs-lookup"><span data-stu-id="9a8dd-105">After a proforma invoice is confirmed, the status of the project invoice updates to **Confirmed**.</span></span> <span data-ttu-id="9a8dd-106">เมื่อใบแจ้งหนี้ได้รับการยืนยัน จะกลายเป็นแบบอ่านอย่างเดียว</span><span class="sxs-lookup"><span data-stu-id="9a8dd-106">When an invoice is confirmed, it becomes read-only.</span></span> <span data-ttu-id="9a8dd-107">นับจากนี้จะสามารถแก้ไขใบแจ้งหนี้ได้ก็ต่อเมื่อมีการแก้ไขหรือเครดิตที่ลูกค้าเป็นผู้เริ่มต้นหรือเมื่อมีการทำเครื่องหมายใบแจ้งหนี้ว่าชำระเงินแล้ว</span><span class="sxs-lookup"><span data-stu-id="9a8dd-107">Going forward, the invoice can only be corrected if there are any customer-initiated corrections or credits, of if the invoice is marked as paid.</span></span>

<span data-ttu-id="9a8dd-108">ตารางต่อไปนี้แสดงรายการจริงที่สร้างโดยระบบ</span><span class="sxs-lookup"><span data-stu-id="9a8dd-108">The following table lists the actuals created by the system.</span></span> <span data-ttu-id="9a8dd-109">ข้อมูลจริงเหล่านี้ถูกสร้างขึ้นเมื่อมีการดำเนินการบางอย่างในใบแจ้งหนี้โครงการแบบร่างก่อนที่จะได้รับการยืนยัน</span><span class="sxs-lookup"><span data-stu-id="9a8dd-109">These actuals are created when certain operations are performed on the draft project invoice before it is confirmed.</span></span>

<table border="0" cellspacing="0" cellpadding="0">
    <tbody>
        <tr>
            <td width="216" valign="top">
                <p><span data-ttu-id="9a8dd-110">
                    <strong>สถานการณ์สมมติ</strong>
                </span><span class="sxs-lookup"><span data-stu-id="9a8dd-110">
                    <strong>Scenario</strong>
                </span></span></p>
            </td>
            <td width="808" valign="top">
                <p><span data-ttu-id="9a8dd-111">
                    <strong>สิ่งที่เกิดขึ้นจริงสร้างขึ้นจากการยืนยัน</strong>
                </span><span class="sxs-lookup"><span data-stu-id="9a8dd-111">
                    <strong>Actuals created on confirmation</strong>
                </span></span></p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="9a8dd-112">ออกใบแจ้งหนี้หรือค่าธรรมเนียมล่วงหน้า</span><span class="sxs-lookup"><span data-stu-id="9a8dd-112">Invoicing an advance or retainer</span></span> </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="9a8dd-113">การขายที่เรียกเก็บเงินจริงของประเภท <strong>ค่าธรรมเนียมล่วงหน้า</strong> ถูกสร้างขึ้นสำหรับจำนวนเงินล่วงหน้าหรือค่าธรรมเนียมล่วงหน้า</span><span class="sxs-lookup"><span data-stu-id="9a8dd-113">A billed sales actual of type, <strong>Retainer</strong> is created for the amount on the advance or retainer.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="9a8dd-114">การขายจริงที่ยังไม่ได้เรียกเก็บเงินของจำนวนเงินติดลบของค่าธรรมเนียมล่วงหน้าเพื่อจะใช้สำหรับการกระทบยอด</span><span class="sxs-lookup"><span data-stu-id="9a8dd-114">An unbilled sales actual of a negative amount of the retainer or advance to be used for reconciliation.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="9a8dd-115">หลังจากกระทบยอดค่าธรรมเนียมล่วงหน้าเต็มหรือจำนวนเงินล่วงหน้าในใบแจ้งหนี้</span><span class="sxs-lookup"><span data-stu-id="9a8dd-115">After fully reconciling a retainer or advance on an invoice.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="9a8dd-116">การกลับรายการการขายที่ยังไม่เรียกเก็บเงินของค่าธรรมเนียมล่วงหน้าหรือจำนวนเงินล่วงหน้าที่สร้างขึ้นสำหรับการกระทบยอด</span><span class="sxs-lookup"><span data-stu-id="9a8dd-116">An unbilled sales reversal of the retainer or advance that was created for reconciliation.</span></span> <span data-ttu-id="9a8dd-117">จำนวนนี้เป็นค่าบวกเนื่องจากมีวัตถุประสงค์เพื่อยกเลิกค่าลบที่สร้างขึ้นเมื่อมีการออกใบแจ้งหนี้ค่าธรรมเนียมล่วงหน้าหรือเงินล่วงหน้า</span><span class="sxs-lookup"><span data-stu-id="9a8dd-117">This amount is positive as it's meant to cancel out the negative that was created when the retainer or advance was invoiced.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="9a8dd-118">การกลับรายการขายที่เรียกเก็บเงินจริงสำหรับยอดเงินในใบแจ้งหนี้นี้</span><span class="sxs-lookup"><span data-stu-id="9a8dd-118">A billed sales actual for the amount on this invoice.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="3" valign="top">
                <p>
<span data-ttu-id="9a8dd-119">หลังจากกระทบยอดค่าธรรมเนียมล่วงหน้าบางส่วนหรือจำนวนเงินล่วงหน้าในใบแจ้งหนี้</span><span class="sxs-lookup"><span data-stu-id="9a8dd-119">After partially reconciling a retainer or advance on an invoice.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="9a8dd-120">การกลับรายการการขายที่ยังไม่เรียกเก็บเงินของค่าธรรมเนียมล่วงหน้าหรือจำนวนเงินล่วงหน้าที่สร้างขึ้นสำหรับการกระทบยอด</span><span class="sxs-lookup"><span data-stu-id="9a8dd-120">An unbilled sales reversal of the retainer or advance that was created for reconciliation.</span></span> <span data-ttu-id="9a8dd-121">จำนวนนี้เป็นค่าบวกเนื่องจากมีวัตถุประสงค์เพื่อยกเลิกค่าลบที่สร้างขึ้นเมื่อมีการออกใบแจ้งหนี้ค่าธรรมเนียมล่วงหน้าหรือเงินล่วงหน้า</span><span class="sxs-lookup"><span data-stu-id="9a8dd-121">This amount is positive as it's meant to cancel out the negative that was created when the retainer or advance was invoiced.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="9a8dd-122">การกลับรายการขายที่เรียกเก็บเงินจริงสำหรับยอดเงินในใบแจ้งหนี้นี้</span><span class="sxs-lookup"><span data-stu-id="9a8dd-122">A billed sales actual for the amount on this invoice.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="9a8dd-123">การขายจริงที่ยังไม่ได้เรียกเก็บเงินที่ติดลบของค่าธรรมเนียมล่วงหน้าหรือจำนวนเงินล่วงหน้าเพื่อจะใช้สำหรับการกระทบยอดใบแจ้งหนี้ในอนาคต</span><span class="sxs-lookup"><span data-stu-id="9a8dd-123">A negative unbilled sales actual of the remaining retainer or advance amount to be used for reconciliation on future invoices.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="9a8dd-124">การออกใบแจ้งหนี้ธุรกรรมเวลาโดยไม่มีการแก้ไขใดๆ ในแบบร่างใบแจ้งหนี้</span><span class="sxs-lookup"><span data-stu-id="9a8dd-124">Invoicing a time transaction without any edits on the draft invoice.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="9a8dd-125">การกลับการขายที่ไม่ได้เรียกเก็บเงินสำหรับชั่วโมงและจำนวนเงินในการอนุมัติเวลาตามเดิม</span><span class="sxs-lookup"><span data-stu-id="9a8dd-125">An unbilled sales reversal for the hours and amount on the original time approval.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="9a8dd-126">การขายที่มีการเรียกเก็บเงินจริงสำหรับชั่วโมงและจำนวนเงินในการอนุมัติเวลาตามเดิม</span><span class="sxs-lookup"><span data-stu-id="9a8dd-126">A billed sales actual for the hours and amount on the original time approval.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="3" valign="top">
                <p>
<span data-ttu-id="9a8dd-127">การออกใบแจ้งหนี้ธุรกรรมเวลาที่แก้ไขเพื่อลดปริมาณ</span><span class="sxs-lookup"><span data-stu-id="9a8dd-127">Invoicing a time transaction that was edited to reduce the quantity.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="9a8dd-128">การกลับการขายที่ไม่ได้เรียกเก็บเงินสำหรับชั่วโมงและจำนวนเงินในการอนุมัติเวลาตามเดิม</span><span class="sxs-lookup"><span data-stu-id="9a8dd-128">An unbilled sales reversal for the hours and amount on the original time approval.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="9a8dd-129">การขายจริงใหม่ที่ยังไม่เรียกเก็บเงินซึ่งคิดค่าธรรมเนียมเป็นชั่วโมงและจำนวนเงินในรายละเอียดรายการใบแจ้งหนี้ที่แก้ไข การย้อนกลับของการขายจริงและเทียบเท่ากับการขายจริงที่เรียกเก็บเงิน</span><span class="sxs-lookup"><span data-stu-id="9a8dd-129">A new unbilled sales actual that is chargeable for the hours and amount on the edited invoice line detail, a reversal of the sales actual, and an equivalent billed sales actual.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="9a8dd-130">การขายจริงใหม่ที่ยังไม่เรียกเก็บเงินซึ่งไม่คิดค่าธรรมเนียมเป็นชั่วโมงและจำนวนเงินที่เหลือหลังจากการลดการกำหนดค่าที่แก้ไขในรายละเอียดรายการใบแจ้งหนี้ที่แก้ไข การย้อนกลับของการขายจริงและเทียบเท่ากับการขายจริงที่เรียกเก็บเงิน</span><span class="sxs-lookup"><span data-stu-id="9a8dd-130">A new unbilled sales actual that is non-chargeable for the remaining hours and amount after deducting the corrected figures on edited invoice line detail, a reversal of the sales actual, and an equivalent billed sales actual.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="9a8dd-131">การออกใบแจ้งหนี้ธุรกรรมเวลาที่แก้ไขเพื่อเพิ่มปริมาณ</span><span class="sxs-lookup"><span data-stu-id="9a8dd-131">Invoicing a time transaction that was edited to increase the quantity.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="9a8dd-132">การกลับการขายที่ไม่ได้เรียกเก็บเงินสำหรับชั่วโมงและจำนวนเงินในการอนุมัติเวลาตามเดิม</span><span class="sxs-lookup"><span data-stu-id="9a8dd-132">An unbilled sales reversal for the hours and amount on the original time approval.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="9a8dd-133">การขายจริงใหม่ที่ยังไม่เรียกเก็บเงินซึ่งคิดค่าธรรมเนียมเป็นชั่วโมงและจำนวนเงินในรายละเอียดรายการใบแจ้งหนี้ที่แก้ไข การย้อนกลับของการขายจริงที่ไม่ได้เรียกเก็บเงินและเทียบเท่ากับการขายจริงที่เรียกเก็บเงิน</span><span class="sxs-lookup"><span data-stu-id="9a8dd-133">A new unbilled sales actual that is chargeable for the hours and amount on the edited invoice line detail, a reversal of the unbilled sales actual, and an equivalent billed sales actual.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="9a8dd-134">การออกธุรกรรมค่าใช้จ่ายโดยไม่มีการแก้ไขใดๆ ในแบบร่างใบแจ้งหนี้</span><span class="sxs-lookup"><span data-stu-id="9a8dd-134">Invoicing an expense transaction without any edits on draft invoice.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="9a8dd-135">การกลับการขายที่ไม่ได้เรียกเก็บเงินสำหรับปริมาณและจำนวนเงินในการอนุมัติค่าใช้จ่ายตามเดิม</span><span class="sxs-lookup"><span data-stu-id="9a8dd-135">An unbilled sales reversal for the quantity and amount on the original expense approval.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="9a8dd-136">การขายจริงที่เรียกเก็บเงินสำหรับปริมาณและจำนวนเงินในการอนุมัติค่าใช้จ่ายตามเดิม</span><span class="sxs-lookup"><span data-stu-id="9a8dd-136">A billed sales actual for the quantity and amount on the original expense approval</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="3" valign="top">
                <p>
<span data-ttu-id="9a8dd-137">การออกใบแจ้งหนี้ธุรกรรมค่าใช้จ่ายที่แก้ไขเพื่อลดปริมาณ</span><span class="sxs-lookup"><span data-stu-id="9a8dd-137">Invoicing an expense transaction that was edited to reduce the quantity.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="9a8dd-138">การกลับการขายที่ไม่ได้เรียกเก็บเงินสำหรับปริมาณและจำนวนเงินในการอนุมัติค่าใช้จ่ายตามเดิม</span><span class="sxs-lookup"><span data-stu-id="9a8dd-138">An unbilled sales reversal for the quantity and amount on the original expense approval.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="9a8dd-139">การขายจริงใหม่ที่ยังไม่เรียกเก็บเงินซึ่งคิดค่าธรรมเนียมเป็นปริมาณและจำนวนเงินในรายละเอียดรายการใบแจ้งหนี้ที่แก้ไข การย้อนกลับของการขายจริงที่ไม่ได้เรียกเก็บเงินและเทียบเท่ากับการขายจริงที่เรียกเก็บเงิน</span><span class="sxs-lookup"><span data-stu-id="9a8dd-139">A new unbilled sales actual that is chargeable for the quantity and amount on the edited invoice line detail, a reversal of the unbilled sales actual, and an equivalent billed sales actual.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="9a8dd-140">การขายจริงใหม่ที่ยังไม่เรียกเก็บเงินซึ่งไม่คิดค่าธรรมเนียมเป็นปริมาณและจำนวนเงินที่เหลือหลังจากการลดการกำหนดค่าที่แก้ไขในรายละเอียดรายการใบแจ้งหนี้ที่แก้ไข การย้อนกลับของการขายจริงที่ไม่ได้เรียกเก็บเงินและเทียบเท่ากับการขายจริงที่เรียกเก็บเงิน</span><span class="sxs-lookup"><span data-stu-id="9a8dd-140">A new unbilled sales actual that is non-chargeable for the remaining quantity and amount after deducting the corrected figures on the edited invoice line detail, a reversal of the unbilled sales actual, and an equivalent billed sales actual.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="9a8dd-141">การออกใบแจ้งหนี้ธุรกรรมค่าใช้จ่ายที่แก้ไขเพื่อเพิ่มปริมาณ</span><span class="sxs-lookup"><span data-stu-id="9a8dd-141">Invoicing an expense transaction that was edited to increase the quantity.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="9a8dd-142">การกลับการขายที่ไม่ได้เรียกเก็บเงินสำหรับปริมาณและจำนวนเงินในการอนุมัติค่าใช้จ่ายตามเดิม</span><span class="sxs-lookup"><span data-stu-id="9a8dd-142">An unbilled sales reversal for the quantity and amount on the original expense approval.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="9a8dd-143">การขายจริงใหม่ที่ยังไม่เรียกเก็บเงินซึ่งคิดค่าธรรมเนียมเป็นปริมาณและจำนวนเงินในรายละเอียดรายการใบแจ้งหนี้ที่แก้ไข การย้อนกลับของการขายจริงที่ไม่ได้เรียกเก็บเงินและเทียบเท่ากับการขายจริงที่เรียกเก็บเงิน</span><span class="sxs-lookup"><span data-stu-id="9a8dd-143">A new unbilled sales actual that is chargeable for quantity and amount on the edited invoice line detail, a reversal of the unbilled sales actual, and an equivalent billed sales actual.</span></span> 
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="9a8dd-144">ออกใบแจ้งหนี้ค่าธรรมเนียม</span><span class="sxs-lookup"><span data-stu-id="9a8dd-144">Invoicing a fee.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="9a8dd-145">การกลับการขายที่ไม่ได้เรียกเก็บเงินสำหรับจำนวนค่าธรรมเนียมในบรรทัดสมุดรายวันตามเดิม</span><span class="sxs-lookup"><span data-stu-id="9a8dd-145">An unbilled sales reversal for the fee amount on the original journal line.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="9a8dd-146">การขายจริงที่เรียกเก็บเงินสำหรับปริมาณและจำนวนเงินในบรรทัดสมุดรายวันตามเดิม</span><span class="sxs-lookup"><span data-stu-id="9a8dd-146">A billed sales actual for the quantity and amount on the original fee journal line.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" valign="top">
                <p>
<span data-ttu-id="9a8dd-147">การออกใบแจ้งหนี้เหตุการณ์สำคัญ</span><span class="sxs-lookup"><span data-stu-id="9a8dd-147">Invoicing a milestone.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="9a8dd-148">การขายจริงที่เรียกเก็บเงินสำหรับจำนวนเหตุการณ์สำคัญบนเหตุการณ์สำคัญเดิมในรายละเอียดการให้บริการตามสัญญาของโครงการ</span><span class="sxs-lookup"><span data-stu-id="9a8dd-148">A billed sales actual for the milestone amount on the original milestone on the project contract line.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" valign="top">
                <p>
<span data-ttu-id="9a8dd-149">การออกใบแจ้งหนี้รายละเอียดการให้บริการตามสัญญาตามผลิตภัณฑ์</span><span class="sxs-lookup"><span data-stu-id="9a8dd-149">Invoicing a product-based contract line.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="9a8dd-150">ยอดขายจริงที่เรียกเก็บเงินสำหรับรายการผลิตภัณฑ์ที่มีปริมาณและจำนวนเงินที่มาจากรายละเอียดการให้บริการตามสัญญาตามผลิตภัณฑ์</span><span class="sxs-lookup"><span data-stu-id="9a8dd-150">A billed sales actual for the product line with the quantity and amount coming from the product-based contract line.</span></span>
                </p>
            </td>
        </tr>
    </tbody>
</table>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]