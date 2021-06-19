---
title: ใบแจ้งหนี้ตามโครงการที่แก้ไข
description: หัวข้อนี้ให้ข้อมูลเกี่ยวกับวิธีสร้างและยืนยันใบแจ้งหนี้ตามโครงการที่มีการแก้ไขใน Project Operations
author: rumant
ms.date: 03/29/2021
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: f6b6670f823577bf7f784443f97f0b77e1e9a6aa
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 05/10/2021
ms.locfileid: "6012294"
---
# <a name="corrective-project-based-invoices"></a><span data-ttu-id="9cf0b-103">ใบแจ้งหนี้ตามโครงการที่แก้ไข</span><span class="sxs-lookup"><span data-stu-id="9cf0b-103">Corrective project-based invoices</span></span>

<span data-ttu-id="9cf0b-104">_**นำไปใช้กับ:** Project Operations สำหรับสถานการณ์ตามทรัพยากร/วัสดุที่ไม่ได้เก็บในคลัง_</span><span class="sxs-lookup"><span data-stu-id="9cf0b-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

<span data-ttu-id="9cf0b-105">ใบแจ้งหนี้โครงการที่ได้รับการยืนยันสามารถแก้ไขเพื่อประมวลผลการเปลี่ยนแปลงหรือเครดิตตามที่เจรจากับลูกค้าและผู้จัดการโครงการ</span><span class="sxs-lookup"><span data-stu-id="9cf0b-105">A confirmed project invoice can be corrected to process changes or credits as negotiated with the customer and project manager.</span></span>

<span data-ttu-id="9cf0b-106">หากต้องการแก้ไขใบแจ้งหนี้ที่ได้รับการยืนยัน ให้เปิดใบแจ้งหนี้ที่ยืนยันแล้วเลือก **แก้ไขใบแจ้งหนี้นี้**</span><span class="sxs-lookup"><span data-stu-id="9cf0b-106">To make edits to a confirmed invoice, open the confirmed invoice and select **Correct this Invoice**.</span></span> 

> [!NOTE]
> <span data-ttu-id="9cf0b-107">ตัวเลือกนี้ไม่สามารถใช้ได้เว้นแต่ใบแจ้งหนี้โครงการจะได้รับการยืนยันหรือใบแจ้งหนี้ตามโครงการมีการเบิกเงินล่วงหน้าหรือค่าธรรมเนียมล่วงหน้าหรือการกระทบยอดของการเบิกเงินล่วงหน้าหรือค่าธรรมเนียมล่วงหน้า</span><span class="sxs-lookup"><span data-stu-id="9cf0b-107">This selection isn't available unless a project invoice is confirmed or the project-based invoice has advances or retainers or reconciliations of advances or retainers.</span></span>

<span data-ttu-id="9cf0b-108">ร่างใบแจ้งหนี้ใหม่ถูกสร้างขึ้นจากใบแจ้งหนี้ที่ได้รับการยืนยัน</span><span class="sxs-lookup"><span data-stu-id="9cf0b-108">A new draft invoice is created from the confirmed invoice.</span></span> <span data-ttu-id="9cf0b-109">รายละเอียดรายการใบแจ้งหนี้ทั้งหมดจากใบแจ้งหนี้ที่ยืนยันก่อนหน้านี้จะถูกคัดลอกไปยังแบบร่างใหม่</span><span class="sxs-lookup"><span data-stu-id="9cf0b-109">All invoice line details from the previously confirmed invoice are copied to the new draft.</span></span> <span data-ttu-id="9cf0b-110">ต่อไปนี้เป็นประเด็นสำคัญบางประการที่ควรทำความเข้าใจเกี่ยวกับรายละเอียดรายการในใบแจ้งหนี้ที่แก้ไขใหม่:</span><span class="sxs-lookup"><span data-stu-id="9cf0b-110">The following are some of the key points to understand about the line details on the new corrected invoice:</span></span>

