---
title: เครดิตและใบแจ้งหนี้ที่แก้ไข
description: หัวข้อนี้ให้ข้อมูลเกี่ยวกับใบแจ้งหนี้ที่แก้ไขใน Project Operations
author: rumant
manager: Annbe
ms.date: 10/15/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: d2187627439d42b37222dce0a491c62dafc358d5
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 10/16/2020
ms.locfileid: "4086043"
---
# <a name="credits-and-corrected-invoices"></a><span data-ttu-id="7939e-103">เครดิตและใบแจ้งหนี้ที่แก้ไข</span><span class="sxs-lookup"><span data-stu-id="7939e-103">Credits and corrected invoices</span></span>

<span data-ttu-id="7939e-104">_**นำไปใช้กับ:** การปรับใช้งานแบบ Lite - จัดการกับการออกใบแจ้งหนี้ชั่วคราว_</span><span class="sxs-lookup"><span data-stu-id="7939e-104">_**Applies To:** Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="7939e-105">ใบแจ้งหนี้โครงการที่ได้รับการยืนยันสามารถแก้ไขเพื่อประมวลผลการเปลี่ยนแปลงหรือเครดิตตามที่เจรจากับลูกค้าและผู้จัดการโครงการ</span><span class="sxs-lookup"><span data-stu-id="7939e-105">A confirmed project invoice can be corrected to process changes or credits as negotiated with the customer and project manager.</span></span>

<span data-ttu-id="7939e-106">หากต้องการแก้ไขใบแจ้งหนี้ที่ได้รับการยืนยัน ให้เปิดใบแจ้งหนี้ที่ยืนยันแล้วเลือก **แก้ไขใบแจ้งหนี้นี้**</span><span class="sxs-lookup"><span data-stu-id="7939e-106">To make edits to a confirmed invoice, open the confirmed invoice and select **Correct this Invoice**.</span></span> 

> [!NOTE]
> <span data-ttu-id="7939e-107">ตัวเลือกนี้ใช้ไม่ได้ เว้นแต่จะได้รับการยืนยันใบแจ้งหนี้โครงการ</span><span class="sxs-lookup"><span data-stu-id="7939e-107">This selection isn't available unless a project invoice is confirmed.</span></span>

<span data-ttu-id="7939e-108">ร่างใบแจ้งหนี้ใหม่ถูกสร้างขึ้นจากใบแจ้งหนี้ที่ได้รับการยืนยัน</span><span class="sxs-lookup"><span data-stu-id="7939e-108">A new draft invoice is created from the confirmed invoice.</span></span> <span data-ttu-id="7939e-109">รายละเอียดรายการใบแจ้งหนี้ทั้งหมดจากใบแจ้งหนี้ที่ยืนยันก่อนหน้านี้จะถูกคัดลอกไปยังแบบร่างใหม่</span><span class="sxs-lookup"><span data-stu-id="7939e-109">All invoice line details from the previously confirmed invoice are copied to the new draft.</span></span> <span data-ttu-id="7939e-110">ต่อไปนี้เป็นประเด็นสำคัญบางประการที่ควรทำความเข้าใจเกี่ยวกับรายละเอียดรายการในใบแจ้งหนี้ที่แก้ไขใหม่:</span><span class="sxs-lookup"><span data-stu-id="7939e-110">The following are some of the key points to understand about the line details on the new corrected invoice:</span></span>

