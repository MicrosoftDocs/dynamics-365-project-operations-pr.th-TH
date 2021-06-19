---
title: ใบแจ้งหนี้โครงการที่แก้ไข
description: หัวข้อนี้ให้ข้อมูลเกี่ยวกับวิธีสร้างและยืนยันใบแจ้งหนี้ที่แก้ไขใน Project Operations
author: rumant
ms.date: 04/05/2021
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: dfa5535597ee6e144259c9246b33075f3492285e
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 05/10/2021
ms.locfileid: "6004104"
---
# <a name="corrective-project-invoices"></a><span data-ttu-id="52cc8-103">ใบแจ้งหนี้โครงการที่แก้ไข</span><span class="sxs-lookup"><span data-stu-id="52cc8-103">Corrective project invoices</span></span>

<span data-ttu-id="52cc8-104">_**นำไปใช้กับ:** การปรับใช้งานแบบ Lite - จัดการกับการออกใบแจ้งหนี้ชั่วคราว_</span><span class="sxs-lookup"><span data-stu-id="52cc8-104">_**Applies To:** Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="52cc8-105">ใบแจ้งหนี้โครงการที่ได้รับการยืนยันสามารถแก้ไขเพื่อประมวลผลการเปลี่ยนแปลงหรือเครดิตตามที่เจรจากับลูกค้าและผู้จัดการโครงการ</span><span class="sxs-lookup"><span data-stu-id="52cc8-105">A confirmed project invoice can be corrected to process changes or credits as negotiated with the customer and project manager.</span></span>

<span data-ttu-id="52cc8-106">หากต้องการแก้ไขใบแจ้งหนี้ที่ได้รับการยืนยัน ให้เปิดใบแจ้งหนี้ที่ยืนยันแล้วเลือก **แก้ไขใบแจ้งหนี้นี้**</span><span class="sxs-lookup"><span data-stu-id="52cc8-106">To make edits to a confirmed invoice, open the confirmed invoice and select **Correct this Invoice**.</span></span> 

> [!NOTE]
> <span data-ttu-id="52cc8-107">ตัวเลือกนี้ใช้ไม่ได้ เว้นแต่จะได้รับการยืนยันใบแจ้งหนี้โครงการ</span><span class="sxs-lookup"><span data-stu-id="52cc8-107">This selection isn't available unless a project invoice is confirmed.</span></span>

<span data-ttu-id="52cc8-108">ร่างใบแจ้งหนี้ใหม่ถูกสร้างขึ้นจากใบแจ้งหนี้ที่ได้รับการยืนยัน</span><span class="sxs-lookup"><span data-stu-id="52cc8-108">A new draft invoice is created from the confirmed invoice.</span></span> <span data-ttu-id="52cc8-109">รายละเอียดรายการใบแจ้งหนี้ทั้งหมดจากใบแจ้งหนี้ที่ยืนยันก่อนหน้านี้จะถูกคัดลอกไปยังแบบร่างใหม่</span><span class="sxs-lookup"><span data-stu-id="52cc8-109">All invoice line details from the previously confirmed invoice are copied to the new draft.</span></span> <span data-ttu-id="52cc8-110">ต่อไปนี้เป็นประเด็นสำคัญบางประการที่ควรทำความเข้าใจเกี่ยวกับรายละเอียดรายการในใบแจ้งหนี้ที่แก้ไขใหม่:</span><span class="sxs-lookup"><span data-stu-id="52cc8-110">The following are some of the key points to understand about the line details on the new corrected invoice:</span></span>