- <span data-ttu-id="9cf0b-111">ปริมาณทั้งหมดจะถูกอัปเดตเป็นศูนย์</span><span class="sxs-lookup"><span data-stu-id="9cf0b-111">All quantities are updated to zero.</span></span> <span data-ttu-id="9cf0b-112">Dynamics 365 Project Operations จะถือว่าสินค้าในใบแจ้งหนี้ทั้งหมดได้รับเครดิตเต็มจำนวน</span><span class="sxs-lookup"><span data-stu-id="9cf0b-112">Dynamics 365 Project Operations assumes that all invoiced items are fully credited.</span></span> <span data-ttu-id="9cf0b-113">หากจำเป็นคุณสามารถอัปเดตปริมาณเหล่านี้ด้วยตนเองเพื่อให้สอดคล้องกับปริมาณที่จะถูกออกใบแจ้งหนี้ ไม่ใช่ปริมาณการให้สินเชื่อ</span><span class="sxs-lookup"><span data-stu-id="9cf0b-113">If needed, you can manually update these quantities to reflect the quantity that is being invoiced, and not the quantity that is being credited.</span></span> <span data-ttu-id="9cf0b-114">ตามปริมาณที่คุณป้อน แอปพลิเคชันจะคำนวณปริมาณการให้สินเชื่อ</span><span class="sxs-lookup"><span data-stu-id="9cf0b-114">Based on the quantity you enter, the application calculates the credited quantity.</span></span> <span data-ttu-id="9cf0b-115">จำนวนเงินนี้จะแสดงในข้อมูลจริงที่สร้างขึ้นเมื่อมีการยืนยันใบแจ้งหนี้ที่แก้ไขแล้ว</span><span class="sxs-lookup"><span data-stu-id="9cf0b-115">This amount is reflected in the actuals that are created when the corrected invoice is confirmed.</span></span> <span data-ttu-id="9cf0b-116">หากคุณกำลังทำการเปลี่ยนแปลงจำนวนภาษี คุณต้องป้อนจำนวนภาษีที่ถูกต้อง ไม่ใช่จำนวนเงินภาษีที่มีการให้สินเชื่อ</span><span class="sxs-lookup"><span data-stu-id="9cf0b-116">If you are making changes to the tax amount, you must enter the correct tax amount and not the tax amount that is being credited.</span></span>
- <span data-ttu-id="9cf0b-117">การแก้ไขหลักเป้าหมายจะถูกประมวลผลเป็นการให้สินเชื่อเต็มรูปแบบเสมอ</span><span class="sxs-lookup"><span data-stu-id="9cf0b-117">Milestone corrections are always processed as full credits.</span></span>


> [!IMPORTANT]
> <span data-ttu-id="9cf0b-118">สำหรับรายละเอียดรายการใบแจ้งหนี้ที่แก้ไขการเรียกเก็บเงินอื่นๆ ที่ออกใบแจ้งหนี้แล้ว มีการตั้งค่าฟิลด์ **การแก้ไข** เป็น **ใช่**</span><span class="sxs-lookup"><span data-stu-id="9cf0b-118">For invoice line details that are corrections to other already invoiced charges, the **Correction** field is set to **Yes**.</span></span> <span data-ttu-id="9cf0b-119">สำหรับใบแจ้งหนี้ที่มีการแก้ไขรายละเอียดรายการใบแจ้งหนี้ มีการตั้งค่าฟิลด์ **มีการแก้ไข** เป็น **ใช่**</span><span class="sxs-lookup"><span data-stu-id="9cf0b-119">For invoices that have corrected invoice line details, the **Has corrections** field is set to **Yes**.</span></span>

## <a name="actuals-created-when-a-corrective-invoice-is-confirmed"></a><span data-ttu-id="9cf0b-120">ข้อมูลจริงที่สร้างขึ้นเมื่อมีการยืนยันใบแจ้งหนี้ที่แก้ไข:</span><span class="sxs-lookup"><span data-stu-id="9cf0b-120">Actuals created when a corrective invoice is confirmed</span></span>

<span data-ttu-id="9cf0b-121">ตารางต่อไปนี้แสดงรายการข้อมูลจริงที่สร้างขึ้นเมื่อมีการยืนยันใบแจ้งหนี้ที่แก้ไข</span><span class="sxs-lookup"><span data-stu-id="9cf0b-121">The following table lists the actuals that are created when a corrective invoice is confirmed.</span></span>

