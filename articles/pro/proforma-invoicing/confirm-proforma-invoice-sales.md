---
title: ยืนยันใบแจ้งหนี้โครงการชั่วคราว
description: หัวข้อนี้ให้ข้อมูลเกี่ยวกับการยืนยันใบแจ้งหนี้โครงการชั่วคราวใน Project Operations
author: rumant
manager: Annbe
ms.date: 04/05/2021
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 144c1b6a49951af8be0c619f41808e7617e59c92
ms.sourcegitcommit: ca0fc078d1a12484eca193fe051b8442c0559db8
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 04/07/2021
ms.locfileid: "5867111"
---
# <a name="confirm-a-proforma-project-invoice"></a><span data-ttu-id="a780a-103">ยืนยันใบแจ้งหนี้โครงการชั่วคราว</span><span class="sxs-lookup"><span data-stu-id="a780a-103">Confirm a proforma project invoice</span></span> 

<span data-ttu-id="a780a-104">_**นำไปใช้กับ:** การปรับใช้งานแบบ Lite - จัดการกับการออกใบแจ้งหนี้ชั่วคราว_</span><span class="sxs-lookup"><span data-stu-id="a780a-104">_**Applies To:** Lite deployment - deal to proforma invoicing_</span></span>


<span data-ttu-id="a780a-105">หลังจากยืนยันใบแจ้งหนี้ Proforma แล้วสถานะของใบแจ้งหนี้โครงการจะอัปเดตเป็น **ได้รับการยืนยัน**</span><span class="sxs-lookup"><span data-stu-id="a780a-105">After a proforma invoice is confirmed, the status of the project invoice updates to **Confirmed**.</span></span> <span data-ttu-id="a780a-106">เมื่อใบแจ้งหนี้ได้รับการยืนยัน จะกลายเป็นแบบอ่านอย่างเดียว</span><span class="sxs-lookup"><span data-stu-id="a780a-106">When an invoice is confirmed, it becomes read-only.</span></span> <span data-ttu-id="a780a-107">นับจากนี้ไปคุณจะสามารถแก้ไขใบแจ้งหนี้ได้ก็ต่อเมื่อมีการแก้ไขหรือเครดิตที่ลูกค้าเป็นผู้เริ่มต้นเท่านั้น</span><span class="sxs-lookup"><span data-stu-id="a780a-107">Going forward, the invoice can only be corrected if there are any customer-initiated corrections or credits.</span></span>

<span data-ttu-id="a780a-108">ตารางต่อไปนี้แสดงรายการจริงที่สร้างโดยระบบ</span><span class="sxs-lookup"><span data-stu-id="a780a-108">The following table lists the actuals created by the system.</span></span> <span data-ttu-id="a780a-109">ข้อมูลจริงเหล่านี้ถูกสร้างขึ้นเมื่อมีการดำเนินการบางอย่างในใบแจ้งหนี้โครงการแบบร่างก่อนที่จะได้รับการยืนยัน</span><span class="sxs-lookup"><span data-stu-id="a780a-109">These actuals are created when certain operations are performed on the draft project invoice before it is confirmed.</span></span>