- <span data-ttu-id="7939e-111">ปริมาณทั้งหมดจะถูกอัปเดตเป็นศูนย์</span><span class="sxs-lookup"><span data-stu-id="7939e-111">All quantities are updated to zero.</span></span> <span data-ttu-id="7939e-112">แอปพลิเคชันจะถือว่ารายการที่ออกใบแจ้งหนี้ทั้งหมดได้รับการให้สินเชื่ออย่างสมบูรณ์</span><span class="sxs-lookup"><span data-stu-id="7939e-112">The application assumes that all invoiced items are fully credited.</span></span> <span data-ttu-id="7939e-113">หากจำเป็นคุณสามารถอัปเดตปริมาณเหล่านี้ด้วยตนเองเพื่อให้สอดคล้องกับปริมาณที่จะถูกออกใบแจ้งหนี้ ไม่ใช่ปริมาณการให้สินเชื่อ</span><span class="sxs-lookup"><span data-stu-id="7939e-113">If needed, you can manually update these quantities to reflect the quantity that is being invoiced, and not the quantity that is being credited.</span></span> <span data-ttu-id="7939e-114">ตามปริมาณที่คุณป้อน แอปพลิเคชันจะคำนวณปริมาณการให้สินเชื่อ</span><span class="sxs-lookup"><span data-stu-id="7939e-114">Based on the quantity you enter, the application calculates the credited quantity.</span></span> <span data-ttu-id="7939e-115">จำนวนเงินนี้จะแสดงในข้อมูลจริงที่สร้างขึ้นเมื่อมีการยืนยันใบแจ้งหนี้ที่แก้ไขแล้ว</span><span class="sxs-lookup"><span data-stu-id="7939e-115">This amount is reflected in the actuals that are created when the corrected invoice is confirmed.</span></span> <span data-ttu-id="7939e-116">หากคุณกำลังทำการเปลี่ยนแปลงจำนวนภาษี คุณต้องป้อนจำนวนภาษีที่ถูกต้อง ไม่ใช่จำนวนเงินภาษีที่มีการให้สินเชื่อ</span><span class="sxs-lookup"><span data-stu-id="7939e-116">If you are making changes to the tax amount, you must enter the correct tax amount and not the tax amount that is being credited.</span></span>
- <span data-ttu-id="7939e-117">ไม่มีการคัดลอกรายละเอียดการให้บริการตามสัญญาที่อิงตามผลิตภัณฑ์ที่ยืนยันก่อนหน้า</span><span class="sxs-lookup"><span data-stu-id="7939e-117">Previously confirmed product-based contract lines are not copied over.</span></span> <span data-ttu-id="7939e-118">ไม่สนับสนุนการประมวลผลการแก้ไขใบแจ้งหนี้โครงการตามผลิตภัณฑ์</span><span class="sxs-lookup"><span data-stu-id="7939e-118">Processing corrections on a product-based project invoice is not supported.</span></span>
- <span data-ttu-id="7939e-119">การแก้ไขเหตุการณ์สำคัญจะถูกประมวลผลเป็นการให้สินเชื่อเต็มรูปแบบเสมอ</span><span class="sxs-lookup"><span data-stu-id="7939e-119">Milestone corrections are always processed as full credits.</span></span>
- <span data-ttu-id="7939e-120">สามารถแก้ไขค่าธรรมเนียมล่วงหน้าหรือจำนวนเงินล่วงหน้าได้หากลูกค้าออกใบแจ้งหนี้เป็นจำนวนเงินที่ไม่ถูกต้อง</span><span class="sxs-lookup"><span data-stu-id="7939e-120">Retainer or advance amounts can be corrected if the customer was invoiced for an incorrect amount.</span></span>
- <span data-ttu-id="7939e-121">การกระทบยอดของค่าธรรมเนียมล่วงหน้าสามารถแก้ไขได้หากใช้จำนวนเงินที่ไม่ถูกต้องเพื่อกระทบยอดกับค่าธรรมเนียมในใบแจ้งหนี้ที่ได้รับการยืนยันก่อนหน้านี้</span><span class="sxs-lookup"><span data-stu-id="7939e-121">Reconciliations of retainers and advances can be corrected if an incorrect amount was used to reconcile against the charges on a previously confirmed invoice.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="7939e-122">รายละเอียดรายการใบแจ้งหนี้ที่แก้ไขค่าใช้จ่ายอื่นๆ ที่ออกใบแจ้งหนี้แล้วมีการตั้งค่าฟิลด์ **การแก้ไข** เป็น **ใช่**</span><span class="sxs-lookup"><span data-stu-id="7939e-122">Invoice line details that are corrections to other already invoiced charges have the field **Correction** set to **Yes**.</span></span> <span data-ttu-id="7939e-123">ใบแจ้งหนี้ที่แก้ไขรายละเอียดรายการใบแจ้งหนี้จะมีฟิลด์ที่เรียกว่า **มีการแก้ไข** ที่ตั้งค่าเป็น **ใช่**</span><span class="sxs-lookup"><span data-stu-id="7939e-123">Invoices that have corrected invoice line details have a field called **Has corrections** that is also set to **Yes**.</span></span>

## <a name="actuals-created-on-confirmation-of-a-corrective-invoice"></a><span data-ttu-id="7939e-124">ข้อมูลจริงที่สร้างขึ้นในการยืนยันใบแจ้งหนี้การแก้ไข:</span><span class="sxs-lookup"><span data-stu-id="7939e-124">Actuals created on Confirmation of a corrective invoice:</span></span>