<table border="0" cellspacing="0" cellpadding="0">
    <tbody>
        <tr>
            <td width="216" valign="top">
                <p><span data-ttu-id="9cf0b-122">
                    <strong>สถานการณ์สมมติ</strong>
                </span><span class="sxs-lookup"><span data-stu-id="9cf0b-122">
                    <strong>Scenario</strong>
                </span></span></p>
            </td>
            <td width="808" valign="top">
                <p><span data-ttu-id="9cf0b-123">
                    <strong>สิ่งที่เกิดขึ้นจริงสร้างขึ้นจากการยืนยัน</strong>
                </span><span class="sxs-lookup"><span data-stu-id="9cf0b-123">
                    <strong>Actuals created on confirmation</strong>
                </span></span></p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="9cf0b-124">การออกใบแจ้งหนี้การให้สินเชื่อเต็มรูปแบบของธุรกรรมเวลาที่ออกใบแจ้งหนี้ก่อนหน้านี้</span><span class="sxs-lookup"><span data-stu-id="9cf0b-124">Invoicing the full credit of a previously invoiced time transaction.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="9cf0b-125">การกลับรายการขายที่เรียกเก็บเงินสำหรับชั่วโมงและจำนวนเงินในรายละเอียดรายการใบแจ้งหนี้เดิมสำหรับเวลา</span><span class="sxs-lookup"><span data-stu-id="9cf0b-125">A billed sales reversal for the hours and amount on the original invoice line detail for time.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="9cf0b-126">การขายจริงที่เรียกเก็บเงินแล้วสำหรับชั่วโมงและจำนวนเงินในรายละเอียดรายการใบแจ้งหนี้เดิมสำหรับเวลา</span><span class="sxs-lookup"><span data-stu-id="9cf0b-126">A new unbilled sales actual for the hours and amount on the original invoice line detail for time.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="3" valign="top">
                <p>
<span data-ttu-id="9cf0b-127">การออกใบแจ้งหนี้การให้สินเชื่อบางส่วนในธุรกรรมเวลา</span><span class="sxs-lookup"><span data-stu-id="9cf0b-127">Invoicing the partial credit on a time transaction.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="9cf0b-128">การกลับรายการขายที่เรียกเก็บเงินสำหรับชั่วโมงและจำนวนเงินที่ออกใบแจ้งหนี้ในรายละเอียดรายการใบแจ้งหนี้เดิมสำหรับเวลา</span><span class="sxs-lookup"><span data-stu-id="9cf0b-128">A billed sales reversal for the hours and amount invoiced on the original invoice line detail for time.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="9cf0b-129">การขายจริงที่ยังไม่เรียกเก็บเงินใหม่ซึ่งคิดค่าธรรมเนียมเป็นชั่วโมงและจำนวนเงินในรายละเอียดรายการใบแจ้งหนี้ที่แก้ไข การกลับรายการนี้ และการขายจริงที่เรียกเก็บเงินแล้วเทียบเท่า</span><span class="sxs-lookup"><span data-stu-id="9cf0b-129">A new unbilled sales actual that is chargeable for the hours and amount on the edited invoice line detail, a reversal of this, and an equivalent billed sales actual.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="9cf0b-130">การขายจริงที่ยังไม่เรียกเก็บเงินใหม่ซึ่งคิดค่าธรรมเนียมสำหรับชั่วโมงและจำนวนที่เหลือหลังจากหักตัวเลขที่แก้ไขแล้วในรายละเอียดรายการใบแจ้งหนี้</span><span class="sxs-lookup"><span data-stu-id="9cf0b-130">A new unbilled sales actual that is chargeable for the remaining hours and amount after deducting the corrected figures on the invoice line detail.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="9cf0b-131">การออกใบแจ้งหนี้การให้สินเชื่อเต็มรูปแบบของธุรกรรมค่าใช้จ่ายที่ออกใบแจ้งหนี้ก่อนหน้านี้</span><span class="sxs-lookup"><span data-stu-id="9cf0b-131">Invoicing the full credit of a previously invoiced expense transaction.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="9cf0b-132">การกลับรายการขายที่เรียกเก็บเงินสำหรับปริมาณและจำนวนเงินที่ออกใบแจ้งหนี้ในรายละเอียดรายการใบแจ้งหนี้เดิมสำหรับค่าใช้จ่าย</span><span class="sxs-lookup"><span data-stu-id="9cf0b-132">A billed sales reversal for the quantity and amount on the original invoice line detail for the expense.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="9cf0b-133">การขายจริงใหม่ที่เรียกเก็บเงินสำหรับปริมาณและจำนวนเงินที่ออกใบแจ้งหนี้ในรายละเอียดรายการใบแจ้งหนี้เดิมสำหรับค่าใช้จ่าย</span><span class="sxs-lookup"><span data-stu-id="9cf0b-133">A new unbilled sales actual for the quantity and amount on the original invoice line detail for the expense.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="3" valign="top">
                <p>