- <span data-ttu-id="52cc8-111">ปริมาณทั้งหมดจะถูกอัปเดตเป็นศูนย์</span><span class="sxs-lookup"><span data-stu-id="52cc8-111">All quantities are updated to zero.</span></span> <span data-ttu-id="52cc8-112">แอปพลิเคชันจะถือว่ารายการที่ออกใบแจ้งหนี้ทั้งหมดได้รับการให้สินเชื่ออย่างสมบูรณ์</span><span class="sxs-lookup"><span data-stu-id="52cc8-112">The application assumes that all invoiced items are fully credited.</span></span> <span data-ttu-id="52cc8-113">หากจำเป็นคุณสามารถอัปเดตปริมาณเหล่านี้ด้วยตนเองเพื่อให้สอดคล้องกับปริมาณที่จะถูกออกใบแจ้งหนี้ ไม่ใช่ปริมาณการให้สินเชื่อ</span><span class="sxs-lookup"><span data-stu-id="52cc8-113">If needed, you can manually update these quantities to reflect the quantity that is being invoiced, and not the quantity that is being credited.</span></span> <span data-ttu-id="52cc8-114">ตามปริมาณที่คุณป้อน แอปพลิเคชันจะคำนวณปริมาณการให้สินเชื่อ</span><span class="sxs-lookup"><span data-stu-id="52cc8-114">Based on the quantity you enter, the application calculates the credited quantity.</span></span> <span data-ttu-id="52cc8-115">จำนวนเงินนี้จะแสดงในข้อมูลจริงที่สร้างขึ้นเมื่อมีการยืนยันใบแจ้งหนี้ที่แก้ไขแล้ว</span><span class="sxs-lookup"><span data-stu-id="52cc8-115">This amount is reflected in the actuals that are created when the corrected invoice is confirmed.</span></span> <span data-ttu-id="52cc8-116">หากคุณกำลังทำการเปลี่ยนแปลงจำนวนภาษี คุณต้องป้อนจำนวนภาษีที่ถูกต้อง ไม่ใช่จำนวนเงินภาษีที่มีการให้สินเชื่อ</span><span class="sxs-lookup"><span data-stu-id="52cc8-116">If you are making changes to the tax amount, you must enter the correct tax amount and not the tax amount that is being credited.</span></span>
- <span data-ttu-id="52cc8-117">ไม่มีการคัดลอกรายละเอียดการให้บริการตามสัญญาที่อิงตามผลิตภัณฑ์ที่ยืนยันก่อนหน้า</span><span class="sxs-lookup"><span data-stu-id="52cc8-117">Previously confirmed product-based contract lines are not copied over.</span></span> <span data-ttu-id="52cc8-118">ไม่สนับสนุนการประมวลผลการแก้ไขใบแจ้งหนี้โครงการตามผลิตภัณฑ์</span><span class="sxs-lookup"><span data-stu-id="52cc8-118">Processing corrections on a product-based project invoice is not supported.</span></span>
- <span data-ttu-id="52cc8-119">การแก้ไขหลักเป้าหมายจะถูกประมวลผลเป็นการให้สินเชื่อเต็มรูปแบบเสมอ</span><span class="sxs-lookup"><span data-stu-id="52cc8-119">Milestone corrections are always processed as full credits.</span></span>
- <span data-ttu-id="52cc8-120">สามารถแก้ไขค่าธรรมเนียมล่วงหน้าหรือจำนวนเงินล่วงหน้าได้หากลูกค้าออกใบแจ้งหนี้เป็นจำนวนเงินที่ไม่ถูกต้อง</span><span class="sxs-lookup"><span data-stu-id="52cc8-120">Retainer or advance amounts can be corrected if the customer was invoiced for an incorrect amount.</span></span>
- <span data-ttu-id="52cc8-121">การกระทบยอดของค่าธรรมเนียมล่วงหน้าสามารถแก้ไขได้หากใช้จำนวนเงินที่ไม่ถูกต้องเพื่อกระทบยอดกับค่าธรรมเนียมในใบแจ้งหนี้ที่ได้รับการยืนยันก่อนหน้านี้</span><span class="sxs-lookup"><span data-stu-id="52cc8-121">Reconciliations of retainers and advances can be corrected if an incorrect amount was used to reconcile against the charges on a previously confirmed invoice.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="52cc8-122">รายละเอียดรายการใบแจ้งหนี้ที่แก้ไขค่าใช้จ่ายอื่นๆ ที่ออกใบแจ้งหนี้แล้วมีการตั้งค่าฟิลด์ **การแก้ไข** เป็น **ใช่**</span><span class="sxs-lookup"><span data-stu-id="52cc8-122">Invoice line details that are corrections to other already invoiced charges have the field **Correction** set to **Yes**.</span></span> <span data-ttu-id="52cc8-123">ใบแจ้งหนี้ที่แก้ไขรายละเอียดรายการใบแจ้งหนี้จะมีฟิลด์ที่เรียกว่า **มีการแก้ไข** ที่ตั้งค่าเป็น **ใช่**</span><span class="sxs-lookup"><span data-stu-id="52cc8-123">Invoices that have corrected invoice line details have a field called **Has corrections** that is also set to **Yes**.</span></span>