<span data-ttu-id="7939e-125">ด้านล่างนี้เป็นข้อมูลจริงที่สร้างขึ้นโดยแอปพลิเคชันในการยืนยันการแก้ไขตามการดำเนินการที่ดำเนินการในใบแจ้งหนี้การแก้ไขฉบับร่างก่อนการยืนยัน</span><span class="sxs-lookup"><span data-stu-id="7939e-125">Below are the actuals created by the application on confirmation of a corrective based on the operations performed on the draft corrective invoice before confirmation.</span></span>

<table border="0" cellspacing="0" cellpadding="0">
    <tbody>
        <tr>
            <td width="216" valign="top">
                <p><span data-ttu-id="7939e-126">
                    <strong>สถานการณ์สมมติ</strong>
                </span><span class="sxs-lookup"><span data-stu-id="7939e-126">
                    <strong>Scenario</strong>
                </span></span></p>
            </td>
            <td width="808" valign="top">
                <p><span data-ttu-id="7939e-127">
                    <strong>สิ่งที่เกิดขึ้นจริงสร้างขึ้นจากการยืนยัน</strong>
                </span><span class="sxs-lookup"><span data-stu-id="7939e-127">
                    <strong>Actuals created on confirmation</strong>
                </span></span></p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="4" valign="top">
                <p>
<span data-ttu-id="7939e-128">ยืนยันการแก้ไขใบแจ้งหนี้ล่วงหน้าหรือค่าธรรมเนียมล่วงหน้า<strong></strong>
                </span><span class="sxs-lookup"><span data-stu-id="7939e-128">Confirm the correction of an invoiced advance or retainer.<strong></strong>
                </span></span></p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="7939e-129">การกลับรายการการขายที่ยังไม่เรียกเก็บเงินของค่าธรรมเนียมล่วงหน้าหรือจำนวนเงินล่วงหน้าที่สร้างขึ้นสำหรับการกระทบยอด</span><span class="sxs-lookup"><span data-stu-id="7939e-129">An unbilled sales reversal of the retainer or advance that was created for reconciliation.</span></span> <span data-ttu-id="7939e-130">จำนวนนี้เป็นค่าบวกเนื่องจากมีวัตถุประสงค์เพื่อยกเลิกค่าลบที่สร้างขึ้นเมื่อมีการออกใบแจ้งหนี้ค่าธรรมเนียมล่วงหน้าหรือเงินล่วงหน้า</span><span class="sxs-lookup"><span data-stu-id="7939e-130">This amount is positive because it is meant to cancel out the negative that was created when the retainer or advance was invoiced.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="7939e-131">การกลับรายการขายที่เรียกเก็บเงินจริงถูกสร้างขึ้นสำหรับยอดเงินบนค่าธรรมเนียมล่วงหน้าหรือเงินล่วงหน้าเพื่อย้อนกลับการขายที่เรียกเก็บเงินเดิม</span><span class="sxs-lookup"><span data-stu-id="7939e-131">A billed sales reversal actual is created for the amount on the retainer or advance to reverse the original billed sales.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="7939e-132">ยอดขายที่เรียกเก็บเงินจริงใหม่จะถูกสร้างขึ้นสำหรับจำนวนเงินที่แก้ไขบนค่าธรรมเนียมล่วงหน้าหรือรายการใบแจ้งหนี้ที่แก้ไขตามรายการล่วงหน้า</span><span class="sxs-lookup"><span data-stu-id="7939e-132">A new billed sales actual is created for the corrected amount on the retainer or advance-based corrected invoice line.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="7939e-133">ยอดขายที่ยังไม่ได้เรียกเก็บเงินจริงของจำนวนเงินติดลบของค่าธรรมเนียมล่วงหน้าหรือรายการใบแจ้งหนี้ที่แก้ไขตามล่วงหน้า ซึ่งจะใช้สำหรับการกระทบยอด</span><span class="sxs-lookup"><span data-stu-id="7939e-133">An unbilled sales actual of negative amount of the retainer or advance-based corrected invoice line, which will be used for reconciliation.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="4" valign="top">
                <p>
