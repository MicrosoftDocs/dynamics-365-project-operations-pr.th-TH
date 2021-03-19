---
title: ยืนยันใบแจ้งหนี้ Proforma
description: หัวข้อนี้ให้ข้อมูลเกี่ยวกับการยืนยันใบแจ้งหนี้ Proforma
author: rumant
manager: AnnBe
ms.date: 10/13/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: b2ed241509d2643d841ce55777e6e316612f70b8
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 02/15/2021
ms.locfileid: "5287891"
---
# <a name="confirm-a-proforma-invoice"></a><span data-ttu-id="6b7d3-103">ยืนยันใบแจ้งหนี้ Proforma</span><span class="sxs-lookup"><span data-stu-id="6b7d3-103">Confirm a proforma invoice</span></span>

<span data-ttu-id="6b7d3-104">_**นำไปใช้กับ:** Project Operations สำหรับสถานการณ์ตามทรัพยากร/วัสดุที่ไม่ได้เก็บในคลัง_</span><span class="sxs-lookup"><span data-stu-id="6b7d3-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

<span data-ttu-id="6b7d3-105">หลังจากยืนยันใบแจ้งหนี้ Proforma แล้วสถานะของใบแจ้งหนี้โครงการจะอัปเดตเป็น **ได้รับการยืนยัน**</span><span class="sxs-lookup"><span data-stu-id="6b7d3-105">After a proforma invoice is confirmed, the status of the project invoice updates to **Confirmed**.</span></span> <span data-ttu-id="6b7d3-106">เมื่อใบแจ้งหนี้ได้รับการยืนยัน จะกลายเป็นแบบอ่านอย่างเดียว</span><span class="sxs-lookup"><span data-stu-id="6b7d3-106">When an invoice is confirmed, it becomes read-only.</span></span> <span data-ttu-id="6b7d3-107">นับจากนี้จะสามารถแก้ไขใบแจ้งหนี้ได้ก็ต่อเมื่อมีการแก้ไขหรือเครดิตที่ลูกค้าเป็นผู้เริ่มต้นหรือเมื่อมีการทำเครื่องหมายว่าชำระเงินแล้ว</span><span class="sxs-lookup"><span data-stu-id="6b7d3-107">Going forward, the invoice can only be corrected if there are any customer-initiated corrections or credits, or when it's marked as paid.</span></span>

<span data-ttu-id="6b7d3-108">ตารางต่อไปนี้แสดงรายการจริงที่สร้างโดยระบบ</span><span class="sxs-lookup"><span data-stu-id="6b7d3-108">The following table lists the actuals created by the system.</span></span> <span data-ttu-id="6b7d3-109">ข้อมูลจริงเหล่านี้ถูกสร้างขึ้นเมื่อมีการดำเนินการบางอย่างในใบแจ้งหนี้โครงการแบบร่างก่อนที่จะได้รับการยืนยัน</span><span class="sxs-lookup"><span data-stu-id="6b7d3-109">These actuals are created when certain operations are performed on the draft project invoice before it is confirmed.</span></span>

<table border="0" cellspacing="0" cellpadding="0">
    <tbody>
        <tr>
            <td width="416" valign="top">
                <p><span data-ttu-id="6b7d3-110">
                    <strong>สถานการณ์สมมติ</strong>
                </span><span class="sxs-lookup"><span data-stu-id="6b7d3-110">
                    <strong>Scenario</strong>
                </span></span></p>
            </td>
            <td width="608" valign="top">
                <p><span data-ttu-id="6b7d3-111">
                    <strong>สิ่งที่เกิดขึ้นจริงสร้างขึ้นจากการยืนยัน</strong>
                </span><span class="sxs-lookup"><span data-stu-id="6b7d3-111">
                    <strong>Actuals created on confirmation</strong>
                </span></span></p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="6b7d3-112">การออกใบแจ้งหนี้ธุรกรรมเวลาโดยไม่มีการแก้ไขใดๆ ในแบบร่างใบแจ้งหนี้</span><span class="sxs-lookup"><span data-stu-id="6b7d3-112">Invoicing a time transaction without any edits on the draft invoice.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="6b7d3-113">การกลับการขายที่ไม่ได้เรียกเก็บเงินสำหรับชั่วโมงและจำนวนเงินในการอนุมัติเวลาตามเดิม</span><span class="sxs-lookup"><span data-stu-id="6b7d3-113">An unbilled sales reversal for the hours and amount on the original time approval.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="6b7d3-114">การขายที่มีการเรียกเก็บเงินจริงสำหรับชั่วโมงและจำนวนเงินในการอนุมัติเวลาตามเดิม</span><span class="sxs-lookup"><span data-stu-id="6b7d3-114">A billed sales actual for the hours and amount on the original time approval.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="3" valign="top">
                <p>