## <a name="actuals-created-when-a-corrective-invoice-is-confirmed"></a><span data-ttu-id="52cc8-124">ข้อมูลจริงที่สร้างขึ้นเมื่อมีการยืนยันใบแจ้งหนี้ที่แก้ไข:</span><span class="sxs-lookup"><span data-stu-id="52cc8-124">Actuals created when a corrective invoice is confirmed</span></span>

<span data-ttu-id="52cc8-125">ตารางต่อไปนี้แสดงรายการข้อมูลจริงที่สร้างขึ้นเมื่อมีการยืนยันใบแจ้งหนี้ที่แก้ไข</span><span class="sxs-lookup"><span data-stu-id="52cc8-125">The following table lists the actuals that are created when a corrective invoice is confirmed.</span></span>

<table border="0" cellspacing="0" cellpadding="0">
    <tbody>
        <tr>
            <td width="216" valign="top">
                <p><span data-ttu-id="52cc8-126">
                    <strong>สถานการณ์สมมติ</strong>
                </span><span class="sxs-lookup"><span data-stu-id="52cc8-126">
                    <strong>Scenario</strong>
                </span></span></p>
            </td>
            <td width="808" valign="top">
                <p><span data-ttu-id="52cc8-127">
                    <strong>สิ่งที่เกิดขึ้นจริงสร้างขึ้นจากการยืนยัน</strong>
                </span><span class="sxs-lookup"><span data-stu-id="52cc8-127">
                    <strong>Actuals created on confirmation</strong>
                </span></span></p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="4" valign="top">
                <p>
<span data-ttu-id="52cc8-128">ยืนยันการแก้ไขใบแจ้งหนี้ล่วงหน้าหรือค่าธรรมเนียมล่วงหน้า<strong></strong>
                </span><span class="sxs-lookup"><span data-stu-id="52cc8-128">Confirm the correction of an invoiced advance or retainer.<strong></strong>
                </span></span></p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="52cc8-129">การกลับรายการการขายที่ยังไม่เรียกเก็บเงินของค่าธรรมเนียมล่วงหน้าหรือจำนวนเงินล่วงหน้าที่สร้างขึ้นสำหรับการกระทบยอด</span><span class="sxs-lookup"><span data-stu-id="52cc8-129">An unbilled sales reversal of the retainer or advance that was created for reconciliation.</span></span> <span data-ttu-id="52cc8-130">จำนวนนี้เป็นค่าบวกเนื่องจากมีวัตถุประสงค์เพื่อยกเลิกค่าลบที่สร้างขึ้นเมื่อมีการออกใบแจ้งหนี้ค่าธรรมเนียมล่วงหน้าหรือเงินล่วงหน้า</span><span class="sxs-lookup"><span data-stu-id="52cc8-130">This amount is positive because it is meant to cancel out the negative that was created when the retainer or advance was invoiced.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="52cc8-131">การกลับรายการขายที่เรียกเก็บเงินจริงถูกสร้างขึ้นสำหรับยอดเงินบนค่าธรรมเนียมล่วงหน้าหรือเงินล่วงหน้าเพื่อย้อนกลับการขายที่เรียกเก็บเงินเดิม</span><span class="sxs-lookup"><span data-stu-id="52cc8-131">A billed sales reversal actual is created for the amount on the retainer or advance to reverse the original billed sales.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="52cc8-132">การขายจริงที่เรียกเก็บเงินแล้วใหม่จะถูกสร้างขึ้นสำหรับจำนวนเงินที่แก้ไขบนค่าธรรมเนียมล่วงหน้าหรือรายการใบแจ้งหนี้ที่แก้ไขตามรายการล่วงหน้า</span><span class="sxs-lookup"><span data-stu-id="52cc8-132">A new billed sales actual is created for the corrected amount on the retainer or advance-based corrected invoice line.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="52cc8-133">ยอดขายที่ยังไม่ได้เรียกเก็บเงินจริงของจำนวนเงินติดลบของค่าธรรมเนียมล่วงหน้าหรือรายการใบแจ้งหนี้ที่แก้ไขตามล่วงหน้า ซึ่งจะใช้สำหรับการกระทบยอด</span><span class="sxs-lookup"><span data-stu-id="52cc8-133">An unbilled sales actual of negative amount of the retainer or advance-based corrected invoice line, which will be used for reconciliation.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="4" valign="top">
                <p>