<table border="0" cellspacing="0" cellpadding="0">
    <tbody>
        <tr>
            <td width="216" valign="top">
                <p><span data-ttu-id="a780a-110">
                    <strong>สถานการณ์สมมติ</strong>
                </span><span class="sxs-lookup"><span data-stu-id="a780a-110">
                    <strong>Scenario</strong>
                </span></span></p>
            </td>
            <td width="808" valign="top">
                <p><span data-ttu-id="a780a-111">
                    <strong>สิ่งที่เกิดขึ้นจริงสร้างขึ้นจากการยืนยัน</strong>
                </span><span class="sxs-lookup"><span data-stu-id="a780a-111">
                    <strong>Actuals created on confirmation</strong>
                </span></span></p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="a780a-112">ออกใบแจ้งหนี้หรือค่าธรรมเนียมล่วงหน้า</span><span class="sxs-lookup"><span data-stu-id="a780a-112">Invoicing an advance or retainer</span></span> </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="a780a-113">การขายที่เรียกเก็บเงินจริงของประเภท <strong>ค่าธรรมเนียมล่วงหน้า</strong> ถูกสร้างขึ้นสำหรับจำนวนเงินล่วงหน้าหรือค่าธรรมเนียมล่วงหน้า</span><span class="sxs-lookup"><span data-stu-id="a780a-113">A billed sales actual of type, <strong>Retainer</strong> is created for the amount on the advance or retainer.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="a780a-114">การขายจริงที่ยังไม่ได้เรียกเก็บเงินของจำนวนเงินติดลบของค่าธรรมเนียมล่วงหน้าเพื่อจะใช้สำหรับการกระทบยอด</span><span class="sxs-lookup"><span data-stu-id="a780a-114">An unbilled sales actual of a negative amount of the retainer or advance to be used for reconciliation.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="a780a-115">หลังจากกระทบยอดค่าธรรมเนียมล่วงหน้าเต็มหรือจำนวนเงินล่วงหน้าในใบแจ้งหนี้</span><span class="sxs-lookup"><span data-stu-id="a780a-115">After fully reconciling a retainer or advance on an invoice.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="a780a-116">การกลับรายการการขายที่ยังไม่เรียกเก็บเงินของค่าธรรมเนียมล่วงหน้าหรือจำนวนเงินล่วงหน้าที่สร้างขึ้นสำหรับการกระทบยอด</span><span class="sxs-lookup"><span data-stu-id="a780a-116">An unbilled sales reversal of the retainer or advance that was created for reconciliation.</span></span> <span data-ttu-id="a780a-117">จำนวนนี้เป็นค่าบวกเนื่องจากมีวัตถุประสงค์เพื่อยกเลิกค่าลบที่สร้างขึ้นเมื่อมีการออกใบแจ้งหนี้ค่าธรรมเนียมล่วงหน้าหรือเงินล่วงหน้า</span><span class="sxs-lookup"><span data-stu-id="a780a-117">This amount is positive as it's meant to cancel out the negative that was created when the retainer or advance was invoiced.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="a780a-118">การกลับรายการขายที่เรียกเก็บเงินจริงสำหรับยอดเงินในใบแจ้งหนี้นี้</span><span class="sxs-lookup"><span data-stu-id="a780a-118">A billed sales actual for the amount on this invoice.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="3" valign="top">
                <p>