<span data-ttu-id="6b7d3-115">การออกใบแจ้งหนี้ธุรกรรมเวลาที่แก้ไขเพื่อลดปริมาณ</span><span class="sxs-lookup"><span data-stu-id="6b7d3-115">Invoicing a time transaction that was edited to reduce the quantity.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="6b7d3-116">การกลับการขายที่ไม่ได้เรียกเก็บเงินสำหรับชั่วโมงและจำนวนเงินในการอนุมัติเวลาตามเดิม</span><span class="sxs-lookup"><span data-stu-id="6b7d3-116">An unbilled sales reversal for the hours and amount on the original time approval.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="6b7d3-117">การขายจริงใหม่ที่ยังไม่เรียกเก็บเงินซึ่งคิดค่าธรรมเนียมเป็นชั่วโมงและจำนวนเงินในรายละเอียดรายการใบแจ้งหนี้ที่แก้ไข การย้อนกลับของการขายจริงที่ไม่ได้เรียกเก็บเงินและเทียบเท่ากับการขายจริงที่เรียกเก็บเงิน</span><span class="sxs-lookup"><span data-stu-id="6b7d3-117">A new unbilled sales actual that is chargeable for the hours and amount on the edited invoice line detail, a reversal of the unbilled sales actual, and an equivalent billed sales actual.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="6b7d3-118">การขายจริงใหม่ที่ยังไม่เรียกเก็บเงินซึ่งไม่คิดค่าธรรมเนียมเป็นชั่วโมงและจำนวนเงินที่เหลือหลังจากการลดการกำหนดค่าที่แก้ไขในรายละเอียดรายการใบแจ้งหนี้ที่แก้ไข การย้อนกลับของการขายจริงที่ไม่ได้เรียกเก็บเงินและเทียบเท่ากับการขายจริงที่เรียกเก็บเงิน</span><span class="sxs-lookup"><span data-stu-id="6b7d3-118">A new unbilled sales actual that is non-chargeable for the remaining hours and amount after deducting the corrected figures on the edited invoice line detail, a reversal of the unbilled sales actual, and an equivalent billed sales actual.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="6b7d3-119">การออกใบแจ้งหนี้ธุรกรรมเวลาที่แก้ไขเพื่อเพิ่มปริมาณ</span><span class="sxs-lookup"><span data-stu-id="6b7d3-119">Invoicing a time transaction that was edited to increase the quantity.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="6b7d3-120">การกลับการขายที่ไม่ได้เรียกเก็บเงินสำหรับชั่วโมงและจำนวนเงินในการอนุมัติเวลาตามเดิม</span><span class="sxs-lookup"><span data-stu-id="6b7d3-120">An unbilled sales reversal for the hours and amount on the original time approval.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="6b7d3-121">การขายจริงใหม่ที่ยังไม่เรียกเก็บเงินซึ่งคิดค่าธรรมเนียมเป็นชั่วโมงและจำนวนเงินในรายละเอียดรายการใบแจ้งหนี้ที่แก้ไข การย้อนกลับของการขายจริงที่ไม่ได้เรียกเก็บเงินและเทียบเท่ากับการขายจริงที่เรียกเก็บเงิน</span><span class="sxs-lookup"><span data-stu-id="6b7d3-121">A new unbilled sales actual that is chargeable for the hours and amount on the edited invoice line detail, a reversal of the unbilled sales actual, and an equivalent billed sales actual.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="6b7d3-122">การออกธุรกรรมค่าใช้จ่ายโดยไม่มีการแก้ไขใดๆ ในแบบร่างใบแจ้งหนี้</span><span class="sxs-lookup"><span data-stu-id="6b7d3-122">Invoicing an expense transaction without any edits on the draft invoice.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="6b7d3-123">การกลับการขายที่ไม่ได้เรียกเก็บเงินสำหรับปริมาณและจำนวนเงินในการอนุมัติค่าใช้จ่ายตามเดิม</span><span class="sxs-lookup"><span data-stu-id="6b7d3-123">An unbilled sales reversal for the quantity and amount on the original expense approval.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="6b7d3-124">การขายจริงที่เรียกเก็บเงินสำหรับปริมาณและจำนวนเงินในการอนุมัติค่าใช้จ่ายตามเดิม</span><span class="sxs-lookup"><span data-stu-id="6b7d3-124">A billed sales actual for the quantity and amount on the original expense approval.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="3" valign="top">
                <p>