<span data-ttu-id="52cc8-134">การยืนยันการแก้ไขค่าธรรมเนียมล่วงหน้าที่กระทบยอดก่อนหน้านี้หรือล่วงหน้า</span><span class="sxs-lookup"><span data-stu-id="52cc8-134">A confirmation of the correction of a previously reconciled retainer or advance.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="52cc8-135">การกลับรายการการขายที่ยังไม่เรียกเก็บเงินของค่าธรรมเนียมล่วงหน้าหรือจำนวนเงินล่วงหน้าที่สร้างขึ้นสำหรับการกระทบยอด</span><span class="sxs-lookup"><span data-stu-id="52cc8-135">An unbilled sales reversal of the retainer or advance that was created for reconciliation.</span></span> <span data-ttu-id="52cc8-136">จำนวนนี้เป็นค่าบวกและมีวัตถุประสงค์เพื่อยกเลิกค่าลบที่สร้างขึ้นเมื่อการกระทบยอดก่อนหน้าเกิดขึ้น</span><span class="sxs-lookup"><span data-stu-id="52cc8-136">This amount is positive and is meant to cancel out the negative that was created when the previous reconciliation occurred.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="52cc8-137">การกลับรายการขายที่เรียกเก็บเงินจริงสำหรับยอดเงินในใบแจ้งหนี้ก่อนหน้า</span><span class="sxs-lookup"><span data-stu-id="52cc8-137">A billed sales reversal actual for the amount on the previous invoice.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="52cc8-138">การขายจริงที่เรียกเก็บเงินแล้วใหม่สำหรับจำนวนเงินที่แก้ไขบนค่าธรรมเนียมล่วงหน้าจะใช้กับใบแจ้งหนี้ที่แก้ไข</span><span class="sxs-lookup"><span data-stu-id="52cc8-138">A new billed sales actual for the corrected retainer amount that is applied on the corrected invoice.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="52cc8-139">ยอดขายที่ยังไม่ได้เรียกเก็บเงินจริงที่มีจำนวนเงินติดลบจากค่าธรรมเนียมล่วงหน้าหรือเงินล่วงหน้าที่เหลือที่ถูกแก้ไข ซึ่งจะใช้สำหรับการกระทบยอดในใบแจ้งหนี้ภายหลัง</span><span class="sxs-lookup"><span data-stu-id="52cc8-139">An unbilled sales actual with a negative amount from the corrected leftover retainer or advance, which will be used for reconciliation on later invoices.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="52cc8-140">การออกใบแจ้งหนี้การให้สินเชื่อเต็มรูปแบบของธุรกรรมเวลาที่ออกใบแจ้งหนี้ก่อนหน้านี้</span><span class="sxs-lookup"><span data-stu-id="52cc8-140">Invoicing the full credit of a previously invoiced time transaction.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="52cc8-141">การกลับรายการขายที่เรียกเก็บเงินสำหรับชั่วโมงและจำนวนเงินในรายละเอียดรายการใบแจ้งหนี้เดิมสำหรับเวลา</span><span class="sxs-lookup"><span data-stu-id="52cc8-141">A billed sales reversal for the hours and amount on the original invoice line detail for time.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="52cc8-142">การขายจริงที่เรียกเก็บเงินแล้วสำหรับชั่วโมงและจำนวนเงินในรายละเอียดรายการใบแจ้งหนี้เดิมสำหรับเวลา</span><span class="sxs-lookup"><span data-stu-id="52cc8-142">A new unbilled sales actual for the hours and amount on the original invoice line detail for time.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="3" valign="top">
                <p>