<span data-ttu-id="7939e-134">การยืนยันการแก้ไขค่าธรรมเนียมล่วงหน้าที่กระทบยอดก่อนหน้านี้หรือล่วงหน้า</span><span class="sxs-lookup"><span data-stu-id="7939e-134">A confirmation of the correction of a previously reconciled retainer or advance.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="7939e-135">การกลับรายการการขายที่ยังไม่เรียกเก็บเงินของค่าธรรมเนียมล่วงหน้าหรือจำนวนเงินล่วงหน้าที่สร้างขึ้นสำหรับการกระทบยอด</span><span class="sxs-lookup"><span data-stu-id="7939e-135">An unbilled sales reversal of the retainer or advance that was created for reconciliation.</span></span> <span data-ttu-id="7939e-136">จำนวนนี้เป็นค่าบวกและมีวัตถุประสงค์เพื่อยกเลิกค่าลบที่สร้างขึ้นเมื่อการกระทบยอดก่อนหน้าเกิดขึ้น</span><span class="sxs-lookup"><span data-stu-id="7939e-136">This amount is positive and is meant to cancel out the negative that was created when the previous reconciliation occurred.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="7939e-137">การกลับรายการขายที่เรียกเก็บเงินจริงสำหรับยอดเงินในใบแจ้งหนี้ก่อนหน้า</span><span class="sxs-lookup"><span data-stu-id="7939e-137">A billed sales reversal actual for the amount on the previous invoice.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="7939e-138">ยอดขายที่เรียกเก็บเงินจริงใหม่สำหรับจำนวนเงินที่แก้ไขบนค่าธรรมเนียมล่วงหน้าจะใช้กับใบแจ้งหนี้ที่แก้ไข</span><span class="sxs-lookup"><span data-stu-id="7939e-138">A new billed sales actual for the corrected retainer amount that is applied on the corrected invoice.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="7939e-139">ยอดขายที่ยังไม่ได้เรียกเก็บเงินจริงที่มีจำนวนเงินติดลบจากค่าธรรมเนียมล่วงหน้าหรือเงินล่วงหน้าที่เหลือที่ถูกแก้ไข ซึ่งจะใช้สำหรับการกระทบยอดในใบแจ้งหนี้ภายหลัง</span><span class="sxs-lookup"><span data-stu-id="7939e-139">An unbilled sales actual with a negative amount from the corrected leftover retainer or advance, which will be used for reconciliation on later invoices.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="7939e-140">การออกใบแจ้งหนี้การให้สินเชื่อเต็มรูปแบบของธุรกรรมเวลาที่ออกใบแจ้งหนี้ก่อนหน้านี้</span><span class="sxs-lookup"><span data-stu-id="7939e-140">Invoicing the full credit of a previously invoiced time transaction.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="7939e-141">การกลับรายการขายที่เรียกเก็บเงินสำหรับชั่วโมงและจำนวนเงินในรายละเอียดรายการใบแจ้งหนี้เดิมสำหรับเวลา</span><span class="sxs-lookup"><span data-stu-id="7939e-141">A billed sales reversal for the hours and amount on the original invoice line detail for time.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="7939e-142">การขายจริงที่เรียกเก็บเงินสำหรับชั่วโมงและจำนวนเงินในรายละเอียดรายการใบแจ้งหนี้เดิมสำหรับเวลา</span><span class="sxs-lookup"><span data-stu-id="7939e-142">A new unbilled sales actual for the hours and amount on the original invoice line detail for time.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="3" valign="top">
                <p>