<span data-ttu-id="9cf0b-134">การออกใบแจ้งหนี้การให้สินเชื่อบางส่วนของธุรกรรมค่าใช้จ่ายที่ออกใบแจ้งหนี้ก่อนหน้านี้</span><span class="sxs-lookup"><span data-stu-id="9cf0b-134">Invoicing the partial credit of a previously invoiced expense transaction.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="9cf0b-135">การกลับรายการขายที่เรียกเก็บเงินสำหรับปริมาณและจำนวนเงินที่ออกใบแจ้งหนี้ในรายละเอียดรายการใบแจ้งหนี้เดิมสำหรับค่าใช้จ่าย</span><span class="sxs-lookup"><span data-stu-id="9cf0b-135">A billed sales reversal for the quantity and amount invoiced on the original invoice line detail for an expense.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="9cf0b-136">การขายจริงที่ยังไม่เรียกเก็บเงินใหม่ซึ่งคิดค่าธรรมเนียมเป็นปริมาณและจำนวนเงินในรายละเอียดรายการใบแจ้งหนี้ที่แก้ไข การกลับรายการนี้ และการขายจริงที่เรียกเก็บเงินแล้วเทียบเท่า</span><span class="sxs-lookup"><span data-stu-id="9cf0b-136">A new unbilled sales actual that is chargeable for the quantity and amount on the corrected invoice line detail, a reversal of this, and an equivalent billed sales actual.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="9cf0b-137">การขายจริงที่ยังไม่เรียกเก็บเงินใหม่ซึ่งคิดค่าธรรมเนียมสำหรับปริมาณและจำนวนที่เหลือหลังจากหักตัวเลขที่แก้ไขแล้วในรายละเอียดรายการใบแจ้งหนี้</span><span class="sxs-lookup"><span data-stu-id="9cf0b-137">A new unbilled sales actual that is chargeable for the remaining quantity and amount after deducting the corrected figures on the invoice line detail.</span></span>
                </p>
            </td>
        </tr>
                <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="9cf0b-138">การออกใบแจ้งหนี้เครดิตเต็มจำนวนของธุรกรรมวัสดุที่ออกใบแจ้งหนี้ก่อนหน้านี้</span><span class="sxs-lookup"><span data-stu-id="9cf0b-138">Invoicing the full credit of a previously invoiced material transaction.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="9cf0b-139">การกลับรายการยอดขายที่เรียกเก็บเงินสำหรับปริมาณและจำนวนเงินในรายละเอียดรายการใบแจ้งหนี้เดิมสำหรับวัสดุ</span><span class="sxs-lookup"><span data-stu-id="9cf0b-139">A billed sales reversal for the quantity and amount on the original invoice line detail for material.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="9cf0b-140">การขายจริงที่ยังไม่เรียกเก็บเงินใหม่สำหรับปริมาณและจำนวนเงินในรายละเอียดรายการใบแจ้งหนี้เดิมสำหรับวัสดุ</span><span class="sxs-lookup"><span data-stu-id="9cf0b-140">A new unbilled sales actual for the quantity and amount on the original invoice line detail for material.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="3" valign="top">
                <p>