<span data-ttu-id="52cc8-143">การออกใบแจ้งหนี้การให้สินเชื่อบางส่วนในธุรกรรมเวลา</span><span class="sxs-lookup"><span data-stu-id="52cc8-143">Invoicing the partial credit on a time transaction.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="52cc8-144">การกลับรายการขายที่เรียกเก็บเงินสำหรับชั่วโมงและจำนวนเงินที่ออกใบแจ้งหนี้ในรายละเอียดรายการใบแจ้งหนี้เดิมสำหรับเวลา</span><span class="sxs-lookup"><span data-stu-id="52cc8-144">A billed sales reversal for the hours and amount invoiced on the original invoice line detail for time.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="52cc8-145">การขายจริงที่ยังไม่เรียกเก็บเงินใหม่ซึ่งคิดค่าธรรมเนียมเป็นชั่วโมงและจำนวนเงินในรายละเอียดรายการใบแจ้งหนี้ที่แก้ไข การกลับรายการนี้ และการขายจริงที่เรียกเก็บเงินแล้วเทียบเท่า</span><span class="sxs-lookup"><span data-stu-id="52cc8-145">A new unbilled sales actual that is chargeable for the hours and amount on the edited invoice line detail, a reversal of this, and an equivalent billed sales actual.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="52cc8-146">การขายจริงที่ยังไม่เรียกเก็บเงินใหม่ซึ่งคิดค่าธรรมเนียมสำหรับชั่วโมงและจำนวนที่เหลือหลังจากหักตัวเลขที่แก้ไขแล้วในรายละเอียดรายการใบแจ้งหนี้</span><span class="sxs-lookup"><span data-stu-id="52cc8-146">A new unbilled sales actual that is chargeable for the remaining hours and amount after deducting the corrected figures on the invoice line detail.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="52cc8-147">การออกใบแจ้งหนี้การให้สินเชื่อเต็มรูปแบบของธุรกรรมค่าใช้จ่ายที่ออกใบแจ้งหนี้ก่อนหน้านี้</span><span class="sxs-lookup"><span data-stu-id="52cc8-147">Invoicing the full credit of a previously invoiced expense transaction.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="52cc8-148">การกลับรายการขายที่เรียกเก็บเงินสำหรับปริมาณและจำนวนเงินที่ออกใบแจ้งหนี้ในรายละเอียดรายการใบแจ้งหนี้เดิมสำหรับค่าใช้จ่าย</span><span class="sxs-lookup"><span data-stu-id="52cc8-148">A billed sales reversal for the quantity and amount on the original invoice line detail for the expense.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="52cc8-149">การขายจริงใหม่ที่เรียกเก็บเงินสำหรับปริมาณและจำนวนเงินที่ออกใบแจ้งหนี้ในรายละเอียดรายการใบแจ้งหนี้เดิมสำหรับค่าใช้จ่าย</span><span class="sxs-lookup"><span data-stu-id="52cc8-149">A new unbilled sales actual for the quantity and amount on the original invoice line detail for the expense.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="3" valign="top">
                <p>