<span data-ttu-id="7939e-143">การออกใบแจ้งหนี้การให้สินเชื่อบางส่วนในธุรกรรมเวลา</span><span class="sxs-lookup"><span data-stu-id="7939e-143">Invoicing the partial credit on a time transaction.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="7939e-144">การกลับรายการขายที่เรียกเก็บเงินสำหรับชั่วโมงและจำนวนเงินที่ออกใบแจ้งหนี้ในรายละเอียดรายการใบแจ้งหนี้เดิมสำหรับเวลา</span><span class="sxs-lookup"><span data-stu-id="7939e-144">A billed sales reversal for the hours and amount invoiced on the original invoice line detail for time.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="7939e-145">การขายจริงใหม่ที่ยังไม่เรียกเก็บเงินซึ่งคิดค่าธรรมเนียมเป็นชั่วโมงและจำนวนเงินในรายละเอียดรายการใบแจ้งหนี้ที่แก้ไข การกลับรายการนี้ และยอดขายจริงที่เรียกเก็บเงินที่เทียบเท่า</span><span class="sxs-lookup"><span data-stu-id="7939e-145">A new unbilled sales actual that is chargeable for the hours and amount on the edited invoice line detail, a reversal of this, and an equivalent billed sales actual.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="7939e-146">การขายจริงใหม่ที่ยังไม่เรียกเก็บเงินซึ่งคิดค่าธรรมเนียมสำหรับชั่วโมงและจำนวนที่เหลือหลังจากหักตัวเลขที่แก้ไขแล้วในรายละเอียดรายการใบแจ้งหนี้</span><span class="sxs-lookup"><span data-stu-id="7939e-146">A new unbilled sales actual that is chargeable for the remaining hours and amount after deducting the corrected figures on the invoice line detail.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="7939e-147">การออกใบแจ้งหนี้การให้สินเชื่อเต็มรูปแบบของธุรกรรมค่าใช้จ่ายที่ออกใบแจ้งหนี้ก่อนหน้านี้</span><span class="sxs-lookup"><span data-stu-id="7939e-147">Invoicing the full credit of a previously invoiced expense transaction.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="7939e-148">การกลับรายการขายที่เรียกเก็บเงินสำหรับปริมาณและจำนวนเงินที่ออกใบแจ้งหนี้ในรายละเอียดรายการใบแจ้งหนี้เดิมสำหรับค่าใช้จ่าย</span><span class="sxs-lookup"><span data-stu-id="7939e-148">A billed sales reversal for the quantity and amount on the original invoice line detail for the expense.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="7939e-149">การขายจริงใหม่ที่เรียกเก็บเงินสำหรับปริมาณและจำนวนเงินที่ออกใบแจ้งหนี้ในรายละเอียดรายการใบแจ้งหนี้เดิมสำหรับค่าใช้จ่าย</span><span class="sxs-lookup"><span data-stu-id="7939e-149">A new unbilled sales actual for the quantity and amount on the original invoice line detail for the expense.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="3" valign="top">
                <p>
<span data-ttu-id="7939e-150">การออกใบแจ้งหนี้การให้สินเชื่อบางส่วนของธุรกรรมค่าใช้จ่ายที่ออกใบแจ้งหนี้ก่อนหน้านี้</span><span class="sxs-lookup"><span data-stu-id="7939e-150">Invoicing the partial credit of a previously invoiced expense transaction.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="7939e-151">การกลับรายการขายที่เรียกเก็บเงินสำหรับปริมาณและจำนวนเงินที่ออกใบแจ้งหนี้ในรายละเอียดรายการใบแจ้งหนี้เดิมสำหรับค่าใช้จ่าย</span><span class="sxs-lookup"><span data-stu-id="7939e-151">A billed sales reversal for the quantity and amount invoiced on the original invoice line detail for an expense.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="7939e-152">การขายจริงใหม่ที่ยังไม่เรียกเก็บเงินซึ่งคิดค่าธรรมเนียมเป็นปริมาณและจำนวนเงินในรายละเอียดรายการใบแจ้งหนี้ที่แก้ไข การกลับรายการนี้ และยอดขายจริงที่เรียกเก็บเงินที่เทียบเท่า</span><span class="sxs-lookup"><span data-stu-id="7939e-152">A new unbilled sales actual that is chargeable for the quantity and amount on the corrected invoice line detail, a reversal of this, and an equivalent billed sales actual.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="7939e-153">การขายจริงใหม่ที่ยังไม่เรียกเก็บเงินซึ่งคิดค่าธรรมเนียมสำหรับปริมาณและจำนวนที่เหลือหลังจากหักตัวเลขที่แก้ไขแล้วในรายละเอียดรายการใบแจ้งหนี้</span><span class="sxs-lookup"><span data-stu-id="7939e-153">A new unbilled sales actual that is chargeable for the remaining quantity and amount after deducting the corrected figures on the invoice line detail.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="7939e-154">การออกใบแจ้งหนี้การให้สินเชื่อเต็มรูปแบบของธุรกรรมค่าธรรมเนียมที่ออกใบแจ้งหนี้ก่อนหน้านี้</span><span class="sxs-lookup"><span data-stu-id="7939e-154">Invoicing the full credit of a previously invoiced fee transaction.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="7939e-155">การกลับรายการขายที่เรียกเก็บเงินสำหรับปริมาณและจำนวนเงินที่ออกใบแจ้งหนี้ในรายละเอียดรายการใบแจ้งหนี้เดิมสำหรับค่าธรรมเนียม</span><span class="sxs-lookup"><span data-stu-id="7939e-155">A billed sales reversal for the quantity and amount on the original invoice line detail for the fee.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="7939e-156">การขายจริงใหม่ที่เรียกเก็บเงินสำหรับปริมาณและจำนวนเงินที่ออกใบแจ้งหนี้ในรายละเอียดรายการใบแจ้งหนี้เดิมสำหรับค่าธรรมเนียม</span><span class="sxs-lookup"><span data-stu-id="7939e-156">A new unbilled sales actual for the quantity and amount on the original invoice line detail for the fee.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="7939e-157">การออกใบแจ้งหนี้การให้สินเชื่อบางส่วนของธุรกรรมค่าธรรมเนียมที่ออกใบแจ้งหนี้ก่อนหน้านี้</span><span class="sxs-lookup"><span data-stu-id="7939e-157">Invoicing the partial credit of a previously invoiced fee transaction.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="7939e-158">การกลับรายการขายที่เรียกเก็บเงินสำหรับปริมาณและจำนวนเงินที่ออกใบแจ้งหนี้ในรายละเอียดรายการใบแจ้งหนี้เดิมสำหรับค่าธรรมเนียม</span><span class="sxs-lookup"><span data-stu-id="7939e-158">A billed sales reversal for the quantity and amount invoiced on the original invoice line detail for fee.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="7939e-159">การขายจริงใหม่ที่ยังไม่เรียกเก็บเงินซึ่งคิดค่าธรรมเนียมเป็นปริมาณและจำนวนเงินในรายละเอียดรายการใบแจ้งหนี้การแก้ไขที่แก้ไข การกลับรายการนี้ และยอดขายจริงที่เรียกเก็บเงินที่เทียบเท่า</span><span class="sxs-lookup"><span data-stu-id="7939e-159">A new unbilled sales actual that is chargeable for the quantity and amount on the edited corrective invoice line detail, a reversal of this, and an equivalent billed sales actual.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" valign="top">
                <p>