<span data-ttu-id="9cf0b-141">การออกใบแจ้งหนี้เครดิตบางส่วนสำหรับธุรกรรมวัสดุ</span><span class="sxs-lookup"><span data-stu-id="9cf0b-141">Invoicing the partial credit on a material transaction.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="9cf0b-142">การกลับรายการยอดขายที่เรียกเก็บเงินสำหรับปริมาณและจำนวนเงินที่ออกใบแจ้งหนี้ในรายละเอียดรายการใบแจ้งหนี้เดิมสำหรับวัสดุ</span><span class="sxs-lookup"><span data-stu-id="9cf0b-142">A billed sales reversal for the quantity and amount invoiced on the original invoice line detail for material.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="9cf0b-143">การขายจริงที่ยังไม่เรียกเก็บเงินใหม่ซึ่งคิดค่าธรรมเนียมได้สำหรับปริมาณและจำนวนเงินในรายละเอียดรายการใบแจ้งหนี้ที่แก้ไข การกลับรายการนี้และการขายจริงที่เรียกเก็บเงินแล้วเทียบเท่า</span><span class="sxs-lookup"><span data-stu-id="9cf0b-143">A new unbilled sales actual that is chargeable for the quantity and amount on the edited invoice line detail, a reversal of this, and an equivalent billed sales actual.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="9cf0b-144">การขายจริงที่ยังไม่เรียกเก็บเงินใหม่ซึ่งคิดค่าธรรมเนียมสำหรับปริมาณและจำนวนที่เหลือหลังจากหักตัวเลขที่แก้ไขแล้วในรายละเอียดรายการใบแจ้งหนี้</span><span class="sxs-lookup"><span data-stu-id="9cf0b-144">A new unbilled sales actual that is chargeable for the remaining quantity and amount after deducting the corrected figures on the invoice line detail.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="9cf0b-145">การออกใบแจ้งหนี้การให้สินเชื่อเต็มรูปแบบของธุรกรรมค่าธรรมเนียมที่ออกใบแจ้งหนี้ก่อนหน้านี้</span><span class="sxs-lookup"><span data-stu-id="9cf0b-145">Invoicing the full credit of a previously invoiced fee transaction.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="9cf0b-146">การกลับรายการขายที่เรียกเก็บเงินสำหรับปริมาณและจำนวนเงินที่ออกใบแจ้งหนี้ในรายละเอียดรายการใบแจ้งหนี้เดิมสำหรับค่าธรรมเนียม</span><span class="sxs-lookup"><span data-stu-id="9cf0b-146">A billed sales reversal for the quantity and amount on the original invoice line detail for the fee.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="9cf0b-147">การขายจริงใหม่ที่เรียกเก็บเงินสำหรับปริมาณและจำนวนเงินที่ออกใบแจ้งหนี้ในรายละเอียดรายการใบแจ้งหนี้เดิมสำหรับค่าธรรมเนียม</span><span class="sxs-lookup"><span data-stu-id="9cf0b-147">A new unbilled sales actual for the quantity and amount on the original invoice line detail for the fee.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="9cf0b-148">การออกใบแจ้งหนี้การให้สินเชื่อบางส่วนของธุรกรรมค่าธรรมเนียมที่ออกใบแจ้งหนี้ก่อนหน้านี้</span><span class="sxs-lookup"><span data-stu-id="9cf0b-148">Invoicing the partial credit of a previously invoiced fee transaction.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="9cf0b-149">การกลับรายการขายที่เรียกเก็บเงินสำหรับปริมาณและจำนวนเงินที่ออกใบแจ้งหนี้ในรายละเอียดรายการใบแจ้งหนี้เดิมสำหรับค่าธรรมเนียม</span><span class="sxs-lookup"><span data-stu-id="9cf0b-149">A billed sales reversal for the quantity and amount invoiced on the original invoice line detail for fee.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="9cf0b-150">การขายจริงที่ยังไม่เรียกเก็บเงินใหม่ซึ่งคิดค่าธรรมเนียมเป็นปริมาณและจำนวนเงินในรายละเอียดรายการใบแจ้งหนี้การแก้ไขที่แก้ไข การกลับรายการนี้ และการขายจริงที่เรียกเก็บเงินแล้วเทียบเท่า</span><span class="sxs-lookup"><span data-stu-id="9cf0b-150">A new unbilled sales actual that is chargeable for the quantity and amount on the edited corrective invoice line detail, a reversal of this, and an equivalent billed sales actual.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" valign="top">
                <p>
<span data-ttu-id="9cf0b-151">การออกใบแจ้งหนี้การให้สินเชื่อเต็มรูปแบบของเหตุการณ์สําคัญที่ออกใบแจ้งหนี้ก่อนหน้านี้</span><span class="sxs-lookup"><span data-stu-id="9cf0b-151">Invoicing the full credit of a previously invoiced milestone.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="9cf0b-152">การกลับรายการขายที่เรียกเก็บเงินสำหรับจำนวนเงินในรายละเอียดรายการใบแจ้งหนี้เดิมสำหรับเหตุการณ์สําคัญ</span><span class="sxs-lookup"><span data-stu-id="9cf0b-152">A billed sales reversal for the amount on the original invoice line detail for the milestone.</span></span>
                </p>
                <p>
<span data-ttu-id="9cf0b-153">สถานะใบแจ้งหนี้ของหลักเป้าหมายได้รับการปรับปรุงจาก <b>ใบแจ้งหนี้ของลูกค้าที่ลงรายการบัญชีแล้ว</b> เป็น <b>พร้อมที่จะออกใบแจ้งหนี้</b></span><span class="sxs-lookup"><span data-stu-id="9cf0b-153">The invoice status of the milestone is updated from <b>Customer Invoice Posted</b> to <b>Ready to Invoice</b>.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" valign="top">
                <p>
<span data-ttu-id="9cf0b-154">การออกใบแจ้งหนี้การให้สินเชื่อบางส่วนของเหตุการณ์สําคัญที่ออกใบแจ้งหนี้ก่อนหน้านี้</span><span class="sxs-lookup"><span data-stu-id="9cf0b-154">Invoicing the partial credit of a previously invoiced milestone.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="9cf0b-155">ไม่สนับสนุนสถานการณ์นี้</span><span class="sxs-lookup"><span data-stu-id="9cf0b-155">This scenario isn't supported.</span></span>
                </p>
            </td>
        </tr>       
    </tbody>
</table>


[!INCLUDE[footer-include](../includes/footer-banner.md)]