<span data-ttu-id="a780a-119">หลังจากกระทบยอดค่าธรรมเนียมล่วงหน้าบางส่วนหรือจำนวนเงินล่วงหน้าในใบแจ้งหนี้</span><span class="sxs-lookup"><span data-stu-id="a780a-119">After partially reconciling a retainer or advance on an invoice.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="a780a-120">การกลับรายการการขายที่ยังไม่เรียกเก็บเงินของค่าธรรมเนียมล่วงหน้าหรือจำนวนเงินล่วงหน้าที่สร้างขึ้นสำหรับการกระทบยอด</span><span class="sxs-lookup"><span data-stu-id="a780a-120">An unbilled sales reversal of the retainer or advance that was created for reconciliation.</span></span> <span data-ttu-id="a780a-121">จำนวนนี้เป็นค่าบวกเนื่องจากมีวัตถุประสงค์เพื่อยกเลิกค่าลบที่สร้างขึ้นเมื่อมีการออกใบแจ้งหนี้ค่าธรรมเนียมล่วงหน้าหรือเงินล่วงหน้า</span><span class="sxs-lookup"><span data-stu-id="a780a-121">This amount is positive as it's meant to cancel out the negative that was created when the retainer or advance was invoiced.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="a780a-122">การกลับรายการขายที่เรียกเก็บเงินจริงสำหรับยอดเงินในใบแจ้งหนี้นี้</span><span class="sxs-lookup"><span data-stu-id="a780a-122">A billed sales actual for the amount on this invoice.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="a780a-123">การขายจริงที่ยังไม่ได้เรียกเก็บเงินที่ติดลบของค่าธรรมเนียมล่วงหน้าหรือจำนวนเงินล่วงหน้าเพื่อจะใช้สำหรับการกระทบยอดใบแจ้งหนี้ในอนาคต</span><span class="sxs-lookup"><span data-stu-id="a780a-123">A negative unbilled sales actual of the remaining retainer or advance amount to be used for reconciliation on future invoices.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="a780a-124">การออกใบแจ้งหนี้ธุรกรรมเวลาโดยไม่มีการแก้ไขใดๆ ในแบบร่างใบแจ้งหนี้</span><span class="sxs-lookup"><span data-stu-id="a780a-124">Invoicing a time transaction without any edits on the draft invoice.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="a780a-125">การกลับการขายที่ไม่ได้เรียกเก็บเงินสำหรับชั่วโมงและจำนวนเงินในการอนุมัติเวลาตามเดิม</span><span class="sxs-lookup"><span data-stu-id="a780a-125">An unbilled sales reversal for the hours and amount on the original time approval.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="a780a-126">การขายที่มีการเรียกเก็บเงินจริงสำหรับชั่วโมงและจำนวนเงินในการอนุมัติเวลาตามเดิม</span><span class="sxs-lookup"><span data-stu-id="a780a-126">A billed sales actual for the hours and amount on the original time approval.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="3" valign="top">
                <p>
<span data-ttu-id="a780a-127">การออกใบแจ้งหนี้ธุรกรรมเวลาที่แก้ไขเพื่อลดปริมาณ</span><span class="sxs-lookup"><span data-stu-id="a780a-127">Invoicing a time transaction that was edited to reduce the quantity.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="a780a-128">การกลับการขายที่ไม่ได้เรียกเก็บเงินสำหรับชั่วโมงและจำนวนเงินในการอนุมัติเวลาตามเดิม</span><span class="sxs-lookup"><span data-stu-id="a780a-128">An unbilled sales reversal for the hours and amount on the original time approval.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="a780a-129">การขายจริงที่ยังไม่เรียกเก็บเงินใหม่ซึ่งคิดค่าธรรมเนียมเป็นชั่วโมงและจำนวนเงินในรายละเอียดรายการใบแจ้งหนี้ที่แก้ไข การย้อนกลับของการขายจริงและการขายจริงที่เรียกเก็บเงินแล้วเทียบเท่า</span><span class="sxs-lookup"><span data-stu-id="a780a-129">A new unbilled sales actual that is chargeable for the hours and amount on the edited invoice line detail, a reversal of the sales actual, and an equivalent billed sales actual.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="a780a-130">การขายจริงที่ยังไม่เรียกเก็บเงินใหม่ซึ่งไม่คิดค่าธรรมเนียมเป็นชั่วโมงและจำนวนเงินที่เหลือหลังจากการลดการกำหนดค่าที่แก้ไขในรายละเอียดรายการใบแจ้งหนี้ที่แก้ไข การย้อนกลับของการขายจริงและการขายจริงที่เรียกเก็บเงินแล้วเทียบเท่า</span><span class="sxs-lookup"><span data-stu-id="a780a-130">A new unbilled sales actual that is non-chargeable for the remaining hours and amount after deducting the corrected figures on edited invoice line detail, a reversal of the sales actual, and an equivalent billed sales actual.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="a780a-131">การออกใบแจ้งหนี้ธุรกรรมเวลาที่แก้ไขเพื่อเพิ่มปริมาณ</span><span class="sxs-lookup"><span data-stu-id="a780a-131">Invoicing a time transaction that was edited to increase the quantity.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="a780a-132">การกลับการขายที่ไม่ได้เรียกเก็บเงินสำหรับชั่วโมงและจำนวนเงินในการอนุมัติเวลาตามเดิม</span><span class="sxs-lookup"><span data-stu-id="a780a-132">An unbilled sales reversal for the hours and amount on the original time approval.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="a780a-133">การขายจริงที่ยังไม่เรียกเก็บเงินใหม่ซึ่งคิดค่าธรรมเนียมเป็นชั่วโมงและจำนวนเงินในรายละเอียดรายการใบแจ้งหนี้ที่แก้ไข การย้อนกลับของการขายจริงที่ไม่ได้เรียกเก็บเงินและการขายจริงที่เรียกเก็บเงินแล้วเทียบเท่า</span><span class="sxs-lookup"><span data-stu-id="a780a-133">A new unbilled sales actual that is chargeable for the hours and amount on the edited invoice line detail, a reversal of the unbilled sales actual, and an equivalent billed sales actual.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="a780a-134">การออกธุรกรรมค่าใช้จ่ายโดยไม่มีการแก้ไขใดๆ ในแบบร่างใบแจ้งหนี้</span><span class="sxs-lookup"><span data-stu-id="a780a-134">Invoicing an expense transaction without any edits on draft invoice.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="a780a-135">การกลับการขายที่ไม่ได้เรียกเก็บเงินสำหรับปริมาณและจำนวนเงินในการอนุมัติค่าใช้จ่ายตามเดิม</span><span class="sxs-lookup"><span data-stu-id="a780a-135">An unbilled sales reversal for the quantity and amount on the original expense approval.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="a780a-136">การขายจริงที่เรียกเก็บเงินแล้วสำหรับปริมาณและจำนวนเงินในการอนุมัติค่าใช้จ่ายตามเดิม</span><span class="sxs-lookup"><span data-stu-id="a780a-136">A billed sales actual for the quantity and amount on the original expense approval</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="3" valign="top">
                <p>
