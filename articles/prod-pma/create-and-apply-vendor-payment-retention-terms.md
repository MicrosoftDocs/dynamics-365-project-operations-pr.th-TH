---
title: สร้างและใช้นโยบายการเก็บรักษาสำหรับการชำระเงินของผู้จัดจำหน่าย
description: หัวข้อนี้ให้ข้อมูลเกี่ยวกับวิธีตั้งค่าและรักษาเงื่อนไขการเก็บรักษาสำหรับการชำระเงินของผู้จัดจำหน่าย
author: Yowelle
ms.date: 05/26/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: andchoi
ms.dyn365.ops.version: 7
ms.search.validFrom: 2019-01-15
ms.openlocfilehash: 09bb30f55ee8e1f24634e9d8b7dea95bd3dbd24f
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 05/10/2021
ms.locfileid: "6006354"
---
# <a name="create-and-apply-vendor-payment-retention-terms"></a><span data-ttu-id="5ccfb-103">สร้างและใช้นโยบายการเก็บรักษาสำหรับการชำระเงินของผู้จัดจำหน่าย</span><span class="sxs-lookup"><span data-stu-id="5ccfb-103">Create and apply vendor payment retention terms</span></span>

[!include [banner](../includes/banner.md)] 

<span data-ttu-id="5ccfb-104">การตั้งค่าเงื่อนไขการเก็บรักษาการชำระเงินของผู้จัดจำหน่ายสำหรับโครงการมีประโยชน์เมื่อองค์กรของคุณต้องการเก็บเงินส่วนหนึ่งของการชำระเงินให้กับผู้จัดจำหน่าย</span><span class="sxs-lookup"><span data-stu-id="5ccfb-104">Setting up vendor payment retention terms for a project is useful when your organization wants to retain part of the payments made to a vendor.</span></span> <span data-ttu-id="5ccfb-105">ตัวอย่างเช่น เมื่อคุณต้องการระงับการชำระเงินให้กับผู้ขายจนกว่าผลิตภัณฑ์ถูกจัดส่งตรงตามความคาดหวังของคุณ</span><span class="sxs-lookup"><span data-stu-id="5ccfb-105">For example, when you want to hold payment to a vendor until the products delivered meet your expectations.</span></span> <span data-ttu-id="5ccfb-106">สามารถระบุเงื่อนไขการเก็บรักษาการชำระเงินของผู้จัดจำหน่ายเมื่อคุณเจรจาสัญญากับผู้จัดจำหน่าย</span><span class="sxs-lookup"><span data-stu-id="5ccfb-106">Vendor payment retention terms can be specified when you negotiate a vendor contract.</span></span>

## <a name="create-vendor-payment-retention-terms"></a><span data-ttu-id="5ccfb-107">สร้างเงื่อนไขนโยบายการเก็บรักษาสำหรับการชำระเงินของผู้จัดจำหน่าย</span><span class="sxs-lookup"><span data-stu-id="5ccfb-107">Create vendor payment retention terms</span></span>

<span data-ttu-id="5ccfb-108">คุณสามารถป้อนเปอร์เซ็นต์ของการชำระเงินของผู้จัดจำหน่ายสำหรับการเก็บรักษาและเปอร์เซ็นต์ของจำนวนเงินคงที่ก่อนหน้านี้ที่จะออก</span><span class="sxs-lookup"><span data-stu-id="5ccfb-108">You can enter the percentage of vendor payment for retention and the percentage of the previously retained amounts to be released.</span></span> <span data-ttu-id="5ccfb-109">จำนวนเงินจะถูกเก็บไว้โดยอัตโนมัติในใบแจ้งหนี้ของผู้จัดจำหน่ายจนกว่าสัญญาจะถึงสถานะเสร็จสิ้นที่ระบุ</span><span class="sxs-lookup"><span data-stu-id="5ccfb-109">Amounts are automatically retained on vendor invoices until the contract reaches the specified state of completion.</span></span> <span data-ttu-id="5ccfb-110">หลังจากที่คุณตั้งค่าเงื่อนไขการเก็บรักษา คุณสามารถนำไปใช้กับโครงการใดๆ สำหรับผู้จัดจำหน่ายรายนั้น</span><span class="sxs-lookup"><span data-stu-id="5ccfb-110">After you set up the retention terms, you can apply them to any project for that vendor.</span></span>