<span data-ttu-id="7939e-160">การออกใบแจ้งหนี้การให้สินเชื่อเต็มรูปแบบของเหตุการณ์สําคัญที่ออกใบแจ้งหนี้ก่อนหน้านี้</span><span class="sxs-lookup"><span data-stu-id="7939e-160">Invoicing the full credit of a previously invoiced milestone.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="7939e-161">การกลับรายการขายที่เรียกเก็บเงินสำหรับจำนวนเงินในรายละเอียดรายการใบแจ้งหนี้เดิมสำหรับเหตุการณ์สําคัญ</span><span class="sxs-lookup"><span data-stu-id="7939e-161">A billed sales reversal for the amount on the original invoice line detail for the milestone.</span></span>
                </p>
                <p>
<span data-ttu-id="7939e-162">ใบแจ้งหนี้เหตุการณ์สําคัญหรือสถานะการเรียกเก็บเงินในรายละเอียดการให้บริการตามสัญญาของโครงการได้รับการอัปเดตเป็น **พร้อมที่จะออกใบแจ้งหนี้**</span><span class="sxs-lookup"><span data-stu-id="7939e-162">The milestone invoice or billing status on the project contract line is updated to **Ready to Invoice**.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" valign="top">
                <p>
<span data-ttu-id="7939e-163">การออกใบแจ้งหนี้การให้สินเชื่อบางส่วนของเหตุการณ์สําคัญที่ออกใบแจ้งหนี้ก่อนหน้านี้</span><span class="sxs-lookup"><span data-stu-id="7939e-163">Invoicing the partial credit of a previously invoiced milestone.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="7939e-164">ไม่สนับสนุน</span><span class="sxs-lookup"><span data-stu-id="7939e-164">Unsupported</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="216" valign="top">
                <p>
<span data-ttu-id="7939e-165">เครดิตและการแก้ไขรายละเอียดการให้บริการตามสัญญาตามผลิตภัณฑ์ที่ออกใบแจ้งหนี้ก่อนหน้านี้</span><span class="sxs-lookup"><span data-stu-id="7939e-165">Credits and corrections of a previously invoiced product-based contract line.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="7939e-166">ไม่สนับสนุน</span><span class="sxs-lookup"><span data-stu-id="7939e-166">Unsupported</span></span> </p>
            </td>
        </tr>
    </tbody>
</table>