<span data-ttu-id="a780a-137">การออกใบแจ้งหนี้ธุรกรรมค่าใช้จ่ายที่แก้ไขเพื่อลดปริมาณ</span><span class="sxs-lookup"><span data-stu-id="a780a-137">Invoicing an expense transaction that was edited to reduce the quantity.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="a780a-138">การกลับการขายที่ไม่ได้เรียกเก็บเงินสำหรับปริมาณและจำนวนเงินในการอนุมัติค่าใช้จ่ายตามเดิม</span><span class="sxs-lookup"><span data-stu-id="a780a-138">An unbilled sales reversal for the quantity and amount on the original expense approval.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="a780a-139">การขายจริงที่ยังไม่เรียกเก็บเงินใหม่ซึ่งคิดค่าธรรมเนียมเป็นปริมาณและจำนวนเงินในรายละเอียดรายการใบแจ้งหนี้ที่แก้ไข การย้อนกลับของการขายจริงที่ไม่ได้เรียกเก็บเงินและการขายจริงที่เรียกเก็บเงินแล้วเทียบเท่า</span><span class="sxs-lookup"><span data-stu-id="a780a-139">A new unbilled sales actual that is chargeable for the quantity and amount on the edited invoice line detail, a reversal of the unbilled sales actual, and an equivalent billed sales actual.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="a780a-140">การขายจริงที่ยังไม่เรียกเก็บเงินใหม่ซึ่งไม่คิดค่าธรรมเนียมเป็นปริมาณและจำนวนเงินที่เหลือหลังจากการลดการกำหนดค่าที่แก้ไขในรายละเอียดรายการใบแจ้งหนี้ที่แก้ไข การย้อนกลับของการขายจริงที่ไม่ได้เรียกเก็บเงินและการขายจริงที่เรียกเก็บเงินแล้วเทียบเท่า</span><span class="sxs-lookup"><span data-stu-id="a780a-140">A new unbilled sales actual that is non-chargeable for the remaining quantity and amount after deducting the corrected figures on the edited invoice line detail, a reversal of the unbilled sales actual, and an equivalent billed sales actual.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="a780a-141">การออกใบแจ้งหนี้ธุรกรรมค่าใช้จ่ายที่แก้ไขเพื่อเพิ่มปริมาณ</span><span class="sxs-lookup"><span data-stu-id="a780a-141">Invoicing an expense transaction that was edited to increase the quantity.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="a780a-142">การกลับการขายที่ไม่ได้เรียกเก็บเงินสำหรับปริมาณและจำนวนเงินในการอนุมัติค่าใช้จ่ายตามเดิม</span><span class="sxs-lookup"><span data-stu-id="a780a-142">An unbilled sales reversal for the quantity and amount on the original expense approval.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="a780a-143">การขายจริงที่ยังไม่เรียกเก็บเงินใหม่ซึ่งคิดค่าธรรมเนียมเป็นปริมาณและจำนวนเงินในรายละเอียดรายการใบแจ้งหนี้ที่แก้ไข การย้อนกลับของการขายจริงที่ไม่ได้เรียกเก็บเงินและการขายจริงที่เรียกเก็บเงินแล้วเทียบเท่า</span><span class="sxs-lookup"><span data-stu-id="a780a-143">A new unbilled sales actual that is chargeable for quantity and amount on the edited invoice line detail, a reversal of the unbilled sales actual, and an equivalent billed sales actual.</span></span> 
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="a780a-144">การออกใบแจ้งหนี้ธุรกรรมวัสดุโดยไม่มีการแก้ไขใดๆ ในร่างใบแจ้งหนี้</span><span class="sxs-lookup"><span data-stu-id="a780a-144">Invoicing a material transaction without any edits on the draft invoice.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="a780a-145">การกลับรายการขายที่ไม่ได้เรียกเก็บเงินสำหรับปริมาณและจำนวนเงินในการอนุมัติการใช้วัสดุของเดิม</span><span class="sxs-lookup"><span data-stu-id="a780a-145">An unbilled sales reversal for the quantity and amount on the original material usage approval.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="a780a-146">การขายจริงที่เรียกเก็บเงินแล้วสำหรับปริมาณและจำนวนเงินในการอนุมัติการใช้วัสดุของเดิม</span><span class="sxs-lookup"><span data-stu-id="a780a-146">A billed sales actual for the quantity and amount on the original material usage approval.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="3" valign="top">
                <p>