<span data-ttu-id="52cc8-150">การออกใบแจ้งหนี้การให้สินเชื่อบางส่วนของธุรกรรมค่าใช้จ่ายที่ออกใบแจ้งหนี้ก่อนหน้านี้</span><span class="sxs-lookup"><span data-stu-id="52cc8-150">Invoicing the partial credit of a previously invoiced expense transaction.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="52cc8-151">การกลับรายการขายที่เรียกเก็บเงินสำหรับปริมาณและจำนวนเงินที่ออกใบแจ้งหนี้ในรายละเอียดรายการใบแจ้งหนี้เดิมสำหรับค่าใช้จ่าย</span><span class="sxs-lookup"><span data-stu-id="52cc8-151">A billed sales reversal for the quantity and amount invoiced on the original invoice line detail for an expense.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="52cc8-152">การขายจริงที่ยังไม่เรียกเก็บเงินใหม่ซึ่งคิดค่าธรรมเนียมเป็นปริมาณและจำนวนเงินในรายละเอียดรายการใบแจ้งหนี้ที่แก้ไข การกลับรายการนี้ และการขายจริงที่เรียกเก็บเงินแล้วเทียบเท่า</span><span class="sxs-lookup"><span data-stu-id="52cc8-152">A new unbilled sales actual that is chargeable for the quantity and amount on the corrected invoice line detail, a reversal of this, and an equivalent billed sales actual.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="52cc8-153">การขายจริงที่ยังไม่เรียกเก็บเงินใหม่ซึ่งคิดค่าธรรมเนียมสำหรับปริมาณและจำนวนที่เหลือหลังจากหักตัวเลขที่แก้ไขแล้วในรายละเอียดรายการใบแจ้งหนี้</span><span class="sxs-lookup"><span data-stu-id="52cc8-153">A new unbilled sales actual that is chargeable for the remaining quantity and amount after deducting the corrected figures on the invoice line detail.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="52cc8-154">การออกใบแจ้งหนี้เครดิตเต็มจำนวนของธุรกรรมวัสดุที่ออกใบแจ้งหนี้ก่อนหน้านี้</span><span class="sxs-lookup"><span data-stu-id="52cc8-154">Invoicing the full credit of a previously invoiced material transaction.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="52cc8-155">การกลับรายการยอดขายที่เรียกเก็บเงินสำหรับปริมาณและจำนวนเงินในรายละเอียดรายการใบแจ้งหนี้เดิมสำหรับวัสดุ</span><span class="sxs-lookup"><span data-stu-id="52cc8-155">A billed sales reversal for the quantity and amount on the original invoice line detail for material.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="52cc8-156">การขายจริงที่ยังไม่เรียกเก็บเงินใหม่สำหรับปริมาณและจำนวนเงินในรายละเอียดรายการใบแจ้งหนี้เดิมสำหรับวัสดุ</span><span class="sxs-lookup"><span data-stu-id="52cc8-156">A new unbilled sales actual for the quantity and amount on the original invoice line detail for material.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="3" valign="top">
                <p>
<span data-ttu-id="52cc8-157">การออกใบแจ้งหนี้เครดิตบางส่วนสำหรับธุรกรรมวัสดุ</span><span class="sxs-lookup"><span data-stu-id="52cc8-157">Invoicing the partial credit on a material transaction.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="52cc8-158">การกลับรายการยอดขายที่เรียกเก็บเงินสำหรับปริมาณและจำนวนเงินที่ออกใบแจ้งหนี้ในรายละเอียดรายการใบแจ้งหนี้เดิมสำหรับวัสดุ</span><span class="sxs-lookup"><span data-stu-id="52cc8-158">A billed sales reversal for the quantity and amount invoiced on the original invoice line detail for material.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="52cc8-159">การขายจริงที่ยังไม่เรียกเก็บเงินใหม่ซึ่งคิดค่าธรรมเนียมได้สำหรับปริมาณและจำนวนเงินในรายละเอียดรายการใบแจ้งหนี้ที่แก้ไข การกลับรายการนี้และการขายจริงที่เรียกเก็บเงินแล้วเทียบเท่า</span><span class="sxs-lookup"><span data-stu-id="52cc8-159">A new unbilled sales actual that is chargeable for the quantity and amount on the edited invoice line detail, a reversal of this, and an equivalent billed sales actual.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="52cc8-160">การขายจริงที่ยังไม่เรียกเก็บเงินใหม่ซึ่งคิดค่าธรรมเนียมสำหรับปริมาณและจำนวนที่เหลือหลังจากหักตัวเลขที่แก้ไขแล้วในรายละเอียดรายการใบแจ้งหนี้</span><span class="sxs-lookup"><span data-stu-id="52cc8-160">A new unbilled sales actual that is chargeable for the remaining quantity and amount after deducting the corrected figures on the invoice line detail.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="52cc8-161">การออกใบแจ้งหนี้การให้สินเชื่อเต็มรูปแบบของธุรกรรมค่าธรรมเนียมที่ออกใบแจ้งหนี้ก่อนหน้านี้</span><span class="sxs-lookup"><span data-stu-id="52cc8-161">Invoicing the full credit of a previously invoiced fee transaction.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="52cc8-162">การกลับรายการขายที่เรียกเก็บเงินสำหรับปริมาณและจำนวนเงินที่ออกใบแจ้งหนี้ในรายละเอียดรายการใบแจ้งหนี้เดิมสำหรับค่าธรรมเนียม</span><span class="sxs-lookup"><span data-stu-id="52cc8-162">A billed sales reversal for the quantity and amount on the original invoice line detail for the fee.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="52cc8-163">การขายจริงใหม่ที่เรียกเก็บเงินสำหรับปริมาณและจำนวนเงินที่ออกใบแจ้งหนี้ในรายละเอียดรายการใบแจ้งหนี้เดิมสำหรับค่าธรรมเนียม</span><span class="sxs-lookup"><span data-stu-id="52cc8-163">A new unbilled sales actual for the quantity and amount on the original invoice line detail for the fee.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="52cc8-164">การออกใบแจ้งหนี้การให้สินเชื่อบางส่วนของธุรกรรมค่าธรรมเนียมที่ออกใบแจ้งหนี้ก่อนหน้านี้</span><span class="sxs-lookup"><span data-stu-id="52cc8-164">Invoicing the partial credit of a previously invoiced fee transaction.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="52cc8-165">การกลับรายการขายที่เรียกเก็บเงินสำหรับปริมาณและจำนวนเงินที่ออกใบแจ้งหนี้ในรายละเอียดรายการใบแจ้งหนี้เดิมสำหรับค่าธรรมเนียม</span><span class="sxs-lookup"><span data-stu-id="52cc8-165">A billed sales reversal for the quantity and amount invoiced on the original invoice line detail for fee.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="52cc8-166">การขายจริงที่ยังไม่เรียกเก็บเงินใหม่ซึ่งคิดค่าธรรมเนียมเป็นปริมาณและจำนวนเงินในรายละเอียดรายการใบแจ้งหนี้การแก้ไขที่แก้ไข การกลับรายการนี้ และการขายจริงที่เรียกเก็บเงินแล้วเทียบเท่า</span><span class="sxs-lookup"><span data-stu-id="52cc8-166">A new unbilled sales actual that is chargeable for the quantity and amount on the edited corrective invoice line detail, a reversal of this, and an equivalent billed sales actual.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" valign="top">
                <p>