<span data-ttu-id="5ccfb-111">ใช้ขั้นตอนต่อไปนี้เพื่อตั้งค่าและรักษาเงื่อนไขการเก็บรักษาสำหรับการชำระเงินของผู้จัดจำหน่าย</span><span class="sxs-lookup"><span data-stu-id="5ccfb-111">Use the following steps to set up and maintain retention terms for vendor payments.</span></span> 

1. <span data-ttu-id="5ccfb-112">ไปที่ **การจัดการโครงการและการบัญชี** > **การเก็บรักษา** > **เงื่อนไขการเก็บรักษาการชำระเงินของผู้จัดจำหน่าย**</span><span class="sxs-lookup"><span data-stu-id="5ccfb-112">Go to **Project management and accounting** > **Retention** > **Vendor payment retention terms**.</span></span>
2. <span data-ttu-id="5ccfb-113">เลือก **ใหม่** เพื่อเพิ่มเงื่อนไขการรักษาผู้จัดจำหน่ายใหม่</span><span class="sxs-lookup"><span data-stu-id="5ccfb-113">Select **New** to add a new vendor retention term.</span></span> <span data-ttu-id="5ccfb-114">ค่า **รหัสกฎ** ของคำใหม่จะถูกป้อนโดยอัตโนมัติ</span><span class="sxs-lookup"><span data-stu-id="5ccfb-114">The **Rule ID** value for the new term is automatically entered.</span></span> 
3. <span data-ttu-id="5ccfb-115">ป้อนคำอธิบายสั้นๆ ในฟิลด์ **คำอธิบาย** และบนแท็บด่วน **เงื่อนไข** เลือก **เพิ่มรายการ** เพื่อป้อนค่าคำสำหรับสิ่งต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="5ccfb-115">Enter a brief description in the **Description** field, and on the **Terms** FastTab, select **Add line** to enter term values for the following:</span></span>

   - <span data-ttu-id="5ccfb-116">**เปอร์เซ็นต์ของหน่วยที่จัดส่ง**: ป้อนเปอร์เซ็นต์ความสำเร็จของคำ</span><span class="sxs-lookup"><span data-stu-id="5ccfb-116">**Percentage of units delivered**: Enter a percentage of completion for the term.</span></span> <span data-ttu-id="5ccfb-117">จำนวนเงินจะถูกเก็บไว้โดยอัตโนมัติในใบแจ้งหนี้ของผู้จัดจำหน่ายจนกว่าความสมบูรณ์ของขั้นตอนของโครงการสัญญาจะถึงเปอร์เซ็นต์ที่ระบุ</span><span class="sxs-lookup"><span data-stu-id="5ccfb-117">Amounts are automatically retained on vendor invoices until the project stage of completion is equal to the specified percentage.</span></span> <span data-ttu-id="5ccfb-118">ตัวอย่างเช่น หากคุณป้อน 50.00 จำนวนเงินจะยังคงอยู่จนกว่าโครงการจะเสร็จสมบูรณ์ 50 เปอร์เซ็นต์</span><span class="sxs-lookup"><span data-stu-id="5ccfb-118">For example, if you enter 50.00, amounts are retained until the project is 50 percent completed.</span></span>
   - <span data-ttu-id="5ccfb-119">**เปอร์เซ็นต์ที่จะคงไว้**: ป้อนเปอร์เซ็นต์ของยอดเงินในใบแจ้งหนี้ของผู้จัดจำหน่ายที่จะคงไว้</span><span class="sxs-lookup"><span data-stu-id="5ccfb-119">**Percentage to retain**: Enter a percentage of the vendor invoice amount to be retained.</span></span> <span data-ttu-id="5ccfb-120">ตัวอย่างเช่น ถ้าคุณป้อน 10.00 10 เปอร์เซ็นต์ของจำนวนเงินในใบแจ้งหนี้ของผู้จัดจำหน่ายจะถูกเก็บไว้จนกว่าโครงการจะถึงเปอร์เซ็นต์ของความสำเร็จตามที่ตั้งไว้ใน **ฟิลด์เปอร์เซ็นต์ของหน่วยที่จัดส่ง**</span><span class="sxs-lookup"><span data-stu-id="5ccfb-120">For example, if you enter 10.00, then 10 percent of the amount on a vendor invoice is retained until the project reaches the percentage of completion as set in the **Percentage of units delivered field**.</span></span>
   - <span data-ttu-id="5ccfb-121">**เปอร์เซ็นต์ที่จะปล่อย**: เลือก **เพิ่มรายการ** เพื่อป้อนเปอร์เซ็นต์ของจำนวนเงินที่เก็บไว้ก่อนหน้านี้ที่จะปล่อยสำหรับระดับความสำเร็จของโครงการที่เลือก</span><span class="sxs-lookup"><span data-stu-id="5ccfb-121">**Percentage to release**: Select **Add line** to enter a percentage of any previously retained amounts to be released for the selected level of project completion.</span></span>