<span data-ttu-id="a780a-147">การออกใบแจ้งหนี้ธุรกรรมวัสดุที่แก้ไขเพื่อลดปริมาณ</span><span class="sxs-lookup"><span data-stu-id="a780a-147">Invoicing a material transaction that was edited to reduce the quantity.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="a780a-148">การกลับรายการขายที่ไม่ได้เรียกเก็บเงินสำหรับปริมาณและจำนวนเงินในการอนุมัติเวลาของเดิม</span><span class="sxs-lookup"><span data-stu-id="a780a-148">An unbilled sales reversal for the quantity and amount on the original time approval.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="a780a-149">การขายจริงที่ยังไม่เรียกเก็บเงินใหม่ซึ่งคิดค่าธรรมเนียมเป็นปริมาณและจำนวนเงินในรายละเอียดรายการใบแจ้งหนี้ที่แก้ไข การย้อนกลับของการขายจริงที่ไม่ได้เรียกเก็บเงินและการขายจริงที่เรียกเก็บเงินแล้วเทียบเท่า</span><span class="sxs-lookup"><span data-stu-id="a780a-149">A new unbilled sales actual that is chargeable for the quantity and amount on the edited invoice line detail, a reversal of the unbilled sales actual, and an equivalent billed sales actual.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="a780a-150">การขายจริงที่ยังไม่เรียกเก็บเงินใหม่ซึ่งไม่คิดค่าธรรมเนียมเป็นปริมาณและจำนวนเงินที่เหลือหลังจากการลดการกำหนดค่าที่แก้ไขในรายละเอียดรายการใบแจ้งหนี้ที่แก้ไข การย้อนกลับของการขายจริงที่ไม่ได้เรียกเก็บเงินและการขายจริงที่เรียกเก็บเงินแล้วเทียบเท่า</span><span class="sxs-lookup"><span data-stu-id="a780a-150">A new unbilled sales actual that is non-chargeable for the remaining quantity and amount after deducting the corrected figures on the edited invoice line detail, a reversal of the unbilled sales actual, and an equivalent billed sales actual.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="a780a-151">การออกใบแจ้งหนี้ธุรกรรมวัสดุที่แก้ไขเพื่อเพิ่มปริมาณ</span><span class="sxs-lookup"><span data-stu-id="a780a-151">Invoicing a material transaction that was edited to increase the quantity.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="a780a-152">การกลับรายการขายที่ไม่ได้เรียกเก็บเงินสำหรับปริมาณและจำนวนเงินในการอนุมัติการใช้วัสดุของเดิม</span><span class="sxs-lookup"><span data-stu-id="a780a-152">An unbilled sales reversal for the quantity and amount on the original material usage approval.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="a780a-153">การขายจริงที่ยังไม่เรียกเก็บเงินใหม่ซึ่งคิดค่าธรรมเนียมเป็นปริมาณและจำนวนเงินในรายละเอียดรายการใบแจ้งหนี้ที่แก้ไข การย้อนกลับของการขายจริงที่ไม่ได้เรียกเก็บเงินและการขายจริงที่เรียกเก็บเงินแล้วเทียบเท่า</span><span class="sxs-lookup"><span data-stu-id="a780a-153">A new unbilled sales actual that is chargeable for the quantity and amount on the edited invoice line detail, a reversal of the unbilled sales actual, and an equivalent billed sales actual.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="a780a-154">ออกใบแจ้งหนี้ค่าธรรมเนียม</span><span class="sxs-lookup"><span data-stu-id="a780a-154">Invoicing a fee.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="a780a-155">การกลับการขายที่ไม่ได้เรียกเก็บเงินสำหรับจำนวนค่าธรรมเนียมในบรรทัดสมุดรายวันตามเดิม</span><span class="sxs-lookup"><span data-stu-id="a780a-155">An unbilled sales reversal for the fee amount on the original journal line.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="a780a-156">การขายจริงที่เรียกเก็บเงินแล้วสำหรับปริมาณและจำนวนเงินในบรรทัดสมุดรายวันตามเดิม</span><span class="sxs-lookup"><span data-stu-id="a780a-156">A billed sales actual for the quantity and amount on the original fee journal line.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" valign="top">
                <p>