<span data-ttu-id="52cc8-167">การออกใบแจ้งหนี้การให้สินเชื่อเต็มรูปแบบของเหตุการณ์สําคัญที่ออกใบแจ้งหนี้ก่อนหน้านี้</span><span class="sxs-lookup"><span data-stu-id="52cc8-167">Invoicing the full credit of a previously invoiced milestone.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="52cc8-168">การกลับรายการขายที่เรียกเก็บเงินสำหรับจำนวนเงินในรายละเอียดรายการใบแจ้งหนี้เดิมสำหรับเหตุการณ์สําคัญ</span><span class="sxs-lookup"><span data-stu-id="52cc8-168">A billed sales reversal for the amount on the original invoice line detail for the milestone.</span></span>
                </p>
                <p>
<span data-ttu-id="52cc8-169">สถานะใบแจ้งหนี้ของหลักเป้าหมายได้รับการปรับปรุงจาก <b>ใบแจ้งหนี้ของลูกค้าที่ลงรายการบัญชีแล้ว</b> เป็น <b>พร้อมที่จะออกใบแจ้งหนี้</b></span><span class="sxs-lookup"><span data-stu-id="52cc8-169">The invoice status of the milestone is updated from <b>Customer Invoice Posted</b> to <b>Ready to Invoice</b>.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" valign="top">
                <p>
<span data-ttu-id="52cc8-170">การออกใบแจ้งหนี้การให้สินเชื่อบางส่วนของเหตุการณ์สําคัญที่ออกใบแจ้งหนี้ก่อนหน้านี้</span><span class="sxs-lookup"><span data-stu-id="52cc8-170">Invoicing the partial credit of a previously invoiced milestone.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="52cc8-171">ไม่สนับสนุน</span><span class="sxs-lookup"><span data-stu-id="52cc8-171">Unsupported</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="216" valign="top">
                <p>
<span data-ttu-id="52cc8-172">เครดิตและการแก้ไขรายละเอียดการให้บริการตามสัญญาตามผลิตภัณฑ์ที่ออกใบแจ้งหนี้ก่อนหน้านี้</span><span class="sxs-lookup"><span data-stu-id="52cc8-172">Credits and corrections of a previously invoiced product-based contract line.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="52cc8-173">ไม่สนับสนุน</span><span class="sxs-lookup"><span data-stu-id="52cc8-173">Unsupported</span></span> </p>
            </td>
        </tr>
    </tbody>
</table>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