> [!NOTE]
> <span data-ttu-id="5ccfb-122">หากคุณมีเหตุการณ์สําคัญมากกว่าหนึ่งรายการสำหรับความสำเร็จของโครงการในระดับต่างๆ ให้ป้อนบรรทัดข้อกำหนดการรักษาผู้จัดจำหน่ายแยกต่างหากสำหรับกฎการเก็บรักษาแต่ละข้อ</span><span class="sxs-lookup"><span data-stu-id="5ccfb-122">If you have more than one milestone for different levels of project completion, enter a separate vendor retention term line for each retention rule.</span></span> <span data-ttu-id="5ccfb-123">แต่ละรายการสามารถระบุเปอร์เซ็นต์การเก็บรักษาที่แตกต่างกันและเปอร์เซ็นต์การเผยแพร่ที่แตกต่างกันสำหรับแต่ละระดับความสำเร็จของโครงการที่กำหนด</span><span class="sxs-lookup"><span data-stu-id="5ccfb-123">Each line can specify a different retention percentage and a different release percentage for each designated level of project completion.</span></span>

<span data-ttu-id="5ccfb-124">หลังจากที่คุณสร้างเงื่อนไขการเก็บรักษาของผู้จัดจำหน่ายสำหรับผู้จัดจำหน่าย คุณสามารถนำคำไปใช้กับโครงการ</span><span class="sxs-lookup"><span data-stu-id="5ccfb-124">After you create vendor retention terms for a vendor, you can apply the terms to a project.</span></span>

## <a name="apply-vendor-retention-terms-to-a-project"></a><span data-ttu-id="5ccfb-125">ใช้เงื่อนไขการรักษาผู้จัดจำหน่ายกับโครงการ</span><span class="sxs-lookup"><span data-stu-id="5ccfb-125">Apply vendor retention terms to a project</span></span>