<span data-ttu-id="a780a-157">การออกใบแจ้งหนี้หลักเป้าหมาย</span><span class="sxs-lookup"><span data-stu-id="a780a-157">Invoicing a milestone.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="a780a-158">การขายจริงที่เรียกเก็บเงินแล้วสำหรับจำนวนหลักเป้าหมายบนหลักเป้าหมายเดิมในรายละเอียดการให้บริการตามสัญญาของโครงการ</span><span class="sxs-lookup"><span data-stu-id="a780a-158">A billed sales actual for the milestone amount on the original milestone on the project contract line.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" valign="top">
                <p>
<span data-ttu-id="a780a-159">การออกใบแจ้งหนี้รายละเอียดการให้บริการตามสัญญาตามผลิตภัณฑ์</span><span class="sxs-lookup"><span data-stu-id="a780a-159">Invoicing a product-based contract line.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="a780a-160">การขายจริงที่เรียกเก็บเงินแล้วสำหรับรายการผลิตภัณฑ์ที่มีปริมาณและจำนวนเงินที่มาจากรายละเอียดการให้บริการตามสัญญาตามผลิตภัณฑ์</span><span class="sxs-lookup"><span data-stu-id="a780a-160">A billed sales actual for the product line with the quantity and amount coming from the product-based contract line.</span></span>
                </p>
            </td>
        </tr>
    </tbody>
</table>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