<span data-ttu-id="6b7d3-125">การออกใบแจ้งหนี้ธุรกรรมค่าใช้จ่ายที่แก้ไขเพื่อลดปริมาณ</span><span class="sxs-lookup"><span data-stu-id="6b7d3-125">Invoicing an expense transaction that was edited to reduce the quantity.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="6b7d3-126">การกลับการขายที่ไม่ได้เรียกเก็บเงินสำหรับปริมาณและจำนวนเงินในการอนุมัติค่าใช้จ่ายตามเดิม</span><span class="sxs-lookup"><span data-stu-id="6b7d3-126">An unbilled sales reversal for the quantity and amount on the original expense approval.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="6b7d3-127">การขายจริงใหม่ที่ยังไม่เรียกเก็บเงินซึ่งคิดค่าธรรมเนียมเป็นปริมาณและจำนวนเงินในรายละเอียดรายการใบแจ้งหนี้ที่แก้ไข การย้อนกลับของการขายจริงที่ไม่ได้เรียกเก็บเงินและเทียบเท่ากับการขายจริงที่เรียกเก็บเงิน</span><span class="sxs-lookup"><span data-stu-id="6b7d3-127">A new unbilled sales actual that is chargeable for the quantity and amount on the edited invoice line detail, a reversal of the unbilled sales actual, and an equivalent billed sales actual.</span></span> 
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="6b7d3-128">การขายจริงใหม่ที่ยังไม่เรียกเก็บเงินซึ่งไม่คิดค่าธรรมเนียมเป็นปริมาณและจำนวนเงินที่เหลือหลังจากการลดการกำหนดค่าที่แก้ไขในรายละเอียดรายการใบแจ้งหนี้ที่แก้ไข การย้อนกลับของการขายจริงที่ไม่ได้เรียกเก็บเงินและเทียบเท่ากับการขายจริงที่เรียกเก็บเงิน</span><span class="sxs-lookup"><span data-stu-id="6b7d3-128">A new unbilled sales actual that is non-chargeable for the remaining quantity and amount after deducting the corrected figures on edited invoice line detail, a reversal of the unbilled sales actual, and an equivalent of the billed sales actual.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="6b7d3-129">การออกใบแจ้งหนี้ธุรกรรมค่าใช้จ่ายที่แก้ไขเพื่อเพิ่มปริมาณ</span><span class="sxs-lookup"><span data-stu-id="6b7d3-129">Invoicing an expense transaction that was edited to increase the quantity.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="6b7d3-130">การกลับการขายที่ไม่ได้เรียกเก็บเงินสำหรับปริมาณและจำนวนเงินในการอนุมัติค่าใช้จ่ายตามเดิม</span><span class="sxs-lookup"><span data-stu-id="6b7d3-130">An unbilled sales reversal for the quantity and amount on the original expense approval.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="6b7d3-131">การขายจริงใหม่ที่ยังไม่เรียกเก็บเงินซึ่งคิดค่าธรรมเนียมเป็นปริมาณและจำนวนเงินในรายละเอียดรายการใบแจ้งหนี้ที่แก้ไข การย้อนกลับของการขายจริงที่ไม่ได้เรียกเก็บเงินและเทียบเท่ากับการขายจริงที่เรียกเก็บเงิน</span><span class="sxs-lookup"><span data-stu-id="6b7d3-131">A new unbilled sales actual that is chargeable for quantity and amount on the edited invoice line detail, a reversal of the untilled sales actual, and an equivalent billed sales actual.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="6b7d3-132">ออกใบแจ้งหนี้ค่าธรรมเนียม</span><span class="sxs-lookup"><span data-stu-id="6b7d3-132">Invoicing a fee.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="6b7d3-133">การกลับการขายที่ไม่ได้เรียกเก็บเงินสำหรับจำนวนค่าธรรมเนียมในบรรทัดสมุดรายวันตามเดิม</span><span class="sxs-lookup"><span data-stu-id="6b7d3-133">An unbilled sales reversal for the fee amount on the original journal line.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="6b7d3-134">การขายจริงที่เรียกเก็บเงินสำหรับปริมาณและจำนวนเงินในบรรทัดสมุดรายวันตามเดิม</span><span class="sxs-lookup"><span data-stu-id="6b7d3-134">A billed sales actual for the quantity and amount on the original fee journal line.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" valign="top">
                <p>
<span data-ttu-id="6b7d3-135">การออกใบแจ้งหนี้เหตุการณ์สำคัญ</span><span class="sxs-lookup"><span data-stu-id="6b7d3-135">Invoicing a milestone.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="6b7d3-136">การขายจริงที่เรียกเก็บเงินสำหรับจำนวนเหตุการณ์สำคัญบนเหตุการณ์สำคัญเดิมในรายละเอียดการให้บริการตามสัญญาของโครงการ</span><span class="sxs-lookup"><span data-stu-id="6b7d3-136">A billed sales actual for the milestone amount on the original milestone on the project contract line.</span></span>
                </p>
            </td>
        </tr>
    </tbody>
</table>


[!INCLUDE[footer-include](../includes/footer-banner.md)]