1. <span data-ttu-id="5ccfb-126">ไปที่ **การจัดการโครงการและการบัญชี** > **โครงการ** > **โครงการทั้งหมด** และเปิดโครงการจากหน้ารายการโครงการ</span><span class="sxs-lookup"><span data-stu-id="5ccfb-126">Go to **Project management and accounting** > **Projects** > **All projects** and open a project from the project list page.</span></span>
2. <span data-ttu-id="5ccfb-127">บน FastTab **ข้อตกลงของผู้จัดจำหน่าย** เลือก **เพิ่มรายการ**</span><span class="sxs-lookup"><span data-stu-id="5ccfb-127">On the **Vendor agreements** FastTab, select **Add line**.</span></span>
3. <span data-ttu-id="5ccfb-128">ใน **ฟิลด์รหัสลูกค้าองค์กร** เลือกหนึ่งในตัวเลือกต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="5ccfb-128">In the **Account code field**, select one of the following options:</span></span> 

   - <span data-ttu-id="5ccfb-129">**ตาราง**: เงื่อนไขการรักษาผู้จัดจำหน่ายใช้กับผู้จัดจำหน่ายรายเดียว</span><span class="sxs-lookup"><span data-stu-id="5ccfb-129">**Table**: The vendor retention terms apply to a single vendor.</span></span>
   - <span data-ttu-id="5ccfb-130">**กลุ่ม**: เงื่อนไขการรักษาผู้จัดจำหน่ายใช้กับผู้จัดจำหน่ายทั้งหมดในกลุ่มผู้จัดจำหน่าย</span><span class="sxs-lookup"><span data-stu-id="5ccfb-130">**Group**: The vendor retention terms apply to all vendors in a vendor group.</span></span>
   - <span data-ttu-id="5ccfb-131">**ทั้งหมด**: เงื่อนไขการรักษาผู้จัดจำหน่ายใช้กับผู้จัดจำหน่ายทั้งหมด</span><span class="sxs-lookup"><span data-stu-id="5ccfb-131">**All**: The vendor retention terms apply to all vendors.</span></span>

4. <span data-ttu-id="5ccfb-132">ใน **ฟิลด์ผู้จัดจำหน่าย/กลุ่มผู้จัดจำหน่าย** เลือกผู้จัดจำหน่ายหรือกลุ่มผู้จัดจำหน่ายที่ใช้เงื่อนไขการเก็บรักษาผู้จัดจำหน่าย</span><span class="sxs-lookup"><span data-stu-id="5ccfb-132">In the **Vendor/Vendor group field**, select the vendor or vendor group to which the vendor retention terms apply.</span></span> <span data-ttu-id="5ccfb-133">ถ้าคุณเลือก **ทั้งหมด** ในขั้นตอนก่อนหน้านี้ ฟิลด์นี้จพใช้งานไม่ได้</span><span class="sxs-lookup"><span data-stu-id="5ccfb-133">If you selected **All** in the previous step, this field is unavailable.</span></span>
5. <span data-ttu-id="5ccfb-134">ในฟิลด์ **เงื่อนไขการรักษาผู้จัดจำหน่าย** เลือกเงื่อนไขการเก็บรักษาที่คุณสร้างไว้ในขั้นตอนก่อนหน้านี้</span><span class="sxs-lookup"><span data-stu-id="5ccfb-134">In the **Vendor retention terms** field, select the retention terms that you created in the previous procedure.</span></span>
6. <span data-ttu-id="5ccfb-135">หากโครงการมีเงื่อนไขการจ่ายเมื่อชำระเงิน (PWP) ที่ตั้งค่าไว้สำหรับผู้จัดจำหน่ายด้วย ให้ป้อนเปอร์เซ็นต์เกณฑ์สำหรับโครงการในฟิลด์ **เปอร์เซ็นต์เกณฑ์ PWP**</span><span class="sxs-lookup"><span data-stu-id="5ccfb-135">If the project also has pay-when-paid (PWP) terms set up for the vendor, enter the threshold percentage for the project in the **PWP threshold percentage** field.</span></span>

<span data-ttu-id="5ccfb-136">เงื่อนไขการรักษาผู้จัดจำหน่ายจะแสดงในใบสั่งซื้อที่คุณสร้างขึ้นสำหรับผู้จัดจำหน่ายด้วย</span><span class="sxs-lookup"><span data-stu-id="5ccfb-136">The vendor retention terms are also displayed on purchase orders that you create for the vendor.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]